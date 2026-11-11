[Fase_2_Entendimento_dos_Dados_CRISP_DM.md](https://github.com/user-attachments/files/34720133/Fase_2_Entendimento_dos_Dados_CRISP_DM.md)
# Fase 2 — Entendimento dos Dados (CRISP-DM)

**Projeto:** Análise dos casos de violência doméstica no Distrito Federal  
**Pergunta de negócio:** Quais regiões administrativas do Distrito Federal apresentam os maiores registros de violência doméstica?  
**Recorte dos dados regionais:** 2024 e 2025

## 2.1 Coleta inicial dos dados

Foram consultados três documentos da Secretaria de Estado de Segurança Pública do Distrito Federal (SSP-DF):

| Documento | Conteúdo | Utilização no projeto |
|---|---|---|
| Balanço Criminal 2024 | Indicadores criminais mensais no DF, inclusive feminicídio e tentativa de feminicídio | Contextualização |
| Balanço Criminal 2025 | Indicadores criminais mensais no DF, inclusive feminicídio e tentativa de feminicídio | Contextualização |
| Relatório de Análise Criminal nº 001/2026 | Violência doméstica ou familiar, com comparação regional 2024–2025 e outros indicadores | **Fonte principal** |

Os balanços criminais gerais não oferecem, por si só, a distribuição dos registros de violência doméstica por região administrativa. Para responder à pergunta do projeto, utiliza-se principalmente a tabela regional do Relatório nº 001/2026 (p. 1).

## 2.2 Descrição dos dados

| Característica | Descrição |
|---|---|
| Fonte | SSP-DF, Banco Millenium — COOAFESP/SGI/SSPDF |
| Cobertura geográfica | 33 regiões administrativas do Distrito Federal |
| Cobertura temporal regional | 2024 e 2025 |
| Unidade de análise | Região administrativa e ano |
| Variável principal | Número de registros de violência doméstica ou familiar |
| Variáveis derivadas | Diferença absoluta e variação percentual entre 2024 e 2025 |
| Outras dimensões disponíveis no relatório | Mês, dia da semana, faixa horária, faixa etária, reincidência, vínculo entre vítima e agressor, entre outras |
| Formato dos arquivos recebidos | PDF, com tabelas e gráficos |

**Observação:** as tabelas são agregadas; não contêm microdados individuais dos casos. A análise deve distinguir *registros de ocorrência* de *número de vítimas*.

## 2.3 Exploração inicial dos dados

### Comparação anual

| Ano | Registros |
|---|---:|
| 2024 | 21.721 |
| 2025 | 23.066 |
| Diferença | +1.345 |
| Variação | +6,2% |

Os registros aumentaram de 2024 para 2025, conforme a tabela regional do relatório principal (p. 1).

### Dez regiões administrativas com mais registros em 2025

| Posição | Região administrativa | Registros em 2025 |
|---:|---|---:|
| 1 | Ceilândia | 3.135 |
| 2 | Planaltina | 1.951 |
| 3 | Samambaia | 1.809 |
| 4 | Taguatinga | 1.339 |
| 5 | Recanto das Emas | 1.303 |
| 6 | Gama | 1.238 |
| 7 | Sol Nascente/Pôr do Sol | 1.233 |
| 8 | Santa Maria | 1.198 |
| 9 | São Sebastião | 1.086 |
| 10 | Brasília | 959 |

Essas dez regiões concentram aproximadamente **66%** dos registros de 2025, conforme destacado no Relatório nº 001/2026 (pp. 1–2).

### Indicadores complementares de 2025

- **Dias da semana:** sábados e domingos concentram, juntos, 36% dos registros (p. 3).
- **Faixa horária:** 34% dos registros ocorreram entre 18h e 23h59 (p. 3).
- **Faixa etária das vítimas:** 63,3% dos casos analisados concentram-se entre 18 e 39 anos (p. 4).
- **Reincidência das vítimas:** entre 20.572 vítimas do sexo feminino identificadas, 2.628 apresentaram dois ou mais registros no ano (12,8%) (p. 4).
- **Local de incidência:** 69,4% das ocorrências ocorreram em residências (p. 7).

Esses indicadores contextualizam o fenômeno, mas a pergunta principal do projeto permanece centrada na distribuição **por região administrativa**.

## 2.4 Verificação da qualidade dos dados

| Aspecto | Avaliação inicial |
|---|---|
| Procedência | Fonte oficial governamental |
| Cobertura regional | 33 regiões administrativas na tabela principal |
| Cobertura temporal | Comparação regional disponível para 2024 e 2025 |
| Estrutura | Dados agregados em tabelas e gráficos dentro de PDFs |
| Valores ausentes | Não foram identificadas lacunas evidentes na tabela regional apresentada; é necessário validar após a extração |
| Atualização | Dados de 2024 e 2025 atualizados em 06/01/2026, sujeitos a alterações, segundo o relatório |
| Limitações | Possível subnotificação; ausência de taxas populacionais na tabela; ausência de microdados; extração do PDF sujeita a erros |

**Cuidados de interpretação:** números absolutos maiores não significam automaticamente maior risco para cada habitante. Para comparar proporcionalmente as regiões, seria necessário incorporar estimativas populacionais compatíveis com os anos estudados. Também não se deve interpretar a variação dos registros como medida exata da variação de todos os episódios de violência, pois nem todos são notificados.

## 2.5 Conclusão do entendimento dos dados

A documentação é adequada para responder à pergunta de negócio em termos de **quantidade absoluta de registros**. A tabela principal permite comparar as 33 regiões administrativas em 2024 e 2025, identificar as regiões com maiores totais e avaliar a variação anual. Em 2025, Ceilândia, Planaltina e Samambaia lideraram o ranking.

Para as etapas seguintes, recomenda-se extrair e conferir a tabela regional, estruturá-la em CSV ou Excel e, se o projeto desejar comparar riscos relativos, acrescentar dados populacionais. O período do estudo deve ser ajustado para **2024–2025**, pois este é o recorte regional documentado nos arquivos fornecidos.

## 2.6 Entregáveis da Fase 2

1. **Relatório de entendimento dos dados:** fontes, descrição das variáveis, exploração inicial e avaliação de qualidade (este documento).
2. **Base estruturada:** tabela de 33 regiões com registros de 2024 e 2025, a ser preparada e validada na fase seguinte.
3. **Visualizações exploratórias:** ranking regional e comparação entre anos, que podem ser reproduzidos a partir da base estruturada.

## Referências documentais

- SSP-DF. *Balanço Criminal — Distrito Federal: Comparativo Mensal 2024 por Natureza*. Arquivo fornecido: `00_DISTRITO-FEDERAL_1.pdf`.
- SSP-DF. *Balanço Criminal — Distrito Federal: Comparativo Mensal 2025 por Natureza*. Arquivo fornecido: `DISTRITO-FEDERAL-2.pdf`.
- SSP-DF. *Relatório de Análise Criminal nº 001/2026 — Violência Doméstica ou Familiar no DF: comparativo 2024 e 2025*. 16 jan. 2026. Arquivo fornecido: `RAC-001_2026-Violencia-Domestica-ou-Familiar-no-DF_-2025.pdf`.
