**Relatório de Verificação de Credenciais Hardcoded**

---

### 1. Objetivo

Avaliar a presença de credenciais, identificadores sensíveis e possíveis más práticas de segurança nos repositórios analisados.

---

### 2. Escopo

* Product_Backend
* MktPlace_Backend
* Lambdas
* Backend_Partners
* Bus_Partner_VTEX
* IA
* IA_Insights
* AnyMarket
* CISP1
* Notifications

---

### 3. Achados

**Informativo**

**MktPlace_Backend**

* Arquivo `.env` identificado no histórico do repositório contendo apenas dados de desenvolvimento.
  **Análise:** não foram identificadas credenciais sensíveis; sem impacto no cenário atual.

* AWS Account ID presente em arquivos de build/template:

  * Product_Backend (`buildspec.yml`)
  * MktPlace_Backend (`buildspec.yml`)
  * Lambdas (`lambda_3d_retopology/template.yml`)
  * IA (`buildspec.yml`)
  * IA_Insights (`buildspec.yml`)
  * AnyMarket (`buildspec.yml`)
  * CISP1 (`buildspec.yml`)
  * Notifications (`buildspec.yml`)
  * Backend_Partners (`buildspec.yml`)
    **Análise:** não é considerado sensível no contexto atual.

**Baixa**

**Bus_Partner_VTEX**

* Arquivo `default.toml` sem evidência de uso.
  **Análise:** a utilização ou não do Dynaconf é indiferente neste contexto.
  **Ação:** validar necessidade ou remover.

---

### 4. Observação

* Serviços em ECS utilizam gerenciamento seguro de variáveis via secrets (boa prática).

---

### 5. Conclusão

Não foram identificadas credenciais sensíveis expostas. O `.env` presente no histórico contém apenas dados de desenvolvimento, sem impacto. Os demais pontos são apenas melhorias de organização.

---

