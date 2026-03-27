# Database: partners_core

[← Voltar ao índice](../README.md)

> **2** collection(s) · ~**763** documentos estimados

## Sumário

| Collection | Documentos (est.) |
|------------|-------------------|
| [product_files](#product_files) | 747 |
| [users](#users) | 16 |

---

## product_files

**Documentos (estimado):** 747

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `bg_url` | String | 100% | URL da imagem BG do produto. |
| `created_at` | Date | 100% | Data de criação do registro na base de dados. |
| `dealer_page` | String | 100% | URL/caminho da página de dealer. |
| `hero_image` | String | 100% | URL ou caminho da imagem principal (hero) do produto. |
| `images` | Array<Object> | 100% | Lista de imagens associadas ao registro. |
| `images[].is_cover_bg_image` | Boolean | 774% | Indica se a imagem é a capa do BG Word. |
| `images[].main` | Boolean | 774% | Indica se é a imagem principal do produto. |
| `images[].name` | String | 774% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `images[].order` | Integer | 774% | Ordem de exibição da imagem. |
| `images[].s3_filename` | String | 774% | Nome do arquivo armazenado no Amazon S3. |
| `model` | String | 100% | Modelo do produto, essencial. Não utilizado na VTEX. |
| `product_details` | Object | 100% | Detalhes do produto. |
| `product_details.category` | String | 100% | Categoria do produto. |
| `product_details.created_at` | Date | 100% | Data de criação do registro. |
| `product_details.family` | String | 100% | Família do produto. |
| `product_details.name` | String | 100% | Nome do produto. |
| `product_details.overview` | String | 100% | Visão geral do produto. |
| `product_details.part_number` | String | 100% | Part number do produto. |
| `product_details.product_type` | String | 100% | Tipo de produto. |
| `product_details.status` | String | 100% | Status do cadastro. |
| `product_details.updated_at` | Date | 100% | Data de atualização do registro. |
| `s3_base_path` | String | 100% | Caminho base no Amazon S3 para os arquivos. |
| `sync_source` | String | 100% | Fonte de sincronização dos dados. |
| `updated_at` | Date | 100% | Data em que o registro foi atualizado. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `model_1` | `model` (ASC) | — |
| `product_details.category_1` | `product_details.category` (ASC) | — |
| `product_details.family_1` | `product_details.family` (ASC) | — |
| `product_details.name_1` | `product_details.name` (ASC) | — |
| `product_details.part_number_1` | `product_details.part_number` (ASC) | — |
| `product_details.product_type_1` | `product_details.product_type` (ASC) | — |

---

## users

**Documentos (estimado):** 16

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `email` | String | 100% | Endereço de e-mail. |
| `username` | String | 100% | Nome de usuário para autenticação. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---
