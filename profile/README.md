<div align="center">

<h1>
    The organisation for
    <a href="https://pzwiki.net/wiki/Leaf">
        <img src="https://github.com/LeafPZ.png" width="24px" alt="LeafPZ Icon" style="border-radius: 50%;"/>
        leaf
    </a>
</h1>

![Maven status](https://img.shields.io/website?url=https%3A%2F%2Fmaven.aoqia.dev%2F&label=Maven)
![LGBTQ badge](https://pride-badges.pony.workers.dev/static/v1?label=LGBTQ%2B+Ally&labelColor=%23555&stripeWidth=6&stripeColors=ED8E89%2CF7B685%2CF3EBA5%2C94C691%2C9BD6D9%2CB4A8E0)

</div>

The LeafPZ organisation contains all the repositories for Leaf, the most powerful Project Zomboid Java modding
toolchain! It is a hard fork of the well-known [Fabric](https://github.com/FabricMC/) modding toolchain, often
seen and used with Minecraft!

> [!CAUTION]
> You should be informed about the potential risks of Java modding before installing *any* unofficial modding toolchain.
> There are safeguards that are provided such as leaf mod verification and hashing, but leaf **WILL NOT** stop you from
> loading a malicious mod from the Workshop or any other source if you allow it to do so.
>
> It is always recommended to **deny** loading any mod that you do not trust. If you need help verifying the trust of a
> given mod, ask around for advice from people with experience. A good place to ask is in the official or unofficial
> Project Zomboid Discord servers.

## Index

This section details the toolchain repositories and gives a quick summary of what it does, starting from least to most
user-facing. Other repositories exist which are not detailed here, of which are not important enough to list here.

- **[leaf][Leaf]** - Storage site for JSON files containing important game data like version information and file hashes
- ~~**[leaf-filament][LeafFilament]**~~ - **(NOT CURRENTLY USED)** A helper Gradle plugin that yarn uses internally
- ~~**[leaf-yarn][LeafYarn]**~~ - **(NOT CURRENTLY USED)** Open mappings for the game's Java code
- **[leaf-loom][LeafLoom]** - Gradle plugin used to greatly improve the setup and environment of Leaf mod development
- **[leaf-example-mod][LeafExampleMod]** - Example mod template to help you create your first Leaf mod
- **[leaf-loader][LeafLoader]** - The mod loader that powers Leaf for both development and production
- **[leaf-loader-proxy][LeafLoaderProxy]** - Proxy loader Java agent which sits in-between the game launcher and Java
- **[leaf-loader-proxy-native][LeafLoaderProxyNative]** - Native agent required on Windows platforms (only) to fix a bug<br>
  <sub><sup>Seriously, that is its only function due to a bug in the official game launcher!</sup></sub>
- **[leaf-api][LeafApi]** - Common API provided officially by Leaf to cover common Java use-cases
- **[leaf-installer][LeafInstaller]** - Platform-independent installer that guides installation of Leaf in production

## Background

The goal was to port this toolchain to Project Zomboid while keeping the familiar Fabric style which helps
modders who come working from Fabric and want to mod Project Zomboid. This is, however, not the only reason
why it was decided to use Fabric; there is many, such as it being already set up to work nicely with Project
Zomboid as the two games share similarities.

I (aoqia) have been working on this project solo since mid to late 2024, taking a break roughly around late 2025 to
early 2026 due to burnout. Please understand that I can only do so much, especially since I refuse to vibecode yet
another mod loader -- as many of you have probably seen recently with the uprising in slop mods across all games.

### Support

If you need any help whatsoever with Leaf, you can discuss anything leaf-related on Discord through the
official [Project Zomboid Modding Community](https://discord.gg/2Vr6Wyh6Am) Discord using the appropriate channels.
I am always active there, and you may ping me whenever you like for whatever reason, so long as you are reasonable.

## Policies

You may find all the policies regarding the LeafPZ organisation and it's encompassing repositories below.

### LLM and Generative AI

**This project has a strict NO LLM policy under ANY circumstances.**
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

### Special Thanks

- The entire [FabricMC team](https://github.com/FabricMC/)!
- [albion](https://github.com/demiurgeQuantified)
- GigaWatte
- electrisoma
- [SimKDT](https://github.com/SimKDT)

and everyone else who's contributed to Leaf in other ways!

[Leaf]: https://github.com/LeafPZ/leaf
[LeafFilament]: https://github.com/LeafPZ/leaf-filament
[LeafYarn]: https://github.com/LeafPZ/leaf-yarn
[LeafLoom]: https://github.com/LeafPZ/leaf-loom
[LeafExampleMod]: https://github.com/LeafPZ/leaf-example-mod
[LeafLoader]: https://github.com/LeafPZ/leaf-loader
[LeafLoaderProxy]: https://github.com/LeafPZ/leaf-loader-proxy
[LeafLoaderProxyNative]: https://github.com/LeafPZ/leaf-loader-proxy-native
[LeafApi]: https://github.com/LeafPZ/leaf-api
[LeafInstaller]: https://github.com/LeafPZ/leaf-installer
[ConventionalCommits]: https://www.conventionalcommits.org
