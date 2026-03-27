# Database: partners_events

[← Voltar ao índice](../README.md)

> **2** collection(s) · ~**23** documentos estimados

## Sumário

| Collection | Documentos (est.) |
|------------|-------------------|
| [audit_logs](#audit_logs) | 21 |
| [events](#events) | 2 |

---

## audit_logs

**Documentos (estimado):** 21

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `action` | String | 100% | Ação realizada pelo usuário. |
| `data` | Object | 100% | Dados do payload do evento. |
| `data.args` | Array<Object> | 100% | Argumentos da função. |
| `data.args[].Body` | String | 100% | — |
| `data.args[].MD5OfBody` | String | 100% | — |
| `data.args[].MessageId` | String | 100% | — |
| `data.args[].ReceiptHandle` | String | 100% | — |
| `data.function_name` | String | 100% | Nome da função executada. |
| `data.kwargs` | Object | 100% | Keyword arguments da função. |
| `data.module` | String | 100% | Módulo do sistema. |
| `duration_seconds` | Double | 100% | Duração da execução (segundos). |
| `error` | null | 0% | Mensagem de erro (se houver). |
| `ip_address` | null | 0% | Endereço IP de origem. |
| `log_id` | String | 100% | ID único do log. |
| `status` | String | 100% | Status utilizado para o ciclo de vida de um produto, acompanhando do nascimento até a integração com a VTEX/outros integradores. |
| `timestamp` | Date | 100% | Data/hora do evento. |
| `user_agent` | null | 0% | User-Agent da requisição. |
| `user_id` | null | 0% | ID do usuário associado. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `action_1` | `action` (ASC) | — |
| `status_1` | `status` (ASC) | — |
| `timestamp_1` | `timestamp` (ASC) | — |
| `user_id_1` | `user_id` (ASC) | — |

---

## events

**Documentos (estimado):** 2

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `aggregate_id` | String | 100% | ID do agregado (event sourcing). |
| `aggregate_type` | String | 100% | Tipo do agregado (event sourcing). |
| `data` | Object | 100% | Dados do payload do evento. |
| `data.args` | Array<Object> | 100% | Argumentos da função. |
| `data.args[].Body` | String | 100% | — |
| `data.args[].MD5OfBody` | String | 100% | — |
| `data.args[].MessageId` | String | 100% | — |
| `data.args[].ReceiptHandle` | String | 100% | — |
| `data.duration_seconds` | Double | 50% | Duração da execução (segundos). |
| `data.ended_at` | String | 50% | Data/hora de término da execução. |
| `data.function_name` | String | 100% | Nome da função executada. |
| `data.kwargs` | Object | 100% | Keyword arguments da função. |
| `data.module` | String | 100% | Módulo do sistema. |
| `data.process_id` | String | 100% | ID do processo. |
| `data.status` | String | 50% | Status da execução. |
| `event_id` | String | 100% | ID único do evento. |
| `event_type` | String | 100% | Tipo do evento. |
| `event_version` | Integer | 100% | Versão do esquema do evento. |
| `metadata` | Object | 100% | Metadados do evento. |
| `metadata.causation_id` | String | 50% | ID de causalidade (evento que originou este). |
| `metadata.correlation_id` | String | 100% | ID de correlação para rastreio entre serviços. |
| `metadata.ip_address` | null | 0% | Endereço IP de origem. |
| `metadata.user_agent` | null | 0% | User-Agent da requisição. |
| `metadata.user_id` | null | 0% | ID do usuário que originou o evento. |
| `sequence` | Integer | 100% | Número sequencial do evento no agregado. |
| `timestamp` | Date | 100% | Data/hora do evento. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `aggregate_id_1` | `aggregate_id` (ASC) | — |
| `aggregate_id_1_sequence_1` | `aggregate_id` (ASC), `sequence` (ASC) | — |
| `aggregate_type_1` | `aggregate_type` (ASC) | — |
| `event_type_1` | `event_type` (ASC) | — |
| `metadata.correlation_id_1` | `metadata.correlation_id` (ASC) | — |
| `timestamp_1` | `timestamp` (ASC) | — |

---
