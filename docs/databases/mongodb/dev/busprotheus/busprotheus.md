# Database: busprotheus

[← Voltar ao índice](../README.md)

> **2** collection(s) · ~**21** documentos estimados

## Sumário

| Collection | Documentos (est.) |
|------------|-------------------|
| [product](#product) | 9 |
| [stock](#stock) | 12 |

---

## product

**Documentos (estimado):** 9

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `codigo_barra_ean` | String | 100% | Código de barras EAN do produto. |
| `codigo_grupo` | String | 100% | Código do grupo no Protheus. |
| `descricao` | String | 100% | Descrição do produto no Protheus. |
| `familia` | String | 100% | Família do produto no Protheus. |
| `modelo` | String | 100% | Modelo do produto no Protheus. |
| `origem` | String | 100% | Origem do produto (nacional/importado). |
| `partnumber` | String | 100% | Part number do produto. |
| `product_line` | String | 100% | Linha do produto. |
| `segmento` | String | 78% | Segmento de mercado. |
| `serial_number` | null | 0% | Número de série. |
| `spec1` | String | 78% | Especificação complementar 1. |
| `spec2` | String | 78% | Especificação complementar 2. |
| `spec3` | String | 78% | Especificação complementar 3. |
| `spec4` | String | 33% | Especificação complementar 4. |
| `spec5` | String | 78% | Especificação complementar 5. |
| `spec6` | String | 56% | Especificação complementar 6. |
| `specs` | String | 100% | Especificações gerais. |
| `tipo` | String | 100% | Tipo do item. |
| `tipo_produto` | String | 100% | Tipo de produto no Protheus. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## stock

**Documentos (estimado):** 12

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `armazem` | String | 100% | Código do armazém. |
| `custo_medio` | Double | 100% | Custo médio unitário do produto. |
| `disponivel` | Double | 100% | Quantidade disponível em estoque. |
| `empenhado` | Double | 100% | Quantidade empenhada (reservada para pedidos). |
| `filial` | String | 100% | Código da filial. |
| `partnumber` | String | 100% | Part number do produto. |
| `pedido` | Double | 100% | Quantidade em pedido de compra. |
| `reservado` | Double | 100% | Quantidade reservada. |
| `saldo` | Double | 100% | Saldo total em estoque. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---
