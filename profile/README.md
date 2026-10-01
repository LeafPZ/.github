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
![Binaware](https://pride-badges.pony.workers.dev/static/v1?label=binaware&labelColor=%23555&stripeWidth=6&stripeColors=D52D00%2CEF7627%2CFF9A56%2CFFFFFF%2CD162A4%2CB55690%2CA30262)

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

- [LLM and Generative AI](policies/AI.md)
- [Contribution](policies/CONTRIBUTION.md)

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
