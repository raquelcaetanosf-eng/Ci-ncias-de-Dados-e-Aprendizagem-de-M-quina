[01-aula1-conceitos.md](https://github.com/user-attachments/files/34397163/01-aula1-conceitos.md)
<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# Aula 1 — Conceitos e classificação de problemas

## Identificação

- Estudante ou equipe: **Raquel Caetano Nascimento**
- Turma: **Sistemas de Informação — 2026.2 Noturno**
- Data de realização: **28/10/2026**
- Integrantes e contribuições (se em equipe): **Individual**

## Objetivos

Distinguir programação tradicional e Machine Learning, identificar atributos e alvo e diferenciar classificação, regressão e agrupamento.

## 1. Explicação com suas palavras

1. Como um modelo aprende com dados? **Um modelo aprende identificando padrões em exemplos durante o treinamento e ajustando seus parâmetros para reduzir erros. Depois, aplica esses padrões a novos dados, com desempenho que precisa ser avaliado em dados separados.**
2. Qual diferença entre algoritmo e modelo? **O algoritmo é o procedimento usado para aprender; o modelo é o resultado ajustado aos dados, utilizado para fazer previsões.**
3. Compare uma regra de bloqueio de palavra com um modelo de spam. **Uma regra bloqueia mensagens quando encontra uma palavra previamente definida, mesmo em contextos legítimos. Um classificador de spam aprende combinações de características a partir de mensagens rotuladas e pode reconhecer padrões mais variados, mas também comete erros.**
4. Dê um exemplo de atributo e alvo e defina o momento da previsão. **Para prever evasão ao fim do semestre, a frequência até a quarta semana é um atributo e evasão (sim/não) é o alvo. A previsão é feita após a quarta semana, antes de conhecer o desfecho final.**

## 2. Quadro comparativo

| Critério | Supervisionado | Não supervisionado |
| --- | --- | --- |
| Presença de alvo no treino | Sim, há rótulo conhecido | Não há alvo rotulado |
| Pergunta que pode responder | Qual a categoria ou valor esperado? | Quais padrões ou grupos existem? |
| Tipo de saída | Classe ou valor numérico | Grupos, perfis ou estruturas |
| Tarefas e exemplo | Classificação de spam; regressão de vendas | Agrupamento de perfis de clientes |
| Dados necessários | Exemplos com atributos e respostas conhecidas | Exemplos com atributos, sem respostas pré-definidas |
| Forma de avaliação | Acurácia, sensibilidade ou MAE em dados separados | Coerência e estabilidade dos grupos; interpretação especializada |
| Limitação | Dependência de rótulos confiáveis e risco de sobreajuste | Grupos podem ser arbitrários e difíceis de interpretar |

## 3. Situações-problema

Os casos são cenários didáticos. Escolha **pelo menos cinco** e justifique sua classificação pelo significado do alvo ou por sua ausência.

| Caso | Situação-problema |
| --- | --- |
| 1 Educação | Prever evadiu/permaneceu com histórico rotulado de turmas anteriores. |
| 2 Saúde | Estimar o tempo de espera em minutos a partir de registros de atendimento. |
| 3 Comércio | Descobrir perfis de compra sem categorias prévias de clientes. |
| 4 Finanças | Prever inadimplente/adimplente com contratos e desfechos conhecidos. |
| 5 Segurança digital | Distinguir spam/legítima com mensagens já revisadas. |
| 6 Comércio | Estimar o total de vendas em reais na próxima semana. |
| 7 Educação | Agrupar perfis de acesso ao ambiente virtual sem rótulo de evasão. |
| 8 Saúde | Classificar exames em categorias previamente definidas por especialistas. |

| Caso escolhido | Alvo ou ausência de alvo | Categoria, quantidade ou grupos? | Abordagem e justificativa | Dados necessários e limitação |
| --- | --- | --- | --- | --- |
| 1 Educação | Evadiu/permaneceu | Categoria | Classificação supervisionada, pois o desfecho histórico é conhecido. | Frequência e entregas anteriores; rótulos podem refletir vieses. |
| 2 Saúde | Tempo de espera em minutos | Quantidade | Regressão supervisionada, pois estima um valor numérico. | Horário, demanda e atendimentos; mudanças operacionais reduzem precisão. |
| 3 Comércio | Sem alvo | Grupos | Agrupamento não supervisionado, pois não existem perfis rotulados previamente. | Histórico de compras; perfis não representam identidades fixas. |
| 4 Finanças | Adimplente/inadimplente | Categoria | Classificação supervisionada com contratos e desfechos rotulados. | Histórico de pagamentos; exige cuidado com discriminação e dados sensíveis. |
| 5 Segurança digital | Spam/legítima | Categoria | Classificação supervisionada com mensagens previamente revisadas. | Textos e rótulos; novas formas de spam podem reduzir desempenho. |

## 4. Raciocínio crítico

“Detectar fraude” define sozinho o tipo de aprendizado? Compare o uso de exemplos rotulados e a busca de operações atípicas sem rótulos. **Não. Com operações rotuladas como fraude ou legítimas, é possível treinar classificação supervisionada. Sem rótulos, pode-se buscar anomalias ou agrupamentos por aprendizado não supervisionado. Uma anomalia não prova fraude: precisa de investigação humana.**

## Entrega

Salve este arquivo preenchido. Critérios: distinção conceitual, pertinência dos dados, justificativa e clareza. [Voltar ao início](README.md).
