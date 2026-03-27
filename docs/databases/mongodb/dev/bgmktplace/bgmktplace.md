# Database: bgmktplace

[← Voltar ao índice](../README.md)

> **13** collection(s) · ~**1,173** documentos estimados

## Sumário

| Collection | Documentos (est.) |
|------------|-------------------|
| [BgFile](#bgfile) | 18 |
| [Category](#category) | 53 |
| [Family](#family) | 1 |
| [Permission](#permission) | 14 |
| [Product](#product) | 18 |
| [ProductSpecification](#productspecification) | 18 |
| [ProductTimeline](#producttimeline) | 0 |
| [ProductType](#producttype) | 2 |
| [Sku](#sku) | 0 |
| [SpecificationMonitor](#specificationmonitor) | 3 |
| [SpecificationNotebook](#specificationnotebook) | 15 |
| [UserDatabase](#userdatabase) | 33 |
| [UserLog](#userlog) | 998 |

---

## BgFile

**Documentos (estimado):** 18

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `bg_word_filename` | String | 100% | Nome do arquivo BG Word gerado. |
| `hero_image` | String | 78% | URL ou caminho da imagem principal (hero) do produto. |
| `url_dealer_page` | String | 78% | URL da página do dealer para o produto. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Category

**Documentos (estimado):** 53

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `meta_tag_description` | String | 100% | Tags para SEO do produto na acerstore VTEX. |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `product_type` | DBRef → `ProductType` | 100% | Tipo de produto (ex: Notebook, Monitor, Desktop). |
| `vtex_id` | Integer | 100% | ID do registro na plataforma VTEX. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Family

**Documentos (estimado):** 1

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `All-In-One` | Array<String> | 100% | — |
| `Desktops` | Array<String> | 100% | — |
| `Especiais` | Array<String> | 100% | — |
| `Mini-Desktop` | Array<String> | 100% | — |
| `Monitores` | Array<String> | 100% | — |
| `Notebooks` | Array<String> | 100% | — |
| `Projetores` | Array<String> | 100% | — |
| `Vestuario` | Array<String> | 100% | — |
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

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

## Product

**Documentos (estimado):** 18

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `ad_words_remarketing_code` | null | 0% | Código de remarketing do Google Ads. |
| `alphanumeric_model` | String | 78% | Modelo alfanumérico do produto. |
| `bg_file` | DBRef → `BgFile` | 100% | Referência ao arquivo de imagem BG Word. |
| `brand_id` | Integer | 100% | Identificador da marca utilizado pela VTEX. |
| `category` | DBRef → `Category` | 78% | Categoria à qual o produto está associado. |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `department_id` | Integer | 100% | Identificador do departamento utilizado pela VTEX. |
| `description` | String | 78% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `description_short` | String | 100% | Descrição curta de um produto, até o momento utilizado apenas para a VTEX. |
| `family` | String | 33% | Família do produto. Este campo não existe na VTEX. |
| `is_active` | Boolean | 100% | Flag para identificar se o produto está ativado na VTEX. |
| `is_complete` | Boolean | 67% | Indica se o cadastro do produto está completo. |
| `is_visible` | Boolean | 100% | Flag para identificar se o produto está visível na VTEX. |
| `key_words` | String | 100% | Palavras-chaves utilizadas para SEO na acerstore VTEX (str concatenada com vírgula). |
| `link_id` | String | 100% | Slug para a página de produto na acerstore VTEX. |
| `lomadee_campaign_code` | null | 0% | Código de campanha Lomadee (afiliados). |
| `meta_tag_description` | String | 100% | Tags para SEO do produto na acerstore VTEX. |
| `name` | String | 83% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `product_specification` | DBRef → `ProductSpecification` | 100% | Referência ao documento de especificações do produto. |
| `product_vtex_id` | Integer | 100% | ID do produto na plataforma VTEX. |
| `ref_id` | String | 100% | Identificador único de um produto, mais conhecido como Part Number. Nome adotado por ser utilizado desta maneira na VTEX. |
| `release_date` | String | 100% | Data de lançamento do produto, não se sabe a regra de negócio envolvida na acerstore/criação do produto. |
| `score` | null | 0% | Campo de ranqueamento utilizado pela VTEX. |
| `show_without_stock` | Boolean | 100% | Flag para definir se o produto é mostrado mesmo sem estoque na acerstore VTEX. |
| `sku` | DBRef → `Sku` | 100% | Relacionamento com SKU, atualmente tratado como 1-1 mas deve ser 1-N (DBRef). |
| `specifications_vtex` | Object | 28% | Especificações sincronizadas com a VTEX. |
| `specifications_vtex.filters` | Array<Object> | 28% | Especificações técnicas utilizada pela VTEX para popular a acerstore. |
| `specifications_vtex.filters[].field_id` | Integer | 11% | ID do campo de especificação na VTEX. |
| `specifications_vtex.filters[].name` | String | 11% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `specifications_vtex.filters[].values` | Array<String> | 11% | Valores do campo de especificação. |
| `specifications_vtex.icons` | Array | 28% | Especificações técnicas utilizada pela VTEX para popular a acerstore. |
| `status` | String | 100% | Status utilizado para o ciclo de vida de um produto, acompanhando do nascimento até a integração com a VTEX/outros integradores. |
| `supplier_id` | null | 0% | ID do fornecedor. |
| `tax_code` | String | 100% | Código do produto, não se sabe a regra. |
| `title` | String | 100% | Título da página quando o produto é acessado na acerstore VTEX. |
| `updated_at` | String | 100% | Data em que o registro foi atualizado. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## ProductSpecification

**Documentos (estimado):** 18

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `specification_monitor` | DBRef → `SpecificationMonitor` | 17% | Referência às especificações técnicas de monitor. |
| `specification_notebook` | DBRef → `SpecificationNotebook` | 83% | Referência às especificações técnicas de notebook. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## ProductTimeline

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## ProductType

**Documentos (estimado):** 2

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

## Sku

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## SpecificationMonitor

**Documentos (estimado):** 3

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `active_display_area` | Array<String> | 100% | Área ativa do display. |
| `angle_inclination` | Array<String> | 100% | Ângulo de inclinação. |
| `anti_reflective_screen` | Array<String> | 100% | Indica tela antirreflexo. |
| `brightness` | Array<String> | 100% | Brilho da tela (nits). |
| `buttons` | Array<String> | 100% | Botões de controle. |
| `certifications` | Array<String> | 100% | Certificações do produto. |
| `color` | Array<String> | 100% | Cor(es) do produto. |
| `color_depth` | Array<String> | 100% | Profundidade de cor. |
| `color_gamut` | Array<String> | 100% | Gama de cores. |
| `dimension_with_packaging` | Array<String> | 100% | Dimensões com embalagem. |
| `dimension_without_packaging` | Array<String> | 100% | Dimensões sem embalagem. |
| `ean` | Array<String> | 100% | Código de barras EAN. |
| `energy_consumption` | Array<String> | 100% | Consumo de energia. |
| `height_adjustment` | Array<String> | 100% | Ajuste de altura. |
| `inputs` | Array<String> | 100% | Entradas/conexões disponíveis. |
| `maximum_contrast` | Array<String> | 100% | Contraste máximo. |
| `model` | Array<String> | 100% | Modelo do produto, essencial. Não utilizado na VTEX. |
| `mtbf` | Array<String> | 100% | Tempo médio entre falhas (MTBF). |
| `native_contrast` | Array<String> | 100% | Contraste nativo. |
| `ncm` | Array<String> | 100% | Código NCM (Nomenclatura Comum do Mercosul). |
| `package_contents` | Array<String> | 100% | Conteúdo da embalagem. |
| `panel_type` | Array<String> | 100% | Tipo de painel (IPS, VA, TN, etc.). |
| `part_number` | Array<String> | 100% | Part number do serviço/produto. |
| `pivo_adjustment` | Array<String> | 100% | Ajuste de pivô (rotação 90°). |
| `pixel_pitch` | Array<String> | 100% | Distância entre pixels (pitch). |
| `power_supply` | Array<String> | 100% | Fonte de alimentação. |
| `resolution_refresh_rate` | Array<String> | 100% | Resolução e taxa de atualização. |
| `response_time` | Array<String> | 100% | Tempo de resposta (ms). |
| `rotation` | Array<String> | 100% | Suporte a rotação. |
| `screen_design` | Array<String> | 100% | Design da tela. |
| `screen_frame` | Array<String> | 100% | Moldura da tela. |
| `screen_ratio` | Array<String> | 100% | Proporção da tela (aspect ratio). |
| `screen_size` | Array<String> | 100% | Tamanho da tela (polegadas). |
| `speakers` | Array<String> | 100% | Auto-falantes integrados. |
| `summary` | Array<String> | 100% | Resumo das especificações. |
| `total_color` | Array<String> | 100% | Total de cores exibíveis. |
| `vertical_horizontal_frequency` | Array<String> | 100% | Frequência vertical/horizontal. |
| `vesa` | Array<String> | 100% | Padrão VESA para montagem em parede/braço. |
| `viewing_angle` | Array<String> | 100% | Ângulo de visão. |
| `warranty` | Array<String> | 100% | Informações de garantia. |
| `weight_with_packaging` | Array<String> | 100% | Peso com embalagem. |
| `weight_without_packaging` | Array<String> | 100% | Peso sem embalagem. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## SpecificationNotebook

**Documentos (estimado):** 15

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `alphanumeric_model` | Array<String> | 100% | Modelo alfanumérico do produto. |
| `anatel_code` | Array<String> | 100% | Código de homologação Anatel. |
| `audio` | Array<String> | 100% | Especificações de áudio. |
| `color` | Array<String> | 100% | Cor(es) do produto. |
| `control` | Array<String> | 100% | Controles do dispositivo. |
| `cpu_chipset` | Array<String> | 100% | Processador e chipset. |
| `dimensions_and_weight` | Array<String> | 100% | Dimensões e peso. |
| `display` | Array<String> | 100% | Especificações da tela. |
| `ean_number` | Array<String> | 100% | Número EAN. |
| `graphics` | Array<String> | 100% | Placa de vídeo / gráficos. |
| `input_and_control` | Array<String> | 100% | Entradas e controles. |
| `memory` | Array<String> | 100% | Especificações de memória. |
| `ncm_number` | Array<String> | 100% | Número NCM. |
| `operating_system` | Array<String> | 100% | Sistema operacional. |
| `package_content` | Array<String> | 100% | Conteúdo da embalagem. |
| `part_number` | Array<String> | 100% | Part number do serviço/produto. |
| `power_battery` | Array<String> | 100% | Bateria e alimentação. |
| `product_observation` | Array<String> | 100% | Observações sobre o produto. |
| `product_view` | Array<String> | 100% | Descrição desconhecida. |
| `security` | Array<String> | 100% | Recursos de segurança. |
| `storage` | Array<String> | 100% | Armazenamento. |
| `summary` | Array<String> | 100% | Resumo das especificações. |
| `upc_number` | Array<String> | 100% | Número UPC. |
| `upgrades` | Array<String> | 100% | Opções de upgrade. |
| `warranty` | Array<String> | 100% | Informações de garantia. |
| `webcam` | Array<String> | 100% | Especificações da webcam. |
| `windows_desktop_apps` | Array<String> | 100% | Aplicativos Windows incluídos. |
| `wireless_networking` | Array<String> | 100% | Rede sem fio (Wi-Fi/Bluetooth). |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## UserDatabase

**Documentos (estimado):** 33

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

## UserLog

**Documentos (estimado):** 998

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
