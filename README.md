<div align="center">
  <img src="public/logo.png" width="144" height="144" alt="ForgePilot" />

  <h1>ForgePilot</h1>

  <p><strong>AI-powered engineering workspace for building, debugging, and shipping software.</strong></p>

  <p>
    <a href="https://forgepilot.dev">Website</a>
    ·
    <a href="https://forgepilot.dev/docs">Documentation</a>
    ·
    <a href="https://github.com/your-org/forgepilot">Repository</a>
  </p>

  <p>
    <img src="https://img.shields.io/badge/version-0.1.0-blue" alt="version" />
    <img src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey" alt="platform" />
    <img src="https://img.shields.io/badge/AI-local%20%26%20cloud-purple" alt="AI" />
    <img src="https://img.shields.io/badge/license-Apache--2.0-green" alt="license" />
  </p>
</div>

---

## What is ForgePilot?

**ForgePilot** is a native AI-assisted development workspace designed to bring the most important parts of the software development workflow into one place.

Instead of switching constantly between a terminal, editor, Git client, browser, and AI coding assistant, ForgePilot combines them into a single engineering environment.

It provides:

* A native terminal
* AI coding assistance
* Project-aware agents
* Source control
* Code editing
* File navigation
* Local application previews
* Multiple workspaces
* Customizable developer environments

ForgePilot can work with **cloud AI providers or local models**, allowing developers to choose how their code and prompts are processed.

The application is built around a native desktop architecture using **Tauri and Rust**, with a modern web-based interface.

---

## Why ForgePilot?

Modern development often looks like this:

```text
Terminal
   ↓
Code Editor
   ↓
Git Client
   ↓
Browser
   ↓
AI Assistant
   ↓
Documentation
   ↓
Back to Terminal
```

ForgePilot brings these workflows together:

```text
                ┌──────────────────────┐
                │     ForgePilot AI    │
                └──────────┬───────────┘
                           │
        ┌──────────────────┼──────────────────┐
        ↓                  ↓                  ↓
   Code Editor          Terminal             Git
        │                  │                  │
        └──────────────────┼──────────────────┘
                           ↓
                    Project Workspace
                           │
                           ↓
                    Local Web Preview
```

The goal is simple:

> **Give developers one workspace where they can understand, modify, run, test, and ship their projects.**

---

# Core Capabilities

## 🖥️ Native Development Terminal

ForgePilot includes a terminal designed specifically for software development.

### Terminal capabilities

* Multiple terminal sessions
* Tabbed workflows
* Horizontal and vertical splits
* Background process execution
* ANSI and true-color support
* Search within terminal output
* Clickable URLs
* Shell-aware command execution
* File drag-and-drop
* Persistent working directories
* Cross-platform shell support

Supported environments include:

* Bash
* Zsh
* Fish
* PowerShell
* Windows Command Prompt
* WSL environments

The terminal is backed by a native PTY layer instead of relying on a browser-only terminal implementation.

---

# ✨ AI Engineering Assistant

ForgePilot includes an AI workspace that understands the project you are currently working on.

Instead of treating every prompt as an isolated conversation, the agent can operate against the current development environment.

### Project-aware operations

The AI can:

* Inspect project files
* Search the repository
* Understand directory structure
* Read source files
* Modify files
* Create new files
* Apply targeted edits
* Review changes
* Execute approved commands
* Inspect command output
* Run background processes
* Work through multi-step tasks

Example workflow:

```text
Developer:
"Add authentication to this application."

        ↓

ForgePilot Agent

        ↓

Analyze project structure
        ↓
Identify existing API architecture
        ↓
Inspect authentication dependencies
        ↓
Create implementation plan
        ↓
Modify backend
        ↓
Update frontend
        ↓
Run tests
        ↓
Show changes for review
```

---

# 🧠 Agent Workflows

ForgePilot supports different modes of AI-assisted development.

### Ask Mode

Use the AI for questions, explanations, debugging, and code exploration.

### Plan Mode

For larger tasks, the agent first creates an implementation plan before making changes.

Example:

```text
Task
 ↓
Repository analysis
 ↓
Implementation plan
 ↓
Developer approval
 ↓
Code changes
 ↓
Validation
 ↓
Review
```

### Agent Mode

The agent can use development tools to work through a task while respecting approval boundaries.

Operations can include:

* `read`
* `write`
* `edit`
* `search`
* `grep`
* `glob`
* `terminal`
* `process`

Sensitive operations can require explicit developer approval.

---

# 🔌 AI Provider Support

ForgePilot is designed around provider flexibility.

Developers can connect their own AI infrastructure instead of being locked into a single provider.

Potential providers include:

* OpenAI
* Anthropic
* Google Gemini
* DeepSeek
* Mistral
* Groq
* xAI
* OpenRouter
* Custom OpenAI-compatible APIs

### Local AI

ForgePilot can also connect to local inference servers such as:

* Ollama
* LM Studio
* MLX
* Other OpenAI-compatible local endpoints

This makes it possible to build workflows where source code remains within the developer's chosen environment.

---

# 📝 Code Workspace

The built-in editor provides a focused environment for working directly on project files.

### Editor capabilities

* JavaScript / TypeScript
* React
* Vue
* Svelte
* Python
* Rust
* Go
* Java
* C / C++
* HTML
* CSS
* JSON
* Markdown
* YAML
* SQL

Additional capabilities include:

* Syntax highlighting
* Autocomplete
* Diagnostics
* Formatting
* Code navigation
* Search and replace
* Multi-file editing
* Markdown preview
* Vim-style editing
* AI-assisted editing

---

# 🔍 AI Code Changes

AI-generated modifications are presented as reviewable changes rather than silently modifying the project.

Developers can inspect:

```text
┌─────────────────────────────────────┐
│ auth/service.ts                     │
├─────────────────────────────────────┤
│ + Added token validation            │
│ + Added session handling            │
│ - Removed duplicated middleware     │
│                                     │
│ [Accept] [Reject] [Review]          │
└─────────────────────────────────────┘
```

This makes AI-assisted development easier to review and control.

---

# 🌳 Git & Source Control

Git workflows are integrated directly into the development workspace.

### Supported workflows

* View modified files
* Stage changes
* Unstage changes
* Commit changes
* Push changes
* Switch branches
* Create branches
* Inspect commit history
* Search commits
* Review diffs
* Track merge history

ForgePilot also provides a visual representation of repository history.

```text
main ─────●────●────●────────●
           \          \
            ●────●     ●────●
            feature    release
```

---

# 📁 Project Explorer

The project explorer provides a fast way to navigate large repositories.

Features include:

* File tree navigation
* Fuzzy search
* Quick file opening
* Inline rename
* Context actions
* Live filesystem updates
* File attachments for AI conversations
* Drag-and-drop support

Files can be attached directly to an AI task so the agent can work with the relevant project context.

---

# 🌐 Local Application Preview

ForgePilot can detect locally running development servers and provide a preview workspace.

For example:

```text
npm run dev
      ↓
localhost:5173
      ↓
ForgePilot detects server
      ↓
Preview opens inside workspace
```

This is useful for frontend and full-stack development because developers can edit code, run the application, and inspect the result without constantly switching applications.

---

# 🧩 Workspaces

A workspace represents a complete development context.

A workspace can preserve:

* Open files
* Terminal sessions
* Working directories
* Split layouts
* Running development servers
* Project context
* AI conversation context

This makes it easier to return to a project exactly where you left it.

---

# 🎨 Developer Customization

ForgePilot is designed to be highly customizable.

Developers can customize:

* Application theme
* Editor theme
* Terminal appearance
* Font preferences
* Backgrounds
* Panel layout
* Workspace configuration

Themes can be created, exported, imported, and shared.

---

# 🔐 Privacy by Design

ForgePilot does not require a mandatory developer account for local development workflows.

AI credentials are stored using the operating system's secure credential storage.

The architecture is designed around:

* Local-first development
* User-controlled AI providers
* Explicit tool permissions
* No unnecessary telemetry
* Local model support
* Transparent AI operations

Your development environment should remain under your control.

---

# ⚙️ Architecture

ForgePilot uses a native desktop architecture:

```text
┌─────────────────────────────────────────┐
│              ForgePilot UI              │
│                                         │
│ React + TypeScript + Vite               │
│ Editor · Explorer · Git · AI · Preview  │
└───────────────────┬─────────────────────┘
                    │
                    │ Tauri IPC
                    ↓
┌─────────────────────────────────────────┐
│             Native Runtime              │
│                                         │
│ Rust + Tauri                            │
│                                         │
│ PTY · Filesystem · Processes · Git      │
└───────────────────┬─────────────────────┘
                    │
        ┌───────────┼───────────┐
        ↓           ↓           ↓
      Shell       Git       Local Apps
```

### Main technologies

* Tauri 2
* Rust
* React
* TypeScript
* Vite
* Tailwind CSS
* xterm.js
* CodeMirror
* Zustand

---

# 🚀 Installation

Download the latest version from the project's releases page.

### Windows

ForgePilot supports:

* PowerShell
* Windows PowerShell
* CMD
* WSL

WSL environments can be treated as development workspaces rather than simply launching them as child processes.

### macOS

Native desktop builds are available for supported macOS architectures.

### Linux

Linux packages can be distributed through formats such as:

* AppImage
* `.deb`
* `.rpm`

Distribution-specific installation methods may also be provided as the project evolves.

---

# 🤖 Configure AI

Open:

```text
Settings
   ↓
AI Providers
   ↓
Select Provider
   ↓
Configure Credentials
```

For local inference:

```text
ForgePilot
    ↓
Local AI Endpoint
    ↓
Ollama / LM Studio / MLX
    ↓
Local Model
```

For cloud providers, developers can configure their own API credentials.

---

# 🛠️ Build From Source

## Requirements

Install:

* Rust stable
* Node.js 22+
* pnpm
* Tauri platform prerequisites

### Install dependencies

```bash
pnpm install
```

### Development

```bash
pnpm tauri dev
```

### Production build

```bash
pnpm tauri build
```

---

# ✅ Development Checks

Run the frontend checks:

```bash
pnpm lint
pnpm check-types
pnpm test
```

Run Rust checks:

```bash
cd src-tauri

cargo clippy --all-targets --locked -- -D warnings
```

Run Rust tests:

```bash
cargo test --locked
```

---

# 🧱 Project Structure

A simplified project layout:

```text
forgepilot/
├── src/
│   ├── components/
│   ├── features/
│   ├── editor/
│   ├── terminal/
│   ├── explorer/
│   ├── git/
│   ├── ai/
│   └── workspace/
│
├── src-tauri/
│   ├── src/
│   ├── commands/
│   ├── services/
│   └── main.rs
│
├── public/
├── docs/
├── package.json
├── vite.config.ts
└── README.md
```

---

# 🗺️ Roadmap

ForgePilot is being developed around a simple objective: make AI-assisted engineering feel like a natural part of the development environment.

Planned areas include:

* Improved multi-agent workflows
* Better repository indexing
* Advanced code intelligence
* Remote development
* Container workflows
* Improved debugging tools
* Test-aware agents
* CI/CD integrations
* Plugin architecture
* Team workspaces
* Advanced project memory
* More local model integrations

---

# 🤝 Contributing

Contributions are welcome.

You can contribute by:

* Reporting bugs
* Opening feature requests
* Improving documentation
* Submitting pull requests
* Creating integrations
* Improving developer tooling
* Building extensions

Before contributing, review the project's contribution guidelines and development documentation.

---

# 📄 License

ForgePilot is released under the **Apache License 2.0**.

See the `LICENSE` file for the complete license text.

---

<div align="center">

### Build faster. Understand more. Ship with confidence.

**ForgePilot — your AI-native engineering workspace.**

</div>
