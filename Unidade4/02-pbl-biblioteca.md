[02-pbl-biblioteca.md](https://github.com/user-attachments/files/34397195/02-pbl-biblioteca.md)
<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# PBL — Biblioteca em Foco

## Identificação

- Estudante ou equipe: **Raquel Caetano Nascimento**
- Turma: **Sistemas de Informação — 2026.2 Noturno**
- Data de realização: **28/10/2026**
- Integrantes e contribuições (se em equipe): **Individual**

## Situação-problema

Uma biblioteca universitária enfrenta filas em horários específicos e baixa utilização de alguns serviços. A coordenação deseja melhorar o atendimento e planejar recursos. Este é um cenário didático.

**Público-alvo:** estudantes usuários, equipe de atendimento e gestão.

**Questão norteadora:** como os dados podem orientar o planejamento da biblioteca e a oferta de serviços sem identificar ou discriminar seus usuários?

## Investigação em equipe

1. Delimitem o problema e a decisão a apoiar.
2. Registrem o que já sabem e o que precisam investigar.
3. Formulem duas perguntas de negócio.
4. Definam a unidade de análise, os atributos e o alvo, quando houver.
5. Justifiquem a abordagem e indiquem se uma análise descritiva já seria suficiente.
6. Proponham avaliação, cuidados com os dados e limitações.

## Canvas da equipe

| Campo | Registro |
| --- | --- |
| Problema e decisão | Identificar horários de pico e serviços pouco utilizados para redistribuir atendentes e ajustar a oferta, sem identificar usuários. |
| Público-alvo | Estudantes, atendentes e gestão da biblioteca. |
| O que sabemos | Há filas em determinados horários e baixa utilização de alguns serviços, conforme o cenário didático. |
| O que precisamos investigar | Medições reais por faixa horária, capacidade da equipe, duração dos atendimentos e procura por serviço. |
| Pergunta de negócio 1 | Em quais dias e horários a demanda supera a capacidade de atendimento? |
| Pergunta de negócio 2 | Quais serviços têm menor utilização e quais ajustes de horário ou divulgação podem melhorar o acesso? |
| Unidade de análise e período | Faixa de uma hora por dia e tipo de serviço, observada por 8 semanas. |
| Atributos, unidades e origem pretendida | Dia da semana (calendário); horário (hora, sistema de atendimento); número de atendimentos (contagem, sistema); tempo médio de espera (minutos, senhas anônimas); equipe disponível (quantidade, escala); serviço utilizado (categoria, registros agregados). |
| Alvo e momento em que será conhecido, ou ausência de alvo | Para eventual regressão, alvo = tempo médio de espera na faixa futura, conhecido após seu encerramento. Na análise descritiva, não há alvo preditivo. |
| Abordagem e justificativa | Começar com estatísticas descritivas e gráficos de horários; se houver dados suficientes, usar regressão supervisionada para prever espera por faixa. |
| Alternativa sem ML | Painel de médias, medianas e volume de atendimentos por hora, suficiente para uma primeira redistribuição de recursos. |
| Como avaliar a proposta | Comparar tempo de espera e volume antes e depois de ajustes; em previsão, comparar MAE em semanas posteriores com referência simples. |
| Privacidade e limitações | Usar contagens agregadas, evitar nomes e matrículas, limitar acesso, definir retenção; períodos atípicos e dados incompletos podem distorcer conclusões. |

## Registro de colaboração

| Integrante | Papel | Contribuição |
| --- | --- | --- |
| Raquel Caetano Nascimento | Elaboração da proposta | Delimitação, perguntas de negócio, dados, abordagem e cuidados éticos. |

## Conclusão da equipe

**Proposta:** Implantar coleta agregada por faixa horária, produzir painel de demanda e testar redistribuição da equipe; só avaliar ML se a análise descritiva não for suficiente.

**Dúvida ainda aberta:** Qual é o volume mínimo de registros necessário para identificar padrões estáveis em semanas letivas e de provas?

**Feedback recebido e melhoria realizada:** Aguardando feedback da professora/equipe; melhoria proposta: revisar faixas horárias e incluir semanas de provas após retorno.

## Entrega

Canvas preenchido e síntese para apresentação de dois minutos. Avaliar coerência da pergunta, dados, abordagem, responsabilidade e colaboração. [Voltar ao início](README.md).
