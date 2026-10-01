# Conventions

This policy (or rather the collection of common convention policies) details all the general rules and recommendations
for those who may want to contribute to Leaf. These conventions are subject to change and are general recommendations,
not final decisions!

## Repository name conventions

Repository names under the LeafPZ organisation generally should follow the kebab-case format, containing no capital
letters, spaces, underscores, etc. ASCII-only names are required. Try to keep numbers out of repository names (such as
"v2" or "2026" etc. The repository names must start with `leaf-` if directly related to the Leaf project, and if not
you should use your own discretion as to the naming convention; make it clear as to what the project relates to.

## Commit name conventions

All commits to Leaf must follow the [conventional commits][ConventionalCommits] standard as close as possible, however
it does not need to be followed exactly - only close enough that it is clear and organised.

## Issue and Pull Request conventions

Generally, issues and pull requests to LeafPZ repositories should read as a short sentence without ending punctuation
describing what the issue or pull request is about (with brevity in mind). These aren't to be followed exactly, as I
myself (aoqia) am not too pedantic in this regard, but I'd highly recommend it. Generally, issue titles should describe
what the issue *is*, and issue descriptions should describe *how* the issue is replicated and any other details. Pull
request titles should describe what the pull request indends to achieve/do, and pull request descriptions should
describe *how* it should be implemented, what areas of the repository it touches (if necessary), etc.

If a repository contains specific issue and or pull request templates, be sure to follow those as well.

Some **good** issue/PR titles might look like:

- `Missing detailed exception message when game can't be found`
- `Improper handling when no game arguments are provided`
- `Latest stable release breaks bytecode patches`
- `Disable game hash checks by default` 

Some **bad** issue/PR titles might look like:

- `bug: missing exception message` - Using conventional commits as issue/PR titles is not clean here, and the title
  itself is vague enough at a glance.
- `IMPROPER HANDLING WHEN NO GAME ARGUMENTS ARE PROVIDED` - Using all uppercase makes it hard to read at a glance
- `Latest stable releases breaks EntrypointPatch bytecode patches which results in the loader crashing upon startup
  in development and production environments` - Really verbose/long issue titles should be avoided, add more details
  in the issue details itself.

## Branch name conventions

The default branch should always be `main` for any given repository. The main branch should always be treated as a
rolling branch which may contain the latest changes ready for release - you may think of this branch as the staging
area for features and fixes ready to be published in the next release. Generally I (aoqia) may include things here
that don't directly fit under that category, but if you are a contributor external to the LeafPZ organisation, keep
this in mind as it is important.

Non-default branch names should be named according to contributor discretion, but it is highly recommended to follow
a [Conventional Commits][ConventionalCommits]-like approach. Branch names should also follow kebab-case, similar
to repository names.

For example, some **good** branch names:

- `main` (default) - The default branch should always be main!
- `dev` (staging) - There may be a situation where an intermediate staging area is required, thus something like
  dev, develop, staging, etc should be used. Most commonly, you will see `dev` however
- `feat/new-feature` - An example of a branch containing a new feature
- `feat/api-v2` - In this case, it's ok to include stuff like "v2", "v3", etc to briefly indicate an improvement,
  however this should be used sparingly
- `fix/big-bad-bug` - An example of a branch containing a bug fix
- `refactor/api-cleanup` - A branch that contains a refactor such as a cleanup

Generally, these three should be enough for most situations, but there is no harm in specifying at a deeper level if
you feel it is required to do so.

Some **bad** branch names:

- `jane-fix-bad-bug` - Including author names in branches is not good
- `FixBigBadBug` - Not following kebab-case style
- `lmao67` - Doesn't detail anything relating to the branch or what it is meant to be

Branch names such as `master`, `slave`, etc or branch names that contain information not relevant to the
feature/fix/other should be avoided for obvious reasons, though this is primarily for branches in the repository
itself and not necessarily for branches on third-party forks such as PR branch sources.
