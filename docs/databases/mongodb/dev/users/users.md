# Database: users

[← Voltar ao índice](../README.md)

> **2** collection(s) · ~**18** documentos estimados

## Sumário

| Collection | Documentos (est.) |
|------------|-------------------|
| [Permission](#permission) | 14 |
| [UserDatabase](#userdatabase) | 4 |

---

## Permission

**Documentos (estimado):** 14

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## UserDatabase

**Documentos (estimado):** 4

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `changed_password` | Boolean | 100% | Indica se o usuário já alterou a senha temporária. |
| `email` | String | 100% | Endereço de e-mail. |
| `temp_password` | String | 100% | Senha temporária gerada para primeiro acesso ou reset. |
| `username` | String | 100% | Nome de usuário para autenticação. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---
