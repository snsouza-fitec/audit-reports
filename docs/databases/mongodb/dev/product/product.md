# Database: product

[← Voltar ao índice](../README.md)

> **22** collection(s) · ~**9,597** documentos estimados

## Sumário

| Collection | Documentos (est.) |
|------------|-------------------|
| [Agency](#agency) | 11 |
| [AnymarketCharacteristic](#anymarketcharacteristic) | 3 |
| [Bom](#bom) | 1,434 |
| [BomDetails](#bomdetails) | 10 |
| [Category](#category) | 15 |
| [Collection](#collection) | 23 |
| [Family](#family) | 51 |
| [GoogleGlobalCategory](#googleglobalcategory) | 5,595 |
| [HeroDealerUpload](#herodealerupload) | 22 |
| [Model](#model) | 1,022 |
| [PartnerFiles](#partnerfiles) | 199 |
| [Product](#product) | 147 |
| [ProductTimeline](#producttimeline) | 238 |
| [ProductType](#producttype) | 5 |
| [QuickSummary](#quicksummary) | 541 |
| [Service](#service) | 16 |
| [Settings](#settings) | 1 |
| [Sku](#sku) | 184 |
| [SlaNotify](#slanotify) | 0 |
| [Specification](#specification) | 78 |
| [StockSyncDate](#stocksyncdate) | 1 |
| [Template](#template) | 1 |

---

## Agency

**Documentos (estimado):** 11

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `is_active` | Boolean | 100% | Flag para identificar se o produto está ativado na VTEX. |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `responsibles` | Array<Object> | 100% | — |
| `responsibles[].email` | String | 164% | Endereço de e-mail. |
| `responsibles[].name` | String | 164% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `updated_at` | String | 100% | Data em que o registro foi atualizado. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## AnymarketCharacteristic

**Documentos (estimado):** 3

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `characteristics` | Object | 100% | — |
| `characteristics.Acessórios incluídos` | String | 33% | — |
| `characteristics.Altura` | String | 33% | — |
| `characteristics.Altura com embalagem` | String | 33% | — |
| `characteristics.Altura com suporte` | String | 33% | — |
| `characteristics.Altura x Comprimento x Profundidade` | String | 33% | — |
| `characteristics.Brilho` | String | 33% | — |
| `characteristics.Brilho da imagem` | String | 33% | — |
| `characteristics.Cabos incluídos` | String | 67% | — |
| `characteristics.Capacidade máxima suportada da memória RAM` | String | 33% | — |
| `characteristics.Com Bluetooth` | String | 33% | — |
| `characteristics.Com HDMI` | String | 33% | — |
| `characteristics.Com USB` | String | 33% | — |
| `characteristics.Com Wi-Fi` | String | 33% | — |
| `characteristics.Com alto-falante` | String | 33% | — |
| `characteristics.Com alto-falantes embutidos` | String | 33% | — |
| `characteristics.Com altura ajustável` | String | 33% | — |
| `characteristics.Com controle remoto` | String | 33% | — |
| `characteristics.Com função de pivote` | String | 33% | — |
| `characteristics.Com leitor de cartão de memória` | String | 33% | — |
| `characteristics.Com leitor de impressão digital` | String | 33% | — |
| `characteristics.Com microfone` | String | 33% | — |
| `characteristics.Com modo Eco` | String | 33% | — |
| `characteristics.Com montagem VESA` | String | 33% | — |
| `characteristics.Com porta ethernet` | String | 33% | — |
| `characteristics.Com saída para fones de ouvido` | String | 33% | — |
| `characteristics.Com teclado numérico` | String | 33% | — |
| `characteristics.Com teclado retroiluminado` | String | 33% | — |
| `characteristics.Com tecnologia sem flicker` | String | 33% | — |
| `characteristics.Com tela antirreflexo` | String | 33% | — |
| `characteristics.Com tela tátil` | String | 67% | — |
| `characteristics.Com webcam` | String | 33% | — |
| `characteristics.Comprimento com embalagem` | String | 33% | — |
| `characteristics.Comprimento com suporte` | String | 33% | — |
| `characteristics.Conexões de entrada` | String | 33% | — |
| `characteristics.Conexões de saída` | String | 33% | — |
| `characteristics.Conexões do monitor do computador` | String | 33% | — |
| `characteristics.Consumo energético` | String | 33% | — |
| `characteristics.Contraste` | String | 33% | — |
| `characteristics.Cor` | String | 100% | — |
| `characteristics.Duração máxima da bateria` | String | 33% | — |
| `characteristics.Edição do sistema operacional` | String | 33% | — |
| `characteristics.Fontes de luz` | String | 33% | — |
| `characteristics.Frequência de sincronização horizontal` | String | 33% | — |
| `characteristics.Frequência de sincronização vertical` | String | 33% | — |
| `characteristics.Gama de cores` | String | 33% | — |
| `characteristics.Homologação Anatel Nº` | String | 33% | — |
| `characteristics.Idioma do teclado` | String | 33% | — |
| `characteristics.Intervalo de distância de projeção` | String | 33% | — |
| `characteristics.Largura` | String | 33% | — |
| `characteristics.Largura com embalagem` | String | 33% | — |
| `characteristics.Largura com suporte` | String | 33% | — |
| `characteristics.Linha` | String | 100% | — |
| `characteristics.Linha do processador` | String | 33% | — |
| `characteristics.Marca` | String | 100% | — |
| `characteristics.Marca do processador` | String | 33% | — |
| `characteristics.Memória RAM` | String | 33% | — |
| `characteristics.Memória de vídeo` | String | 33% | — |
| `characteristics.Modelo` | String | 100% | — |
| `characteristics.Modelo alfanumérico` | String | 100% | — |
| `characteristics.Modelo detalhado` | String | 100% | — |
| `characteristics.Modelo do processador` | String | 33% | — |
| `characteristics.Modos de som` | String | 33% | — |
| `characteristics.Nome do sistema operacional` | String | 33% | — |
| `characteristics.Peso` | String | 67% | — |
| `characteristics.Peso com embalagem` | String | 33% | — |
| `characteristics.Peso e dimensões` | String | 67% | — |
| `characteristics.Peso sem embalagem` | String | 33% | — |
| `characteristics.Placa gráfica` | String | 33% | — |
| `characteristics.Portas de vídeo` | String | 33% | — |
| `characteristics.Profundidade` | String | 33% | — |
| `characteristics.Quantidade de alto-falantes` | String | 33% | — |
| `characteristics.Quantidade de cores da tela` | String | 33% | — |
| `characteristics.Quantidade de núcleos` | String | 33% | — |
| `characteristics.Quantidade de slots para a memória RAM` | String | 33% | — |
| `characteristics.Quantidade total de portas USB` | String | 33% | — |
| `characteristics.Relação de aspecto` | String | 67% | — |
| `characteristics.Relação de contraste` | String | 33% | — |
| `characteristics.Resolução da tela` | String | 67% | — |
| `characteristics.Resolução de vídeo da webcam` | String | 33% | — |
| `characteristics.Resolução nativa` | String | 33% | — |
| `characteristics.Sistemas operacionais compatíveis` | String | 33% | — |
| `characteristics.Software incluídos` | String | 33% | — |
| `characteristics.Tamanho da imagem` | String | 33% | — |
| `characteristics.Tamanho da tela` | String | 67% | — |
| `characteristics.Taxa de atualização` | String | 33% | — |
| `characteristics.Taxa de atualização da tela` | String | 33% | — |
| `characteristics.Tecnologia de projeção` | String | 33% | — |
| `characteristics.Tempo de resposta` | String | 33% | — |
| `characteristics.Tipo de bateria` | String | 33% | — |
| `characteristics.Tipo de memória RAM` | String | 33% | — |
| `characteristics.Tipo de painel` | String | 67% | — |
| `characteristics.Tipo de resolução` | String | 33% | — |
| `characteristics.Tipo de resolução da tela` | String | 33% | — |
| `characteristics.Tipo de resolução de vídeo da webcam` | String | 33% | — |
| `characteristics.Tipo de resolução suportada` | String | 33% | — |
| `characteristics.Tipo de tela` | String | 67% | — |
| `characteristics.Tipos de memória de vídeo` | String | 33% | — |
| `characteristics.Velocidade da memória RAM` | String | 33% | — |
| `characteristics.Velocidade máxima do processador` | String | 33% | — |
| `characteristics.Versão do sistema operacional` | String | 33% | — |
| `characteristics.Vida útil da fonte de luz (modo padrão)` | String | 33% | — |
| `characteristics.Voltagem` | String | 67% | — |
| `characteristics.É 2 em 1` | String | 33% | — |
| `characteristics.É antirreflexo` | String | 33% | — |
| `characteristics.É curvo` | String | 33% | — |
| `characteristics.É gamer` | String | 67% | — |
| `characteristics.É giratório` | String | 33% | — |
| `characteristics.É mini` | String | 33% | — |
| `characteristics.É netbook` | String | 33% | — |
| `characteristics.É portátil` | String | 33% | — |
| `characteristics.É reclinável` | String | 33% | — |
| `characteristics.É ultrabook` | String | 33% | — |
| `product_type` | String | 100% | Tipo de produto (ex: Notebook, Monitor, Desktop). |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Bom

**Documentos (estimado):** 1,434

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `a_cover` | String | 100% | Descrição desconhecida. |
| `accessory_1` | String | 100% | Acessório 1. |
| `accessory_2` | String | 100% | Acessório 2. |
| `accessory_3` | String | 100% | Acessório 3. |
| `accessory_4` | String | 100% | Acessório 4. |
| `accessory_5` | String | 100% | Acessório 5. |
| `accessory_6` | String | 100% | Acessório 6. |
| `accessory_7` | String | 100% | Acessório 7. |
| `account_name` | String | 100% | Nome da conta/cliente. |
| `adapter` | String | 100% | Adaptador de energia. |
| `adapter_2` | String | 100% | Adaptador secundário. |
| `b_cover` | String | 100% | Descrição desconhecida. |
| `battery` | String | 100% | Bateria principal. |
| `battery_2` | String | 100% | Bateria secundária. |
| `bom_name` | String | 100% | Nome/código do BOM (Bill of Materials). |
| `brand` | String | 100% | Marca do produto. |
| `camera` | String | 100% | Câmera / webcam. |
| `camera_2` | String | 100% | Câmera secundária. |
| `camera_3` | String | 100% | Câmera terciária. |
| `card_reader` | String | 100% | Leitor de cartão. |
| `cd` | String | 100% | Unidade óptica (CD/DVD). |
| `cobrand_royalty` | String | 100% | Descrição desconhecida. |
| `country` | String | 100% | País de destino. |
| `country_kit` | String | 100% | Descrição desconhecida. |
| `cpu` | String | 100% | Processador do equipamento. |
| `description` | String | 100% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `ean` | String | 100% | Código de barras EAN. |
| `extra_ap` | String | 100% | Descrição desconhecida. |
| `extra_battery` | String | 100% | Bateria extra. |
| `finger_print` | String | 100% | Sensor de impressão digital. |
| `for_description` | String | 100% | Descrição desconhecida. |
| `hdd_1` | String | 100% | Armazenamento (slot 1). |
| `hdd_2` | String | 100% | Armazenamento (slot 2). |
| `hdd_3` | String | 100% | Armazenamento (slot 3). |
| `hdd_4` | String | 100% | Armazenamento (slot 4). |
| `kb` | String | 100% | Teclado. |
| `label` | String | 100% | Descrição desconhecida. |
| `lcd` | String | 100% | Tela / display LCD. |
| `logo` | String | 100% | Descrição desconhecida. |
| `marketing_name` | String | 100% | Nome de marketing do produto. |
| `memory_1` | String | 100% | Módulo de memória RAM (slot 1). |
| `memory_2` | String | 100% | Módulo de memória RAM (slot 2). |
| `memory_3` | String | 100% | Módulo de memória RAM (slot 3). |
| `memory_4` | String | 100% | Módulo de memória RAM (slot 4). |
| `model` | String | 100% | Modelo do produto, essencial. Não utilizado na VTEX. |
| `ms_special` | String | 100% | Descrição desconhecida. |
| `nb_chipset` | String | 100% | Chipset da placa-mãe. |
| `ns` | String | 100% | Descrição desconhecida. |
| `odd_1` | String | 100% | Unidade óptica (ODD). |
| `odm` | String | 100% | Fabricante ODM (Original Design Manufacturer). |
| `os` | String | 100% | Sistema operacional. |
| `os_2` | String | 100% | Sistema operacional secundário. |
| `os_country_kit` | String | 100% | Descrição desconhecida. |
| `os_manual` | String | 100% | Descrição desconhecida. |
| `pn_apply_time` | String | 100% | Descrição desconhecida. |
| `pn_cfm_time` | String | 100% | Descrição desconhecida. |
| `power_cord` | String | 100% | Cabo de energia. |
| `printing` | String | 100% | Descrição desconhecida. |
| `product_name` | String | 100% | Nome do produto. |
| `project_name` | String | 100% | Nome do projeto interno. |
| `ref_id` | String | 100% | Identificador único de um produto, mais conhecido como Part Number. Nome adotado por ser utilizado desta maneira na VTEX. |
| `ro` | String | 100% | Descrição desconhecida. |
| `ship_mark` | String | 100% | Descrição desconhecida. |
| `sim_lock` | String | 100% | Descrição desconhecida. |
| `softload` | String | 100% | Descrição desconhecida. |
| `special_package` | String | 100% | Descrição desconhecida. |
| `special_request` | String | 100% | Descrição desconhecida. |
| `sub_brand` | String | 100% | Submarca. |
| `tender_type` | String | 100% | Descrição desconhecida. |
| `unique_itens_remark` | String | 100% | Descrição desconhecida. |
| `upc` | String | 100% | Código de barras UPC. |
| `users_guide` | String | 100% | Manual do usuário. |
| `vga_chip` | String | 100% | Chip de vídeo. |
| `vram_1` | String | 100% | Memória de vídeo (slot 1). |
| `vram_2` | String | 100% | Memória de vídeo (slot 2). |
| `vram_3` | String | 100% | Memória de vídeo (slot 3). |
| `vram_4` | String | 100% | Memória de vídeo (slot 4). |
| `warranty_card` | String | 100% | Cartão de garantia. |
| `wireless_lan` | String | 100% | Módulo de Wi-Fi / rede sem fio. |
| `wwan` | String | 100% | Módulo WWAN (3G/4G/5G). |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## BomDetails

**Documentos (estimado):** 10

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `detail` | String | 40% | Detalhe/observação sobre a importação do BOM. |
| `file` | String | 100% | Nome do arquivo importado. |
| `imported_at` | String | 100% | Data/hora da importação. |
| `is_main` | Boolean | 100% | Indica se é o BOM principal. |
| `status` | String | 100% | Status utilizado para o ciclo de vida de um produto, acompanhando do nascimento até a integração com a VTEX/outros integradores. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Category

**Documentos (estimado):** 15

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `active_store_front_link` | Boolean | 100% | Link ativo na vitrine da loja. |
| `anymarket_id` | Integer | 27% | ID do registro no Anymarket. |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `description` | String | 100% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `father_category_id` | Integer | 100% | ID da categoria pai na VTEX. |
| `global_category_id` | Integer | 100% | ID da categoria global (Google). |
| `global_category_name` | String | 100% | Nome da categoria global (Google). |
| `is_active` | Boolean | 100% | Flag para identificar se o produto está ativado na VTEX. |
| `keywords` | String | 100% | Palavras-chave da categoria (SEO). |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `product_type` | DBRef → `ProductType` | 100% | Tipo de produto (ex: Notebook, Monitor, Desktop). |
| `show_brand_filter` | Boolean | 100% | Exibir filtro por marca na categoria. |
| `show_in_store_front` | Boolean | 100% | Exibir categoria na vitrine da loja. |
| `stock_keeping_unit_selection_mode` | String | 100% | Descrição desconhecida. |
| `title` | String | 100% | Título da página quando o produto é acessado na acerstore VTEX. |
| `updated_at` | String | 100% | Data em que o registro foi atualizado. |
| `vtex_id` | Integer | 100% | ID do registro na plataforma VTEX. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Collection

**Documentos (estimado):** 23

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `date_from` | Date | 100% | Data de início (vigência). |
| `date_to` | Date | 100% | Data de término (vigência). |
| `description` | String | 100% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `highlight` | Boolean | 100% | Indica se está em destaque. |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `products` | Array<String> | 100% | Lista de IDs de produtos vinculados. |
| `searchable` | Boolean | 100% | Indica se é pesquisável. |
| `type` | null | 0% | Tipo de registro (ex: info, warning, error). |
| `vtex_id` | Integer | 100% | ID do registro na plataforma VTEX. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Family

**Documentos (estimado):** 51

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `product_type` | String | 100% | Tipo de produto (ex: Notebook, Monitor, Desktop). |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `name_1` | `name` (ASC) | — |

---

## GoogleGlobalCategory

**Documentos (estimado):** 5,595

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `google_id` | Integer | 100% | ID da categoria no Google Merchant. |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## HeroDealerUpload

**Documentos (estimado):** 22

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `dealer_s3_filename` | String | 100% | Nome do arquivo de dealer no S3. |
| `detail` | String | 36% | Detalhe/observação sobre a importação do BOM. |
| `hero_s3_filename` | String | 100% | Nome do arquivo hero no S3. |
| `product_id` | String | 100% | ID do produto relacionado. |
| `status` | String | 100% | Status utilizado para o ciclo de vida de um produto, acompanhando do nascimento até a integração com a VTEX/outros integradores. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Model

**Documentos (estimado):** 1,022

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `family` | DBRef → `Family` | 100% | Família do produto. Este campo não existe na VTEX. |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |
| `family_1` | `family` (ASC) | — |
| `name_1` | `name` (ASC) | — |

---

## PartnerFiles

**Documentos (estimado):** 199

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `dealer_page_partner_url` | String | 40% | URL da página do dealer no parceiro. |
| `hero_image_partner_url` | String | 14% | URL da imagem hero no parceiro. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Product

**Documentos (estimado):** 147

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `brand_id` | Integer | 100% | Identificador da marca utilizado pela VTEX. |
| `category` | DBRef → `Category` \| Object | 100% | Categoria à qual o produto está associado. |
| `category.active_store_front_link` | Boolean | 4% | Link ativo na vitrine da loja. |
| `category.anymarket_id` | Integer | 2% | ID do registro no Anymarket. |
| `category.created_at` | String | 4% | Data de criação do registro na base de dados. |
| `category.description` | String | 4% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `category.father_category_id` | Integer | 4% | ID da categoria pai na VTEX. |
| `category.global_category_id` | Integer | 4% | ID da categoria global (Google). |
| `category.global_category_name` | String | 4% | Nome da categoria global (Google). |
| `category.id` | ObjectId | 4% | — |
| `category.is_active` | Boolean | 4% | Flag para identificar se o produto está ativado na VTEX. |
| `category.keywords` | String | 4% | Palavras-chave da categoria (SEO). |
| `category.name` | String | 4% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `category.product_type` | Object | 4% | Tipo de produto (ex: Notebook, Monitor, Desktop). |
| `category.product_type.global_category` | Object | 4% | Referência à categoria global do Google. |
| `category.product_type.global_category.google_id` | Integer | 4% | ID da categoria no Google Merchant. |
| `category.product_type.global_category.id` | ObjectId | 4% | — |
| `category.product_type.global_category.name` | String | 4% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `category.product_type.id` | ObjectId | 4% | — |
| `category.product_type.name` | String | 4% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `category.product_type.vtex_id` | Integer | 4% | ID do registro na plataforma VTEX. |
| `category.show_brand_filter` | Boolean | 4% | Exibir filtro por marca na categoria. |
| `category.show_in_store_front` | Boolean | 4% | Exibir categoria na vitrine da loja. |
| `category.stock_keeping_unit_selection_mode` | String | 4% | Descrição desconhecida. |
| `category.title` | String | 4% | Título da página quando o produto é acessado na acerstore VTEX. |
| `category.updated_at` | String | 4% | Data em que o registro foi atualizado. |
| `category.vtex_id` | Integer | 4% | ID do registro na plataforma VTEX. |
| `collections` | Array<DBRef → `Collection`> | 10% | Coleções / vitrines às quais o produto pertence. |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `department_id` | Integer | 88% | Identificador do departamento utilizado pela VTEX. |
| `description` | String | 100% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `description_short` | String | 8% | Descrição curta de um produto, até o momento utilizado apenas para a VTEX. |
| `external_characteristics` | String | 94% | Características externas de um produto. |
| `family` | String | 100% | Família do produto. Este campo não existe na VTEX. |
| `filters` | Array<Object> | 84% | Especificações técnicas utilizada pela VTEX para popular a acerstore. |
| `filters[].field_id` | Integer | 78% | ID do campo de especificação na VTEX. |
| `filters[].name` | String | 78% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `filters[].values` | Array<String> | 78% | Valores do campo de especificação. |
| `has_upgrade` | Boolean | 12% | Flag para identificar se o produto tem upgrade, utilizado apenas para VTEX. |
| `icons` | Array | 82% | Especificações técnicas utilizada pela VTEX para popular a acerstore. |
| `id` | ObjectId | 4% | — |
| `integrated_channels` | Object | 100% | Objeto com identificadores para onde o produto foi enviado (CISP1, Anymarket ou VTEX). |
| `integrated_channels.anymarket` | Object | 100% | Status de integração com Anymarket. |
| `integrated_channels.anymarket.id` | Integer | 4% | — |
| `integrated_channels.anymarket.integrated` | Boolean | 100% | Indica se está integrado ao canal. |
| `integrated_channels.cisp1` | Object | 100% | Status de integração com CISP1. |
| `integrated_channels.cisp1.id` | Integer | 2% | — |
| `integrated_channels.cisp1.integrated` | Boolean | 100% | Indica se está integrado ao canal. |
| `integrated_channels.cisp1.was_sent` | Boolean | 6% | Indica se foi enviado ao canal. |
| `integrated_channels.vtex` | Object | 100% | Status de integração com VTEX. |
| `integrated_channels.vtex.id` | Integer | 94% | — |
| `integrated_channels.vtex.integrated` | Boolean | 100% | Indica se está integrado ao canal. |
| `is_active` | Boolean | 94% | Flag para identificar se o produto está ativado na VTEX. |
| `is_b2b` | null | 0% | Flag para identificar se um produto está vinculado a políticas comerciais B2B na VTEX. |
| `is_protheus_imported` | Boolean | 14% | Flag para identificar se o produto foi sincronizado do Protheus. |
| `is_service` | Boolean | 100% | Flag para saber se o produto é do tipo serviço. |
| `is_visible` | Boolean | 90% | Flag para identificar se o produto está visível na VTEX. |
| `key_words` | String | 24% | Palavras-chaves utilizadas para SEO na acerstore VTEX (str concatenada com vírgula). |
| `kit_type` | null | 0% | Flag para saber qual tipo de KIT é (brinde ou junção de dois itens pagos). |
| `link_id` | String | 94% | Slug para a página de produto na acerstore VTEX. |
| `meta_tag_description` | String | 100% | Tags para SEO do produto na acerstore VTEX. |
| `model` | String | 100% | Modelo do produto, essencial. Não utilizado na VTEX. |
| `name` | String | 94% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `overview` | String | 94% | Resumo do produto, campo opcional mas pedido pelo cliente. |
| `partner_files` | DBRef → `PartnerFiles` \| Object | 100% | Relacionamento com arquivos do AcerParceiros (DBRef). |
| `partner_files.dealer_page_partner_url` | String | 4% | URL da página do dealer no parceiro. |
| `partner_files.hero_image_partner_url` | String | 4% | URL da imagem hero no parceiro. |
| `partner_files.id` | ObjectId | 4% | — |
| `products_ids` | Array<String> | 2% | — |
| `ref_id` | String | 100% | Identificador único de um produto, mais conhecido como Part Number. Nome adotado por ser utilizado desta maneira na VTEX. |
| `release_date` | String | 88% | Data de lançamento do produto, não se sabe a regra de negócio envolvida na acerstore/criação do produto. |
| `score` | Integer | 82% | Campo de ranqueamento utilizado pela VTEX. |
| `services` | Array<Object> | 100% | Serviços vinculado a um produto, enviado pelo gestão de serviços para ser integrado na VTEX. |
| `services[].salles_channels` | Array<Object> | 18% | Canais de venda do serviço. |
| `services[].salles_channels[].campaign` | Object | 10% | — |
| `services[].salles_channels[].campaign.call` | String | 10% | — |
| `services[].salles_channels[].campaign.description` | String | 10% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `services[].salles_channels[].campaign.end_date` | String | 10% | Data/hora de término da sincronização. |
| `services[].salles_channels[].campaign.name` | String | 10% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `services[].salles_channels[].campaign.start_date` | String | 10% | Data/hora de início da sincronização. |
| `services[].salles_channels[].campaign.status` | Boolean | 10% | Status utilizado para o ciclo de vida de um produto, acompanhando do nascimento até a integração com a VTEX/outros integradores. |
| `services[].salles_channels[].campaign.tag` | String | 10% | — |
| `services[].salles_channels[].cost` | Double | 38% | — |
| `services[].salles_channels[].name` | String | 38% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `services[].salles_channels[].price` | Double | 38% | Preço do SKU. |
| `services[].salles_channels[].product_part_number` | String | 4% | — |
| `services[].salles_channels[].recommended` | String | 38% | — |
| `services[].service_details` | Object | 18% | Detalhes do serviço associado. |
| `services[].service_details._id` | ObjectId | 18% | Identificador utilizado pelo MongoDB (ObjectId). |
| `services[].service_details.benefits` | Array<String> | 18% | Lista de benefícios do serviço. |
| `services[].service_details.business_type` | String | 16% | Tipo de negócio (B2B, B2C, etc.). |
| `services[].service_details.commercial_name` | String | 18% | Nome comercial do serviço. |
| `services[].service_details.contractual_term_url` | String | 18% | URL do termo contratual. |
| `services[].service_details.description` | String | 18% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `services[].service_details.general_condition_url` | String | 18% | URL das condições gerais. |
| `services[].service_details.gs_id` | String | 18% | Descrição desconhecida. |
| `services[].service_details.imported_by` | String | 18% | Usuário/sistema que realizou a importação. |
| `services[].service_details.name` | String | 18% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `services[].service_details.part_number` | String | 18% | Part number do serviço/produto. |
| `services[].service_details.products_associateds` | Array<String> | 18% | Lista de produtos associados ao serviço. |
| `services[].service_details.published` | Boolean | 16% | Indica se o serviço está publicado. |
| `services[].service_details.revision_id` | null | 0% | — |
| `services[].service_details.service_type` | String | 18% | Tipo do serviço (ex: garantia, seguro). |
| `services[].service_details.term` | String | 18% | Prazo do serviço. |
| `show_without_stock` | Boolean | 90% | Flag para definir se o produto é mostrado mesmo sem estoque na acerstore VTEX. |
| `sku` | DBRef → `Sku` \| Object | 100% | Relacionamento com SKU, atualmente tratado como 1-1 mas deve ser 1-N (DBRef). |
| `sku.activate_if_possible` | null | 0% | Descrição desconhecida. |
| `sku.anymarket_id` | null | 0% | ID do registro no Anymarket. |
| `sku.commercial_condition_id` | null | 0% | ID da condição comercial na VTEX. |
| `sku.created_at` | String | 4% | Data de criação do registro na base de dados. |
| `sku.creation_date` | null | 0% | Data de criação do SKU. |
| `sku.cubic_weight` | null | 0% | Peso cúbico para cálculo de frete. |
| `sku.estimated_date_arrival` | null | 0% | Data estimada de chegada ao estoque. |
| `sku.height` | null | 0% | Altura do produto (cm). |
| `sku.id` | ObjectId | 4% | — |
| `sku.is_active` | null | 0% | Flag para identificar se o produto está ativado na VTEX. |
| `sku.is_kit` | null | 0% | Indica se o SKU é um kit de produtos. |
| `sku.kit_itens_sell_apart` | null | 0% | Indica se os itens do kit podem ser vendidos separadamente. |
| `sku.length` | null | 0% | Comprimento do produto (cm). |
| `sku.low_stock_anymarket` | null | 0% | Limite de estoque baixo para alerta no Anymarket. |
| `sku.low_stock_vtex` | null | 0% | Limite de estoque baixo para alerta na VTEX. |
| `sku.manufacturer_code` | null | 0% | Código do fabricante. |
| `sku.measurement_unit` | null | 0% | Unidade de medida do produto. |
| `sku.modal_type` | null | 0% | Descrição desconhecida. |
| `sku.name` | null | 0% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `sku.packaged_height` | null | 0% | Altura com embalagem (cm). |
| `sku.packaged_length` | null | 0% | Comprimento com embalagem (cm). |
| `sku.packaged_weight_kg` | null | 0% | Peso com embalagem (kg). |
| `sku.packaged_width` | null | 0% | Largura com embalagem (cm). |
| `sku.prices` | Object | 2% | Objeto com preços por canal de venda. |
| `sku.prices.anymarket` | null | 0% | — |
| `sku.prices.cisp1` | null | 0% | — |
| `sku.prices.vtex` | null | 0% | — |
| `sku.ref_id` | null | 0% | Identificador único de um produto, mais conhecido como Part Number. Nome adotado por ser utilizado desta maneira na VTEX. |
| `sku.reward_value` | null | 0% | Descrição desconhecida. |
| `sku.sku_files` | Array<Object> | 4% | Lista de arquivos (imagens) associados ao SKU. |
| `sku.sku_files[].is_cover_bg_image` | Boolean | 4% | Indica se a imagem é a capa do BG Word. |
| `sku.sku_files[].main` | null | 0% | Indica se é a imagem principal do produto. |
| `sku.sku_files[].name` | String | 4% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `sku.sku_files[].order` | null | 0% | Ordem de exibição da imagem. |
| `sku.sku_files[].s3_filename` | String | 4% | Nome do arquivo armazenado no Amazon S3. |
| `sku.sku_kit_itens` | Array | 4% | Lista de itens que compõem o kit. |
| `sku.stock_protheus` | Array<Object> | 4% | Dados de estoque importados do ERP Protheus. |
| `sku.stock_protheus[].company_branch` | String | 8% | — |
| `sku.stock_protheus[].stock_quantity` | Integer | 8% | — |
| `sku.stock_protheus[].warehouse` | String | 8% | — |
| `sku.stock_quantity_anymarket` | null | 0% | Quantidade em estoque sincronizada com Anymarket. |
| `sku.stock_quantity_vtex` | null | 0% | Quantidade em estoque sincronizada com VTEX. |
| `sku.stock_virtual_quantity_vtex` | null | 0% | Quantidade virtual de estoque na VTEX. |
| `sku.unit_multiplier` | null | 0% | Multiplicador de unidade de venda. |
| `sku.updated_at` | String | 4% | Data em que o registro foi atualizado. |
| `sku.videos` | null | 0% | URLs de vídeos do produto. |
| `sku.vtex_id` | null | 0% | ID do registro na plataforma VTEX. |
| `sku.weight_kg` | null | 0% | Peso do produto (kg). |
| `sku.width` | null | 0% | Largura do produto (cm). |
| `status` | String | 100% | Status utilizado para o ciclo de vida de um produto, acompanhando do nascimento até a integração com a VTEX/outros integradores. |
| `support_files` | null | 0% | Arquivos de suporte para agência/criação de um produto, não é enviado para VTEX. |
| `tax_code` | String | 10% | Código do produto, não se sabe a regra. |
| `technical_specification` | Object | 94% | Especificações técnicas do produto de acordo com os campos da VTEX. É um campo VTEX mas extremamente importante para o produto. |
| `technical_specification.123` | String | 6% | — |
| `technical_specification.12313` | Array<String> \| String | 12% | — |
| `technical_specification.321231` | String | 6% | — |
| `technical_specification.7126387126` | String | 6% | — |
| `technical_specification.Acer PN` | Array<String> \| String | 18% | — |
| `technical_specification.Aplicativos` | Array<String> \| String | 16% | — |
| `technical_specification.Armazenamento` | Array<String> \| String | 20% | — |
| `technical_specification.Bateria e Alimentação` | Array<String> \| String | 18% | — |
| `technical_specification.CBH_ProductName` | Array<String> \| String | 12% | — |
| `technical_specification.CRF_ProductName` | Array<String> \| String | 12% | — |
| `technical_specification.Conexão` | Array<String> | 2% | — |
| `technical_specification.Conteúdo da Embalagem` | Array<String> \| String | 18% | — |
| `technical_specification.Controle` | Array<String> \| String | 18% | — |
| `technical_specification.Cor` | Array<String> \| String | 20% | — |
| `technical_specification.Código ANATEL` | Array<String> \| String | 16% | — |
| `technical_specification.Dimensões e Peso` | Array<String> \| String | 18% | — |
| `technical_specification.EAN` | Array<String> \| String | 18% | — |
| `technical_specification.Garantia` | String | 10% | — |
| `technical_specification.Garantia ` | Array<String> | 6% | — |
| `technical_specification.Garantia do Fabricante` | Array<String> | 6% | — |
| `technical_specification.Gráficos` | Array<String> \| String | 20% | — |
| `technical_specification.MGZ_ProductName` | Array<String> \| String | 12% | — |
| `technical_specification.Memória` | Array<String> \| String | 18% | — |
| `technical_specification.Memória RAM` | String | 2% | — |
| `technical_specification.Observações do Produto` | Array<String> \| String | 16% | — |
| `technical_specification.Processador e Chipset` | Array<String> \| String | 20% | — |
| `technical_specification.Resolução de Tela` | Array<String> | 2% | — |
| `technical_specification.SOBRE O PRODUTO` | Array<String> | 6% | — |
| `technical_specification.Saiba Mais` | String | 10% | — |
| `technical_specification.Saiba Mais ` | Array<String> | 6% | — |
| `technical_specification.Sistema Operacional` | Array<String> \| String | 18% | — |
| `technical_specification.Teclados e  Touchpad` | Array<String> \| String | 18% | — |
| `technical_specification.Tela` | Array<String> \| String | 18% | — |
| `technical_specification.Upgrades` | Array<String> \| String | 16% | — |
| `technical_specification.Vídeo` | Array<String> | 6% | — |
| `technical_specification.Webcam` | Array<String> \| String | 18% | — |
| `technical_specification.Wi-Fi e Rede` | Array<String> \| String | 18% | — |
| `technical_specification.teste cache` | String | 6% | — |
| `technical_specification.teste cache 1233` | String | 6% | — |
| `technical_specification.teste cache 2` | String | 6% | — |
| `technical_specification.teste cache 3` | String | 6% | — |
| `technical_specification.teste cache 4` | String | 6% | — |
| `technical_specification.teste cache 5` | String | 6% | — |
| `technical_specification.teste new form` | String | 6% | — |
| `technical_specification.Áudio e Microfone` | Array<String> \| String | 18% | — |
| `title` | String | 98% | Título da página quando o produto é acessado na acerstore VTEX. |
| `updated_at` | String | 100% | Data em que o registro foi atualizado. |
| `vtex_legacy` | Boolean | 100% | Flag para identificar se o produto foi importado da VTEX. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## ProductTimeline

**Documentos (estimado):** 238

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `date` | String | 100% | Data/hora do evento. |
| `description` | String | 6% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `product_id` | String | 100% | ID do produto relacionado. |
| `status` | String | 100% | Status utilizado para o ciclo de vida de um produto, acompanhando do nascimento até a integração com a VTEX/outros integradores. |
| `user_id` | String | 100% | ID do usuário associado. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## ProductType

**Documentos (estimado):** 5

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `global_category` | DBRef → `GoogleGlobalCategory` | 100% | Referência à categoria global do Google. |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `vtex_id` | Integer | 100% | ID do registro na plataforma VTEX. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## QuickSummary

**Documentos (estimado):** 541

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `alerts` | String | 100% | Alertas gerados pela análise. |
| `created_at` | Date | 100% | Data de criação do registro na base de dados. |
| `highlights` | String | 100% | Destaques do produto. |
| `quick_summary` | String | 100% | Resumo rápido do produto. |
| `suggestions` | String | 100% | Sugestões de melhoria. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Service

**Documentos (estimado):** 16

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `benefits` | Array<String> | 100% | Lista de benefícios do serviço. |
| `business_type` | String | 100% | Tipo de negócio (B2B, B2C, etc.). |
| `commercial_name` | String | 100% | Nome comercial do serviço. |
| `contractual_term_url` | String | 100% | URL do termo contratual. |
| `description` | String | 100% | Descrição de um produto, não exclusivo da VTEX, é um resumo das especificações técnicas preenchidas. |
| `general_condition_url` | String | 100% | URL das condições gerais. |
| `gs_id` | String | 100% | Descrição desconhecida. |
| `imported_by` | String | 100% | Usuário/sistema que realizou a importação. |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `part_number` | String | 100% | Part number do serviço/produto. |
| `products_associateds` | Array<String> | 100% | Lista de produtos associados ao serviço. |
| `published` | Boolean | 100% | Indica se o serviço está publicado. |
| `service_type` | String | 100% | Tipo do serviço (ex: garantia, seguro). |
| `term` | String | 100% | Prazo do serviço. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Settings

**Documentos (estimado):** 1

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `sla_days` | Object | 100% | Configuração de dias de SLA por status. |
| `sla_days.EM RASCUNHO DO PRODUTO` | Integer | 100% | Dias de SLA para status Em Rascunho do Produto. |
| `sla_days.EM RASCUNHO NO E-COMMERCE` | Integer | 100% | Dias de SLA para status Em Rascunho no E-Commerce. |
| `sla_days.PENDENTE DE CADASTRO NO PROTHEUS` | Integer | 100% | Dias de SLA para status Pendente de Cadastro no Protheus. |
| `sla_days.PENDENTE DE ENVIO PARA AGÊNCIA` | Integer | 100% | Dias de SLA para status Pendente de Envio para Agência. |
| `sla_days.PENDENTE DE LIBERAÇÃO DA AGÊNCIA` | Integer | 100% | Dias de SLA para status Pendente de Liberação da Agência. |
| `sla_days.PENDENTE DE PRECIFICAÇÃO` | Integer | 100% | Dias de SLA para status Pendente de Precificação. |
| `stock` | Object | 100% | Configurações de estoque. |
| `stock.cronjob_time` | String | 100% | Horário do cron job de sincronização de estoque. |
| `stock.minimal_stock` | Integer | 100% | Estoque mínimo para gerar alerta. |
| `stock.type_of_alert` | String | 100% | Tipo de alerta de estoque. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Sku

**Documentos (estimado):** 184

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `activate_if_possible` | Boolean | 82% | Descrição desconhecida. |
| `anymarket_id` | Integer | 2% | ID do registro no Anymarket. |
| `commercial_condition_id` | Integer | 82% | ID da condição comercial na VTEX. |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `creation_date` | String | 82% | Data de criação do SKU. |
| `cubic_weight` | Double | 82% | Peso cúbico para cálculo de frete. |
| `estimated_date_arrival` | String | 8% | Data estimada de chegada ao estoque. |
| `height` | Double | 82% | Altura do produto (cm). |
| `is_active` | Boolean | 82% | Flag para identificar se o produto está ativado na VTEX. |
| `is_kit` | Boolean | 82% | Indica se o SKU é um kit de produtos. |
| `kit_itens_sell_apart` | Boolean | 82% | Indica se os itens do kit podem ser vendidos separadamente. |
| `length` | Double | 82% | Comprimento do produto (cm). |
| `low_stock_anymarket` | null | 0% | Limite de estoque baixo para alerta no Anymarket. |
| `low_stock_vtex` | null | 0% | Limite de estoque baixo para alerta na VTEX. |
| `manufacturer_code` | String | 22% | Código do fabricante. |
| `measurement_unit` | String | 82% | Unidade de medida do produto. |
| `modal_type` | String | 6% | Descrição desconhecida. |
| `name` | String | 82% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `packaged_height` | Double | 82% | Altura com embalagem (cm). |
| `packaged_length` | Double | 82% | Comprimento com embalagem (cm). |
| `packaged_weight_kg` | Double | 82% | Peso com embalagem (kg). |
| `packaged_width` | Double | 82% | Largura com embalagem (cm). |
| `price` | null | 0% | Preço do SKU. |
| `price_anymarket` | Integer | 2% | Preço no canal Anymarket. |
| `prices` | Object | 86% | Objeto com preços por canal de venda. |
| `prices.anymarket` | Integer | 4% | — |
| `prices.cisp1` | Double | 4% | — |
| `prices.vtex` | Double \| Integer | 60% | — |
| `ref_id` | String | 82% | Identificador único de um produto, mais conhecido como Part Number. Nome adotado por ser utilizado desta maneira na VTEX. |
| `reward_value` | Integer | 16% | Descrição desconhecida. |
| `sku_files` | Array<Object> | 100% | Lista de arquivos (imagens) associados ao SKU. |
| `sku_files[].is_cover_bg_image` | Boolean | 156% | Indica se a imagem é a capa do BG Word. |
| `sku_files[].main` | Boolean | 118% | Indica se é a imagem principal do produto. |
| `sku_files[].name` | String | 156% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `sku_files[].order` | Integer | 26% | Ordem de exibição da imagem. |
| `sku_files[].s3_filename` | String | 156% | Nome do arquivo armazenado no Amazon S3. |
| `sku_kit_itens` | Array<Object> | 100% | Lista de itens que compõem o kit. |
| `sku_kit_itens[].family` | String | 12% | Família do produto. Este campo não existe na VTEX. |
| `sku_kit_itens[].image` | String | 12% | — |
| `sku_kit_itens[].model` | String | 12% | Modelo do produto, essencial. Não utilizado na VTEX. |
| `sku_kit_itens[].product_id` | ObjectId | 12% | ID do produto relacionado. |
| `sku_kit_itens[].product_name` | String | 12% | Nome do produto. |
| `sku_kit_itens[].ref_id` | String | 12% | Identificador único de um produto, mais conhecido como Part Number. Nome adotado por ser utilizado desta maneira na VTEX. |
| `sku_kit_itens[].sku_id` | ObjectId | 16% | — |
| `sku_kit_itens[].sku_name` | String | 16% | — |
| `sku_kit_itens[].sku_vtex_id` | Integer | 16% | — |
| `stock_protheus` | Array<Object> | 100% | Dados de estoque importados do ERP Protheus. |
| `stock_protheus[].company_branch` | String | 34% | — |
| `stock_protheus[].stock_quantity` | Double \| Integer | 34% | — |
| `stock_protheus[].warehouse` | String | 34% | — |
| `stock_quantity_anymarket` | Integer | 2% | Quantidade em estoque sincronizada com Anymarket. |
| `stock_quantity_vtex` | Integer | 2% | Quantidade em estoque sincronizada com VTEX. |
| `stock_virtual_quantity_vtex` | null | 0% | Quantidade virtual de estoque na VTEX. |
| `unit_multiplier` | Double | 82% | Multiplicador de unidade de venda. |
| `updated_at` | String | 100% | Data em que o registro foi atualizado. |
| `videos` | Array<String> | 82% | URLs de vídeos do produto. |
| `vtex_id` | Integer | 76% | ID do registro na plataforma VTEX. |
| `weight_kg` | Double | 82% | Peso do produto (kg). |
| `width` | Double | 82% | Largura do produto (cm). |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## SlaNotify

**Documentos (estimado):** 0

> ⚠️ Collection vazia — nenhum documento encontrado.

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Specification

**Documentos (estimado):** 78

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `default_value` | String | 18% | Valor padrão do campo de especificação. |
| `field_group_id` | Integer | 100% | ID do grupo de campos na VTEX. |
| `field_type_id` | Integer | 100% | ID do tipo de campo na VTEX. |
| `is_active` | Boolean | 100% | Flag para identificar se o produto está ativado na VTEX. |
| `is_filter` | Boolean | 100% | Indica se o campo é usado como filtro. |
| `is_on_product_details` | Boolean | 100% | Indica se o campo aparece nos detalhes do produto. |
| `is_required` | Boolean | 100% | Indica se o campo é obrigatório. |
| `is_side_menu_link_active` | Boolean | 100% | Link ativo no menu lateral para este campo. |
| `is_stock_keeping_unit` | Boolean | 100% | Indica se o campo é nível SKU. |
| `is_top_menu_link_active` | Boolean | 100% | Link ativo no menu superior para este campo. |
| `name` | String | 100% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `position` | Integer | 100% | Posição/ordem de exibição do campo. |
| `product_type` | DBRef → `ProductType` | 100% | Tipo de produto (ex: Notebook, Monitor, Desktop). |
| `updated_at` | String | 100% | Data em que o registro foi atualizado. |
| `vtex_id` | Integer | 100% | ID do registro na plataforma VTEX. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## StockSyncDate

**Documentos (estimado):** 1

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `end_date` | null | 0% | Data/hora de término da sincronização. |
| `start_date` | String | 100% | Data/hora de início da sincronização. |
| `status` | String | 100% | Status utilizado para o ciclo de vida de um produto, acompanhando do nascimento até a integração com a VTEX/outros integradores. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## Template

**Documentos (estimado):** 1

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `created_at` | String | 100% | Data de criação do registro na base de dados. |
| `model` | String | 100% | Modelo do produto, essencial. Não utilizado na VTEX. |
| `product_type` | DBRef → `ProductType` | 100% | Tipo de produto (ex: Notebook, Monitor, Desktop). |
| `technical_specification` | Object | 100% | Especificações técnicas do produto de acordo com os campos da VTEX. É um campo VTEX mas extremamente importante para o produto. |
| `technical_specification.123` | String | 100% | — |
| `technical_specification.12313` | String | 100% | — |
| `technical_specification.321231` | String | 100% | — |
| `technical_specification.7126387126` | String | 100% | — |
| `technical_specification.Aplicativos` | String | 100% | — |
| `technical_specification.Armazenamento` | String | 100% | — |
| `technical_specification.CBH_ProductName` | String | 100% | — |
| `technical_specification.Conteúdo da Embalagem` | String | 100% | — |
| `technical_specification.Cor` | String | 100% | — |
| `technical_specification.EAN` | String | 100% | — |
| `technical_specification.Garantia` | String | 100% | — |
| `technical_specification.Gráficos` | String | 100% | — |
| `technical_specification.MGZ_ProductName` | String | 100% | — |
| `technical_specification.Memória` | String | 100% | — |
| `technical_specification.Processador e Chipset` | String | 100% | — |
| `technical_specification.Sistema Operacional` | String | 100% | — |
| `technical_specification.Teclados e Touchpad` | String | 100% | — |
| `technical_specification.Tela` | String | 100% | — |
| `technical_specification.Upgrades` | String | 100% | — |
| `technical_specification.Webcam` | String | 100% | — |
| `technical_specification.Wi-Fi e Rede` | String | 100% | — |
| `technical_specification.teste cache` | String | 100% | — |
| `technical_specification.teste cache 3` | String | 100% | — |
| `technical_specification.teste new form` | String | 100% | — |
| `technical_specification.Áudio e Microfone` | String | 100% | — |
| `updated_at` | String | 100% | Data em que o registro foi atualizado. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---
