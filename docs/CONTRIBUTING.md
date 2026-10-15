# Contributing

Thanks for your interest in contributing! This guide covers the basics. By participating, you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md).

## Licensing

By contributing, you agree that your contributions will be licensed under the same license as the respective project.

## LLM and Generative AI

> [!CAUTION]
> **This project has a strict NO LLM policy under ANY circumstances.**

LLMs and Generative AI are **NOT** welcome here, both for contributions and for issue reporting. Any such cases will be
marked as slop issues/PRs, and given enough infractions you will have the ability to do so removed at the discretion of
myself (aoqia). The choice of this is to preserve modding as a hobby and passion. LLMs have proven countless times to
remove people from said passion, and I am not interested in having anyone who doesn't share this passion contribute to
Leaf.

That all being said, I will - *for now at least* - tolerate LLM-assisted issues created under the guise of **security** due
to my inability to look the other way when it comes to security as it is a serious topic. The issue must be reviewed by a
human and replication must be confirmed by a human before the issue will be taken seriously. If you cannot follow those
basic rules, you will have the ability to create issues or contribute to Leaf removed at the discretion of myself (aoqia).

For more information on issue creation and contribution guidelines, see the repositories' issue and pull request templates
if applicable. If there is no such templates or guidelines specified on the given repository, you should ***NOT*** make
the assumption that AI use is allowed.

I (aoqia) will allow any discussion about this policy to be talked about in a reasonable manner. If you cannot be, you
will probably be ignored.

## Ways to contribute

- Report bugs
- Suggest features or improvements
- Improve documentation
- Submit code fixes or new features
- Anything else to help leaf (just discussion helps a lot!)

## Reporting bugs and requesting features

1. Search existing issues for the respective project first to avoid duplicates
2. Open a new issue and fill out the template (if there is one)

Make sure your issue's title follows the [conventions](#conventions) listed below.

For questions or general help, you can join the PZMC Discord (recommended for general discussion) or use the project's discussions (checked less frequently) rather than opening an issue.

**Security vulnerabilities:** please don't file these publicly. See [SECURITY.md](SECURITY.md)!!

## Submitting a pull request

1. Fork the repository and create a branch from `main`
2. Make your changes, keeping each PR focused on a single concern
3. Add or update tests and documentation where it makes sense
4. Make sure it builds and tests pass (where applicable)
5. Commit with a clear message following the [conventions](#conventions) and push to your branch
6. Open a pull request and fill out the PR template. Remember to link any related issues, for example `Closes #123`

For large or breaking changes, it's preferrable to discuss the approach before writing code.

## Commit messages

- Use the imperative mood: "feat: add retry logic", not "feat: added retry logic"
- Explain the *why* in the body when it isn't obvious

## Review process

A maintainer or LeafPZ member will review your pull request. You may be asked to make changes. Once approved and passing CI, a maintainer will merge it.

# Conventions

This contributing policy (or rather the collection of common policies) details all the general rules and
recommendations for those who may want to contribute to Leaf. These conventions are subject to change!

### Repository name conventions

Repository names under the LeafPZ organisation generally should follow the kebab-case format, containing no capital
letters, spaces, underscores, etc. ASCII-only names are required. Try to keep numbers out of repository names (such as
"v2" or "2026" etc. The repository names must start with `leaf-` if directly related to the Leaf project, and if not
you should use your own discretion as to the naming convention; make it clear as to what the project relates to.

### Commit name conventions

All commits to Leaf must follow the [conventional commits][ConventionalCommits] standard as close as possible, however
it does not need to be followed exactly - only close enough that it is clear and organised.

### Issue and Pull Request conventions

Generally, issues and pull requests to LeafPZ repositories should read as a short sentence without ending punctuation
describing what the issue or pull request is about (with brevity in mind). These aren't to be followed exactly, as I
myself (aoqia) am not too pedantic in this regard, but I'd highly recommend it. Generally, issue titles should describe
what the issue *is*, and issue descriptions should describe *how* the issue is replicated and any other details. Pull
request titles should describe what the pull request indends to achieve/do, and pull request descriptions should
describe *how* it should be implemented, what areas of the repository it touches (if necessary), etc.

If a repository contains specific issue and or pull request templates, be sure to follow those as well.

Some **good** issue/PR titles might look like:

- `bug: missing detailed exception message when game can't be found`
- `fix: resolve improper handling when no game arguments are provided`
- `bug: latest stable release breaks bytecode patches`
- `fix: disable game hash checks by default`
- `feat: load mods from custom folder`

Some **bad** issue/PR titles might look like:

- `missing exception message` - Using conventional commits as issue/PR titles is required, and the title
  itself is vague at a glance.
- `BUG: IMPROPER HANDLING WHEN NO GAME ARGUMENTS ARE PROVIDED` - Using all uppercase makes it hard to read at a glance
- `bug: latest stable releases breaks EntrypointPatch bytecode patches which results in the loader crashing upon startup
  in development and production environments` - Really verbose/long issue titles should be avoided, add more details
  in the issue details itself.

### Branch name conventions

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

