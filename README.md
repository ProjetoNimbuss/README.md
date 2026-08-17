<div align="center">

<img src="https://raw.githubusercontent.com/vinihoudini/rmr-alertas/main/docs/assets/nimbus_logo.jpg" alt="Nimbus — Sistema de Monitoramento e Alertas" width="420"/>


**Sistema Integrado de Dados e Alertas Meteorológicos**

*Monitoramento climático em tempo real para a Região Metropolitana do Recife.*

---

</div>

## Sobre o Projeto

A Região Metropolitana do Recife concentra mais de 4 milhões de pessoas em uma das áreas mais expostas a eventos climáticos extremos do Brasil. Enchentes, tempestades, ressacas e deslizamentos chegam todos os anos — e a antecedência com que são comunicados pode salvar vidas.

O **Nimbus** é uma plataforma de inteligência climática que reúne, processa e entrega dados meteorológicos de múltiplas fontes em um único lugar, em tempo real e com histórico desde 1961.

---

## O Que Fazemos

**📡 Monitoramos** condições de tempo, chuva, vento e mar em tempo real para toda a RMR.

**⚠️ Alertamos** sobre eventos extremos com antecedência — enchentes, ressacas e tempestades severas — para que gestores e cidadãos possam agir antes do impacto.

**📜 Preservamos** a memória climática da região com séries históricas de pluviometria de Pernambuco desde 1961.

**🧑‍🤝‍🧑 Conectamos** os dados climáticos com a realidade social dos bairros, identificando áreas de maior vulnerabilidade com base no Censo IBGE 2022.

**📍 Recebemos** reports diretamente de cidadãos e equipes de campo sobre condições e riscos observados no território.

---

## Fontes de Dados

Integramos dados de fontes abertas, oficiais e especializadas:

- 🌤️ **Open-Meteo** — previsão meteorológica e oceânica global (GFS + ECMWF)
- ⚡ **Tomorrow.io** — nowcasting e previsão de alta precisão
- 🌧️ **CEMADEN / APAC** — telemetria pluviométrica em tempo real de Pernambuco
- 📊 **APAC Histórico** — série pluviométrica desde 1961 (5 mesorregiões)
- 🗺️ **IBGE Censo 2022** — dados demográficos e domiciliares por bairro
- 🚨 **REINDESC** — histórico de ocorrências de desastres naturais

---

## Arquitetura

Construído sobre uma **Medallion Architecture** com infraestrutura local hoje e migração planejada para GCP e MagaluCloud.

```
APIs & Scraping → MinIO (Data Lake) → DuckDB → dbt → FastAPI → Next.js
```

| Camada | Tecnologia |
| :--- | :--- |
| Storage (Raw) | MinIO → Google Cloud Storage |
| Analítico (Bronze/Silver/Gold) | DuckDB → BigQuery |
| Transformação | dbt Core |
| Orquestração | Prefect |
| API | FastAPI |
| Frontend | Next.js |

---

## Repositórios

| Repositório | Descrição |
| :--- | :--- |
| [`rmr-alertas`](https://github.com/vinihoudini/rmr-alertas) | Pipeline de dados, API e documentação técnica |

---

<div align="center">

**Nimbus · Recife · 2026**

*Dados que salvam vidas.*

</div>
# README.md
