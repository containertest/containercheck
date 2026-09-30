# RepoScan - pnpm Monorepo

A monorepo for repository scanning tools built with pnpm workspaces.

## 📋 Project Structure 

```
reposcan/
├── packages/
│   └── core/              # Core scanning library
├── apps/
│   └── cli/               # Command-line interface
├── tools/                 # Development tools
├── package.json           # Root package configuration
├── pnpm-workspace.yaml    # Workspace configuration
├── pnpm-lock.yaml         # Dependency lock file
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Node.js >= 18.0.0
- pnpm >= 8.0.0

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/reposcan.git
cd reposcan

# Install dependencies
pnpm install
```

### Available Commands

```bash
# Development mode (all packages)
pnpm dev

# Build all packages
pnpm build

# Run tests
pnpm test

# Lint code
pnpm lint
```

## 📦 Packages

### @reposcan/core
Core scanning functionality and utilities.

```bash
cd packages/core
pnpm dev
```

### @reposcan/cli
Command-line interface for repository scanning.

```bash
cd apps/cli
pnpm build
npm install -g ./dist
reposcan --help
```

## 🔧 Workspace Configuration

The `pnpm-workspace.yaml` defines the workspace structure:
- `packages/*` - Reusable libraries
- `apps/*` - Applications
- `tools/*` - Development tools

## 📝 Features

- ✅ pnpm workspaces for monorepo management
- ✅ TypeScript support
- ✅ ESLint for code quality
- ✅ Prettier for code formatting
- ✅ Parallel task execution

## 🛠️ Development

### Adding a New Package

1. Create directory: `mkdir packages/mypackage`
2. Create `package.json` with package name `@reposcan/mypackage`
3. Add to workspace automatically (pnpm discovers it)
4. Run `pnpm install`

### Using Workspace Dependencies

Reference other workspace packages using workspace protocol:

```json
{
  "dependencies": {
    "@reposcan/core": "workspace:*"
  }
}
```

## 📄 License

MIT

## 👤 Author

Your Name

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

---

**Ready to upload to GitHub!** 🚀
