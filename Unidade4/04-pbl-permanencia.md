[04-pbl-permanencia.md](https://github.com/user-attachments/files/34397279/04-pbl-permanencia.md)
<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# PBL integrador — Apoio à Permanência

## Identificação

- Estudante ou equipe: **Raquel Caetano Nascimento**
- Turma: **Sistemas de Informação — 2026.2 Noturno**
- Data de realização: **04/11/2026**
- Integrantes e contribuições (se em equipe): **Individual**

## Contexto

Uma instituição quer compreender sinais associados à evasão e oferecer apoio antes do fim do semestre. Público-alvo: estudantes matriculados e equipe de apoio acadêmico. O cenário é didático e a prática usa dados sintéticos.

**Questão norteadora:** como identificar situações que merecem atenção e oferecer apoio, reconhecendo erros do modelo e dificuldades que os dados não capturam?

## Proposta da equipe

### 1. Delimitação

- Problema e público: **Estudantes matriculados que podem precisar de apoio acadêmico; equipe de permanência e orientação.**
- Decisão que o resultado pode apoiar: **Oferecer contato voluntário e serviços de apoio, nunca punição ou desligamento automático.**
- Definição de evasão, unidade e horizonte: **Unidade: estudante; evasão = não permanência até o encerramento do semestre, conforme critério institucional a definir; previsão após a semana 4.**

### 2. Perguntas de negócio

1. **Quais indicadores disponíveis na semana 4 se associam à não permanência ao final do semestre?**
2. **Como oferecer apoio eficaz sem prejudicar estudantes sinalizados incorretamente?**

### 3. Dados necessários

| Dado | Papel no projeto | Disponível quando? | Origem pretendida | Necessidade e risco |
| --- | --- | --- | --- | --- |
| Frequência até semana 4 | Atributo preditivo | Semana 4 | Registros acadêmicos | Necessário para sinal inicial; pode refletir dificuldades externas. |
| Nota até semana 4 | Atributo preditivo | Semana 4 | Sistema acadêmico | Pode variar por disciplina e critério de avaliação. |
| Entregas até semana 4 | Atributo preditivo | Semana 4 | Ambiente virtual | Nem toda disciplina registra entregas igualmente. |
| Evasão ao fim do semestre | Alvo binário | Fim do semestre | Registro acadêmico | Exige definição consistente e não deve ser acessível ao modelo na previsão. |

Diferencie dados usados na simulação e dados que seriam necessários para uma investigação real: **Na simulação há apenas frequência, nota e entregas da semana 4, além do desfecho sintético. Um estudo real exigiria verificar qualidade, cobertura, definições, consentimento/base legal aplicável e acesso aos serviços, sem presumir que variáveis adicionais sejam apropriadas.**

### 4. Abordagem e algoritmo

- Classificação, regressão ou outra formulação, com justificativa: **Classificação supervisionada, porque o resultado esperado é uma categoria (evadiu ou permaneceu).**
- Algoritmo introdutório escolhido: **Árvore de decisão introdutória, interpretável e adequada ao exercício.**
- Referência simples: **Classificador que prevê sempre a classe majoritária (DummyClassifier).**

### 5. Avaliação

- Preparação, divisão e validação: **Separar treino/teste estratificados; escolher parâmetros por validação cruzada somente no treino; testar uma vez ao final.**
- Métricas e razão da escolha: **Acurácia para visão geral, sensibilidade para identificar possíveis evasões e matriz de confusão para analisar erros.**
- Resultados efetivamente calculados e link da evidência: **No laboratório sintético executado, árvore com acurácia de teste 0,7800, sensibilidade 0,6885 e matriz TN=75, FP=14, FN=19, TP=42; evidência em [notebook executado](notebooks/laboratorio-equipe.ipynb).**
- Erros relevantes e consequências: **Falso positivo: preocupação e contato desnecessário; falso negativo: deixar de oferecer apoio a quem poderia precisar.**

### 6. Limites e proteção

- Por que os resultados não demonstram causalidade? **Associação estatística pode refletir fatores não observados e não comprova que baixa frequência cause evasão.**
- Por que dados sintéticos não validam uso institucional? **A simulação usa relações artificiais e não demonstra desempenho, justiça ou utilidade em estudantes reais.**
- Que grupos podem ser mal representados? Como investigar isso com evidências apropriadas? **Estudantes com baixa conectividade, necessidades de acessibilidade, jornadas de trabalho extensas ou registros incompletos podem ter erros diferentes. Avaliar com dados reais autorizados e análises agregadas de desempenho por grupos pertinentes, respeitando privacidade.**
- Como minimizar dados, restringir acesso e definir retenção? **Coletar apenas dados necessários, limitar perfis de acesso, registrar acessos e estabelecer prazo de exclusão conforme política institucional e legislação.**
- Como garantir revisão humana e contestação? **Equipe capacitada revisa sinais e contexto antes do contato; oferecer canal para corrigir registros e contestar decisões.**

### 7. Recomendações de apoio

- Ação voluntária proposta: **Convite privado e voluntário para orientação acadêmica, tutoria e apoio institucional, sem mencionar rótulos de risco.**
- Como acolher estudantes não sinalizados pelo modelo: **Divulgar apoio universal e manter solicitação espontânea, independentemente da classificação.**
- O que precisa ser verificado antes de aplicação real: **Validar dados reais, métricas, vieses, segurança, base legal, impacto das intervenções e governança com responsáveis institucionais.**

Previsões não são certezas. Priorize apoio e revisão humana, sem punições ou decisões automáticas prejudiciais.

## Apresentação de cinco minutos

| Tempo | Conteúdo | Responsável |
| --- | --- | --- |
| 1 minuto | Problema e dados | Raquel|
| 2 minutos | Método e resultados | Raquel|
| 1 minuto | Limitações | Raquel |
| 1 minuto | Recomendações de apoio | Raquel|

## Contribuições

| Integrante | Contribuição verificável |
| --- | --- |
| Raquel Caetano Nascimento | Estruturação da proposta, definição dos dados, método e salvaguardas. |

[Voltar ao início](README.md).
