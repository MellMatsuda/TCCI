# Identificação de Alvos Terapêuticos para Adenocarcinoma Ductal Pancreático Baseado em Análise de Dados Transcriptômicos e Aprendizado de Máquina

**Autora:** Mell Amisa Matsuda  
**Curso:** Bacharelado em Informática Biomédica (UFCSPA)  
**Orientador:** Prof. Dr. Muriel Figueredo Franco  
**Coorientador:** Prof. Dr. Pedro Luiz Porfírio Xavier (USP)  
**Ano:** 2026

---

## Sobre o projeto

Proposta computacional para priorização de biomarcadores prognósticos e potenciais alvos terapêuticos no adenocarcinoma ductal pancreático (PDAC), integrando análise transcriptômica de RNA-seq e aprendizado de máquina supervisionado. O pipeline parte do transcriptoma completo (sem restrição prévia a vias biológicas) e incorpora etapas sistemáticas de padronização e integração de múltiplas coortes públicas (TCGA e GEO).

**Pergunta de pesquisa:** Em que medida dados transcriptômicos públicos, integrados a técnicas de aprendizado de máquina, podem ser empregados para a priorização de potenciais alvos terapêuticos associados ao prognóstico do PDAC?

---

## Estrutura do repositório

```
📁 revisao-escopo/
   ├── artigos-incluidos/        # 29 artigos incluídos na revisão final
   ├── fluxo-prisma.pdf          # Fluxograma PRISMA-ScR do processo de seleção
   └── planilha-selecao.xlsx     # Triagem completa com critérios de elegibilidade

📁 TCCI/
   ├── TCCI_MellMatsuda.pdf      # Documento do projeto de pesquisa (TCC I)
   └── figuras/                  # Figuras originais utilizadas no artigo

📁 datasets/                    # Amostras ilustrativas dos datasets
                                 # (primeiras linhas das matrizes de expressão)
                                 # Os dados completos devem ser baixados nas fontes
                                 # originais — ver seção Datasets abaixo

README.md
```

---

## Datasets

Os dados completos **não estão incluídos** neste repositório por questões de tamanho. As amostras ilustrativas em `datasets/` mostram apenas o formato das matrizes de expressão.

| Dataset | Fonte | Amostras | Tipo | Plataforma | Dados de sobrevida | Uso previsto |
|---|---|---|---|---|---|---|
| TCGA-PAAD | TCGA | 183 | Tumor primário | Illumina | Sim | Treinamento |
| GSE205154 | GEO | 289 | Tumor primário e metastático | Illumina | Sim | Validação principal |
| GSE242915 | GEO | 79 | Tumor primário | Illumina | Sim | Validação secundária |

**Links para download:**
- TCGA-PAAD: https://portal.gdc.cancer.gov (via pacote `TCGAbiolinks` no R)
- GSE205154: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE205154
- GSE242915: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE242915

---

## Status do projeto

| Etapa | Status |
|---|---|
| Revisão de escopo (PRISMA-ScR) | ✅ Concluída |
| Levantamento e seleção dos datasets | ✅ Concluída |
| Escrita e revisão do TCC I | ✅ Concluída |
| Pré-processamento e normalização | ⏳ Pendente |
| Seleção de atributos (feature selection) | ⏳ Pendente |
| Desenvolvimento dos modelos de ML | ⏳ Pendente |
| Validação externa (GSE205154, GSE242915) | ⏳ Pendente |
| Priorização de potenciais alvos terapêuticos | ⏳ Pendente |
| Escrita e revisão do TCC II | ⏳ Pendente |

---

## Reprodutibilidade

Os scripts desenvolvidos ao longo do projeto serão disponibilizados neste repositório, com controle de versões e documentação do código-fonte, visando garantir transparência e reprodutibilidade científica.
