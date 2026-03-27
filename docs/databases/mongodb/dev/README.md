# Documentação MongoDB — Ambiente DEV

> Gerado automaticamente em 27/03/2026 16:31:04
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
| **Descrição** | Descrição do propósito/significado do campo. |
| **DBRef → Collection** | Referência a um documento em outra collection (similar a uma foreign key em bancos relacionais). |
| **Array\<Tipo\>** | Campo do tipo lista (array) cujos elementos são do tipo indicado entre `< >`. |
| **Índices** | Índices criados na collection para otimizar consultas. |
| **ASC / DESC** | Direção do índice: ASC = ascendente, DESC = descendente. |
| **UNIQUE** | Índice que impede valores duplicados no(s) campo(s) indexado(s). |
| **SPARSE** | Índice que ignora documentos onde o campo indexado não existe. |
| **TTL** | Time To Live — índice que auto-remove documentos após o tempo especificado (em segundos). |


## Sumário

> **13** databases · **56** collections · ~**622,649** documentos estimados

- **[bgmktplace](bgmktplace/bgmktplace.md)** — 13 collection(s), ~1,173 docs
  - [BgFile](bgmktplace/bgmktplace.md#bgfile) (18)
  - [Category](bgmktplace/bgmktplace.md#category) (53)
  - [Family](bgmktplace/bgmktplace.md#family) (1)
  - [Permission](bgmktplace/bgmktplace.md#permission) (14)
  - [Product](bgmktplace/bgmktplace.md#product) (18)
  - [ProductSpecification](bgmktplace/bgmktplace.md#productspecification) (18)
  - [ProductTimeline](bgmktplace/bgmktplace.md#producttimeline) (0)
  - [ProductType](bgmktplace/bgmktplace.md#producttype) (2)
  - [Sku](bgmktplace/bgmktplace.md#sku) (0)
  - [SpecificationMonitor](bgmktplace/bgmktplace.md#specificationmonitor) (3)
  - [SpecificationNotebook](bgmktplace/bgmktplace.md#specificationnotebook) (15)
  - [UserDatabase](bgmktplace/bgmktplace.md#userdatabase) (33)
  - [UserLog](bgmktplace/bgmktplace.md#userlog) (998)
- **[busprotheus](busprotheus/busprotheus.md)** — 2 collection(s), ~21 docs
  - [product](busprotheus/busprotheus.md#product) (9)
  - [stock](busprotheus/busprotheus.md#stock) (12)
- **[logs](logs/logs.md)** — 1 collection(s), ~1,110 docs
  - [UserLog](logs/logs.md#userlog) (1,110)
- **[notifications](notifications/notifications.md)** — 2 collection(s), ~606,476 docs
  - [Notification](notifications/notifications.md#notification) (28,680)
  - [UserNotification](notifications/notifications.md#usernotification) (577,796)
- **[parceiros_core](parceiros_core/parceiros_core.md)** — 1 collection(s), ~0 docs
  - [product_files](parceiros_core/parceiros_core.md#product_files) (0)
- **[partners_core](partners_core/partners_core.md)** — 2 collection(s), ~763 docs
  - [product_files](partners_core/partners_core.md#product_files) (747)
  - [users](partners_core/partners_core.md#users) (16)
- **[partners_events](partners_events/partners_events.md)** — 2 collection(s), ~23 docs
  - [audit_logs](partners_events/partners_events.md#audit_logs) (21)
  - [events](partners_events/partners_events.md#events) (2)
- **[product](product/product.md)** — 22 collection(s), ~9,597 docs
  - [Agency](product/product.md#agency) (11)
  - [AnymarketCharacteristic](product/product.md#anymarketcharacteristic) (3)
  - [Bom](product/product.md#bom) (1,434)
  - [BomDetails](product/product.md#bomdetails) (10)
  - [Category](product/product.md#category) (15)
  - [Collection](product/product.md#collection) (23)
  - [Family](product/product.md#family) (51)
  - [GoogleGlobalCategory](product/product.md#googleglobalcategory) (5,595)
  - [HeroDealerUpload](product/product.md#herodealerupload) (22)
  - [Model](product/product.md#model) (1,022)
  - [PartnerFiles](product/product.md#partnerfiles) (199)
  - [Product](product/product.md#product) (147)
  - [ProductTimeline](product/product.md#producttimeline) (238)
  - [ProductType](product/product.md#producttype) (5)
  - [QuickSummary](product/product.md#quicksummary) (541)
  - [Service](product/product.md#service) (16)
  - [Settings](product/product.md#settings) (1)
  - [Sku](product/product.md#sku) (184)
  - [SlaNotify](product/product.md#slanotify) (0)
  - [Specification](product/product.md#specification) (78)
  - [StockSyncDate](product/product.md#stocksyncdate) (1)
  - [Template](product/product.md#template) (1)
- **[scraping](scraping/scraping.md)** — 4 collection(s), ~3,460 docs
  - [amd_processors](scraping/scraping.md#amd_processors) (574)
  - [intel_processors](scraping/scraping.md#intel_processors) (2,865)
  - [nvidia_video](scraping/scraping.md#nvidia_video) (12)
  - [parceiros_acer](scraping/scraping.md#parceiros_acer) (9)
- **[test](test/test.md)** — 1 collection(s), ~8 docs
  - [coll](test/test.md#coll) (8)
- **[test_parceiros_core](test_parceiros_core/test_parceiros_core.md)** — 2 collection(s), ~0 docs
  - [product_files](test_parceiros_core/test_parceiros_core.md#product_files) (0)
  - [users](test_parceiros_core/test_parceiros_core.md#users) (0)
- **[test_partners_core](test_partners_core/test_partners_core.md)** — 2 collection(s), ~0 docs
  - [product_files](test_partners_core/test_partners_core.md#product_files) (0)
  - [users](test_partners_core/test_partners_core.md#users) (0)
- **[users](users/users.md)** — 2 collection(s), ~18 docs
  - [Permission](users/users.md#permission) (14)
  - [UserDatabase](users/users.md#userdatabase) (4)
