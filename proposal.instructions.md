# Proposal Instructions

These instructions define the local workflow for creating and submitting proposals to the `ai-spec` repository.

## 1. Start from the Template Branch

Start from the `proposal/template` branch:

```bash
git checkout proposal/template
git pull origin proposal/template
```

Ensure the working tree is clean before continuing.

## 2. Create Your Work Branch

Create a branch using the standard naming convention:

```bash
git checkout -b proposal/<username|org>
```

Replace `<username|org>` with your GitHub username or organization name.

## 3. Choose the Scope

All specification documents belong to a scope under `spec/`.

The standard structure is:

```text
spec/
└── <scope>/
    ├── <scope>.md
    ├── rfcs/
    └── decisions/
```

If the appropriate scope already exists, use it.

Otherwise, create a new scope following this structure.

## 4. Create or Update the Scope Index

Every scope must have an index named after the scope:

```text
spec/<scope>/<scope>.md
```

For a new scope, initialize the index from the template:

```bash
cp spec/template/template.md spec/<scope>/<scope>.md
```

If the scope already exists, update its existing index. Do not replace it.

Keep the index concise and update it whenever its RFCs or global decisions change.

## 5. Determine the Proposal Number

RFC and Decision numbers are scoped independently.

For an RFC, find the highest existing RFC number in the scope:

```bash
ls spec/<scope>/rfcs/
```

For a Decision, find the highest existing Decision number:

```bash
ls spec/<scope>/decisions/
```

Use the next available four-digit number. If no documents exist, start with `0001`.

## 6. Create the Proposal

Use the corresponding template:

```bash
# RFC
cp spec/template/rfcs/rfc.md spec/<scope>/rfcs/<number>-<descriptive-name>.md

# Decision
cp spec/template/decisions/decisions.md spec/<scope>/decisions/<number>-<descriptive-name>.md
```

Use the correct scope and proposal number.

When creating a new RFC or global decision, update the scope index with the corresponding entry.

## 7. Update References

When adding or modifying specification documents:

- Keep the scope index up to date.
- Place RFCs under the appropriate status section.
- Update an RFC's position in the index when its status changes.
- Keep links and descriptions accurate.
- Add relevant relationships between RFCs, decisions, discussions, and other specification resources.

Do not duplicate detailed proposal content in the scope index.

## 8. Edit and Validate

Use the template as the starting point and adapt it to the proposal.

Before submitting:

- Replace all placeholders.
- Remove template instructions that are not part of the final document.
- Keep the content focused on the proposal.
- Add or remove sections when appropriate.
- Verify links and references.
- Ensure the document is located under the correct scope.
- Ensure the scope index is up to date.

Templates provide recommended structures and may be adapted when necessary.

## 9. Commit Your Changes

Make regular commits as you work:

```bash
git commit -m "feat(agents): add proposal for agent file structure"
```

Use an appropriate scope for the area being changed.

## 10. Push and Open the Pull Request

Push the proposal branch:

```bash
git push origin proposal/<username|org>
```

Open a pull request targeting the `proposal/template` branch.

Link the relevant discussion in the pull request so the proposal can be reviewed alongside the community discussion.

## Repository Templates

The proposal templates are located under:

```text
spec/template/
├── template.md          # Scope index
├── rfcs/
│   └── rfc.md           # RFC
└── decisions/
    └── decisions.md     # Decision
```

The broader contribution process, including discussions, community feedback, and proposal review, is described in `CONTRIBUTING.md`.
