# Database: scraping

[← Voltar ao índice](../README.md)

> **4** collection(s) · ~**3,460** documentos estimados

## Sumário

| Collection | Documentos (est.) |
|------------|-------------------|
| [amd_processors](#amd_processors) | 574 |
| [intel_processors](#intel_processors) | 2,865 |
| [nvidia_video](#nvidia_video) | 12 |
| [parceiros_acer](#parceiros_acer) | 9 |

---

## amd_processors

**Documentos (estimado):** 574

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `*Suporte a SO` | String | 100% | — |
| `AMD Ryzen AI` | String | 58% | — |
| `Aumento de clock máx` | Object | 100% | — |
| `Aumento de clock máx.` | String | 100% | — |
| `Bandeja com identificação do produto` | String | 100% | — |
| `Cache L1` | String | 30% | — |
| `Cache L2` | String | 100% | — |
| `Cache L3` | String | 100% | — |
| `Canais de memória` | Integer | 100% | — |
| `Clock básico` | String | 100% | — |
| `Contagem de núcleos gráficos` | Integer | 78% | — |
| `Data de lançamento` | String | 40% | — |
| `Desbloqueado para overclocking` | String | 86% | — |
| `Especificação da memória do sistema` | String | 18% | — |
| `Família` | String | 100% | — |
| `Fator de forma` | String | 100% | — |
| `Frequência de gráficos` | String | 78% | — |
| `ID do produto MPK` | String | 16% | — |
| `ID do produto na caixa` | String | 32% | — |
| `Modelo da placa de vídeo` | String | 100% | — |
| `Nome` | String | 100% | — |
| `Nº de núcleos de CPU` | Integer | 100% | — |
| `Nº de threads` | Integer | 100% | — |
| `PCI Express® Version` | String | 100% | — |
| `Recommended Cooler` | String | 8% | — |
| `Solução Térmica (PIB)` | String | 26% | — |
| `Soquete da CPU` | String | 100% | — |
| `Série` | String | 100% | — |
| `TDP configurável AMD (cTDP)` | String | 70% | — |
| `TDP padrão` | String | 94% | — |
| `Tecnologia de processador para núcleos de CPU` | String | 100% | — |
| `Tecnologias compatíveis` | String | 30% | — |
| `Temperatura máx` | Object | 100% | — |
| `Temperatura máx. de funcionamento (Tjmax)` | String | 100% | — |
| `Thermal Solution (MPK)` | String | 4% | — |
| `Tipo de memória do sistema` | String | 100% | — |
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## intel_processors

**Documentos (estimado):** 2,865

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `# of Displays Supported ‡` | Integer | 90% | — |
| `# of Efficient-cores` | Integer | 100% | — |
| `# of Low Power Efficient-cores` | Integer | 40% | — |
| `# of Performance-cores` | Integer | 100% | — |
| `AI Datatype Support on CPU` | String | 18% | — |
| `AI Datatype Support on GPU` | String | 18% | — |
| `AI Datatype Support on NPU` | String | 18% | — |
| `AI Software Frameworks Supported by CPU` | String | 40% | — |
| `AI Software Frameworks Supported by GPU` | String | 40% | — |
| `AI Software Frameworks Supported by NPU` | String | 40% | — |
| `AV1 Encode/Decode` | String | 40% | — |
| `Cache` | String | 100% | — |
| `Chipset / PCH PCIe Revision` | String | 28% | — |
| `Code Name` | String | 100% | — |
| `Datasheet` | String | 60% | — |
| `Device ID` | String | 90% | — |
| `Direct Media Interface (DMI) Revision` | Double | 32% | — |
| `DirectX* Support` | Double \| Integer | 90% | — |
| `ECC Memory Supported   ‡` | String | 82% | — |
| `Efficient-core Base Frequency` | String | 80% | — |
| `Efficient-core Max Turbo Frequency` | String | 100% | — |
| `Embedded Options Available` | String | 100% | — |
| `Enhanced Intel SpeedStep® Technology` | String | 26% | — |
| `Execute Disable Bit ‡` | String | 94% | — |
| `Execution Units` | Integer | 50% | — |
| `GPU Name‡` | String | 90% | — |
| `Graphics Base Frequency` | String | 14% | — |
| `Graphics Max Dynamic Frequency` | String | 90% | — |
| `Graphics Output` | String | 90% | — |
| `H_264 Hardware Encode/Decode` | String | 40% | — |
| `H_265 (HEVC) Hardware Encode/Decode` | String | 40% | — |
| `Idle States` | String | 26% | — |
| `Instruction Set` | String | 100% | — |
| `Instruction Set Extensions` | String | 100% | — |
| `Intel vPro® Eligibility ‡` | String | 76% | — |
| `Intel® 64 ‡` | String | 26% | — |
| `Intel® AES New Instructions` | String | 100% | — |
| `Intel® Active Management Technology (AMT) ‡` | String | 62% | — |
| `Intel® Adaptive Boost Technology` | String | 12% | — |
| `Intel® Adaptix™ Technology` | String | 74% | — |
| `Intel® Boot Guard` | String | 100% | — |
| `Intel® Clear Video HD Technology` | String | 16% | — |
| `Intel® Control-Flow Enforcement Technology` | String | 94% | — |
| `Intel® Deep Learning Boost (Intel® DL Boost) on CPU` | String | 100% | — |
| `Intel® Deep Learning Boost (Intel® DL Boost) on GPU` | String | 40% | — |
| `Intel® Flex Memory Access` | String | 74% | — |
| `Intel® Gaussian & Neural Accelerator` | Double | 100% | — |
| `Intel® Hardware Shield Eligibility ‡` | String | 78% | — |
| `Intel® High Definition Audio` | String | 74% | — |
| `Intel® Hyper-Threading Technology ‡` | String | 100% | — |
| `Intel® Image Processing Unit` | Double | 68% | — |
| `Intel® OS Guard` | String | 100% | — |
| `Intel® One-Click Recovery ‡` | String | 64% | — |
| `Intel® Quick Sync Video` | String | 90% | — |
| `Intel® QuickAssist Software Acceleration` | String | 20% | — |
| `Intel® Remote Platform Erase (RPE) ‡` | String | 62% | — |
| `Intel® Smart Sound Technology` | String | 74% | — |
| `Intel® Speed Shift Technology` | String | 100% | — |
| `Intel® Stable IT Platform Program (SIPP)` | String | 60% | — |
| `Intel® Standard Manageability (ISM) ‡` | String | 90% | — |
| `Intel® Thermal Velocity Boost` | String | 16% | — |
| `Intel® Thermal Velocity Boost Frequency` | String | 16% | — |
| `Intel® Thread Director` | String | 100% | — |
| `Intel® Threat Detection Technology (TDT)` | String | 82% | — |
| `Intel® Thunderbolt™ 4` | String | 68% | — |
| `Intel® Total Memory Encryption` | String | 8% | — |
| `Intel® Total Memory Encryption - Multi Key` | String | 62% | — |
| `Intel® Trusted Execution Technology ‡` | String | 76% | — |
| `Intel® Turbo Boost Max Technology 3_0 Frequency ‡` | String | 42% | — |
| `Intel® Turbo Boost Max Technology 3_0 ‡` | String | 72% | — |
| `Intel® Turbo Boost Technology ‡` | Double | 26% | — |
| `Intel® VT-x with Extended Page Tables (EPT) ‡` | String | 100% | — |
| `Intel® Virtualization Technology (VT-x) ‡` | String | 100% | — |
| `Intel® Virtualization Technology for Directed I/O (VT-d) ‡` | String | 100% | — |
| `Intel® Virtualization Technology with Redirect Protection (VT-rp) ‡` | String | 62% | — |
| `Intel® Volume Management Device (VMD)` | String | 100% | — |
| `Intel® Wake on Voice` | String | 70% | — |
| `Launch Date` | String | 100% | — |
| `Lithography` | String | 60% | — |
| `Low Power Efficient-core Base Frequency` | String | 40% | — |
| `Low Power Efficient-core Max Turbo Frequency` | String | 40% | — |
| `MIPI SoundWire*` | Double | 34% | — |
| `Marketing Status` | String | 100% | — |
| `Max # of DMI Lanes` | Integer | 32% | — |
| `Max # of Memory Channels` | Integer | 100% | — |
| `Max # of PCI Express Lanes` | Integer | 100% | — |
| `Max CPU Configuration` | Integer | 100% | — |
| `Max Frequency` | String | 40% | — |
| `Max Memory Bandwidth` | String | 32% | — |
| `Max Memory Size (dependent on memory type)` | String | 100% | — |
| `Max Operating Temperature` | String | 78% | — |
| `Max Resolution (DP)‡` | String | 90% | — |
| `Max Resolution (HDMI)‡` | String | 90% | — |
| `Max Resolution (eDP - Integrated Flat Panel)‡` | String | 90% | — |
| `Max Turbo Frequency` | String | 100% | — |
| `Maximum Assured Power` | String | 38% | — |
| `Maximum Turbo Power` | String | 100% | — |
| `Memory Types` | String | 100% | — |
| `Microprocessor PCIe Revision` | String | 28% | — |
| `Minimum Assured Power` | String | 70% | — |
| `Mode-based Execute Control (MBEC)` | String | 94% | — |
| `Multi-Format Codec Engines` | Integer | 90% | — |
| `NPU Name‡` | String | 40% | — |
| `OpenCL* Support` | Double | 90% | — |
| `OpenGL* Support` | Double | 90% | — |
| `PCI Express Configurations ‡` | String | 72% | — |
| `PCI Express Revision` | String | 32% | — |
| `PCI Support` | Double \| String | 40% | — |
| `Package Size` | String | 100% | — |
| `Performance-core Base Frequency` | String | 80% | — |
| `Performance-core Max Turbo Frequency` | String | 100% | — |
| `Processor Base Frequency` | String | 2% | — |
| `Processor Base Power` | String | 100% | — |
| `Processor Number` | String | 100% | — |
| `Product Collection` | String | 100% | — |
| `Product Tuning (Embedded Uses)` | String | 18% | — |
| `Ray Tracing` | String | 40% | — |
| `Recommended Customer Price` | String | 72% | — |
| `Scalability` | String | 32% | — |
| `Secure Key` | String | 100% | — |
| `Sockets Supported` | String | 66% | — |
| `Sparsity Support` | String | 40% | — |
| `TJUNCTION` | String | 60% | — |
| `Thermal Monitoring Technologies` | String | 100% | — |
| `Thermal Solution Specification` | String | 24% | — |
| `Total Cores` | Integer | 100% | — |
| `Total L2 Cache` | String | 26% | — |
| `Total Threads` | Integer | 100% | — |
| `Use Conditions` | String | 26% | — |
| `VP9 Bitstream & Decoding` | String | 40% | — |
| `Vertical Segment` | String | 100% | — |
| `Windows Studio Effects Support` | String | 40% | — |
| `Xe-cores` | Integer | 40% | — |
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `scrape` | String | 100% | Descrição desconhecida. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## nvidia_video

**Documentos (estimado):** 12

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `bcPID` | Integer | 100% | Descrição desconhecida. |
| `bestSeller` | Boolean | 100% | Indica se é produto mais vendido. |
| `category` | String | 100% | Categoria à qual o produto está associado. |
| `certified` | Boolean | 100% | Indica se é produto certificado. |
| `compareProductInfo` | Array<Object> | 100% | Informações para comparação de produtos. |
| `compareProductInfo[].name` | String | 400% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `compareProductInfo[].value` | String | 400% | — |
| `customerReviewCount` | null | 0% | Quantidade de avaliações de clientes. |
| `digitialRiverID` | null | 0% | Descrição desconhecida. |
| `displayName` | String | 100% | Nome de exibição do produto. |
| `gpu` | String | 100% | Modelo da GPU. |
| `imageURL` | String | 100% | URL da imagem do produto. |
| `isFeaturedProdcutFoundInSecondSearch` | Boolean | 100% | Descrição desconhecida. |
| `isFeaturedProduct` | Boolean | 100% | Indica se é produto em destaque. |
| `isFounderEdition` | Boolean | 100% | Indica se é edição Founders. |
| `isOffer` | Boolean | 100% | Indica se está em oferta. |
| `locale` | String | 100% | Localidade/idioma. |
| `manufacturer` | String | 100% | Fabricante. |
| `maxShipDays` | null | 0% | Prazo máximo de envio (dias). |
| `minShipDays` | null | 0% | Prazo mínimo de envio (dias). |
| `mrp` | String | 75% | Preço sugerido de venda (MRP). |
| `offerText` | String | 100% | Texto da oferta. |
| `prdStatus` | String | 100% | Status do produto. |
| `productAvailable` | Boolean | 100% | Indica se o produto está disponível. |
| `productID` | Integer | 100% | ID do produto. |
| `productInfo` | Array<Object> | 100% | Informações do produto. |
| `productInfo[].name` | String | 300% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `productInfo[].value` | String | 300% | — |
| `productPrice` | String | 100% | Preço do produto. |
| `productRating` | null | 0% | Avaliação média do produto. |
| `productSKU` | String | 100% | SKU do produto. |
| `productTitle` | String | 100% | Título do produto. |
| `productUPC` | String | 100% | Código UPC do produto. |
| `productUPCOriginal` | String | 100% | Código UPC original do produto. |
| `purchaseOption` | String | 100% | Opção de compra disponível. |
| `retailers` | Array<Object> | 100% | Lista de varejistas que vendem o produto. |
| `retailers[].bestSeller` | Boolean | 117% | Indica se é produto mais vendido. |
| `retailers[].directPurchaseLink` | String | 75% | — |
| `retailers[].hasOffer` | Boolean | 117% | — |
| `retailers[].isAvailable` | Boolean | 117% | — |
| `retailers[].logoUrl` | String | 100% | — |
| `retailers[].mrp` | String | 117% | Preço sugerido de venda (MRP). |
| `retailers[].offerText` | null | 0% | Texto da oferta. |
| `retailers[].partnerId` | String | 117% | — |
| `retailers[].productId` | Integer | 117% | — |
| `retailers[].productTitle` | String | 117% | Título do produto. |
| `retailers[].purchaseLink` | String | 117% | — |
| `retailers[].retailerName` | String | 117% | — |
| `retailers[].salePrice` | String | 117% | — |
| `retailers[].sku` | String | 117% | Relacionamento com SKU, atualmente tratado como 1-1 mas deve ser 1-N (DBRef). |
| `retailers[].stock` | Integer | 117% | Configurações de estoque. |
| `retailers[].storeId` | String | 117% | — |
| `retailers[].type` | Integer | 117% | Tipo de registro (ex: info, warning, error). |
| `retailers[].upc` | String | 117% | Código de barras UPC. |
| `shipInfo` | null | 0% | Informações de envio. |
| `totalCount` | Integer | 100% | Total de resultados encontrados. |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---

## parceiros_acer

**Documentos (estimado):** 9

### Schema

| Campo | Tipo(s) | Presença | Descrição |
|-------|---------|----------|-----------|
| `_id` | ObjectId | 100% | Identificador utilizado pelo MongoDB (ObjectId). |
| `families` | Array<Object> | 100% | Lista de famílias de produto por tipo. |
| `families[].models` | Array<String> | 578% | — |
| `families[].name` | String | 578% | Nome do produto, essencial para o sistema, também utilizado na VTEX. |
| `product_type` | String | 100% | Tipo de produto (ex: Notebook, Monitor, Desktop). |

### Índices

| Nome | Campos | Propriedades |
|------|--------|--------------|
| `_id_` | `_id` (ASC) | — |

---
