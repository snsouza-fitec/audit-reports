# Audit Reports & Technical Documentation

Repositório centralizado de relatórios de auditoria e documentações técnicas de infraestrutura.

## Estrutura

```
├── reports/               # Relatórios de auditoria
│   └── security/          # Auditorias de segurança
└── docs/                  # Documentações técnicas
    └── databases/         # Bancos de dados
        └── mongodb/       # MongoDB (schemas, índices, etc.)
```

## Convenções

- **Relatórios:** `AAAA-MM-descricao-curta.md` (ex: `2026-03-hardcoded-credentials.md`)
- **Documentações:** nome descritivo em kebab-case (ex: `dev-schema.md`)
- Todos os documentos em **Markdown**
- Datas no formato **ISO 8601** (`AAAA-MM-DD`)

## Índice de Relatórios

### Segurança

| Data | Relatório | Descrição |
|------|-----------|-----------|
| 2026-03 | [Credenciais Hardcoded](reports/security/2026-03-hardcoded-credentials.md) | Verificação de credenciais e dados sensíveis nos repositórios |

## Índice de Documentações

### Bancos de Dados

| Ambiente | Documento | Descrição |
|----------|-----------|-----------|
| DEV | [MongoDB Schema](docs/databases/mongodb/dev-schema.md) | Schema inferido das collections do ambiente de desenvolvimento |


