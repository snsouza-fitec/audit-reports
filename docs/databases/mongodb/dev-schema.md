# Documentação MongoDB — Ambiente DEV

> Gerado automaticamente em 27/03/2026 09:17:40
>
> Amostra de **50** documentos por collection para inferência de tipos.

## Glossário

| Termo | Descrição |
|-------|-----------|
| **Documentos (estimado)** | Quantidade aproximada de documentos na collection, obtida via metadados internos do MongoDB (sem percorrer todos os registros). Pode ter pequena variação em relação ao total real. |
| **Schema** | Estrutura dos campos inferida automaticamente a partir de uma amostra de documentos. Como o MongoDB é schemaless, o schema real pode variar entre documentos. |
| **Campo** | Nome do campo no documento. Campos aninhados usam notação de ponto (ex: `endereco.cidade`). Campos dentro de arrays usam `[]` (ex: `itens[].preco`). |
| **Tipo(s)** | Tipo de dado do campo. Quando um campo tem tipos diferentes entre documentos, todos os tipos encontrados são listados separados por `\|`. |
| **Presença** | Percentual dos documentos amostrados em que o campo existe com valor **não nulo**. 100% = presente em todos; 0% = sempre nulo ou inexistente na amostra. |
| **DBRef → Collection** | Referência a um documento em outra collection (similar a uma foreign key em bancos relacionais). |
| **Array\<Tipo\>** | Campo do tipo lista (array) cujos elementos são do tipo indicado entre `< >`. |
| **Índices** | Índices criados na collection para otimizar consultas. |
| **ASC / DESC** | Direção do índice: ASC = ascendente, DESC = descendente. |
| **UNIQUE** | Índice que impede valores duplicados no(s) campo(s) indexado(s). |
| **SPARSE** | Índice que ignora documentos onde o campo indexado não existe. |
| **TTL** | Time To Live — índice que auto-remove documentos após o tempo especificado (em segundos). |


## Sumário

> **13** databases · **56** collections · ~**622,642** documentos estimados

- [bgmktplace](#bgmktplace) — 13 collection(s), ~1,173 docs
  - [BgFile](#bgfile) (18)
  - [Category](#category) (53)
  - [Family](#family) (1)
  - [Permission](#permission) (14)
  - [Product](#product) (18)
  - [ProductSpecification](#productspecification) (18)
  - [ProductTimeline](#producttimeline) (0)
  - [ProductType](#producttype) (2)
  - [Sku](#sku) (0)
  - [SpecificationMonitor](#specificationmonitor) (3)
  - [SpecificationNotebook](#specificationnotebook) (15)
  - [UserDatabase](#userdatabase) (33)
  - [UserLog](#userlog) (998)
- [busprotheus](#busprotheus) — 2 collection(s), ~21 docs
  - [product](#product) (9)
  - [stock](#stock) (12)
- [logs](#logs) — 1 collection(s), ~1,110 docs
  - [UserLog](#userlog) (1,110)
- [notifications](#notifications) — 2 collection(s), ~606,476 docs
  - [Notification](#notification) (28,680)
  - [UserNotification](#usernotification) (577,796)
- [parceiros_core](#parceiros_core) — 1 collection(s), ~0 docs
  - [product_files](#product_files) (0)
- [partners_core](#partners_core) — 2 collection(s), ~763 docs
  - [product_files](#product_files) (747)
  - [users](#users) (16)
- [partners_events](#partners_events) — 2 collection(s), ~23 docs
  - [audit_logs](#audit_logs) (21)
  - [events](#events) (2)
- [product](#product) — 22 collection(s), ~9,590 docs
  - [Agency](#agency) (11)
  - [AnymarketCharacteristic](#anymarketcharacteristic) (3)
  - [Bom](#bom) (1,434)
  - [BomDetails](#bomdetails) (10)
  - [Category](#category) (15)
  - [Collection](#collection) (23)
  - [Family](#family) (51)
  - [GoogleGlobalCategory](#googleglobalcategory) (5,595)
  - [HeroDealerUpload](#herodealerupload) (22)
  - [Model](#model) (1,022)
  - [PartnerFiles](#partnerfiles) (199)
  - [Product](#product) (147)
  - [ProductTimeline](#producttimeline) (238)
  - [ProductType](#producttype) (5)
  - [QuickSummary](#quicksummary) (534)
  - [Service](#service) (16)
  - [Settings](#settings) (1)
  - [Sku](#sku) (184)
  - [SlaNotify](#slanotify) (0)
  - [Specification](#specification) (78)
  - [StockSyncDate](#stocksyncdate) (1)
  - [Template](#template) (1)
- [scraping](#scraping) — 4 collection(s), ~3,460 docs
  - [amd_processors](#amd_processors) (574)
  - [intel_processors](#intel_processors) (2,865)
  - [nvidia_video](#nvidia_video) (12)
  - [parceiros_acer](#parceiros_acer) (9)
- [test](#test) — 1 collection(s), ~8 docs
  - [coll](#coll) (8)
- [test_parceiros_core](#test_parceiros_core) — 2 collection(s), ~0 docs
  - [product_files](#product_files) (0)
  - [users](#users) (0)
- [test_partners_core](#test_partners_core) — 2 collection(s), ~0 docs
  - [product_files](#product_files) (0)
  - [users](#users) (0)
- [users](#users) — 2 collection(s), ~18 docs
  - [Permission](#permission) (14)
  - [UserDatabase](#userdatabase) (4)

---

## bgmktplace

### BgFile

**Documentos (estimado):** 18

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `bg_word_filename` | String | 100% |
| `hero_image` | String | 78% |
| `url_dealer_page` | String | 78% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Category

**Documentos (estimado):** 53

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `meta_tag_description` | String | 100% |
| `name` | String | 100% |
| `product_type` | DBRef → `ProductType` | 100% |
| `vtex_id` | Integer | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Family

**Documentos (estimado):** 1

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `All-In-One` | Array<String> | 100% |
| `Desktops` | Array<String> | 100% |
| `Especiais` | Array<String> | 100% |
| `Mini-Desktop` | Array<String> | 100% |
| `Monitores` | Array<String> | 100% |
| `Notebooks` | Array<String> | 100% |
| `Projetores` | Array<String> | 100% |
| `Vestuario` | Array<String> | 100% |
| `_id` | ObjectId | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Permission

**Documentos (estimado):** 14

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `name` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Product

**Documentos (estimado):** 18

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `ad_words_remarketing_code` | null | 0% |
| `alphanumeric_model` | String | 78% |
| `bg_file` | DBRef → `BgFile` | 100% |
| `brand_id` | Integer | 100% |
| `category` | DBRef → `Category` | 78% |
| `created_at` | String | 100% |
| `department_id` | Integer | 100% |
| `description` | String | 78% |
| `description_short` | String | 100% |
| `family` | String | 33% |
| `is_active` | Boolean | 100% |
| `is_complete` | Boolean | 67% |
| `is_visible` | Boolean | 100% |
| `key_words` | String | 100% |
| `link_id` | String | 100% |
| `lomadee_campaign_code` | null | 0% |
| `meta_tag_description` | String | 100% |
| `name` | String | 83% |
| `product_specification` | DBRef → `ProductSpecification` | 100% |
| `product_vtex_id` | Integer | 100% |
| `ref_id` | String | 100% |
| `release_date` | String | 100% |
| `score` | null | 0% |
| `show_without_stock` | Boolean | 100% |
| `sku` | DBRef → `Sku` | 100% |
| `specifications_vtex` | Object | 28% |
| `specifications_vtex.filters` | Array<Object> | 28% |
| `specifications_vtex.filters[].field_id` | Integer | 11% |
| `specifications_vtex.filters[].name` | String | 11% |
| `specifications_vtex.filters[].values` | Array<String> | 11% |
| `specifications_vtex.icons` | Array | 28% |
| `status` | String | 100% |
| `supplier_id` | null | 0% |
| `tax_code` | String | 100% |
| `title` | String | 100% |
| `updated_at` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### ProductSpecification

**Documentos (estimado):** 18

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `specification_monitor` | DBRef → `SpecificationMonitor` | 17% |
| `specification_notebook` | DBRef → `SpecificationNotebook` | 83% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### ProductTimeline

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### ProductType

**Documentos (estimado):** 2

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `name` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Sku

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### SpecificationMonitor

**Documentos (estimado):** 3

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `active_display_area` | Array<String> | 100% |
| `angle_inclination` | Array<String> | 100% |
| `anti_reflective_screen` | Array<String> | 100% |
| `brightness` | Array<String> | 100% |
| `buttons` | Array<String> | 100% |
| `certifications` | Array<String> | 100% |
| `color` | Array<String> | 100% |
| `color_depth` | Array<String> | 100% |
| `color_gamut` | Array<String> | 100% |
| `dimension_with_packaging` | Array<String> | 100% |
| `dimension_without_packaging` | Array<String> | 100% |
| `ean` | Array<String> | 100% |
| `energy_consumption` | Array<String> | 100% |
| `height_adjustment` | Array<String> | 100% |
| `inputs` | Array<String> | 100% |
| `maximum_contrast` | Array<String> | 100% |
| `model` | Array<String> | 100% |
| `mtbf` | Array<String> | 100% |
| `native_contrast` | Array<String> | 100% |
| `ncm` | Array<String> | 100% |
| `package_contents` | Array<String> | 100% |
| `panel_type` | Array<String> | 100% |
| `part_number` | Array<String> | 100% |
| `pivo_adjustment` | Array<String> | 100% |
| `pixel_pitch` | Array<String> | 100% |
| `power_supply` | Array<String> | 100% |
| `resolution_refresh_rate` | Array<String> | 100% |
| `response_time` | Array<String> | 100% |
| `rotation` | Array<String> | 100% |
| `screen_design` | Array<String> | 100% |
| `screen_frame` | Array<String> | 100% |
| `screen_ratio` | Array<String> | 100% |
| `screen_size` | Array<String> | 100% |
| `speakers` | Array<String> | 100% |
| `summary` | Array<String> | 100% |
| `total_color` | Array<String> | 100% |
| `vertical_horizontal_frequency` | Array<String> | 100% |
| `vesa` | Array<String> | 100% |
| `viewing_angle` | Array<String> | 100% |
| `warranty` | Array<String> | 100% |
| `weight_with_packaging` | Array<String> | 100% |
| `weight_without_packaging` | Array<String> | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### SpecificationNotebook

**Documentos (estimado):** 15

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `alphanumeric_model` | Array<String> | 100% |
| `anatel_code` | Array<String> | 100% |
| `audio` | Array<String> | 100% |
| `color` | Array<String> | 100% |
| `control` | Array<String> | 100% |
| `cpu_chipset` | Array<String> | 100% |
| `dimensions_and_weight` | Array<String> | 100% |
| `display` | Array<String> | 100% |
| `ean_number` | Array<String> | 100% |
| `graphics` | Array<String> | 100% |
| `input_and_control` | Array<String> | 100% |
| `memory` | Array<String> | 100% |
| `ncm_number` | Array<String> | 100% |
| `operating_system` | Array<String> | 100% |
| `package_content` | Array<String> | 100% |
| `part_number` | Array<String> | 100% |
| `power_battery` | Array<String> | 100% |
| `product_observation` | Array<String> | 100% |
| `product_view` | Array<String> | 100% |
| `security` | Array<String> | 100% |
| `storage` | Array<String> | 100% |
| `summary` | Array<String> | 100% |
| `upc_number` | Array<String> | 100% |
| `upgrades` | Array<String> | 100% |
| `warranty` | Array<String> | 100% |
| `webcam` | Array<String> | 100% |
| `windows_desktop_apps` | Array<String> | 100% |
| `wireless_networking` | Array<String> | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### UserDatabase

**Documentos (estimado):** 33

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `changed_password` | Boolean | 100% |
| `email` | String | 100% |
| `temp_password` | String | 100% |
| `username` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### UserLog

**Documentos (estimado):** 998

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `action` | String | 100% |
| `area` | String | 100% |
| `date` | String | 100% |
| `type` | String | 100% |
| `user` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---


## busprotheus

### product

**Documentos (estimado):** 9

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `codigo_barra_ean` | String | 100% |
| `codigo_grupo` | String | 100% |
| `descricao` | String | 100% |
| `familia` | String | 100% |
| `modelo` | String | 100% |
| `origem` | String | 100% |
| `partnumber` | String | 100% |
| `product_line` | String | 100% |
| `segmento` | String | 78% |
| `serial_number` | null | 0% |
| `spec1` | String | 78% |
| `spec2` | String | 78% |
| `spec3` | String | 78% |
| `spec4` | String | 33% |
| `spec5` | String | 78% |
| `spec6` | String | 56% |
| `specs` | String | 100% |
| `tipo` | String | 100% |
| `tipo_produto` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### stock

**Documentos (estimado):** 12

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `armazem` | String | 100% |
| `custo_medio` | Double | 100% |
| `disponivel` | Double | 100% |
| `empenhado` | Double | 100% |
| `filial` | String | 100% |
| `partnumber` | String | 100% |
| `pedido` | Double | 100% |
| `reservado` | Double | 100% |
| `saldo` | Double | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---


## logs

### UserLog

**Documentos (estimado):** 1,110

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `action` | String | 100% |
| `area` | String | 100% |
| `date` | String | 100% |
| `type` | String | 100% |
| `user` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---


## notifications

### Notification

**Documentos (estimado):** 28,680

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `created_at` | String | 100% |
| `description` | Object | 100% |
| `description.days_exceeded` | null | 0% |
| `description.name` | String | 100% |
| `description.notification_type` | String | 100% |
| `description.platform` | null | 0% |
| `description.status` | String | 100% |
| `description.stock_quantity` | null | 0% |
| `description.type_of_alert` | String | 100% |
| `groups` | Array<String> | 100% |
| `product_id` | String | 100% |
| `updated_at` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### UserNotification

**Documentos (estimado):** 577,796

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `created_at` | String | 100% |
| `notification_id` | String | 100% |
| `read` | Boolean | 100% |
| `read_at` | String | 18% |
| `updated_at` | String | 100% |
| `user_id` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `user_id_1_read_1_autocreated` | `user_id` (ASC), `read` (ASC) | — |

---


## parceiros_core

### product_files

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

#### Índices

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


## partners_core

### product_files

**Documentos (estimado):** 747

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `bg_url` | String | 100% |
| `created_at` | Date | 100% |
| `dealer_page` | String | 100% |
| `hero_image` | String | 100% |
| `images` | Array<Object> | 100% |
| `images[].is_cover_bg_image` | Boolean | 774% |
| `images[].main` | Boolean | 774% |
| `images[].name` | String | 774% |
| `images[].order` | Integer | 774% |
| `images[].s3_filename` | String | 774% |
| `model` | String | 100% |
| `product_details` | Object | 100% |
| `product_details.category` | String | 100% |
| `product_details.created_at` | Date | 100% |
| `product_details.family` | String | 100% |
| `product_details.name` | String | 100% |
| `product_details.overview` | String | 100% |
| `product_details.part_number` | String | 100% |
| `product_details.product_type` | String | 100% |
| `product_details.status` | String | 100% |
| `product_details.updated_at` | Date | 100% |
| `s3_base_path` | String | 100% |
| `sync_source` | String | 100% |
| `updated_at` | Date | 100% |

#### Índices

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

### users

**Documentos (estimado):** 16

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `email` | String | 100% |
| `username` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---


## partners_events

### audit_logs

**Documentos (estimado):** 21

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `action` | String | 100% |
| `data` | Object | 100% |
| `data.args` | Array<Object> | 100% |
| `data.args[].Body` | String | 100% |
| `data.args[].MD5OfBody` | String | 100% |
| `data.args[].MessageId` | String | 100% |
| `data.args[].ReceiptHandle` | String | 100% |
| `data.function_name` | String | 100% |
| `data.kwargs` | Object | 100% |
| `data.module` | String | 100% |
| `duration_seconds` | Double | 100% |
| `error` | null | 0% |
| `ip_address` | null | 0% |
| `log_id` | String | 100% |
| `status` | String | 100% |
| `timestamp` | Date | 100% |
| `user_agent` | null | 0% |
| `user_id` | null | 0% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `action_1` | `action` (ASC) | — |
| `status_1` | `status` (ASC) | — |
| `timestamp_1` | `timestamp` (ASC) | — |
| `user_id_1` | `user_id` (ASC) | — |

---

### events

**Documentos (estimado):** 2

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `aggregate_id` | String | 100% |
| `aggregate_type` | String | 100% |
| `data` | Object | 100% |
| `data.args` | Array<Object> | 100% |
| `data.args[].Body` | String | 100% |
| `data.args[].MD5OfBody` | String | 100% |
| `data.args[].MessageId` | String | 100% |
| `data.args[].ReceiptHandle` | String | 100% |
| `data.duration_seconds` | Double | 50% |
| `data.ended_at` | String | 50% |
| `data.function_name` | String | 100% |
| `data.kwargs` | Object | 100% |
| `data.module` | String | 100% |
| `data.process_id` | String | 100% |
| `data.status` | String | 50% |
| `event_id` | String | 100% |
| `event_type` | String | 100% |
| `event_version` | Integer | 100% |
| `metadata` | Object | 100% |
| `metadata.causation_id` | String | 50% |
| `metadata.correlation_id` | String | 100% |
| `metadata.ip_address` | null | 0% |
| `metadata.user_agent` | null | 0% |
| `metadata.user_id` | null | 0% |
| `sequence` | Integer | 100% |
| `timestamp` | Date | 100% |

#### Índices

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


## product

### Agency

**Documentos (estimado):** 11

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `created_at` | String | 100% |
| `is_active` | Boolean | 100% |
| `name` | String | 100% |
| `responsibles` | Array<Object> | 100% |
| `responsibles[].email` | String | 164% |
| `responsibles[].name` | String | 164% |
| `updated_at` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### AnymarketCharacteristic

**Documentos (estimado):** 3

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `characteristics` | Object | 100% |
| `characteristics.Acessórios incluídos` | String | 33% |
| `characteristics.Altura` | String | 33% |
| `characteristics.Altura com embalagem` | String | 33% |
| `characteristics.Altura com suporte` | String | 33% |
| `characteristics.Altura x Comprimento x Profundidade` | String | 33% |
| `characteristics.Brilho` | String | 33% |
| `characteristics.Brilho da imagem` | String | 33% |
| `characteristics.Cabos incluídos` | String | 67% |
| `characteristics.Capacidade máxima suportada da memória RAM` | String | 33% |
| `characteristics.Com Bluetooth` | String | 33% |
| `characteristics.Com HDMI` | String | 33% |
| `characteristics.Com USB` | String | 33% |
| `characteristics.Com Wi-Fi` | String | 33% |
| `characteristics.Com alto-falante` | String | 33% |
| `characteristics.Com alto-falantes embutidos` | String | 33% |
| `characteristics.Com altura ajustável` | String | 33% |
| `characteristics.Com controle remoto` | String | 33% |
| `characteristics.Com função de pivote` | String | 33% |
| `characteristics.Com leitor de cartão de memória` | String | 33% |
| `characteristics.Com leitor de impressão digital` | String | 33% |
| `characteristics.Com microfone` | String | 33% |
| `characteristics.Com modo Eco` | String | 33% |
| `characteristics.Com montagem VESA` | String | 33% |
| `characteristics.Com porta ethernet` | String | 33% |
| `characteristics.Com saída para fones de ouvido` | String | 33% |
| `characteristics.Com teclado numérico` | String | 33% |
| `characteristics.Com teclado retroiluminado` | String | 33% |
| `characteristics.Com tecnologia sem flicker` | String | 33% |
| `characteristics.Com tela antirreflexo` | String | 33% |
| `characteristics.Com tela tátil` | String | 67% |
| `characteristics.Com webcam` | String | 33% |
| `characteristics.Comprimento com embalagem` | String | 33% |
| `characteristics.Comprimento com suporte` | String | 33% |
| `characteristics.Conexões de entrada` | String | 33% |
| `characteristics.Conexões de saída` | String | 33% |
| `characteristics.Conexões do monitor do computador` | String | 33% |
| `characteristics.Consumo energético` | String | 33% |
| `characteristics.Contraste` | String | 33% |
| `characteristics.Cor` | String | 100% |
| `characteristics.Duração máxima da bateria` | String | 33% |
| `characteristics.Edição do sistema operacional` | String | 33% |
| `characteristics.Fontes de luz` | String | 33% |
| `characteristics.Frequência de sincronização horizontal` | String | 33% |
| `characteristics.Frequência de sincronização vertical` | String | 33% |
| `characteristics.Gama de cores` | String | 33% |
| `characteristics.Homologação Anatel Nº` | String | 33% |
| `characteristics.Idioma do teclado` | String | 33% |
| `characteristics.Intervalo de distância de projeção` | String | 33% |
| `characteristics.Largura` | String | 33% |
| `characteristics.Largura com embalagem` | String | 33% |
| `characteristics.Largura com suporte` | String | 33% |
| `characteristics.Linha` | String | 100% |
| `characteristics.Linha do processador` | String | 33% |
| `characteristics.Marca` | String | 100% |
| `characteristics.Marca do processador` | String | 33% |
| `characteristics.Memória RAM` | String | 33% |
| `characteristics.Memória de vídeo` | String | 33% |
| `characteristics.Modelo` | String | 100% |
| `characteristics.Modelo alfanumérico` | String | 100% |
| `characteristics.Modelo detalhado` | String | 100% |
| `characteristics.Modelo do processador` | String | 33% |
| `characteristics.Modos de som` | String | 33% |
| `characteristics.Nome do sistema operacional` | String | 33% |
| `characteristics.Peso` | String | 67% |
| `characteristics.Peso com embalagem` | String | 33% |
| `characteristics.Peso e dimensões` | String | 67% |
| `characteristics.Peso sem embalagem` | String | 33% |
| `characteristics.Placa gráfica` | String | 33% |
| `characteristics.Portas de vídeo` | String | 33% |
| `characteristics.Profundidade` | String | 33% |
| `characteristics.Quantidade de alto-falantes` | String | 33% |
| `characteristics.Quantidade de cores da tela` | String | 33% |
| `characteristics.Quantidade de núcleos` | String | 33% |
| `characteristics.Quantidade de slots para a memória RAM` | String | 33% |
| `characteristics.Quantidade total de portas USB` | String | 33% |
| `characteristics.Relação de aspecto` | String | 67% |
| `characteristics.Relação de contraste` | String | 33% |
| `characteristics.Resolução da tela` | String | 67% |
| `characteristics.Resolução de vídeo da webcam` | String | 33% |
| `characteristics.Resolução nativa` | String | 33% |
| `characteristics.Sistemas operacionais compatíveis` | String | 33% |
| `characteristics.Software incluídos` | String | 33% |
| `characteristics.Tamanho da imagem` | String | 33% |
| `characteristics.Tamanho da tela` | String | 67% |
| `characteristics.Taxa de atualização` | String | 33% |
| `characteristics.Taxa de atualização da tela` | String | 33% |
| `characteristics.Tecnologia de projeção` | String | 33% |
| `characteristics.Tempo de resposta` | String | 33% |
| `characteristics.Tipo de bateria` | String | 33% |
| `characteristics.Tipo de memória RAM` | String | 33% |
| `characteristics.Tipo de painel` | String | 67% |
| `characteristics.Tipo de resolução` | String | 33% |
| `characteristics.Tipo de resolução da tela` | String | 33% |
| `characteristics.Tipo de resolução de vídeo da webcam` | String | 33% |
| `characteristics.Tipo de resolução suportada` | String | 33% |
| `characteristics.Tipo de tela` | String | 67% |
| `characteristics.Tipos de memória de vídeo` | String | 33% |
| `characteristics.Velocidade da memória RAM` | String | 33% |
| `characteristics.Velocidade máxima do processador` | String | 33% |
| `characteristics.Versão do sistema operacional` | String | 33% |
| `characteristics.Vida útil da fonte de luz (modo padrão)` | String | 33% |
| `characteristics.Voltagem` | String | 67% |
| `characteristics.É 2 em 1` | String | 33% |
| `characteristics.É antirreflexo` | String | 33% |
| `characteristics.É curvo` | String | 33% |
| `characteristics.É gamer` | String | 67% |
| `characteristics.É giratório` | String | 33% |
| `characteristics.É mini` | String | 33% |
| `characteristics.É netbook` | String | 33% |
| `characteristics.É portátil` | String | 33% |
| `characteristics.É reclinável` | String | 33% |
| `characteristics.É ultrabook` | String | 33% |
| `product_type` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Bom

**Documentos (estimado):** 1,434

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `a_cover` | String | 100% |
| `accessory_1` | String | 100% |
| `accessory_2` | String | 100% |
| `accessory_3` | String | 100% |
| `accessory_4` | String | 100% |
| `accessory_5` | String | 100% |
| `accessory_6` | String | 100% |
| `accessory_7` | String | 100% |
| `account_name` | String | 100% |
| `adapter` | String | 100% |
| `adapter_2` | String | 100% |
| `b_cover` | String | 100% |
| `battery` | String | 100% |
| `battery_2` | String | 100% |
| `bom_name` | String | 100% |
| `brand` | String | 100% |
| `camera` | String | 100% |
| `camera_2` | String | 100% |
| `camera_3` | String | 100% |
| `card_reader` | String | 100% |
| `cd` | String | 100% |
| `cobrand_royalty` | String | 100% |
| `country` | String | 100% |
| `country_kit` | String | 100% |
| `cpu` | String | 100% |
| `description` | String | 100% |
| `ean` | String | 100% |
| `extra_ap` | String | 100% |
| `extra_battery` | String | 100% |
| `finger_print` | String | 100% |
| `for_description` | String | 100% |
| `hdd_1` | String | 100% |
| `hdd_2` | String | 100% |
| `hdd_3` | String | 100% |
| `hdd_4` | String | 100% |
| `kb` | String | 100% |
| `label` | String | 100% |
| `lcd` | String | 100% |
| `logo` | String | 100% |
| `marketing_name` | String | 100% |
| `memory_1` | String | 100% |
| `memory_2` | String | 100% |
| `memory_3` | String | 100% |
| `memory_4` | String | 100% |
| `model` | String | 100% |
| `ms_special` | String | 100% |
| `nb_chipset` | String | 100% |
| `ns` | String | 100% |
| `odd_1` | String | 100% |
| `odm` | String | 100% |
| `os` | String | 100% |
| `os_2` | String | 100% |
| `os_country_kit` | String | 100% |
| `os_manual` | String | 100% |
| `pn_apply_time` | String | 100% |
| `pn_cfm_time` | String | 100% |
| `power_cord` | String | 100% |
| `printing` | String | 100% |
| `product_name` | String | 100% |
| `project_name` | String | 100% |
| `ref_id` | String | 100% |
| `ro` | String | 100% |
| `ship_mark` | String | 100% |
| `sim_lock` | String | 100% |
| `softload` | String | 100% |
| `special_package` | String | 100% |
| `special_request` | String | 100% |
| `sub_brand` | String | 100% |
| `tender_type` | String | 100% |
| `unique_itens_remark` | String | 100% |
| `upc` | String | 100% |
| `users_guide` | String | 100% |
| `vga_chip` | String | 100% |
| `vram_1` | String | 100% |
| `vram_2` | String | 100% |
| `vram_3` | String | 100% |
| `vram_4` | String | 100% |
| `warranty_card` | String | 100% |
| `wireless_lan` | String | 100% |
| `wwan` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### BomDetails

**Documentos (estimado):** 10

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `detail` | String | 40% |
| `file` | String | 100% |
| `imported_at` | String | 100% |
| `is_main` | Boolean | 100% |
| `status` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Category

**Documentos (estimado):** 15

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `active_store_front_link` | Boolean | 100% |
| `anymarket_id` | Integer | 27% |
| `created_at` | String | 100% |
| `description` | String | 100% |
| `father_category_id` | Integer | 100% |
| `global_category_id` | Integer | 100% |
| `global_category_name` | String | 100% |
| `is_active` | Boolean | 100% |
| `keywords` | String | 100% |
| `name` | String | 100% |
| `product_type` | DBRef → `ProductType` | 100% |
| `show_brand_filter` | Boolean | 100% |
| `show_in_store_front` | Boolean | 100% |
| `stock_keeping_unit_selection_mode` | String | 100% |
| `title` | String | 100% |
| `updated_at` | String | 100% |
| `vtex_id` | Integer | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Collection

**Documentos (estimado):** 23

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `date_from` | Date | 100% |
| `date_to` | Date | 100% |
| `description` | String | 100% |
| `highlight` | Boolean | 100% |
| `name` | String | 100% |
| `products` | Array<String> | 100% |
| `searchable` | Boolean | 100% |
| `type` | null | 0% |
| `vtex_id` | Integer | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Family

**Documentos (estimado):** 51

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `name` | String | 100% |
| `product_type` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `name_1` | `name` (ASC) | — |

---

### GoogleGlobalCategory

**Documentos (estimado):** 5,595

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `google_id` | Integer | 100% |
| `name` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### HeroDealerUpload

**Documentos (estimado):** 22

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `created_at` | String | 100% |
| `dealer_s3_filename` | String | 100% |
| `detail` | String | 36% |
| `hero_s3_filename` | String | 100% |
| `product_id` | String | 100% |
| `status` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Model

**Documentos (estimado):** 1,022

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `family` | DBRef → `Family` | 100% |
| `name` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `family_1` | `family` (ASC) | — |
| `name_1` | `name` (ASC) | — |

---

### PartnerFiles

**Documentos (estimado):** 199

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `dealer_page_partner_url` | String | 40% |
| `hero_image_partner_url` | String | 14% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Product

**Documentos (estimado):** 147

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `brand_id` | Integer | 100% |
| `category` | DBRef → `Category` \| Object | 100% |
| `category.active_store_front_link` | Boolean | 4% |
| `category.anymarket_id` | Integer | 2% |
| `category.created_at` | String | 4% |
| `category.description` | String | 4% |
| `category.father_category_id` | Integer | 4% |
| `category.global_category_id` | Integer | 4% |
| `category.global_category_name` | String | 4% |
| `category.id` | ObjectId | 4% |
| `category.is_active` | Boolean | 4% |
| `category.keywords` | String | 4% |
| `category.name` | String | 4% |
| `category.product_type` | Object | 4% |
| `category.product_type.global_category` | Object | 4% |
| `category.product_type.global_category.google_id` | Integer | 4% |
| `category.product_type.global_category.id` | ObjectId | 4% |
| `category.product_type.global_category.name` | String | 4% |
| `category.product_type.id` | ObjectId | 4% |
| `category.product_type.name` | String | 4% |
| `category.product_type.vtex_id` | Integer | 4% |
| `category.show_brand_filter` | Boolean | 4% |
| `category.show_in_store_front` | Boolean | 4% |
| `category.stock_keeping_unit_selection_mode` | String | 4% |
| `category.title` | String | 4% |
| `category.updated_at` | String | 4% |
| `category.vtex_id` | Integer | 4% |
| `collections` | Array<DBRef → `Collection`> | 10% |
| `created_at` | String | 100% |
| `department_id` | Integer | 88% |
| `description` | String | 100% |
| `description_short` | String | 8% |
| `external_characteristics` | String | 94% |
| `family` | String | 100% |
| `filters` | Array<Object> | 84% |
| `filters[].field_id` | Integer | 78% |
| `filters[].name` | String | 78% |
| `filters[].values` | Array<String> | 78% |
| `has_upgrade` | Boolean | 12% |
| `icons` | Array | 82% |
| `id` | ObjectId | 4% |
| `integrated_channels` | Object | 100% |
| `integrated_channels.anymarket` | Object | 100% |
| `integrated_channels.anymarket.id` | Integer | 4% |
| `integrated_channels.anymarket.integrated` | Boolean | 100% |
| `integrated_channels.cisp1` | Object | 100% |
| `integrated_channels.cisp1.id` | Integer | 2% |
| `integrated_channels.cisp1.integrated` | Boolean | 100% |
| `integrated_channels.cisp1.was_sent` | Boolean | 6% |
| `integrated_channels.vtex` | Object | 100% |
| `integrated_channels.vtex.id` | Integer | 94% |
| `integrated_channels.vtex.integrated` | Boolean | 100% |
| `is_active` | Boolean | 94% |
| `is_b2b` | null | 0% |
| `is_protheus_imported` | Boolean | 14% |
| `is_service` | Boolean | 100% |
| `is_visible` | Boolean | 90% |
| `key_words` | String | 24% |
| `kit_type` | null | 0% |
| `link_id` | String | 94% |
| `meta_tag_description` | String | 100% |
| `model` | String | 100% |
| `name` | String | 94% |
| `overview` | String | 94% |
| `partner_files` | DBRef → `PartnerFiles` \| Object | 100% |
| `partner_files.dealer_page_partner_url` | String | 4% |
| `partner_files.hero_image_partner_url` | String | 4% |
| `partner_files.id` | ObjectId | 4% |
| `products_ids` | Array<String> | 2% |
| `ref_id` | String | 100% |
| `release_date` | String | 88% |
| `score` | Integer | 82% |
| `services` | Array<Object> | 100% |
| `services[].salles_channels` | Array<Object> | 18% |
| `services[].salles_channels[].campaign` | Object | 10% |
| `services[].salles_channels[].campaign.call` | String | 10% |
| `services[].salles_channels[].campaign.description` | String | 10% |
| `services[].salles_channels[].campaign.end_date` | String | 10% |
| `services[].salles_channels[].campaign.name` | String | 10% |
| `services[].salles_channels[].campaign.start_date` | String | 10% |
| `services[].salles_channels[].campaign.status` | Boolean | 10% |
| `services[].salles_channels[].campaign.tag` | String | 10% |
| `services[].salles_channels[].cost` | Double | 38% |
| `services[].salles_channels[].name` | String | 38% |
| `services[].salles_channels[].price` | Double | 38% |
| `services[].salles_channels[].product_part_number` | String | 4% |
| `services[].salles_channels[].recommended` | String | 38% |
| `services[].service_details` | Object | 18% |
| `services[].service_details._id` | ObjectId | 18% |
| `services[].service_details.benefits` | Array<String> | 18% |
| `services[].service_details.business_type` | String | 16% |
| `services[].service_details.commercial_name` | String | 18% |
| `services[].service_details.contractual_term_url` | String | 18% |
| `services[].service_details.description` | String | 18% |
| `services[].service_details.general_condition_url` | String | 18% |
| `services[].service_details.gs_id` | String | 18% |
| `services[].service_details.imported_by` | String | 18% |
| `services[].service_details.name` | String | 18% |
| `services[].service_details.part_number` | String | 18% |
| `services[].service_details.products_associateds` | Array<String> | 18% |
| `services[].service_details.published` | Boolean | 16% |
| `services[].service_details.revision_id` | null | 0% |
| `services[].service_details.service_type` | String | 18% |
| `services[].service_details.term` | String | 18% |
| `show_without_stock` | Boolean | 90% |
| `sku` | DBRef → `Sku` \| Object | 100% |
| `sku.activate_if_possible` | null | 0% |
| `sku.anymarket_id` | null | 0% |
| `sku.commercial_condition_id` | null | 0% |
| `sku.created_at` | String | 4% |
| `sku.creation_date` | null | 0% |
| `sku.cubic_weight` | null | 0% |
| `sku.estimated_date_arrival` | null | 0% |
| `sku.height` | null | 0% |
| `sku.id` | ObjectId | 4% |
| `sku.is_active` | null | 0% |
| `sku.is_kit` | null | 0% |
| `sku.kit_itens_sell_apart` | null | 0% |
| `sku.length` | null | 0% |
| `sku.low_stock_anymarket` | null | 0% |
| `sku.low_stock_vtex` | null | 0% |
| `sku.manufacturer_code` | null | 0% |
| `sku.measurement_unit` | null | 0% |
| `sku.modal_type` | null | 0% |
| `sku.name` | null | 0% |
| `sku.packaged_height` | null | 0% |
| `sku.packaged_length` | null | 0% |
| `sku.packaged_weight_kg` | null | 0% |
| `sku.packaged_width` | null | 0% |
| `sku.prices` | Object | 2% |
| `sku.prices.anymarket` | null | 0% |
| `sku.prices.cisp1` | null | 0% |
| `sku.prices.vtex` | null | 0% |
| `sku.ref_id` | null | 0% |
| `sku.reward_value` | null | 0% |
| `sku.sku_files` | Array<Object> | 4% |
| `sku.sku_files[].is_cover_bg_image` | Boolean | 4% |
| `sku.sku_files[].main` | null | 0% |
| `sku.sku_files[].name` | String | 4% |
| `sku.sku_files[].order` | null | 0% |
| `sku.sku_files[].s3_filename` | String | 4% |
| `sku.sku_kit_itens` | Array | 4% |
| `sku.stock_protheus` | Array<Object> | 4% |
| `sku.stock_protheus[].company_branch` | String | 8% |
| `sku.stock_protheus[].stock_quantity` | Integer | 8% |
| `sku.stock_protheus[].warehouse` | String | 8% |
| `sku.stock_quantity_anymarket` | null | 0% |
| `sku.stock_quantity_vtex` | null | 0% |
| `sku.stock_virtual_quantity_vtex` | null | 0% |
| `sku.unit_multiplier` | null | 0% |
| `sku.updated_at` | String | 4% |
| `sku.videos` | null | 0% |
| `sku.vtex_id` | null | 0% |
| `sku.weight_kg` | null | 0% |
| `sku.width` | null | 0% |
| `status` | String | 100% |
| `support_files` | null | 0% |
| `tax_code` | String | 10% |
| `technical_specification` | Object | 94% |
| `technical_specification.123` | String | 6% |
| `technical_specification.12313` | Array<String> \| String | 12% |
| `technical_specification.321231` | String | 6% |
| `technical_specification.7126387126` | String | 6% |
| `technical_specification.Acer PN` | Array<String> \| String | 18% |
| `technical_specification.Aplicativos` | Array<String> \| String | 16% |
| `technical_specification.Armazenamento` | Array<String> \| String | 20% |
| `technical_specification.Bateria e Alimentação` | Array<String> \| String | 18% |
| `technical_specification.CBH_ProductName` | Array<String> \| String | 12% |
| `technical_specification.CRF_ProductName` | Array<String> \| String | 12% |
| `technical_specification.Conexão` | Array<String> | 2% |
| `technical_specification.Conteúdo da Embalagem` | Array<String> \| String | 18% |
| `technical_specification.Controle` | Array<String> \| String | 18% |
| `technical_specification.Cor` | Array<String> \| String | 20% |
| `technical_specification.Código ANATEL` | Array<String> \| String | 16% |
| `technical_specification.Dimensões e Peso` | Array<String> \| String | 18% |
| `technical_specification.EAN` | Array<String> \| String | 18% |
| `technical_specification.Garantia` | String | 10% |
| `technical_specification.Garantia ` | Array<String> | 6% |
| `technical_specification.Garantia do Fabricante` | Array<String> | 6% |
| `technical_specification.Gráficos` | Array<String> \| String | 20% |
| `technical_specification.MGZ_ProductName` | Array<String> \| String | 12% |
| `technical_specification.Memória` | Array<String> \| String | 18% |
| `technical_specification.Memória RAM` | String | 2% |
| `technical_specification.Observações do Produto` | Array<String> \| String | 16% |
| `technical_specification.Processador e Chipset` | Array<String> \| String | 20% |
| `technical_specification.Resolução de Tela` | Array<String> | 2% |
| `technical_specification.SOBRE O PRODUTO` | Array<String> | 6% |
| `technical_specification.Saiba Mais` | String | 10% |
| `technical_specification.Saiba Mais ` | Array<String> | 6% |
| `technical_specification.Sistema Operacional` | Array<String> \| String | 18% |
| `technical_specification.Teclados e  Touchpad` | Array<String> \| String | 18% |
| `technical_specification.Tela` | Array<String> \| String | 18% |
| `technical_specification.Upgrades` | Array<String> \| String | 16% |
| `technical_specification.Vídeo` | Array<String> | 6% |
| `technical_specification.Webcam` | Array<String> \| String | 18% |
| `technical_specification.Wi-Fi e Rede` | Array<String> \| String | 18% |
| `technical_specification.teste cache` | String | 6% |
| `technical_specification.teste cache 1233` | String | 6% |
| `technical_specification.teste cache 2` | String | 6% |
| `technical_specification.teste cache 3` | String | 6% |
| `technical_specification.teste cache 4` | String | 6% |
| `technical_specification.teste cache 5` | String | 6% |
| `technical_specification.teste new form` | String | 6% |
| `technical_specification.Áudio e Microfone` | Array<String> \| String | 18% |
| `title` | String | 98% |
| `updated_at` | String | 100% |
| `vtex_legacy` | Boolean | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### ProductTimeline

**Documentos (estimado):** 238

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `date` | String | 100% |
| `description` | String | 6% |
| `product_id` | String | 100% |
| `status` | String | 100% |
| `user_id` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### ProductType

**Documentos (estimado):** 5

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `global_category` | DBRef → `GoogleGlobalCategory` | 100% |
| `name` | String | 100% |
| `vtex_id` | Integer | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### QuickSummary

**Documentos (estimado):** 534

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `alerts` | String | 100% |
| `created_at` | Date | 100% |
| `highlights` | String | 100% |
| `quick_summary` | String | 100% |
| `suggestions` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Service

**Documentos (estimado):** 16

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `benefits` | Array<String> | 100% |
| `business_type` | String | 100% |
| `commercial_name` | String | 100% |
| `contractual_term_url` | String | 100% |
| `description` | String | 100% |
| `general_condition_url` | String | 100% |
| `gs_id` | String | 100% |
| `imported_by` | String | 100% |
| `name` | String | 100% |
| `part_number` | String | 100% |
| `products_associateds` | Array<String> | 100% |
| `published` | Boolean | 100% |
| `service_type` | String | 100% |
| `term` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Settings

**Documentos (estimado):** 1

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `sla_days` | Object | 100% |
| `sla_days.EM RASCUNHO DO PRODUTO` | Integer | 100% |
| `sla_days.EM RASCUNHO NO E-COMMERCE` | Integer | 100% |
| `sla_days.PENDENTE DE CADASTRO NO PROTHEUS` | Integer | 100% |
| `sla_days.PENDENTE DE ENVIO PARA AGÊNCIA` | Integer | 100% |
| `sla_days.PENDENTE DE LIBERAÇÃO DA AGÊNCIA` | Integer | 100% |
| `sla_days.PENDENTE DE PRECIFICAÇÃO` | Integer | 100% |
| `stock` | Object | 100% |
| `stock.cronjob_time` | String | 100% |
| `stock.minimal_stock` | Integer | 100% |
| `stock.type_of_alert` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Sku

**Documentos (estimado):** 184

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `activate_if_possible` | Boolean | 82% |
| `anymarket_id` | Integer | 2% |
| `commercial_condition_id` | Integer | 82% |
| `created_at` | String | 100% |
| `creation_date` | String | 82% |
| `cubic_weight` | Double | 82% |
| `estimated_date_arrival` | String | 8% |
| `height` | Double | 82% |
| `is_active` | Boolean | 82% |
| `is_kit` | Boolean | 82% |
| `kit_itens_sell_apart` | Boolean | 82% |
| `length` | Double | 82% |
| `low_stock_anymarket` | null | 0% |
| `low_stock_vtex` | null | 0% |
| `manufacturer_code` | String | 22% |
| `measurement_unit` | String | 82% |
| `modal_type` | String | 6% |
| `name` | String | 82% |
| `packaged_height` | Double | 82% |
| `packaged_length` | Double | 82% |
| `packaged_weight_kg` | Double | 82% |
| `packaged_width` | Double | 82% |
| `price` | null | 0% |
| `price_anymarket` | Integer | 2% |
| `prices` | Object | 86% |
| `prices.anymarket` | Integer | 4% |
| `prices.cisp1` | Double | 4% |
| `prices.vtex` | Double \| Integer | 60% |
| `ref_id` | String | 82% |
| `reward_value` | Integer | 16% |
| `sku_files` | Array<Object> | 100% |
| `sku_files[].is_cover_bg_image` | Boolean | 156% |
| `sku_files[].main` | Boolean | 118% |
| `sku_files[].name` | String | 156% |
| `sku_files[].order` | Integer | 26% |
| `sku_files[].s3_filename` | String | 156% |
| `sku_kit_itens` | Array<Object> | 100% |
| `sku_kit_itens[].family` | String | 12% |
| `sku_kit_itens[].image` | String | 12% |
| `sku_kit_itens[].model` | String | 12% |
| `sku_kit_itens[].product_id` | ObjectId | 12% |
| `sku_kit_itens[].product_name` | String | 12% |
| `sku_kit_itens[].ref_id` | String | 12% |
| `sku_kit_itens[].sku_id` | ObjectId | 16% |
| `sku_kit_itens[].sku_name` | String | 16% |
| `sku_kit_itens[].sku_vtex_id` | Integer | 16% |
| `stock_protheus` | Array<Object> | 100% |
| `stock_protheus[].company_branch` | String | 34% |
| `stock_protheus[].stock_quantity` | Double \| Integer | 34% |
| `stock_protheus[].warehouse` | String | 34% |
| `stock_quantity_anymarket` | Integer | 2% |
| `stock_quantity_vtex` | Integer | 2% |
| `stock_virtual_quantity_vtex` | null | 0% |
| `unit_multiplier` | Double | 82% |
| `updated_at` | String | 100% |
| `videos` | Array<String> | 82% |
| `vtex_id` | Integer | 76% |
| `weight_kg` | Double | 82% |
| `width` | Double | 82% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### SlaNotify

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Specification

**Documentos (estimado):** 78

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `created_at` | String | 100% |
| `default_value` | String | 18% |
| `field_group_id` | Integer | 100% |
| `field_type_id` | Integer | 100% |
| `is_active` | Boolean | 100% |
| `is_filter` | Boolean | 100% |
| `is_on_product_details` | Boolean | 100% |
| `is_required` | Boolean | 100% |
| `is_side_menu_link_active` | Boolean | 100% |
| `is_stock_keeping_unit` | Boolean | 100% |
| `is_top_menu_link_active` | Boolean | 100% |
| `name` | String | 100% |
| `position` | Integer | 100% |
| `product_type` | DBRef → `ProductType` | 100% |
| `updated_at` | String | 100% |
| `vtex_id` | Integer | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### StockSyncDate

**Documentos (estimado):** 1

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `end_date` | null | 0% |
| `start_date` | String | 100% |
| `status` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### Template

**Documentos (estimado):** 1

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `created_at` | String | 100% |
| `model` | String | 100% |
| `product_type` | DBRef → `ProductType` | 100% |
| `technical_specification` | Object | 100% |
| `technical_specification.123` | String | 100% |
| `technical_specification.12313` | String | 100% |
| `technical_specification.321231` | String | 100% |
| `technical_specification.7126387126` | String | 100% |
| `technical_specification.Aplicativos` | String | 100% |
| `technical_specification.Armazenamento` | String | 100% |
| `technical_specification.CBH_ProductName` | String | 100% |
| `technical_specification.Conteúdo da Embalagem` | String | 100% |
| `technical_specification.Cor` | String | 100% |
| `technical_specification.EAN` | String | 100% |
| `technical_specification.Garantia` | String | 100% |
| `technical_specification.Gráficos` | String | 100% |
| `technical_specification.MGZ_ProductName` | String | 100% |
| `technical_specification.Memória` | String | 100% |
| `technical_specification.Processador e Chipset` | String | 100% |
| `technical_specification.Sistema Operacional` | String | 100% |
| `technical_specification.Teclados e Touchpad` | String | 100% |
| `technical_specification.Tela` | String | 100% |
| `technical_specification.Upgrades` | String | 100% |
| `technical_specification.Webcam` | String | 100% |
| `technical_specification.Wi-Fi e Rede` | String | 100% |
| `technical_specification.teste cache` | String | 100% |
| `technical_specification.teste cache 3` | String | 100% |
| `technical_specification.teste new form` | String | 100% |
| `technical_specification.Áudio e Microfone` | String | 100% |
| `updated_at` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---


## scraping

### amd_processors

**Documentos (estimado):** 574

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `*Suporte a SO` | String | 100% |
| `AMD Ryzen AI` | String | 58% |
| `Aumento de clock máx` | Object | 100% |
| `Aumento de clock máx.` | String | 100% |
| `Bandeja com identificação do produto` | String | 100% |
| `Cache L1` | String | 30% |
| `Cache L2` | String | 100% |
| `Cache L3` | String | 100% |
| `Canais de memória` | Integer | 100% |
| `Clock básico` | String | 100% |
| `Contagem de núcleos gráficos` | Integer | 78% |
| `Data de lançamento` | String | 40% |
| `Desbloqueado para overclocking` | String | 86% |
| `Especificação da memória do sistema` | String | 18% |
| `Família` | String | 100% |
| `Fator de forma` | String | 100% |
| `Frequência de gráficos` | String | 78% |
| `ID do produto MPK` | String | 16% |
| `ID do produto na caixa` | String | 32% |
| `Modelo da placa de vídeo` | String | 100% |
| `Nome` | String | 100% |
| `Nº de núcleos de CPU` | Integer | 100% |
| `Nº de threads` | Integer | 100% |
| `PCI Express® Version` | String | 100% |
| `Recommended Cooler` | String | 8% |
| `Solução Térmica (PIB)` | String | 26% |
| `Soquete da CPU` | String | 100% |
| `Série` | String | 100% |
| `TDP configurável AMD (cTDP)` | String | 70% |
| `TDP padrão` | String | 94% |
| `Tecnologia de processador para núcleos de CPU` | String | 100% |
| `Tecnologias compatíveis` | String | 30% |
| `Temperatura máx` | Object | 100% |
| `Temperatura máx. de funcionamento (Tjmax)` | String | 100% |
| `Thermal Solution (MPK)` | String | 4% |
| `Tipo de memória do sistema` | String | 100% |
| `_id` | ObjectId | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### intel_processors

**Documentos (estimado):** 2,865

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `# of Displays Supported ‡` | Integer | 90% |
| `# of Efficient-cores` | Integer | 100% |
| `# of Low Power Efficient-cores` | Integer | 40% |
| `# of Performance-cores` | Integer | 100% |
| `AI Datatype Support on CPU` | String | 18% |
| `AI Datatype Support on GPU` | String | 18% |
| `AI Datatype Support on NPU` | String | 18% |
| `AI Software Frameworks Supported by CPU` | String | 40% |
| `AI Software Frameworks Supported by GPU` | String | 40% |
| `AI Software Frameworks Supported by NPU` | String | 40% |
| `AV1 Encode/Decode` | String | 40% |
| `Cache` | String | 100% |
| `Chipset / PCH PCIe Revision` | String | 28% |
| `Code Name` | String | 100% |
| `Datasheet` | String | 60% |
| `Device ID` | String | 90% |
| `Direct Media Interface (DMI) Revision` | Double | 32% |
| `DirectX* Support` | Double \| Integer | 90% |
| `ECC Memory Supported   ‡` | String | 82% |
| `Efficient-core Base Frequency` | String | 80% |
| `Efficient-core Max Turbo Frequency` | String | 100% |
| `Embedded Options Available` | String | 100% |
| `Enhanced Intel SpeedStep® Technology` | String | 26% |
| `Execute Disable Bit ‡` | String | 94% |
| `Execution Units` | Integer | 50% |
| `GPU Name‡` | String | 90% |
| `Graphics Base Frequency` | String | 14% |
| `Graphics Max Dynamic Frequency` | String | 90% |
| `Graphics Output` | String | 90% |
| `H_264 Hardware Encode/Decode` | String | 40% |
| `H_265 (HEVC) Hardware Encode/Decode` | String | 40% |
| `Idle States` | String | 26% |
| `Instruction Set` | String | 100% |
| `Instruction Set Extensions` | String | 100% |
| `Intel vPro® Eligibility ‡` | String | 76% |
| `Intel® 64 ‡` | String | 26% |
| `Intel® AES New Instructions` | String | 100% |
| `Intel® Active Management Technology (AMT) ‡` | String | 62% |
| `Intel® Adaptive Boost Technology` | String | 12% |
| `Intel® Adaptix™ Technology` | String | 74% |
| `Intel® Boot Guard` | String | 100% |
| `Intel® Clear Video HD Technology` | String | 16% |
| `Intel® Control-Flow Enforcement Technology` | String | 94% |
| `Intel® Deep Learning Boost (Intel® DL Boost) on CPU` | String | 100% |
| `Intel® Deep Learning Boost (Intel® DL Boost) on GPU` | String | 40% |
| `Intel® Flex Memory Access` | String | 74% |
| `Intel® Gaussian & Neural Accelerator` | Double | 100% |
| `Intel® Hardware Shield Eligibility ‡` | String | 78% |
| `Intel® High Definition Audio` | String | 74% |
| `Intel® Hyper-Threading Technology ‡` | String | 100% |
| `Intel® Image Processing Unit` | Double | 68% |
| `Intel® OS Guard` | String | 100% |
| `Intel® One-Click Recovery ‡` | String | 64% |
| `Intel® Quick Sync Video` | String | 90% |
| `Intel® QuickAssist Software Acceleration` | String | 20% |
| `Intel® Remote Platform Erase (RPE) ‡` | String | 62% |
| `Intel® Smart Sound Technology` | String | 74% |
| `Intel® Speed Shift Technology` | String | 100% |
| `Intel® Stable IT Platform Program (SIPP)` | String | 60% |
| `Intel® Standard Manageability (ISM) ‡` | String | 90% |
| `Intel® Thermal Velocity Boost` | String | 16% |
| `Intel® Thermal Velocity Boost Frequency` | String | 16% |
| `Intel® Thread Director` | String | 100% |
| `Intel® Threat Detection Technology (TDT)` | String | 82% |
| `Intel® Thunderbolt™ 4` | String | 68% |
| `Intel® Total Memory Encryption` | String | 8% |
| `Intel® Total Memory Encryption - Multi Key` | String | 62% |
| `Intel® Trusted Execution Technology ‡` | String | 76% |
| `Intel® Turbo Boost Max Technology 3_0 Frequency ‡` | String | 42% |
| `Intel® Turbo Boost Max Technology 3_0 ‡` | String | 72% |
| `Intel® Turbo Boost Technology ‡` | Double | 26% |
| `Intel® VT-x with Extended Page Tables (EPT) ‡` | String | 100% |
| `Intel® Virtualization Technology (VT-x) ‡` | String | 100% |
| `Intel® Virtualization Technology for Directed I/O (VT-d) ‡` | String | 100% |
| `Intel® Virtualization Technology with Redirect Protection (VT-rp) ‡` | String | 62% |
| `Intel® Volume Management Device (VMD)` | String | 100% |
| `Intel® Wake on Voice` | String | 70% |
| `Launch Date` | String | 100% |
| `Lithography` | String | 60% |
| `Low Power Efficient-core Base Frequency` | String | 40% |
| `Low Power Efficient-core Max Turbo Frequency` | String | 40% |
| `MIPI SoundWire*` | Double | 34% |
| `Marketing Status` | String | 100% |
| `Max # of DMI Lanes` | Integer | 32% |
| `Max # of Memory Channels` | Integer | 100% |
| `Max # of PCI Express Lanes` | Integer | 100% |
| `Max CPU Configuration` | Integer | 100% |
| `Max Frequency` | String | 40% |
| `Max Memory Bandwidth` | String | 32% |
| `Max Memory Size (dependent on memory type)` | String | 100% |
| `Max Operating Temperature` | String | 78% |
| `Max Resolution (DP)‡` | String | 90% |
| `Max Resolution (HDMI)‡` | String | 90% |
| `Max Resolution (eDP - Integrated Flat Panel)‡` | String | 90% |
| `Max Turbo Frequency` | String | 100% |
| `Maximum Assured Power` | String | 38% |
| `Maximum Turbo Power` | String | 100% |
| `Memory Types` | String | 100% |
| `Microprocessor PCIe Revision` | String | 28% |
| `Minimum Assured Power` | String | 70% |
| `Mode-based Execute Control (MBEC)` | String | 94% |
| `Multi-Format Codec Engines` | Integer | 90% |
| `NPU Name‡` | String | 40% |
| `OpenCL* Support` | Double | 90% |
| `OpenGL* Support` | Double | 90% |
| `PCI Express Configurations ‡` | String | 72% |
| `PCI Express Revision` | String | 32% |
| `PCI Support` | Double \| String | 40% |
| `Package Size` | String | 100% |
| `Performance-core Base Frequency` | String | 80% |
| `Performance-core Max Turbo Frequency` | String | 100% |
| `Processor Base Frequency` | String | 2% |
| `Processor Base Power` | String | 100% |
| `Processor Number` | String | 100% |
| `Product Collection` | String | 100% |
| `Product Tuning (Embedded Uses)` | String | 18% |
| `Ray Tracing` | String | 40% |
| `Recommended Customer Price` | String | 72% |
| `Scalability` | String | 32% |
| `Secure Key` | String | 100% |
| `Sockets Supported` | String | 66% |
| `Sparsity Support` | String | 40% |
| `TJUNCTION` | String | 60% |
| `Thermal Monitoring Technologies` | String | 100% |
| `Thermal Solution Specification` | String | 24% |
| `Total Cores` | Integer | 100% |
| `Total L2 Cache` | String | 26% |
| `Total Threads` | Integer | 100% |
| `Use Conditions` | String | 26% |
| `VP9 Bitstream & Decoding` | String | 40% |
| `Vertical Segment` | String | 100% |
| `Windows Studio Effects Support` | String | 40% |
| `Xe-cores` | Integer | 40% |
| `_id` | ObjectId | 100% |
| `scrape` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### nvidia_video

**Documentos (estimado):** 12

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `bcPID` | Integer | 100% |
| `bestSeller` | Boolean | 100% |
| `category` | String | 100% |
| `certified` | Boolean | 100% |
| `compareProductInfo` | Array<Object> | 100% |
| `compareProductInfo[].name` | String | 400% |
| `compareProductInfo[].value` | String | 400% |
| `customerReviewCount` | null | 0% |
| `digitialRiverID` | null | 0% |
| `displayName` | String | 100% |
| `gpu` | String | 100% |
| `imageURL` | String | 100% |
| `isFeaturedProdcutFoundInSecondSearch` | Boolean | 100% |
| `isFeaturedProduct` | Boolean | 100% |
| `isFounderEdition` | Boolean | 100% |
| `isOffer` | Boolean | 100% |
| `locale` | String | 100% |
| `manufacturer` | String | 100% |
| `maxShipDays` | null | 0% |
| `minShipDays` | null | 0% |
| `mrp` | String | 75% |
| `offerText` | String | 100% |
| `prdStatus` | String | 100% |
| `productAvailable` | Boolean | 100% |
| `productID` | Integer | 100% |
| `productInfo` | Array<Object> | 100% |
| `productInfo[].name` | String | 300% |
| `productInfo[].value` | String | 300% |
| `productPrice` | String | 100% |
| `productRating` | null | 0% |
| `productSKU` | String | 100% |
| `productTitle` | String | 100% |
| `productUPC` | String | 100% |
| `productUPCOriginal` | String | 100% |
| `purchaseOption` | String | 100% |
| `retailers` | Array<Object> | 100% |
| `retailers[].bestSeller` | Boolean | 117% |
| `retailers[].directPurchaseLink` | String | 75% |
| `retailers[].hasOffer` | Boolean | 117% |
| `retailers[].isAvailable` | Boolean | 117% |
| `retailers[].logoUrl` | String | 100% |
| `retailers[].mrp` | String | 117% |
| `retailers[].offerText` | null | 0% |
| `retailers[].partnerId` | String | 117% |
| `retailers[].productId` | Integer | 117% |
| `retailers[].productTitle` | String | 117% |
| `retailers[].purchaseLink` | String | 117% |
| `retailers[].retailerName` | String | 117% |
| `retailers[].salePrice` | String | 117% |
| `retailers[].sku` | String | 117% |
| `retailers[].stock` | Integer | 117% |
| `retailers[].storeId` | String | 117% |
| `retailers[].type` | Integer | 117% |
| `retailers[].upc` | String | 117% |
| `shipInfo` | null | 0% |
| `totalCount` | Integer | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### parceiros_acer

**Documentos (estimado):** 9

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `families` | Array<Object> | 100% |
| `families[].models` | Array<String> | 578% |
| `families[].name` | String | 578% |
| `product_type` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---


## test

### coll

**Documentos (estimado):** 8

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `date` | Date | 100% |
| `offset` | Integer | 12% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---


## test_parceiros_core

### product_files

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

#### Índices

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

### users

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---


## test_partners_core

### product_files

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

#### Índices

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

### users

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---


## users

### Permission

**Documentos (estimado):** 14

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `name` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

### UserDatabase

**Documentos (estimado):** 4

#### Schema

| Campo | Tipo(s) | Presença |
|-------|---------|----------|
| `_id` | ObjectId | 100% |
| `changed_password` | Boolean | 100% |
| `email` | String | 100% |
| `temp_password` | String | 100% |
| `username` | String | 100% |

#### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

