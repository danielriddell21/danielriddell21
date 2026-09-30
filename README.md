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

### Ecosystem

Solid edges are `require` edges between my Go modules.

```mermaid
flowchart LR
    pandemonium --> crucible
    nemesis --> crucible
    vivarium --> crucible
    galapagos --> crucible
    hegemony --> crucible
    gambit --> crucible
    rubix --> crucible
    autobahn --> crucible

    crucible --> narrata
    hegemony --> galapagos
    galapagos --> gambit
    galapagos --> rubix

    pandemonium --> narrata

    classDef app fill:#1f6feb,stroke:#0d1117,color:#fff;
    classDef lib fill:#238636,stroke:#0d1117,color:#fff;
    class pandemonium,nemesis,vivarium,galapagos,hegemony,autobahn app;
    class gambit,rubix,crucible,narrata lib;
```

### Deployment

Dotted edges are release-time: everything here publishes through
[letsgo](https://github.com/danielriddell21/letsgo), which releases itself the same way.

```mermaid
flowchart TD
    %% Nine repos into one sink lays out as a single wide row. Invisible
    %% links (~~~) fold it into three rows of three; layout only.
    autobahn ~~~ galapagos ~~~ gambit
    hegemony ~~~ narrata ~~~ nemesis
    pandemonium ~~~ rubix ~~~ vivarium

    autobahn & galapagos & gambit -.-> letsgo
    hegemony & narrata & nemesis -.-> letsgo
    pandemonium & rubix & vivarium -.-> letsgo

    classDef ships fill:#863623,stroke:#0d1117,color:#fff;
    classDef tool fill:#862373,stroke:#0d1117,color:#fff;
    class autobahn,galapagos,gambit,hegemony,narrata ships;
    class nemesis,pandemonium,rubix,vivarium ships;
    class letsgo tool;
```

## Projects

| Project | What it is | Tags |
| --- | --- | --- |
| [unum](https://github.com/danielriddell21/unum) | JSON, diff & hash dev toolkit | 🖥️ · 🌐 · 🍺 · 🐳 |
| [pandemonium](https://github.com/danielriddell21/pandemonium) | Procedurally generated, Wolfenstein-3D-style raycaster FPS | 🖥️ · 🍺 |
| [tf-plan-summary-action](https://github.com/danielriddell21/tf-plan-summary-action) | GitHub Action that posts Terraform plan summaries onto PRs | Action |
| [letsgo](https://github.com/danielriddell21/letsgo) | Reproducible release tool for Go, and only Go | 🖥️ |

<details>
<summary><b>Everything else…</b></summary>

| Project | What it is | Tags |
| --- | --- | --- |
| [autobahn](https://github.com/danielriddell21/autobahn) | 3D driving game with a camera-only autopilot, in a procedural British city | 🖥️ · 🍺 |
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
| [merkelbrot](https://github.com/danielriddell21/merkelbrot) | Zoomable, fractal-style visualiser for Merkle DAGs and trees | 📚 · 🖥️ · 🍺 |
| [letsgo-action](https://github.com/danielriddell21/letsgo-action) | GitHub Action that installs letsgo and runs it | Action |
| [letsgo-plugins](https://github.com/danielriddell21/letsgo-plugins) | Plugins for letsgo: ldflags injection, multi-binary archives, Homebrew casks | 🖥️ |
| [retrievium](https://github.com/danielriddell21/retrievium) | Generic search algorithms behind one small interface | 📚 |
| [ordinex](https://github.com/danielriddell21/ordinex) | Generic sorting algorithms behind one small interface | 📚 |

</details>

<sub>Tags: 🖥️ CLI · 🌐 Web · 📚 Library (Go module) · Action (GitHub Action) · 🍺 Homebrew · 🐳 Docker</sub>

The TUIs are built on [Bubble Tea](https://github.com/charmbracelet/bubbletea); most games and sims
run on [Ebitengine](https://ebitengine.org), with autobahn on [raylib](https://www.raylib.com). Most CLIs install from my
[Homebrew tap](https://github.com/danielriddell21/homebrew-tap):

```sh
brew install danielriddell21/tap/<tool>
```

**unum** and **fiat-lux** also run as web apps at [riddellious.dev](https://riddellious.dev), whose
infrastructure I keep as Terraform in
[riddellious-dev](https://github.com/danielriddell21/riddellious-dev).

## letsgo

A release tool for Go, and only Go. One command builds every target and publishes,
recording digests so `letsgo verify` can rebuild the release anywhere and check the
bytes match.

[Read more in the wiki →](https://github.com/danielriddell21/letsgo/wiki)

| Repo | What it is |
| --- | --- |
| [letsgo](https://github.com/danielriddell21/letsgo) | The tool: plan, build, release, verify, diff, tag, yank |
| [letsgo-action](https://github.com/danielriddell21/letsgo-action) | GitHub Action that installs letsgo and runs it |
| [letsgo-plugins](https://github.com/danielriddell21/letsgo-plugins) | Plugins: ldflags injection, multi-binary archives, Homebrew casks |

## Elsewhere

[GitHub](https://github.com/danielriddell21) · [LinkedIn](https://uk.linkedin.com/in/daniel-riddell-418795178)
