# CustomCommitConvention
A Git commit message convention for my projects.
It largely follows conventional commits (see [Extra Links](#links), but has been extended to prevent most commits from falling into either `feat` or `chore`.
`chore` is now unambiguously defined to only relate to diffs that are **not source code**.

# Commit types
- `build`: Build related changes such as package-manager related, adding external dependencies.
- `chore`: A code change that external user won't see (e.g. changes to .gitignore file or .prettierrc file). **A chore commit should not have any edits to the source code** (e.g. in /src).
- `cleanup`: For removing extra clutter such as previously committed console logs or now unused functions **in the source code**.
- `feat`: A new feature.
- `fix`: A bug fix.
- `docs`: Documentation related changes, both used for in-code (e.g. JSdoc) and external (e.g. README).
- `improve` or `change`: Smaller changes to an already implemented feature that changes external behaviour (e.g. feat: and refactor: are not applicable).

	Prefer `change` e.g. when changing already existing lines such as a color to a different one.
	Prefer `improve` e.g. when adding helpful logs that didn't already exist.
- `refactor`: For refactoring code (does not change external behaviour).
- `revert`: For rolling back whole changes that were made in previous commits.
- `perf`: Changes to code that improves performance.
- `style`: Changes related to styling (e.g. linting files).
- `test`: Adding new test(s) or making changes to existing tests.

## Scope (optional)
```
<type>(<scope>): <subject>

e.g.
fix(db): edge case on data fetch
style(front): change to using C-style curly braces
```
Scopes may for example be
`(front)` for frontend,

`(back)` for backend,
 
`(db)` for database,
 
`(test)` for test files,
 
`(ci)` for continuous integration,
 
`(README)` e.g. `docs(README): add link to project website`,
 
`(meta)`,
 
etc.

## Misc
Prefer all lower-case letters in commit message.

Prefer `feat: add input validation for x`
over `feat: added input validation for x`
	(`remove` over `removed`, etc.).
 
Don't add a dot ( . ) at the end of commits.

Temporary commits that should be squashed later on can be marked simply as `WIP` (for work-in-progress) or `FIXUP`.

# Links
https://www.conventionalcommits.org/en/v1.0.0/

https://dev.to/ishanmakadia/git-commit-message-convention-that-you-can-follow-1709
