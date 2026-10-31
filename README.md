<p align="center">
  <img src="assets/logo.png" alt="Xenoblade Chronicles Recompiled" width="720">
</p>

<p align="center">
  An actively developed native PC recompilation project bringing the Xenoblade Chronicles series to Windows.
</p>

## Project Status

**Active Development | Windows First | No Public Release Yet**

**Xenoblade Chronicles Recompiled** is a native PC recompilation project focused on bringing the Xenoblade Chronicles games to Windows, beginning with **Xenoblade Chronicles: Definitive Edition**.

The project uses static ARM64 recompilation to transform the game's original executable code into native PC code, alongside the development of a dedicated runtime, graphics implementation, and supporting tools.

The ultimate goal is to deliver a fully native Windows experience without requiring an emulator or compatibility layer during gameplay.

Development is actively ongoing, with significant progress already made on the recompilation pipeline, native runtime, Vulkan graphics implementation, and game compatibility.

**There is currently no public build, installer, or announced release date.** Development is taking place privately, with plans to publish the source code once the initial game is ready for public testing and play.

## Development Progress

Work on Xenoblade Chronicles: Definitive Edition has already reached several important technical milestones.

### What's Been Accomplished

- **Static ARM64 Recompilation:** A recompilation pipeline for converting the game's ARM64 executable modules into native code.
- **Native Windows Runtime:** Development of a dedicated runtime to handle the game's execution, memory management, and system functionality.
- **Vulkan Graphics:** A native graphics implementation capable of processing game graphics commands, shaders, textures, and rendering operations.
- **Native System Integration:** Implementation of game SDK hooks and replacement services, gradually eliminating dependencies on the transitional Suyu runtime.
- **Title Screen Rendering:** The native implementation can successfully render the game's title screen.
- **Menu Navigation:** Scripted controller input can navigate the game's menus.
- **Save Loading:** The game can detect save files and load an existing save.
- **In-Game Rendering:** The native implementation has successfully reached Colony 9 and rendered an in-game scene, including terrain and HUD elements.

### Current Development Focus

While these milestones represent substantial progress, additional work is required before the game is ready for public testing.

Current priorities include:

- Correcting remaining graphics and shader issues.
- Correcting foliage rendering, including grass and vegetation, following the successful fix for missing character models.
- Improving runtime performance and frame pacing.
- Completing native implementations of remaining system services.
- Refining input, audio, memory management, and save compatibility.
- Testing additional gameplay scenarios and areas.
- Continuing the transition away from the modified Suyu compatibility runtime.

The native implementation is already capable of executing and rendering portions of the game, including character models after a recent rendering fix, but it is **not yet ready for general gameplay or public distribution**.

The objective remains a fully native implementation without reliance on an emulator during gameplay.

## Development Screenshots & Comparisons

The following screenshots show actual output from internal development builds, including side-by-side native gameplay comparisons against Suyu and separate title-screen rendering progress.

### Native Gameplay Progress

The native implementation has loaded an existing save and reached Colony 9, rendering the environment, character models, and HUD. These two side-by-side comparisons help identify differences between the Suyu reference and the native Vulkan renderer.

![Earlier Colony 9 comparison showing missing character models](https://dl.glitxh.tech/r/kMVmhvOb.png)

![Later Colony 9 comparison with character models restored](https://dl.glitxh.tech/r/vDWcojnf.png)

**Development update:** An earlier issue preventing character models from appearing in the native renderer has been fixed. Current graphics work is focused on correcting foliage rendering, including grass and vegetation, and improving visual accuracy.

### Title Screen Rendering Progress

These three title-screen screenshots document rendering iterations, including fixes for visual artifacts and a temporary color-grading regression. They are displayed together at a smaller size, separately from the Colony 9 comparisons.

<table>
  <tr>
    <td align="center" width="33%"><img src="https://dl.glitxh.tech/r/9dJXobVa.png" alt="Title screen rendering iteration" width="260"></td>
    <td align="center" width="33%"><img src="https://dl.glitxh.tech/r/TfBZYg0s.png" alt="Title screen rendering iteration with the Monado" width="260"></td>
    <td align="center" width="33%"><img src="https://dl.glitxh.tech/r/38r7rV18.png" alt="Title screen with Xenoblade Chronicles Definitive Edition logo" width="260"></td>
  </tr>
</table>

### Work in Progress

**All screenshots are from internal development builds and do not represent the final appearance or performance of the project.** Rendering accuracy, foliage, performance, and remaining native system integration are active areas of development.

For further updates or to help with development, [join the Discord community](https://discord.gg/kSXPe7VFhF).

## Development Roadmap

The following roadmap outlines the project's current priorities and long-term development plans.

### Phase 1: Native Windows Development

**Status: In Progress**

Continue development of the native Windows implementation, including:

- Static recompilation and executable integration.
- Native operating system and game service replacements.
- Vulkan graphics compatibility and shader translation.
- Rendering accuracy and stability.
- Memory, threading, audio, and input systems.

### Phase 2: Gameplay Compatibility and Optimization

**Status: Planned / Partially Underway**

- Expand testing beyond the current title screen and Colony 9 scenarios.
- Resolve rendering and gameplay compatibility issues.
- Improve runtime performance and resource management.
- Validate save loading and progression.
- Improve stability across different game systems and areas.

### Phase 3: Launcher and Installation System

**Status: Planned, Early Development Work Completed**

Develop a launcher capable of preparing a native game installation using files supplied by the user.

Planned functionality includes:

- User-selected game files and installation directories.
- Local game extraction and preparation.
- Automated recompilation and shader processing.
- Support for compatible game updates and downloadable content.
- Installation management and launching the native executable.

Launcher development is currently a lower priority than completing the native runtime and improving gameplay compatibility.

### Phase 4: Public Source Code and Testing

**Status: Planned**

Once the initial game is sufficiently developed for public testing:

- Publish the project's source code.
- Provide build and installation documentation.
- Make test builds available when they are ready.
- Establish public issue reporting and contribution guidelines.
- Continue development based on testing and feedback.

**No release date has been announced.**

### Phase 5: Additional Xenoblade Chronicles Games

**Status: Future Development**

The current priority is completing Xenoblade Chronicles: Definitive Edition.

Once development of the first game has progressed sufficiently, the project plans to expand to additional titles:

- **Xenoblade Chronicles 2**
- **Xenoblade Chronicles 3**
- **Xenoblade Chronicles X: Definitive Edition**
- **Xenoblade Chronicles 2: Torna – The Golden Country** (potential standalone support)

These are future development targets and are not currently supported.

### Phase 6: Linux Support

**Status: Future Development**

Native Linux support is also planned for the future.

Windows remains the primary development platform while the core runtime and recompilation systems are established.

Linux development will be explored as the project progresses. There is currently no Linux release or announced availability date.

## Community & Contributing

Join the **Xenoblade Chronicles Recompiled Discord server** to follow development progress, discuss the project, receive updates, and connect with others interested in native recompilation and reverse engineering.

**[Join the Official Discord Server](https://discord.gg/kSXPe7VFhF)**

### Interested in Helping With Development?

**I'm currently the sole developer working on Xenoblade Chronicles Recompiled**, and bringing a project of this scale to completion involves a substantial amount of reverse engineering, programming, debugging, and testing.

If you're an experienced developer interested in contributing, **I'd be happy to hear from you!**

Additional developers could help accelerate progress, tackle outstanding technical challenges, and bring the project closer to its goals.

Areas where development assistance would be particularly valuable include:

- **C/C++ Development:** Native runtime implementation, systems programming, and performance optimization.
- **Reverse Engineering:** ARM64 analysis, executable formats, game internals, and Nintendo Switch system interfaces.
- **Graphics Programming:** Vulkan, shader translation, graphics APIs, and rendering compatibility.
- **Recompilation & Tooling:** Static recompilation, binary analysis, build systems, and supporting development utilities.
- **Testing & Debugging:** Identifying runtime issues, investigating crashes, and improving compatibility.

**If you'd like to help, join the Discord server and contact me directly at @Glitxhhh.**

We can discuss your experience, the areas you'd like to contribute to, and potentially arrange an invitation to the **private source code repository**, where active development is currently taking place.

The project is being developed privately for now, but that doesn't mean development has to remain a one-person undertaking. Contributions from capable and motivated developers are welcome!

## What to Expect

Development is currently taking place in a private repository while the native implementation continues to progress.

This public repository serves as the project's official information and future source code location.

As development progresses, you can expect updates on technical milestones, compatibility improvements, and eventual public testing.

The source code will be published when the first game is ready for the public to test and play.

The intended launcher will create a local installation from game files provided by the user.

**This project does not distribute copyrighted game files, firmware, or encryption keys. Users will be responsible for supplying their own required game files.**

## Support Development

Xenoblade Chronicles Recompiled is a major development project that requires a significant amount of my time, including reverse engineering, recompilation, native runtime development, debugging, and testing.

I dedicate a considerable amount of my free time to working on this project alongside my other responsibilities.

If you enjoy following its progress and would like to support development, **donations are greatly appreciated**.

Your support helps motivate me to continue development and encourages me to dedicate more of my free time to improving the project and working toward its completion.

Every contribution is appreciated, regardless of its size.

### Donation Methods

[![Ko-fi](https://img.shields.io/badge/Ko--fi-donate-ff5e5b.svg?logo=ko-fi&style=for-the-badge)](https://ko-fi.com/glitxh)
[![Patreon](https://img.shields.io/badge/Patreon-donate-f96854.svg?logo=patreon&style=for-the-badge)](https://patreon.bifrosthub.ru/)
[![BTC](https://img.shields.io/badge/BTC-donate-f7931a.svg?logo=bitcoin&style=for-the-badge)](https://www.blockchain.com/explorer/addresses/btc/bc1qnwtms7pp8hdfqnuunvs3juwskgu7tartd532pz)
[![ETH](https://img.shields.io/badge/ETH-donate-3c3c3d.svg?logo=ethereum&style=for-the-badge)](https://etherscan.io/address/0x48240481C69904C35EC41B4f4eBE41Af05D81975)
[![SOL](https://img.shields.io/badge/SOL-donate-9945ff.svg?logo=solana&style=for-the-badge)](https://explorer.solana.com/address/8gLiGa61utSAyqRGy4QtoVzP6BNkL3GjQZZBpuRtY8hK)
[![USDT TRC20](https://img.shields.io/badge/USDT--TRC20-donate-26a17b.svg?logo=tether&style=for-the-badge)](https://tronscan.org/#/address/TDgQTrr4i3ivJQtQpYB5M3nEw92VkAmC6D)

<details>
<summary>Cryptocurrency addresses (click to expand)</summary>

| Network | Address |
| --- | --- |
| Bitcoin (BTC) | `bc1qnwtms7pp8hdfqnuunvs3juwskgu7tartd532pz` |
| Ethereum (ETH) | `0x48240481C69904C35EC41B4f4eBE41Af05D81975` |
| Solana (SOL) | `8gLiGa61utSAyqRGy4QtoVzP6BNkL3GjQZZBpuRtY8hK` |
| Tron (TRX / USDT-TRC20) | `TDgQTrr4i3ivJQtQpYB5M3nEw92VkAmC6D` |

The Ethereum address is also used on compatible networks including Base, Linea, BNB Chain, Polygon, Optimism, Arbitrum, and Arc. Verify that your wallet is using the correct network before making a transfer.

</details>

Donations are entirely optional and do not guarantee early access, specific features, or a release date.

## How This Project Is Developed

In the interest of transparency, large language models (LLM coding assistants), including **Claude and Codex**, are involved in this project's development.

These tools assist with code generation, analysis, debugging, research, and implementation of technical components.

I am the project's lead developer and a working programmer. I establish the project's goals, architecture, and technical direction, direct and review the assistants' work, test the results, and make the final decisions regarding implementation.

**AI assistants are development tools used under my direction, not substitutes for developer oversight or engineering decisions.**

<p align="center">
  <img src="assets/icon.png" alt="Xenoblade Chronicles Recompiled icon" width="112">
</p>

## License

The original source code of Xenoblade Chronicles Recompiled is licensed under the **GNU General Public License, version 3 or any later version (GPL-3.0-or-later)**.

See [LICENSE](LICENSE) for the full license text.

The license covers only this project's original source code. It does not cover:

- Original game code or copyrighted assets.
- Game dumps, updates, or downloadable content.
- User-provided firmware, encryption keys, or save files.
- Files generated from copyrighted game content.
- Third-party components governed by their own licenses.

For additional information, see [LICENSE-SCOPE.md](LICENSE-SCOPE.md).

---

*Xenoblade Chronicles Recompiled is an independent project developed by Glitxh.*
