# Database: logs

[← Voltar ao índice](../README.md)

> **1** collection(s) · ~**1,110** documentos estimados

## Sumário

| Collection | Documentos (est.) |
|------------|-------------------|
| [UserLog](#userlog) | 1,110 |

---

## UserLog

**Documentos (estimado):** 1,110

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `action` | String | 100% | Ação realizada pelo usuário. |
| `area` | String | 100% | Área do sistema onde a ação foi realizada. |
| `date` | String | 100% | Data/hora do evento. |
| `type` | String | 100% | Tipo de registro (ex: info, warning, error). |
| `user` | String | 100% | Usuário que realizou a ação. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---
