# dsh-vietnamese-lang

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![DeepSeek Harness](https://img.shields.io/badge/DSH-plugin-brightgreen)](https://github.com/deepseek-ai/deepseek-harness)

Vietnamese language pack for [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) (`dsh`) Web UI.

English | [Tiếng Việt](README.vi.md)

## Features

- **Full Core UI Coverage**: Comprehensive Vietnamese localization across 50 namespaces (Chat, Conversation, Trajectory, Workspace, Settings, Model Selection, Approvals, File Explorer, Terminal, Deliverables, Diff Viewer, Document Previews, and more).
- **Native Integration**: Registered via the official `LocaleRuntime` API and available in `Settings > General > Language`.
- **Automatic Fallback**: Any missing third-party keys gracefully fall back to English.
- **Zero Core Patching**: Runs entirely as a Cordis client plugin via standard ModuleLoader.

## Installation

Install via the `dsh` CLI:

```sh
dsh plugin --profile web add dsh-vietnamese-lang
```

Or from source / GitHub repository:

```sh
dsh plugin --profile web add https://github.com/lphuxhuq/dsh-vietnamese-lang
```

After installation, refresh the DeepSeek Harness Web GUI, go to **Settings (Cài đặt) > General (Cài đặt chung) > Language (Ngôn ngữ)** and choose **Tiếng Việt**.

## Structure

```
dsh-vietnamese-lang/
├── cordis.patch.yml   # Plugin entry for DSH loader
├── index.mjs          # Host entry (no-op)
├── lib/
│   └── client.js      # Client bundle with 50 localized namespaces
├── package.json       # Manifest with dsh.bundle & dsh.client
└── README.md
```

## License

[MIT](LICENSE)
