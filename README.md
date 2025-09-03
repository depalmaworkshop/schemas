# DePalma Workshop Schemas

Repository for our community schemas that define structures throughout all of DePalma Workshop.

## 🎯 What This Does

- **Commons Standards** - Defines schemas for Commons like Co-Goods, Artifacts, Libraries, and more
- **Quality & Collaboration** - Ensures quality and enables collaboration across our entire community  
- **Universal Structures** - From configurations of our Workshop Engine to Artifacts for colors or avatars
- **Open Ecosystem** - Licensed under CC BY-SA 4.0 to keep our Commons open

## 🚀 Quick Start

### Prerequisites
- Git for cloning and contributing
- JSON Schema knowledge (for creating new schemas)
- Text editor with JSON syntax highlighting (recommended)

### Installation
```bash
# Clone this repository
git clone https://github.com/depalmaworkshop/schemas.git

# Navigate to the repository
cd schemas
```

### Basic Usage
```bash
# Validate a schema against the metaschema
# (Requires a JSON Schema validator like ajv-cli)
ajv validate -s metaschema/versions/1.0.0/schema.json -d your-schema.json

# View available schemas
ls -la schema-*/
```

## 🏗️ Architecture

```
Schema Hierarchy:
┌──────────────────────┐    ┌─────────────────────────────┐    ┌──────────────────────┐
│     Metaschema       │───▶│  Specialized Metaschemas    │───▶│   Commons Schemas    │
│ (Foundation for all) │    │ (e.g., metaschema-artifact) │    │  (Colors, Materials) │
└──────────────────────┘    └─────────────────────────────┘    └──────────────────────┘
```

The metaschema defines what all schemas must contain, ensuring quality and consistency across our community.

## 📁 Project Structure

```
schemas/
├── metaschema/              # The foundation metaschema
│   └── versions/
│       └── 1.0.0/
│           └── schema.json  # Foundation for all schemas
├── metaschema-artifact/     # Metaschema for Artifact schemas
│   └── versions/
│       └── 1.0.0/
│           └── schema.json
├── schema-artifact-color/   # Example: Color artifact schema
│   └── versions/
│       └── 1.0.0/
│           └── schema.json
├── CONTRIBUTING.md          # How to contribute schemas
├── LICENSE                  # CC BY-SA 4.0 license
└── README.md                # This file
```

## 📋 Available Schemas

| Schema                      | Description                           | Version | Status |
| --------------------------- | ------------------------------------- | ------- | ------ |
| `metaschema`                | Foundation metaschema for all schemas | 1.0.0   | Stable |
| `metaschema-artifact`       | Metaschema for Artifact schemas       | 1.0.0   | Draft  |
| `schema-artifact-color`     | Schema for color artifacts            | 1.0.0   | Draft  |
| More schemas coming soon... |                                       |         |        |

## 🛠️ Development

### Creating a New Schema

1. **Fork and clone** this repository
2. **Create your schema folder**: `schema-artifact-{specific}/`
3. **Add version folder**: `versions/1.0.0/`
4. **Create schema.json** that validates against the metaschema
5. **Submit a Pull Request** for review

### Schema Requirements

All schemas must:
- Validate against the [metaschema](metaschema/versions/1.0.0/schema.json)
- Include all required fields (see metaschema)
- Be licensed under CC BY-SA 4.0
- Have clear documentation

### Testing Your Schema
```bash
# Install ajv-cli globally (one-time setup)
npm install -g ajv-cli

# Validate your schema
ajv validate -s metaschema/versions/1.0.0/schema.json -d your-schema.json
```

## 📚 Documentation

- **[Contributing Guide](CONTRIBUTING.md)** - How to submit new schemas
- **[Metaschema Documentation](metaschema/versions/1.0.0/README.md)** - Understanding the foundation
- **[DePalma Workshop](https://depalmaworkshop.com)** - Main project website

## 🤝 Contributing

We welcome schema contributions from our community! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for:
- Schema submission process
- Naming conventions
- Review criteria
- License requirements

All contributors must agree to license their schemas under CC BY-SA 4.0.

## 📄 License

This project is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). This means:
- ✅ Free to use commercially
- ✅ Can modify and extend
- ✅ Must give attribution to DePalma Workwear Limited
- ✅ Must share derivatives under same license

See the [LICENSE](LICENSE) file for full details.

---

Built with ❤️ by [DePalma Workshop](https://depalmaworkshop.com)