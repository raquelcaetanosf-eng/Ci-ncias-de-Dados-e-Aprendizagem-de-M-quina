[Uploading Atividade Prática — Detetives dos Dados.md…]()
# Atividade Prática — Detetives dos Dados

## Ciência de Dados e Aprendizagem de Máquina — Aula 01

**Tema:** Introdução à Ciência de Dados e Big Data  
**Metodologia:** Trabalho em equipe  
**Tempo:** 20 minutos  
**Entregável:** Mapa do Problema de Ciência de Dados

---

## 1. Identificação da equipe

| Campo | Resposta |
|---|---|
| **Turma:** |Sistemas de Informação |
| **Data:** |26/08/2026|
| **Equipe:** |Equipe TCC |
| **Integrante 1:** |Andressa Cristyna Araújo |
| **Integrante 2:** |Raquel Caetano Nascimento|

---

## 2. Objetivo da atividade

Nesta atividade, sua equipe deverá analisar um **problema real** e pensar como uma equipe de Ciência de Dados poderia utilizar dados para compreender a situação e apoiar uma decisão.

O objetivo não é desenvolver um sistema ou modelo de Machine Learning neste momento.

O objetivo é aprender a **pensar como um cientista de dados**:

> **Problema → Dados → Informação → Análise → Decisão → Benefício**

---

## 3. Escolha do problema

Escolha uma área para investigar:

- [ ] Comércio
- [ ] Banco
- [ ] Saúde
- [ ] Transporte
- [ ] Educação
- [ ] Entretenimento
- [ ] Indústria
- [ ] Meio ambiente
- [ ] Esportes
- [x] Outra: Segurança Pública e Computação Forense

### Problema escolhido

**Descreva, em poucas linhas, o problema que sua equipe pretende analisar.**

>A vulnerabilidade e a dificuldade que vítimas de violência doméstica enfrentam para coletar, armazenar e resguardar evidências digitais (como prints, áudios, vídeos e mensagens) de agressões e ameaças. Pela convivência com o agressor e o risco iminente de retaliação, provas cruciais são frequentemente perdidas, apagadas sob coação ou rejeitadas pela justiça por ausência de integridade forense.
---

## 4. Quem possui esse problema?

>Identifique a organização, grupo ou público afetado pelo problema.

**Quem possui ou enfrenta esse problema?**

Vítimas de violência doméstica e familiar que convivem com seus agressores e necessitam reunir provas para instruir denúncias e solicitações de medidas protetivas de urgência com discrição e segurança.

### Quem é afetado pelo problema?

> > Diretamente: As vítimas e seus dependentes, que permanecem vulneráveis e sem respaldo probatório.  
> Indiretamente: Delegacias Especializadas (DEAM), peritos criminais, Ministério Público, Defensoria Pública e magistrados, que enfrentam inquéritos frágeis por falta de material probatório tecnicamente aceito.

---

## 5. Por que esse problema é importante?

Explique por que vale a pena investigar esse problema utilizando dados.

**Qual é o impacto do problema?**

> A análise orientada a dados permite mapear os gargalos que levam ao arquivamento de inquéritos e identificar os tipos de provas mais comumente descartados por quebra de cadeia de custódia. O impacto social é crítico, pois a fragilidade probatória desestimula a formalização de queixas e perpetua o ciclo de agressões; no âmbito jurídico, acarreta ineficiência processual e impunidade.

---

## 6. Qual decisão precisa ser tomada?

Imagine que sua equipe foi contratada para ajudar uma organização.

**Qual decisão a organização precisa tomar?**

>A organização (como uma Secretaria de Segurança Pública ou ONG de apoio) precisa decidir qual modelo de aplicação segura e quais mecanismos de custódia digital e camuflagem devem ser disponibilizados para viabilizar a coleta e o armazenamento de provas com validade forense para as vítimas.

---

# 7. Identificação dos dados

Agora pense:

> **Quais dados seriam necessários para compreender esse problema?**

Liste pelo menos **5 dados**.

| Nº | Dado necessário | Por que esse dado é importante? |
|---:|---|---|
| 1 | | Tipo de arquivo/evidência coletada (áudio, foto, vídeo, texto) | Permite identificar os formatos de mídia mais frequentes para estruturar o armazenamento e a extração. |
| 2 | | Taxa de rejeição pericial ou judicial de provas digitais | Mensura o volume de inquéritos prejudicados por inconsistência na cadeia de custódia.|
| 3 | |Frequência e horário dos registros de violência | Ajuda a compreender padrões temporais dos incidentes para prever rotinas automáticas de backup em nuvem. |
| 4 | | Taxa de concessão de medidas protetivas com vs. sem prova periciada | Avalia o impacto estatístico direto de ter evidências com hash e integridade garantidas.  |
| 5 | | Tempo médio decorrido entre a agressão/ameaça e o registro da denúncia | Ajuda a definir janelas críticas de vulnerabilidade em que os dados podem ser apagados pelo agressor. |

### Exemplos

Podem ser considerados dados como:

- idade;
- localização;
- frequência;
- notas;
- compras;
- valores;
- horários;
- avaliações;
- histórico de utilização;
- registros de atendimento;
- imagens;
- textos;
- localização geográfica.

---

# 8. Que informações queremos descobrir?

Os dados, quando analisados, podem gerar informações úteis.

**O que sua equipe gostaria de descobrir a partir dos dados?**

### Pergunta 1

> Qual percentual de denúncias é indeferido ou arquivado por insuficiência de provas digitais válidas?

### Pergunta 2

> Quais são os tipos de evidência mais vulneráveis à contestação jurídica nos tribunais?

### Pergunta 3

> Qual é a correlação entre a presença de metadados íntegros (como hash e timestamps) e a rapidez no deferimento de medidas protetivas?

### Pergunta 4

> Quais são os períodos do dia e situações em que a vítima mais necessita de mecanismos automáticos ou discretos de captura?

---

# 9. Quais padrões podemos procurar?

Pense como um cientista de dados.

Sua equipe poderia procurar:

- [x] Tendências
- [x] Comparações
- [ ] Grupos semelhantes
- [x] Comportamentos recorrentes
- [x] Valores fora do padrão
- [x] Relações entre variáveis
- [x] Mudanças ao longo do tempo
- [ ] Outros: __________________________

### Explique um padrão que vocês gostariam de encontrar

>A correlação estatística entre o uso de métodos padronizados de preservação de evidência (com hash e custódia preservada) e o aumento da taxa de condenações ou de deferimento ágil de medidas protetivas, comprovando que a integridade técnica reduz a impunidade.
---

# 10. Qual análise poderia ser realizada?

Como os dados poderiam ser analisados?

Marque uma ou mais possibilidades:

- [x] Análise descritiva
- [x] Comparação entre grupos
- [x] Análise temporal
- [x] Visualização por gráficos
- [x] Identificação de padrões
- [x] Classificação
- [ ] Previsão
- [ ] Agrupamento
- [ ] Outra: __________________________

### Explique

> Análise descritiva e comparativa para cruzar a taxa de sucesso judicial de processos que apresentavam provas validadas pericialmente contra aqueles sustentados apenas por relatos ou prints avulsos, além de visualização gráfica dos tipos de evidências mais descartados.

---

# 11. Qual decisão poderia ser tomada?

Depois de analisar os dados, imagine que sua equipe encontrou informações importantes.

**Que decisão poderia ser tomada com base nos resultados?**

> Implementar e padronizar o uso de uma aplicação camuflada dotada de verificação de integridade forense automatizada, priorizando o suporte aos tipos de dados mais descartados pela perícia (ex: áudios e capturas de tela) e simplificando o envio de relatórios probatórios para as DEAMs.

---

# 12. Qual seria o benefício?

Qual seria o possível benefício da decisão para a organização ou para as pessoas envolvidas?

>> Para as vítimas: Segurança na guarda das evidências, discrição contra retaliações e maior agilidade na obtenção de proteção judicial.  
> Para o sistema de segurança/justiça: Redução do tempo de instrução pericial, inquéritos mais consistentes e maior eficácia na responsabilização legal de agressores.

---

# 13. Os 5 Vs do Big Data

Analise o problema escolhido pela equipe.

| V | Pergunta | Resposta da equipe |
|---|---|---|
| **Volume** | Existe uma grande quantidade de dados? |  Sim, envolve milhares de boletins de ocorrência, autos judiciais e arquivos de mídia gerados diariamente em todo o país.|
| **Velocidade** | Os dados são gerados ou processados rapidamente? |Moderada a alta, com fluxos contínuos de mensagens e incidentes em tempo real que demandam salvamento ágil.  |
| **Variedade** | Existem diferentes tipos ou formatos de dados? | Muito alta: áudios, mensagens de texto, imagens, vídeos, metadados de localização e logs de chamadas.  |
| **Veracidade** | Os dados podem apresentar erros ou problemas de qualidade? | Extremamente crítica: arquivos podem ser editados, corrompidos, apagados ou contestados se não houver cálculo de integridade (Hash).|
| **Valor** | Os dados podem gerar algum benefício ou apoiar decisões? |Altíssimo: representa a diferença prática entre a integridade física/vida da vítima e a impunidade do agressor. |

### Qual dos 5 Vs é mais relevante para o problema?

> > *Veracidade*


### Justifique

>No âmbito forense e jurídico, a autenticidade e a não-adulteração dos dados são indispensáveis. Uma evidência sem veracidade comprovada (ausência de hash, quebra de cadeia de custódia) é desqualificada em juízo, anulando seu valor prático na proteção da vítima.

---

# 14. Mapa do Problema de Ciência de Dados

Complete o fluxo abaixo:

```text
┌─────────────────────┐
│       PROBLEMA      │
│ Perda e desqualificação pericial de evidências digitais│
│ em casos de violência doméstica e risco de coação.          │
│                     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│        DADOS        │
│ │ Tipos de arquivos, índices de indeferimento de queixas,│
│ metadados de registros, logs e relatórios de perícia                    │
│                     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│     INFORMAÇÕES     │
│Padrões de evidências mais descartadas e impacto da    │
│ falta de integridade probatória nas decisões judiciais                     │
│                     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│       ANÁLISE       │
│  Comparação descritiva e temporal entre processos com   │
│ provas validadas vs. processos sem cadeia de custódia.                    │
│                     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│       DECISÃO       │
│ Adoção e desenvolvimento de ferramenta segura com      │
│ camuflagem e registro automático de integridade forense                    │
│                     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│      BENEFÍCIO      │
│ Proteção física da vítima, garantia de medidas de      │
│ urgência e maior eficácia penal contra agressores.                      │
│                     │
└─────────────────────┘
```

### Resuma cada etapa

**Problema:**  
> 

**Dados:**  
> 

**Informação:**  
> 

**Análise:**  
> 

**Decisão:**  
> 

**Benefício:**  
> 

---

# 15. Preparação para apresentação

A equipe terá **2 minutos** para apresentar sua proposta.

Organizem a apresentação seguindo esta estrutura:

### 1. Nosso problema

> _________________________________________________

### 2. Precisamos destes dados

> _________________________________________________

### 3. Queremos descobrir

> _________________________________________________

### 4. Pretendemos analisar

> _________________________________________________

### 5. A decisão poderia ser

> _________________________________________________

### 6. O benefício esperado é

> _________________________________________________

---

# 16. Checklist da equipe

Antes de entregar, confira:

- [ ] Definimos um problema real.
- [ ] Identificamos quem é afetado pelo problema.
- [ ] Explicamos por que o problema é importante.
- [ ] Identificamos pelo menos 5 dados necessários.
- [ ] Definimos perguntas que queremos responder.
- [ ] Identificamos possíveis padrões.
- [ ] Indicamos como os dados poderiam ser analisados.
- [ ] Definimos uma possível decisão.
- [ ] Identificamos o benefício esperado.
- [ ] Analisamos os 5 Vs do Big Data.
- [ ] Preenchemos o Mapa do Problema.
- [ ] Estamos preparados para apresentar em 2 minutos.

---

# 17. Reflexão final

Responda individualmente ou em equipe:

> **Ter muitos dados significa necessariamente tomar boas decisões? Por quê?**

**Resposta:**

> ________________________________________________________________
>
> ________________________________________________________________
>
> ________________________________________________________________
>
> ________________________________________________________________

---

## Entrega

### Produto final

A equipe deverá entregar:

**Mapa do Problema de Ciência de Dados**

contendo:

```text
Problema
   ↓
Dados necessários
   ↓
Informações desejadas
   ↓
Análise
   ↓
Decisão
   ↓
Benefício esperado
```

**Formato sugerido:** Markdown, PDF ou documento disponibilizado pelo professor.

**Apresentação:** 2 minutos por equipe.
