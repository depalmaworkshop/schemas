# Schema Contribution

## Description

[Provide a brief description of the schema(s) being added or modified in this PR]

## Type of Change

- [ ] New schema for Commons (adding Artifacts, Co-Goods, Libraries, etc.)
- [ ] Schema update (non-breaking change to existing schema)
- [ ] Breaking change (modification that breaks compatibility)
- [ ] Documentation update
- [ ] Bug fix in schema definition
- [ ] Metaschema update

## Schema Details

**Schema Name**: `schema-artifact-color` (example)  
**Version**: 1.0.0  
**Purpose**: [What aspect of our Commons this schema defines]

## Changes Made

- [List the specific Commons schemas added/modified]
- [Include key structures for Artifacts, Co-Goods, etc.]
- [Mention how this helps our community collaborate]

## Validation

- [ ] Schema validates against the metaschema
- [ ] JSON syntax is valid
- [ ] All required fields are present
- [ ] Tested with example data

### Validation Output
```bash
# Paste validation command output here
ajv validate -s metaschema/versions/1.0.0/schema.json -d [your-schema]
```

## Checklist

- [ ] My schema follows the naming conventions (`schema-artifact-{specific}`)
- [ ] I have included all required fields from the metaschema
- [ ] I have added the CC BY-SA 4.0 license to my schema
- [ ] I have written clear descriptions for all fields
- [ ] I have added appropriate attribution for contributors
- [ ] My schema file is in the correct folder structure
- [ ] I have updated the README.md if adding a new schema category

## License Compliance

- [ ] I agree to license this schema under CC BY-SA 4.0
- [ ] Any referenced standards or specifications are properly attributed
- [ ] No proprietary or incompatibly-licensed content is included

## Examples (if applicable)

```json
// Add an example of your Commons schema in use
// For example, a color artifact:
{
  "name": "ocean-blue",
  "hex": "#006994",
  "pantone": "3155 C"
}
```

## Additional Notes

[Any additional information that reviewers should know]

## Related Issues

Fixes #[issue number]