# Proposal Creation Skill for AI Agents

This skill provides step-by-step instructions for AI agents to create proposals in the opinionated-ts repository following the standardized workflow.

### 1. Start from the Template Branch

Always begin work from the `proposal/template` branch:

```bash
# Checkout the template branch
git checkout proposal/template

# Ensure you have the latest version
git pull origin proposal/template
```

### 2. Create Your Work Branch

Create a branch using the standard naming convention:

```bash
# Replace <username|org> with your GitHub username or organization name
git checkout -b proposal/<username|org>
```

### 3. Choose and Use the Appropriate Template

Select the correct template based on proposal type:

#### For RFCs (Requests for Comments)

Use when proposing new specifications, features, or significant changes:

- Template file: `templates/rfc.md`
- Target location: `ai-spec/<scope>/rfcs/` (e.g., `ai-spec/agents/rfcs/`)
- Filename format: `0001-descriptive-name.md` (increment the number)

#### For Decisions

Use when documenting agreed-upon choices or resolutions:

- Template file: `templates/decisions.md`
- Target location: `ai-spec/<scope>/decisions/` (e.g., `ai-spec/agents/decisions/`)
- Filename format: `0001-descriptive-name.md` (increment the number)

### 4. Copy and Edit the Template

Copy the template to the appropriate location within the scope structure:

```bash
# For an RFC in agents scope
# (e.g., `ai-spec/skills/rfcs/0001-my-proposal.md`)
cp templates/rfc.md ai-spec/skills/rfcs/<rfc-number>-<rfc-name>.md

# For a Decision in agents scope
# (e.g., `ai-spec/mcp/decisions/0001-my-decision.md`)
cp templates/decisions.md ai-spec/mcp/decisions/<decision-number>-<decision-name>.md
```

Then edit the file:

- Replace all placeholder text (like `<Specific Proposal Title>`)
- Fill in each section completely
- Remove instructions/comments that were in the template
- Keep the section headers and structure intact

### 5. Commit Your Changes

Make regular commits as you work:

```bash
# Commit with a descriptive message using the scope (e.g., agents, skills, mcp, hooks, etc.)
git commit -m "feat(agents): add proposal for agent file structure"
# OR
# git commit -m "feat(skills): document decision on visibility enhancement"
# OR
# git commit -m "feat(mcp): propose new MCP server guidelines"
```

You can make multiple commits as you refine your proposal:

```bash
git commit -am "fix(agents): clarify goal statement in section 3"
git commit -am "feat(skills): add reference-level explanation"
```

### 6. Prepare for Pull Request

Before opening your PR:

- Ensure your proposal is complete and readable
- Check that all template placeholders have been replaced
- Verify links and references are correct

### 8. Open the Pull Request

When ready, push your branch and open a PR:

```bash
git push origin proposal/<username|org>
```

Then open a pull request targeting the `proposal/template` branch (not main or other branches).

## Finding the Next Template Number

To determine the next number for your RFC or Decision within a scope:

```bash
# For RFCs in a specific scope
ls ai-spec/<scope>/rfcs/ | sort | tail -1

# For Decisions in a specific scope
ls ai-spec/<scope>/decisions/ | sort | tail -1
```

Increment the number from the latest file found in that scope's directory.

## Notes

The broader process (opening discussions, linking PRs, community feedback) is handled separately as described in CONTRIBUTING.md.
