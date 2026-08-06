# Commit Conventions

Use the Conventional Commits format:

```text
<type>(<scope>): <description>
```

Example:
```text
feat(auth): implement JWT authentication
```

### Types

| Type | Purpose |
|------|---------|
| feat | New feature |
| fix | Bug fix |
| docs | Documentation |
| refactor | Code improvement |
| test | Tests |
| style | Formatting only |
| perf | Performance improvement |
| chore | Maintenance |
| ci | CI/CD changes |
| build | Build configuration |

### Common Scopes

`auth`, `user`, `chat`, `upload`, `documents`, `history`, `frontend`, `backend`, `api`, `database`, `ai`, `rag`, `docker`, `ui`, `config`, `security`, `deployment`, `chromadb`, `ollama`

### Rules

- Keep the subject under **72 characters**.
- Use the **imperative mood** (e.g. `add`, `fix`, `implement`).
- One logical change per commit.
- Reference related issues when applicable.

Example:
```text
feat(chat): add source citations

Closes #24
```

### Avoid

❌ `update`, `changes`, `fix`, `done`, `test`, `latest`, `backend update`, `frontend changes`
