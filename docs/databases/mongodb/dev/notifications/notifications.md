# Database: notifications

[← Voltar ao índice](../README.md)

> **2** collection(s) · ~**606,476** documentos estimados

## Sumário

| Collection | Documentos (est.) |
|------------|-------------------|
| [Notification](#notification) | 28,680 |
| [UserNotification](#usernotification) | 577,796 |

---

## Notification

**Documentos (estimado):** 28,680

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `description` | Object | 100% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `description.days_exceeded` | null | 0% | Dias excedidos em relação ao SLA. |
| `description.name` | String | 100% | Nome do produto/item na notificação. |
| `description.notification_type` | String | 100% | Tipo da notificação (ex: estoque, SLA). |
| `description.platform` | null | 0% | Plataforma relacionada à notificação. |
| `description.status` | String | 100% | Status reportado na notificação. |
| `description.stock_quantity` | null | 0% | Quantidade de estoque reportada na notificação. |
| `description.type_of_alert` | String | 100% | Tipo de alerta da notificação. |
| `groups` | Array<String> | 100% | Grupos de usuários que devem receber a notificação. |
| `product_id` | String | 100% | ID do produto relacionado. |
| `updated_at` | String | 100% | Data em que o registro foi atualizado. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## UserNotification

**Documentos (estimado):** 577,796

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `notification_id` | String | 100% | ID da notificação original. |
| `read` | Boolean | 100% | Indica se a notificação foi lida. |
| `read_at` | String | 18% | Data/hora em que a notificação foi lida. |
| `updated_at` | String | 100% | Data em que o registro foi atualizado. |
| `user_id` | String | 100% | ID do usuário associado. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `user_id_1_read_1_autocreated` | `user_id` (ASC), `read` (ASC) | — |

---
