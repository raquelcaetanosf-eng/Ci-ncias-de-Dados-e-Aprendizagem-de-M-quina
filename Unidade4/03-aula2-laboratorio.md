[03-aula2-laboratorio.md](https://github.com/user-attachments/files/34397242/03-aula2-laboratorio.md)
<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# Aula 2 — Registro do laboratório supervisionado

## Identificação

- Estudante ou equipe: **Raquel Caetano Nascimento**
- Turma: **Sistemas de Informação — 2026.2 Noturno**
- Data de realização: **29/10/2026**
- Integrantes e contribuições (se em equipe): **Individual**

## Percurso escolhido

- [x] Python/Jupyter.
- [ ] Orange Data Mining.

Use o [notebook de apoio](notebooks/laboratorio.ipynb) ou o [CSV sintético](dados/educacionais-sinteticos.csv). O CSV contém 600 registros fictícios. Atributos: `frequencia_sem4`, `nota_sem4`, `entregas_sem4`. Alvo: `evasao_fim_semestre` (0 permaneceu, 1 evadiu). As associações foram definidas pela simulação, sem validade empírica sobre estudantes reais.

## 1. Ambiente e reprodução

| Item | Registro |
| --- | --- |
| Ambiente e data | Python 3.13.5 / Jupyter; execução em 29/10/2026. |
| Versões das ferramentas/bibliotecas | Python 3.13.5; NumPy 2.3.5; pandas 2.2.3; matplotlib 3.10.8; scikit-learn 1.8.0. |
| Semente aleatória | 42, conforme notebook executado. |
| Caminho do notebook executado ou fluxo Orange | notebooks/laboratorio-equipe.ipynb (executado e salvo com saídas). |
| Origem dos dados e condição sintética | 600 registros fictícios gerados pelo notebook com semente 42; CSV original também incluído em dados/educacionais-sinteticos.csv. |

## 2. Problema e preparação

- Pergunta de negócio: **É possível prever evasão ao fim do semestre com indicadores disponíveis na quarta semana?**
- Unidade de análise e horizonte: **Estudante matriculado; previsão na quarta semana para o fim do semestre.**
- Atributos disponíveis no instante da previsão: **frequencia_sem4, nota_sem4 e entregas_sem4.**
- Variável-alvo e sua natureza: **evasao_fim_semestre: alvo binário (0 permaneceu, 1 evadiu).**
- Ausências e outros problemas encontrados: **600 registros e 4 colunas; 30 valores ausentes em nota_sem4; classes: 59% permaneceram (0) e 41% evadiram (1).**
- Tratamentos e conjunto usado para aprendê-los: **Imputação pela mediana em Pipeline ajustado somente nos dados de treino, inclusive dentro das partições de validação.**

## 3. Desenvolvimento e teste

- Método de divisão e justificativa: **Divisão estratificada de 75% treino e 25% teste, com random_state=42, para preservar a distribuição das classes.**
- Quantidades de treino e teste: **450 registros de treino e 150 de teste.**
- Procedimento de validação no treino: **Validação cruzada estratificada com 5 partições no conjunto de treino.**
- Parâmetros da árvore e como foram escolhidos: **Comparadas profundidades 2, 3, 5 e sem limite, mantendo min_samples_leaf=10; seleção pela maior acurácia média em validação cruzada. Profundidade escolhida: 5.**
- Como o teste ficou fora da seleção: **O conjunto de teste foi reservado antes da validação e utilizado somente após selecionar profundidade 5 com os dados de treino.**

### Alternativa Orange

Confira o alvo como categórico. Registre as conexões: File/Select Columns → Test & Score (Data), Tree → Test & Score (Learner), Test & Score → Confusion Matrix (Evaluation Results). Data Table permite inspeção. Se usar Preprocess, conecte o preprocessor ao learner para ajustar transformações dentro do treino. Não use apenas `Test on train data` como avaliação final.

**Fluxo e método de avaliação realmente utilizados:** Não se aplica: percurso Python planejado, não Orange.

Se comparar configurações, use validação no treino e reserve teste independente. Documente em Test & Score as entradas Data e Test Data, quando utilizadas.

## 4. Resultados calculados de classificação

| Modelo | Configuração | Acurácia de treino | Acurácia de validação e dispersão | Acurácia de teste |
| --- | --- | --- | --- | --- |
| Referência | DummyClassifier (classe majoritária) | 0,5911 | Não calculada (CV não implementada para referência) | 0,5933 |
| Árvore final | max_depth=5; min_samples_leaf=10 | 0,8133 | 0,7222 ± 0,0391 (5 folds) | 0,7800 |

Não invente valores. Se sua ferramenta não produziu uma medida, registre “não calculada” e explique.

**Matriz: linhas reais e colunas previstas; classe positiva = 1.**

| Real / previsto | Permaneceu (0) | Evadiu (1) |
| --- | --- | --- |
| Permaneceu (0) | 75 (TN) | 14 (FP) |
| Evadiu (1) | 19 (FN) | 42 (TP) |

- Acurácia calculada manualmente pela matriz: **(75 + 42) / 150 = 117/150 = 0,78 (78%).**
- Sensibilidade da classe 1: **42 / (42 + 19) = 0,6885 (68,85%).**
- Comparação com referência: **Árvore: 78% de acurácia no teste; referência majoritária: 59,33%; ganho de 18,67 pontos percentuais.**
- Consequências dos falsos positivos: **Alunos podem receber contato desnecessário ou rótulos indevidos.**
- Consequências dos falsos negativos: **Alunos que precisariam de apoio podem deixar de recebê-lo.**
- Interpretação do gráfico e da árvore: **A árvore combina limites de frequência, notas e entregas para estimar a classe. A matriz revela 14 falsos positivos e 19 falsos negativos; não é apropriado interpretar essas associações sintéticas como causalidade.**

## 5. Experimentos no treino

Compare parâmetros usando apenas treino/validação. Após conhecer o teste, uma nova seleção exige novo teste independente para avaliação final.

| Experimento | Alteração | Resultado de validação | Interpretação |
| --- | --- | --- | --- |
| 1 | max_depth=2 versus max_depth=5 (folha mínima 10) | 0,6844 ± 0,0425 versus 0,7222 ± 0,0391 | Profundidade 5 melhorou a validação neste conjunto. |
| 2 | max_depth=5 versus sem limite (folha mínima 10) | 0,7222 ± 0,0391 versus 0,7111 ± 0,0477 | A profundidade sem limite não melhorou a generalização. |

Responda:

1. Como a profundidade e o tamanho das folhas podem afetar o sobreajuste? **Árvores profundas e folhas pequenas podem memorizar ruído e sobreajustar; limitar profundidade e exigir mais exemplos por folha pode melhorar generalização, mas deve ser validado.**
2. Retirar um atributo e observar mudança no desempenho prova causalidade? **Não. Mudança de desempenho indica contribuição preditiva naquele conjunto, não relação de causa e efeito.**
3. Se 95% permanecem, o que acontece com um modelo que sempre prevê permanência? **Acurácia de 95%, mas sensibilidade zero para evasão; é uma referência enganosa se a classe de interesse é minoritária.**

## 6. Regressão — seção independente

Execute a seção da biblioteca no notebook ou registre o procedimento equivalente em Orange. Dados também sintéticos. Alvo numérico: empréstimos por semana.

| Item | Registro |
| --- | --- |
| Atributos e alvo | Atributos: usuarios_ativos e horas_abertura; alvo numérico: emprestimos_semana, em 300 registros sintéticos. |
| Divisão e preparação | Divisão 75% treino (225) e 25% teste (75), semente 42; imputação por mediana em Pipeline com regressão linear. |
| MAE do modelo e unidade | 28,59 empréstimos por semana. |
| MAE da referência | 28,59 empréstimos por semana. |
| R² do teste | 0,8774 no teste. |
| Interpretação do gráfico observado/previsto | As previsões acompanham a diagonal observado=previsto, com dispersão residual, consistente com R²=0,8774. |
| Interpretação dos resíduos | Os resíduos variam em torno de zero, com erros positivos e negativos; inspecionar o gráfico no notebook para avaliar dispersão e eventuais padrões. |
| Limitação de extrapolação | Previsões fora da faixa de dados observada podem ser pouco confiáveis. |

Explique por que R² não é porcentagem de acertos: **R² mede a melhora relativa do erro quadrático frente à previsão pela média; pode ser negativo e não representa proporção de previsões corretas.**

## 7. Evidências e conclusão

- Link relativo do notebook/fluxo: **[notebooks/laboratorio-equipe.ipynb](notebooks/laboratorio-equipe.ipynb), executado com saídas e gráficos.**
- Links das imagens, se houver: **Gráficos incorporados às saídas do notebook executado.**
- Principal aprendizado: **A separação entre treino, validação e teste evita avaliações artificialmente otimistas.**
- Limitações de generalização e vieses possíveis: **Dados sintéticos não representam padrões reais; mudanças de população e rótulos enviesados limitam a generalização.**
- Cuidados com privacidade e uso responsável: **Evitar dados identificáveis, restringir acesso e usar previsões somente como apoio à decisão humana.**

Para inserir uma imagem salva, use `![Matriz de confusão](assets/minha-matriz.png)` e confira se o arquivo existe. Mostre apenas dados sintéticos.

[Voltar ao início](README.md).
