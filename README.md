<p align="center">
  <img src="assets/logo.png" alt="Xenoblade Chronicles Recompiled" width="720">
</p>

<p align="center">
  An in-development effort to bring the Xenoblade Chronicles games to PC through native recompilation.
</p>

## Project status

**Active development | Windows first | No public release**

The first target is **Xenoblade Chronicles: Definitive Edition**. Development is ongoing in a private workspace; this public repository currently contains project information, licensing and artwork rather than the working source.

**There is no public build, supported installer or release date.** The current development build is experimental and not ready for general use. The project's source code is intended to be published here once the first game is ready for public testing and play.

### Progress on the first game

The team is working toward a fully native, ahead-of-time-compiled Windows application. A modified compatibility runtime has been used to support development, while a separate native host is being built to replace its remaining platform and graphics dependencies.

Progress demonstrated internally so far includes:

- A static ARM64 recompilation pipeline and host runtime under active development.
- Native hooks for selected game SDK services and an evolving native graphics implementation using Vulkan.
- The ability to render the title screen, navigate menus with scripted input, load a save, and reach a rendered in-game scene in Colony 9.
- Ongoing work on shader translation, GPU command handling, texture formats, rendering accuracy, input, audio and runtime correctness.

**This does not mean the game is playable or complete.** Current in-game rendering has visible issues, including missing party characters and incorrect grass/foliage. Performance is also far below a release-ready target. Some services remain unfinished or transitional, and substantial validation is still required. The long-term goal is to run without Suyu or another emulation layer at play time; that goal has **not** yet been achieved.

## Roadmap

The order below reflects current priorities, not release milestones with dates.

1. **Native Windows foundation (in progress):** Continue replacing transitional platform and graphics functionality with native runtime components, improve shader and render-path correctness, and address outstanding scene-rendering problems.
2. **Gameplay compatibility and performance:** Validate more areas and game systems, stabilize input, audio, saves and memory management, and improve frame pacing and runtime performance.
3. **Launcher and local build workflow:** Resume work on a launcher that builds an installation locally from user-supplied files, with support for appropriate game updates and downloadable content. Launcher work is not the current priority.
4. **Public testing and source release:** Publish source and instructions once the first target is sufficiently ready for people to test. No date is committed.
5. **Additional games and platforms:** Investigate support for other Xenoblade Chronicles titles and, in the future, Linux. These are plans, not working ports or compatibility guarantees.

### Future game support

The project is focused on **Xenoblade Chronicles: Definitive Edition** first. Longer-term targets are:

- Xenoblade Chronicles 2
- Xenoblade Chronicles 3
- Xenoblade Chronicles X: Definitive Edition
- Potentially Xenoblade Chronicles 2: Torna – The Golden Country as a standalone title

These games are **not currently supported**. Linux support is also a future goal, with Windows development taking priority.

## What to expect

For now, this repository is a place to follow the project's direction and future announcements. There is no downloadable game build, public installation procedure, or contribution-ready source tree yet. Development progress and a public testing process will be shared when they are ready.

The intended launcher will use game files supplied by the user to build a local installation. **This project does not distribute game files, firmware or keys.**

## How this project is developed

In the interest of transparency: large language models (LLM coding assistants such as Claude and Codex) are involved in this project's development and help write and analyse code. The lead developer is a working programmer who sets the goals and architecture, directs and reviews the assistants' work, tests the results, and makes the final decisions. The assistants are tools under that direction, not a substitute for it.

<p align="center">
  <img src="assets/icon.png" alt="Xenoblade Chronicles Recompiled icon" width="112">
</p>

## License

The original source code of this project is licensed under the GNU General Public License, version 3 or (at your option) any later version (`GPL-3.0-or-later`); see [LICENSE](LICENSE). The license covers only the project's own source code. It does not cover game code or assets, files you supply (game dumps, updates, downloadable content, firmware, keys, saves), or anything generated from them, and third-party components keep their own licenses. Read [LICENSE-SCOPE.md](LICENSE-SCOPE.md) for the details.
