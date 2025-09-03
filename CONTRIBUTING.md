# Contributing to DePalma Workshop Schemas

Thank you for your interest in contributing to our community! Schemas help us define structures for everything in DePalma Workshop, enabling our community to collaborate properly and build our Commons together.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Development Setup](#development-setup)
- [Submitting Changes](#submitting-changes)
- [Style Guidelines](#style-guidelines)
- [Community](#community)

## Code of Conduct

Please note that this project is released with a [Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

## Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally
3. **Create a branch** for your schema
4. **Create your schema** following our guidelines
5. **Push to your fork** and submit a pull request

## How to Contribute

### 📝 Creating New Schemas

We welcome new schemas that help define our Commons! Schemas help us structure Commons such as:
- **Artifacts** - Colors, materials, textiles, avatars, and other creative elements
- **Co-Goods** - Collaborative creations from our community
- **Libraries** - Shared resources and knowledge

Your contributions help our entire community work together with shared understanding and quality.

Note: Developers working on the Workshop Engine will find additional technical documentation in the engine repository.

### 🐛 Reporting Issues

Before creating issue reports, please check existing issues to avoid duplicates. When creating an issue report, please include:

- A clear and descriptive title
- The schema file(s) affected
- Description of the problem
- Your proposed solution (if any)

### 💡 Suggesting Improvements

Schema improvements are welcome! Please provide:

- A clear and descriptive title
- The motivation for this improvement
- How it helps our Commons
- Examples of use in the community

### 📖 Improving Documentation

Documentation improvements are always welcome! This includes:

- Adding examples to schemas
- Clarifying descriptions
- Improving README files
- Adding use case documentation

## Development Setup

### Prerequisites

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/) (optional, for schema validation)
- Text editor with JSON support (VS Code recommended)
- Basic understanding of [JSON Schema](https://json-schema.org/)

### Installation

```bash
# Clone your fork
git clone https://github.com/your-username/schemas.git
cd schemas

# Create a branch for your schema
git checkout -b schema/your-schema-name

# Optional: Install validation tools
npm install -g ajv-cli
```

### Creating Your Schema

```bash
# Create your schema folder structure
mkdir -p schema-artifact-color/versions/1.0.0/

# Create your schema file
touch schema-artifact-color/versions/1.0.0/schema.json

# Edit your schema (example with VS Code)
code schema-artifact-color/versions/1.0.0/schema.json
```

### Running Validation

```bash
# Validate against metaschema
ajv validate -s metaschema/versions/1.0.0/schema.json \
             -d schema-artifact-color/versions/1.0.0/schema.json

# Check JSON syntax
python -m json.tool your-schema.json
```

## Submitting Changes

### Pull Request Process

1. **Ensure your schema validates** against the metaschema
2. **Include all required fields** as defined in the metaschema
3. **Add CC BY-SA 4.0 license** to your schema
4. **Write clear descriptions** for all fields
5. **Update this README** if adding a new schema category

### Schema Requirements

Your schema MUST include:

```json
{
  "$schema": "https://raw.githubusercontent.com/depalmaworkshop/schemas/main/metaschema/versions/1.0.0/schema.json",
  "$id": "https://raw.githubusercontent.com/depalmaworkshop/schemas/main/schema-artifact-color/versions/1.0.0/schema.json",
  "name": "schema-artifact-color",
  "title": "Color Artifact Schema",
  "version": {
    "schema_version": "1.0.0"
  },
  "license": {
    "type": "CC BY-SA 4.0",
    "url": "https://creativecommons.org/licenses/by-sa/4.0/"
  }
}
```

### Commit Message Format

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: New schema or major addition
- `fix`: Schema correction
- `docs`: Documentation changes
- `refactor`: Schema restructuring
- `chore`: Maintenance tasks

**Example:**
```
feat(artifact): add textile material schema

Added comprehensive schema for textile materials including:
- Fiber composition
- Weave patterns  
- Care instructions
- Sustainability metrics

Closes #45
```

## Style Guidelines

### Schema Style

- Use **lowercase kebab-case** for schema names
- Write **clear, concise descriptions** for every field
- Include **examples** where helpful
- Follow **JSON Schema best practices**
- Maintain **consistent indentation** (2 spaces)

### Documentation Style

- Use **clear, simple language**
- Include **practical examples**
- Keep **line length under 80 characters** in descriptions
- Use **proper markdown formatting** in README files

### Naming Conventions

```
Schema folders:  schema-artifact-{specific}  (e.g., schema-artifact-color)
                schema-commons-{specific}   (e.g., schema-commons-material)
Schema files:    schema.json
Version folders: versions/{major}.{minor}.{patch}/
```

Examples:
- `schema-artifact-color/` - For color artifacts
- `schema-artifact-textile/` - For textile artifacts  
- `schema-commons-material/` - For material definitions

## Community

### Getting Help

- **GitHub Issues**: For questions and discussions
- **Pull Request Comments**: For specific schema feedback
- **DePalma Workshop Website**: [depalmaworkshop.com](https://depalmaworkshop.com)

### Review Process

All schema submissions are reviewed by the DePalma Workshop Schema Committee for:

1. **Quality & Consistency** - Validates against metaschema and follows standards
2. **Community Alignment** - Supports our Commons and collaborative goals
3. **Documentation Clarity** - Clear descriptions that help our community
4. **License Compliance** - CC BY-SA 4.0 to keep our Commons open

### Recognition

Contributors will be recognized in:
- Schema attribution fields
- README.md contributors section
- Release notes

## License Agreement

**Important**: By contributing, you agree that your contributions will be licensed under [CC BY-SA 4.0](LICENSE). This ensures all schemas remain open and accessible to the DePalma Workshop community.

---

Thank you for contributing to DePalma Workshop! 🎉