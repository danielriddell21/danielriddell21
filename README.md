# Dan Riddell

Go developer, came up through C#/.NET. I build small libraries, terminal tools, and a pile of
games and simulations — most shipping through my own Homebrew tap, a couple as web apps.

<p>
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go">
  <img src="https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt="C#">
  <img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white" alt="Terraform">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white" alt="OpenTelemetry">
</p>

## How the projects fit together

Built using the `require` edges between my Go modules:

```mermaid
flowchart LR
    pandemonium --> crucible
    nemesis --> crucible
    vivarium --> crucible
    galapagos --> crucible
    hegemony --> crucible
    gambit --> crucible
    rubix --> crucible

    crucible --> narrata
    crucible --> ordinex
    hegemony --> galapagos
    galapagos --> gambit
    galapagos --> rubix

    tf-plan-summary-action --> unum

    classDef game fill:#1f6feb,stroke:#0d1117,color:#fff;
    classDef tool fill:#862373,stroke:#0d1117,color:#fff;
    classDef lib fill:#238636,stroke:#0d1117,color:#fff;
    classDef action fill:#863623,stroke:#0d1117,color:#fff;
    class pandemonium,nemesis,vivarium,galapagos,hegemony game;
    class unum tool;
    class gambit,rubix,crucible,narrata,ordinex lib;
    class tf-plan-summary-action action;
```

## Projects

| Project | What it is | Tags |
| --- | --- | --- |
| [unum](https://github.com/danielriddell21/unum) | JSON, diff & hash dev toolkit | 🖥️ · 🌐 · 🍺 · 🐳 |
| [pandemonium](https://github.com/danielriddell21/pandemonium) | Procedurally generated, Wolfenstein-3D-style raycaster FPS | 🖥️ · 🍺 |
| [tf-plan-summary-action](https://github.com/danielriddell21/tf-plan-summary-action) | GitHub Action that posts Terraform plan summaries onto PRs | Action |

<details>
<summary><b>Everything else…</b></summary>

| Project | What it is | Tags |
| --- | --- | --- |
| [fiat-lux](https://github.com/danielriddell21/fiat-lux) | An AI agent dropped into an empty world with the tools of creation | 🖥️ · 🌐 · 🍺 · 🐳 |
| [tracearr](https://github.com/danielriddell21/tracearr) | OpenTelemetry trace middleware for the *arr stack | 🖥️ · 🐳 |
| [crucible](https://github.com/danielriddell21/crucible) | Shared Ebitengine engine behind the games: worldgen, raycaster, menus, audio, HUD | 📚 |
| [nemesis](https://github.com/danielriddell21/nemesis) | First-person stealth raycaster: evade an Alien-Isolation-style hunter aboard a derelict station | 🖥️ · 🍺 |
| [galapagos](https://github.com/danielriddell21/galapagos) | Framework for watching learning algorithms evolve in real time | 📚 · 🖥️ · 🍺 |
| [factorio-mcp](https://github.com/danielriddell21/factorio-mcp) | MCP server that lets an LLM play Factorio 2.0 over RCON | 🖥️ · 🍺 |
| [toolshed](https://github.com/danielriddell21/toolshed) | Eleven terminal toys in one binary: fractals, sims, a maze solver | 🖥️ · 🍺 |
| [hegemony](https://github.com/danielriddell21/hegemony) | Territory-war sim where competing algorithms fight over a grid | 🖥️ · 🍺 |
| [vivarium](https://github.com/danielriddell21/vivarium) | 2D ecosystem where behaviour evolves through tiny neural nets | 🖥️ · 🍺 |
| [gambit](https://github.com/danielriddell21/gambit) | Two chess engines play each other; a testbed for search strategies | 📚 · 🖥️ · 🍺 |
| [rubix](https://github.com/danielriddell21/rubix) | Rubik's cube solver, nine ways, with a LEGO Mindstorms EV3 driver | 📚 · 🖥️ · 🍺 |
| [narrata](https://github.com/danielriddell21/narrata) | Embedded, dependency-free narration runtime for Go | 📚 · 🖥️ · 🍺 |
| [retrievium](https://github.com/danielriddell21/retrievium) | Generic search algorithms behind one small interface | 📚 |
| [ordinex](https://github.com/danielriddell21/ordinex) | Generic sorting algorithms behind one small interface | 📚 |

</details>

<sub>Tags: 🖥️ CLI · 🌐 Web · 📚 Library (Go module) · Action (GitHub Action) · 🍺 Homebrew · 🐳 Docker</sub>

The TUIs are built on [Bubble Tea](https://github.com/charmbracelet/bubbletea); the games and sims
run on [Ebitengine](https://ebitengine.org). Most CLIs install from my
[Homebrew tap](https://github.com/danielriddell21/homebrew-tap):

```sh
brew install danielriddell21/tap/<tool>
```

**unum** and **fiat-lux** also run as web apps at [riddellious.dev](https://riddellious.dev), whose
infrastructure I keep as Terraform in
[riddellious-dev](https://github.com/danielriddell21/riddellious-dev).

## Elsewhere

[GitHub](https://github.com/danielriddell21) · [LinkedIn](https://uk.linkedin.com/in/daniel-riddell-418795178)
