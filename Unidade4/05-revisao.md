[05-revisao.md](https://github.com/user-attachments/files/34397303/05-revisao.md)
<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# Questões de revisão — Registro individual

## Identificação

- Estudante ou equipe: **Raquel Caetano Nascimento**
- Turma: **Sistemas de Informação — 2026.2 Noturno**
- Data de realização: **04/11/2026**
- Integrantes e contribuições (se em equipe): **Individual**

Responda com suas palavras e apresente os cálculos quando solicitados. Os números dos exercícios manuais não são os resultados do laboratório.

## 1. Explique a diferença entre regra programada para bloquear uma palavra e modelo de spam treinado com exemplos.

**Resposta:** A regra segue uma instrução fixa: encontrou a palavra, bloqueia. O modelo aprende padrões a partir de mensagens rotuladas, considera características combinadas e pode generalizar, embora erre.

## 2. Por que codificar evadiu/permaneceu como 1/0 não transforma classificação em regressão?

**Resposta:** Porque 0 e 1 representam categorias de desfecho, não uma quantidade contínua. A tarefa continua sendo classificação binária.

## 3. Uma biblioteca quer estimar empréstimos e descobrir perfis. Que tarefas correspondem a cada pergunta?

**Resposta:** Estimar quantidade de empréstimos é regressão; descobrir perfis sem categorias prévias é agrupamento não supervisionado.

## 4. O que são atributo, alvo e unidade de análise no laboratório educacional?

**Resposta:** Atributos são frequência, nota e entregas na semana 4; alvo é evasão no fim do semestre (0/1); unidade de análise é cada estudante fictício.

## 5. Por que calcular a mediana antes de dividir os dados pode invalidar a avaliação?

**Resposta:** Porque a mediana calculada com todos os dados incorpora informações do teste ao treinamento (vazamento). Deve ser ajustada só no treino e aplicada ao teste.

## 6. Em uma matriz didática com TN=80, FP=5, FN=10, TP=5, calcule acurácia e sensibilidade. O resultado é suficiente para aprovar o modelo?

**Resposta:** Total = 80+5+10+5 = 100. Acurácia = (TN+TP)/total = (80+5)/100 = 85%. Sensibilidade = TP/(TP+FN) = 5/(5+10) = 33,3%. Não basta aprovar: dois terços dos casos positivos passam despercebidos.

## 7. Valores reais 100, 120, 140 e previsões 110, 115, 130. Calcule MAE e informe a unidade se o alvo for vendas em reais.

**Resposta:** Erros absolutos: |100−110|=10, |120−115|=5, |140−130|=10. MAE=(10+5+10)/3=8,33 reais.

## 8. Um R² de -0,2 significa “20% de acertos negativos”? Explique.

**Resposta:** Não. R² = −0,2 significa que o modelo teve erro quadrático 20% maior que a referência que prevê a média dos valores reais, nesse conjunto. Não é porcentagem de acertos.

## 9. Uma árvore tem acurácia 1,00 no treino e 0,65 na validação. Que hipótese investigar e como?

**Resposta:** Investigar sobreajuste: o modelo pode memorizar o treino e generalizar mal. Comparar profundidade, tamanho mínimo de folhas e desempenho em validação cruzada, sem usar o teste para seleção.

## 10. Por que escolher a profundidade pelo teste prejudica a estimativa final?

**Resposta:** Porque o teste passa a influenciar a escolha do modelo, produzindo estimativa otimista. A profundidade deve ser escolhida por validação no treino e o teste reservado à avaliação final.

## 11. Baixa frequência associada à evasão demonstra causa? Proponha explicação alternativa.

**Resposta:** Não. Dificuldades financeiras, saúde, trabalho ou acesso à internet podem influenciar tanto frequência quanto permanência. Associação não prova causa.

## 12. Um modelo sinaliza um estudante como possível evasão. Que ação responsável pode ser adotada?

**Resposta:** Oferecer contato privado e voluntário para apoio acadêmico, com revisão humana e possibilidade de contestação; não aplicar punição ou rótulo definitivo.

## Fontes adicionais consultadas

**Enunciados e materiais didáticos do Módulo IV, UDF, 2026. Nenhuma fonte externa foi consultada para esta versão.**

[Voltar ao início](README.md).
