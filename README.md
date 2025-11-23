# Plano de Experimento – Scoping e Planejamento

## 1. Identificação básica

Esta seção apresenta os identificadores, autores e metadados principais do experimento.

### 1.1 Título do experimento

Impacto do uso de especificações OpenAPI na implementação de clientes REST.

### 1.2 ID / código

MED-OPENAPI-CLIENTES-REST-v1.

### 1.3 Versão do documento e histórico de revisão

Versão atual: v1.0 (22/11/2025).

Histórico de revisão (resumo):

- v1.0 (22/11/2025): primeira versão completa das seções 1 a 6 deste plano de experimento.
- v1.0 (23/11/2025): primeira versão completa das seções 7 a 20 deste plano de experimento.

### 1.4 Datas (criação, última atualização)

Data de criação: 22/11/2025.  
Data da última atualização: 23/11/2025.

### 1.5 Autores (nome, área, contato)

- **Autor:** Luca Ferrari Azalim, estudante de Engenharia de Software. Contato: <mailto:lazalim@sga.pucminas.br>.
- **Orientador:** Danilo de Quadros Maia Filho, professor de Engenharia de Software. Contato: <mailto:1514571@sga.pucminas.br>.

### 1.6 Responsável principal (PI / dono do experimento)

Responsável principal: estudante pesquisador, sob orientação do professor responsável pela disciplina/projeto de pesquisa.

### 1.7 Projeto / produto / iniciativa relacionada

Experimento vinculado à disciplina de Medição e Experimentação em Engenharia de Software, inserido em projeto acadêmico com foco em técnicas e ferramentas para desenvolvimento de serviços web e clientes REST.

---

## 2. Contexto e problema

Esta seção descreve o problema investigado, o contexto de aplicação e o embasamento conceitual do experimento.

### 2.1 Descrição do problema / oportunidade

Integrações com serviços _Representational State Transfer (REST)_ são atividades recorrentes em projetos de desenvolvimento de software. Em muitos contextos, equipes implementam clientes REST com base apenas em documentação textual, frequentemente dispersa ou ambígua, o que pode aumentar o esforço de implementação e o número de defeitos de integração. Especificações _OpenAPI_ e ferramentas de geração automática de código cliente surgem como alternativas para padronizar a descrição das _Application Programming Interfaces (APIs)_ e automatizar partes da implementação, mas o impacto efetivo dessas soluções na produtividade e na qualidade da implementação de clientes REST ainda não está claramente quantificado no contexto considerado. Este experimento busca explorar essa oportunidade de quantificação empírica.

### 2.2 Contexto organizacional e técnico

O experimento será conduzido em ambiente acadêmico, com estudantes de Engenharia de Software ou áreas afins, em atividades de laboratório. O domínio técnico é o de aplicações web com serviços _back-end_ expostos por APIs REST, incluindo operações CRUD (_Create, Read, Update, Delete_). A tarefa experimental foca na implementação de clientes REST em JavaScript, em laboratório de informática ou ambiente virtual com VS Code, controle de versão e suíte de testes automatizada.

### 2.3 Trabalhos e evidências prévias (internos e externos)

Diversos trabalhos discutem o uso de especificações formais de APIs e ferramentas de geração de código como meio de reduzir erros de integração e facilitar a evolução de sistemas distribuídos. Estudos sobre evolução de APIs em arquiteturas de _microservices_ identificam estratégias e desafios relacionados à compatibilidade, versionamento e comunicação de mudanças entre produtores e consumidores de APIs, destacando problemas de impacto de mudança e de comunicação ineficaz [Lercher et al. 2024a]. Pesquisas recentes também avaliam abordagens para gerar descrições OpenAPI acuradas a partir de código-fonte Java, evidenciando o papel central da especificação OpenAPI na documentação de APIs REST e o interesse da comunidade em automatizar essa tarefa [Lercher et al. 2024b]. Internamente, práticas de laboratório e projetos de disciplina já utilizam APIs documentadas por meio de ferramentas como _Swagger UI_, mas sem comparação sistemática entre documentação puramente textual e documentação baseada em especificações OpenAPI combinadas com geração automática de código cliente.

### 2.4 Referencial teórico e empírico essencial

O plano fundamenta-se em engenharia de software experimental, medição de esforço e qualidade e desenvolvimento orientado a serviços. A forma de documentação e apoio à implementação é tratada como fator experimental que influencia esforço (tempo) e qualidade (defeitos de integração, aderência ao contrato da API). Estudos sobre ferramentas de apoio indicam que automatização e padronização tendem a reduzir erros e tempo, desde que haja treinamento mínimo. Evidências sobre evolução de APIs em _microservices_ [Lercher et al. 2024a] e sobre geração de descrições OpenAPI a partir de código-fonte [Lercher et al. 2024b] destacam o papel central de especificações OpenAPI precisas na qualidade da documentação e na comunicação de contratos de APIs REST.

---

## 3. Objetivos e questões (Goal / Question / Metric)

Esta seção explicita o objetivo geral, os objetivos específicos, as questões de pesquisa e as métricas associadas.

### 3.1 Objetivo geral (Goal template)

Analisar o efeito do uso de especificações OpenAPI combinadas com geração automática de código cliente na implementação de clientes REST, com o propósito de avaliar impacto em produtividade e qualidade da integração com APIs REST, sob a perspectiva de desenvolvedores em formação (estudantes de Engenharia de Software), no contexto de atividades práticas em laboratório em ambiente acadêmico.

### 3.2 Objetivos específicos

- O1: Comparar o tempo de conclusão da integração de clientes REST entre participantes que utilizam apenas documentação textual da API e participantes que utilizam especificação OpenAPI com geração automática de cliente.
- O2: Comparar a quantidade de defeitos de integração identificados por suíte de testes automatizada entre os dois grupos de participantes.
- O3: Avaliar diferenças em erros de contrato de API (uso incorreto de endpoints, parâmetros ou tipos de dados) entre os grupos.
- O4: Investigar a percepção de esforço, clareza da documentação e confiança na integração relatada pelos participantes em cada condição experimental.

### 3.3 Questões de pesquisa / de negócio

- Q1: O uso de especificações OpenAPI com geração automática de código cliente reduz o tempo de implementação de clientes REST em comparação ao uso exclusivo de documentação textual?
- Q2: O uso de especificações OpenAPI com geração automática de código cliente reduz o número de defeitos de integração identificados por uma suíte de testes automatizada?
- Q3: O uso de especificações OpenAPI com geração automática de código cliente reduz a ocorrência de erros de contrato de API em relação ao uso exclusivo de documentação textual?
- Q4: Como a percepção de esforço, clareza da documentação e confiança na integração difere entre desenvolvedores que utilizam apenas documentação textual e aqueles que utilizam especificações OpenAPI com geração de código cliente?

### 3.4 Métricas associadas (GQM)

Para Q1:

- M1.1 – Tempo de conclusão da tarefa: tempo, em minutos, entre o início da atividade e o momento em que o participante sinaliza ter concluído a implementação do cliente ou atinge o limite de tempo definido. Fonte: registro manual ou automatizado de início e término por participante.

Para Q2:

- M2.1 – Número de testes automatizados falhos: contagem de casos de teste da suíte automatizada que falham para o cliente implementado por cada participante. Fonte: resultados de execução da suíte de testes no ambiente de laboratório.

Para Q3:

- M3.1 – Número de erros de contrato de API: contagem de ocorrências de uso incorreto de endpoints, parâmetros, tipos de dados ou códigos de resposta, conforme categorias predefinidas em checklist de análise. Fonte: inspeção dos resultados de teste e, quando necessário, inspeção do código do cliente.

Para Q4:

- M4.1 – Percepção de esforço: pontuação média em escala _Likert_ de 1 (discordo totalmente) a 5 (concordo totalmente) para itens relacionados a esforço percebido na implementação. Fonte: questionário pós-experimento em Google Forms.
- M4.2 – Percepção de clareza da documentação: pontuação média em escala _Likert_ de 1 (discordo totalmente) a 5 (concordo totalmente) para itens relacionados à clareza e completude da documentação disponível. Fonte: questionário pós-experimento em Google Forms.
- M4.3 – Confiança na integração: pontuação média em escala _Likert_ de 1 (discordo totalmente) a 5 (concordo totalmente) que indica o nível de confiança do participante de que a integração está correta. Fonte: questionário pós-experimento em Google Forms.

---

## 4. Escopo e contexto do experimento

Esta seção delimita o que será coberto pelo experimento, o contexto de realização e suas principais premissas, restrições e limitações.

### 4.1 Escopo funcional / de processo (incluído e excluído)

Incluído no escopo:

- Implementação de clientes REST em JavaScript para a API Swagger Petstore, utilizando a especificação OpenAPI disponibilizada em `https://petstore3.swagger.io/api/v3/openapi.json`, com operações CRUD sobre recursos de exemplo da Petstore.
- Uso de uma única linguagem de programação (JavaScript) e de um ambiente de desenvolvimento padronizado (VS Code) entre os participantes.
- Fornecimento de documentação textual da API em arquivos Markdown para o grupo de controle e, na condição experimental correspondente, especificação OpenAPI com suporte a geração automática de código cliente.
- Execução de suíte de testes automatizada de ponta a ponta (_end-to-end_) com Playwright para avaliar a integração do cliente com a API.
- Aplicação de questionários de perfil (experiência prévia) e de percepção pós-atividade em Google Forms.

Excluído do escopo:

- Desenvolvimento ou evolução da própria API REST além do necessário para o experimento.
- Avaliação de aspectos de desempenho em produção ou carga de usuários reais.
- Análise profunda de manutenção de longo prazo do código gerado ou escrito manualmente.
- Comparação entre diferentes ferramentas de geração de código OpenAPI (o experimento utilizará especificamente o **OpenAPI Generator**).

### 4.2 Contexto do estudo (tipo de organização, projeto, experiência)

O estudo ocorre em instituição de ensino superior, como parte de disciplina de Engenharia de Software ou laboratório de desenvolvimento. O “projeto” é uma atividade prática de integração de cliente com API, em sessão de laboratório com duração limitada. Os participantes são estudantes com experiência básica em programação e HTTP/REST, mas com níveis variados de familiaridade com OpenAPI e ferramentas de geração de código.

### 4.3 Premissas

- A API REST utilizada no experimento estará estável e acessível durante toda a execução das sessões.
- Todos os participantes terão acesso aos mesmos recursos de hardware e software (laboratório ou ambiente virtual padronizado).
- A linguagem de programação, a IDE e a ferramenta de geração de código OpenAPI serão previamente instaladas e testadas.
- Os participantes terão recebido, antes da execução, pelo menos uma breve introdução a REST, à linguagem escolhida e ao ambiente de desenvolvimento.
- O tempo de sessão previsto é suficiente para que a maioria dos participantes consiga concluir a tarefa ou chegar a um ponto mensurável.

### 4.4 Restrições

- Tempo limitado de laboratório para realização da atividade (sessão única de 100 minutos, correspondente a duas aulas de 50 minutos consecutivas, para implementação e testes).
- Tamanho relativamente pequeno da amostra, condicionado ao número de estudantes disponíveis.
- Uso de uma única API de estudo, o que restringe a variedade de cenários de integração.
- Dependência das ferramentas de laboratório e da infraestrutura de rede da instituição.
- Necessidade de utilizar ferramentas e bibliotecas com licenças compatíveis com o ambiente acadêmico e preferencialmente _open source_.

### 4.5 Limitações previstas

- A amostra composta por estudantes pode não representar integralmente o comportamento de desenvolvedores profissionais em ambientes industriais.
- O uso de uma única API e de uma única linguagem de programação reduz a generalização dos resultados para outros domínios e tecnologias.
- O tempo restrito e o formato de atividade em laboratório podem influenciar o comportamento dos participantes, favorecendo estratégias de solução rápidas em detrimento de práticas de engenharia mais cuidadosas.
- A familiaridade desigual dos participantes com REST, OpenAPI ou ferramentas de geração de código pode introduzir variabilidade adicional, mesmo com coleta de dados de perfil.

---

## 5. Stakeholders e impacto esperado

Esta seção identifica os principais stakeholders e discute os impactos esperados do experimento em processo e produto.

### 5.1 Stakeholders principais

- Estudantes participantes do experimento (desenvolvedores em formação).
- Professor orientador e demais docentes envolvidos com a disciplina ou projeto.
- Coordenação de curso ou programa acadêmico interessado em evidências sobre práticas de ensino de desenvolvimento de serviços web.
- Comunidade de pesquisa em engenharia de software experimental, interessada em evidências sobre ferramentas de apoio a desenvolvimento de clientes REST.
- Eventuais equipes técnicas da instituição responsáveis pela manutenção da infraestrutura de laboratório.

### 5.2 Interesses e expectativas dos stakeholders

- Estudantes: obter experiência prática com clientes REST, OpenAPI e ferramentas de geração de código.
- Professor orientador: obter evidências empíricas sobre impacto em produtividade e qualidade para uso didático e em pesquisa.
- Coordenação de curso: avaliar inclusão ou reforço de conteúdos sobre especificações de APIs e ferramentas de apoio.
- Comunidade de pesquisa: acessar resultados replicáveis e bem documentados sobre ferramentas para desenvolvimento de clientes REST.
- Equipe de infraestrutura: garantir que o experimento ocorra sem comprometer a estabilidade dos laboratórios.

### 5.3 Impactos potenciais no processo / produto

No curto prazo, o experimento altera a dinâmica de uma aula ou sessão de laboratório, exigindo organização específica de grupos, materiais e coleta de dados. Em termos de “produto”, o código de clientes REST será usado principalmente como artefato experimental. No médio prazo, os resultados podem influenciar o ensino de serviços web, apoiando a adoção sistemática de especificações OpenAPI e ferramentas de geração de código.

---

## 6. Riscos de alto nível, premissas e critérios de sucesso

Esta seção apresenta os riscos de alto nível, bem como critérios de sucesso e de parada antecipada da execução.

### 6.1 Riscos de alto nível (negócio, técnicos, etc.)

- Indisponibilidade ou instabilidade da API REST durante a execução do experimento, comprometendo a coleta de dados.
- Problemas de infraestrutura de laboratório (falhas de rede, falta de máquinas funcionais, problemas de autenticação) que impeçam participantes de completar a atividade.
- Número de participantes menor do que o planejado, reduzindo o poder estatístico das análises.
- Diferenciais de experiência muito grandes entre participantes que dificultem a comparação entre grupos, mesmo com randomização.
- Resistência de participantes em seguir estritamente o protocolo (por exemplo, compartilhamento de soluções entre grupos) que possa introduzir vieses.
- Atrasos na preparação de materiais (API, especificação OpenAPI, projeto base, testes, questionários) que limitem o tempo disponível para a execução.

### 6.2 Critérios de sucesso globais (go / no-go)

O experimento será considerado bem-sucedido, em termos de execução, se:

- For possível conduzir pelo menos uma sessão completa com número de participantes próximo ao planejado e distribuição equilibrada entre os grupos.
- Todos os instrumentos (API, documentação, especificação OpenAPI, ferramenta de geração de código, suíte de testes e questionários) funcionarem como previsto, permitindo coleta de dados consistente.
- As principais métricas definidas (tempo, defeitos de integração, erros de contrato e percepções de esforço e clareza) forem coletadas para a maior parte dos participantes.
- Os dados obtidos permitirem, ainda que com poder estatístico limitado, comparar tendências entre os grupos e gerar insights úteis para decisões didáticas ou futuras pesquisas.

### 6.3 Critérios de parada antecipada (pré-execução)

O início da execução deve ser adiado ou cancelado se ocorrerem, antes da sessão, situações como:

- Indisponibilidade persistente da API ou falhas graves na infraestrutura que impeçam a comunicação cliente–servidor.
- Falhas críticas na ferramenta de geração de código ou na especificação OpenAPI que não possam ser corrigidas a tempo, tornando inviável a condição experimental correspondente.
- Número de participantes confirmado substancialmente abaixo do mínimo definido para viabilizar a comparação entre grupos.
- Ausência de aprovações acadêmicas ou éticas exigidas pela instituição para experimentos com estudantes.
- Mudanças relevantes no calendário acadêmico que inviabilizem a realização da sessão de laboratório no período planejado.

---

## 7. Modelo conceitual e hipóteses

### 7.1 Modelo conceitual do experimento

O modelo conceitual considera a forma de documentação e apoio à implementação de clientes REST como fator experimental principal, com dois níveis: (i) documentação textual tradicional da API e (ii) especificação OpenAPI combinada com geração automática de código cliente. Esse fator influencia tempo de integração, defeitos de integração, erros de contrato e percepções de esforço, clareza e confiança. Espera-se que especificações OpenAPI precisas e ferramentas de geração reduzam a interpretação manual, diminuam ambiguidades e levem a menor esforço e menos erros em comparação ao uso exclusivo de documentação textual.

### 7.2 Hipóteses formais (H0, H1)

Com base nas questões de pesquisa formuladas na Seção 3.3, definem-se as seguintes hipóteses formais:

Para **Q1 (tempo de implementação):**

- **H0_tempo:** não há diferença estatisticamente significativa no tempo de conclusão da tarefa de implementação de clientes REST entre o grupo que utiliza apenas documentação textual e o grupo que utiliza especificação OpenAPI com geração automática de código cliente.
- **H1_tempo:** o grupo que utiliza especificação OpenAPI com geração automática de código cliente apresenta tempo de conclusão da tarefa estatisticamente menor do que o grupo que utiliza apenas documentação textual.

Para **Q2 (defeitos de integração):**

- **H0_defeitos:** não há diferença estatisticamente significativa no número de defeitos de integração identificados por suíte de testes automatizada entre os dois grupos.
- **H1_defeitos:** o grupo que utiliza especificação OpenAPI com geração automática de código cliente apresenta menor número de defeitos de integração identificados por suíte de testes automatizada em comparação ao grupo que utiliza apenas documentação textual.

Para **Q3 (erros de contrato de API):**

- **H0_contrato:** não há diferença estatisticamente significativa na quantidade de erros de contrato de API (uso incorreto de endpoints, parâmetros ou tipos de dados) entre os dois grupos.
- **H1_contrato:** o grupo que utiliza especificação OpenAPI com geração automática de código cliente apresenta menor quantidade de erros de contrato de API em comparação ao grupo que utiliza apenas documentação textual.

Para **Q4 (percepções subjetivas):**

- **H0_percepcao:** não há diferença estatisticamente significativa nas percepções de esforço, clareza da documentação e confiança na integração entre os grupos.
- **H1_percepcao:** os participantes que utilizam especificação OpenAPI com geração automática de código cliente relatam menor esforço percebido, maior clareza da documentação e maior confiança na integração do que aqueles que utilizam apenas documentação textual.

### 7.3 Nível de significância e considerações de poder

Será adotado nível de significância α = 0,05 para os testes de hipóteses. Como o experimento será realizado em contexto de disciplina, com tamanho de amostra limitado, o poder estatístico tende a ser moderado, o que pode dificultar a detecção de efeitos pequenos. Os resultados serão interpretados com base em significância estatística, tamanhos de efeito e consistência com o modelo conceitual e a literatura.

---

## 8. Variáveis, fatores, tratamentos e objetos de estudo

### 8.1 Objetos de estudo

Os principais objetos de estudo deste experimento são:

- **Clientes REST em código-fonte:** implementações de clientes que consomem a API de teste, escritas na linguagem de programação escolhida para a disciplina.
- **Tarefas de integração:** tarefa prática que consiste em fazer o cliente consumir corretamente os endpoints da API, atendendo aos requisitos funcionais definidos.
- **Suíte de testes automatizada:** conjunto de casos de teste que validam o comportamento do cliente em relação ao contrato da API (endpoints, parâmetros, tipos de dados e códigos de resposta).
- **Artefatos de documentação da API:** documentação textual tradicional e especificação OpenAPI correspondente, incluindo artefatos gerados pelo **OpenAPI Generator**.

### 8.2 Sujeitos / participantes (visão geral)

Os sujeitos do experimento serão **estudantes de Engenharia de Software** (ou cursos afins) matriculados na disciplina de Medição e Experimentação em Engenharia de Software, ofertada em pelo menos duas turmas, cada uma com cerca de 60 alunos. Trata-se de disciplina do sexto período de graduação, em que grande parte dos estudantes já atua profissionalmente em empresas de Tecnologia da Informação (TI). Espera-se que tenham experiência prática em programação e uso de serviços REST, embora com níveis possivelmente distintos de familiaridade com especificações OpenAPI e ferramentas de geração automática de código. O contexto é acadêmico, mas com forte proximidade com a prática profissional.

### 8.3 Variáveis independentes (fatores) e seus níveis

O fator principal (variável independente) considerado é:

- **Forma de documentação/apoio à implementação de clientes REST (Fator Doc):**
  - **Nível 1 – Documentação textual em Markdown:** participantes recebem apenas documentação textual da API em arquivos Markdown, sem acesso à especificação OpenAPI nem ao OpenAPI Generator.
  - **Nível 2 – Especificação OpenAPI + geração automática de código cliente com OpenAPI Generator:** participantes recebem a especificação OpenAPI oficial da Swagger Petstore e acesso ao **OpenAPI Generator** configurado para gerar o cliente base em JavaScript, a partir do qual completarão a integração.

### 8.4 Tratamentos (condições experimentais)

Serão consideradas duas condições experimentais principais:

- **Tratamento T1 – Grupo Documentação Textual (controle):** participantes implementam o cliente REST com base apenas na documentação textual da API, sem acesso à especificação OpenAPI nem ao OpenAPI Generator.
- **Tratamento T2 – Grupo OpenAPI + OpenAPI Generator:** participantes implementam o cliente REST utilizando a especificação OpenAPI da API e o **OpenAPI Generator** previamente configurado. A implementação consiste em configurar o gerador (se necessário), gerar o cliente e completar o código para atender aos requisitos da tarefa.

### 8.5 Variáveis dependentes (respostas)

| Código | Variável                           | Tipo / unidade            | Descrição resumida                                                                                        |
| ------ | ---------------------------------- | ------------------------- | --------------------------------------------------------------------------------------------------------- |
| VD1    | Tempo de conclusão da tarefa       | Minutos                   | Tempo desde o início da atividade até a conclusão da implementação (ou atingimento do limite máximo).     |
| VD2    | Número de defeitos de integração   | Contagem de testes falhos | Número de falhas na suíte de testes automatizada associadas à implementação do cliente.                   |
| VD3    | Número de erros de contrato de API | Contagem de ocorrências   | Ocorrências de uso incorreto de endpoints, parâmetros, tipos de dados ou códigos de resposta (checklist). |
| VD4    | Esforço percebido                  | Escala _Likert_ (1–5)     | Pontuação autorrelatada de esforço subjetivo ao realizar a tarefa.                                        |
| VD5    | Clareza percebida da documentação  | Escala _Likert_ (1–5)     | Pontuação autorrelatada de clareza, completude e facilidade de uso da documentação recebida.              |
| VD6    | Confiança na integração            | Escala _Likert_ (1–5)     | Pontuação autorrelatada de confiança do participante na correção da integração com a API.                 |

### 8.6 Variáveis de controle / bloqueio

| Variável de controle               | Valor / configuração fixa                                     | Justificativa                                                                                 |
| ---------------------------------- | ------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| Linguagem de programação           | Mesma linguagem para todos os participantes                   | Evitar variação de desempenho ou familiaridade causada por diferentes linguagens.             |
| Ambiente de desenvolvimento        | Mesma IDE, compilador/intérprete, bibliotecas e ferramentas   | Reduzir influência de diferenças de ferramentas ou versões na execução da tarefa.             |
| API de teste                       | Mesma API REST (endpoints, modelos de dados e comportamentos) | Garantir que todos integrem com o mesmo contrato de API.                                      |
| Material de instrução da atividade | Mesmas instruções gerais e critérios de sucesso               | Evitar vieses decorrentes de explicações diferentes entre grupos; variar apenas o tratamento. |
| Tempo máximo de sessão             | Mesmo limite de tempo para todos                              | Evitar que diferenças de duração de sessão afetem comparações de tempo ou qualidade.          |

### 8.7 Possíveis variáveis de confusão conhecidas

| Possível variável de confusão                 | Efeito esperado                                                                                | Como será monitorada / considerada                                                                                                                      |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Experiência prévia com REST e clientes HTTP   | Participantes mais experientes podem concluir mais rápido e com menos erros, em qualquer grupo | Coleta em questionário de perfil e uso em análises exploratórias ou bloqueio simples.                                                                   |
| Familiaridade com OpenAPI e OpenAPI Generator | Participantes experientes podem tirar melhor proveito do tratamento T2                         | Perguntas específicas no perfil; análise de subgrupos ou variáveis de ajuste.                                                                           |
| Habilidade geral de programação               | Diferenças individuais podem influenciar tempo e qualidade independentemente do tratamento     | Indicadores indiretos (anos de experiência profissional em TI e autodeclaração de proficiência em programação em escala 1–5) e interpretação cuidadosa. |
| Motivação e engajamento                       | Baixa motivação pode aumentar tempo ou reduzir qualidade                                       | Observações de laboratório e, se possível, perguntas breves sobre engajamento.                                                                          |
| Ruídos de ambiente de laboratório             | Problemas de máquina, rede ou ferramenta podem inflar tempos e causar falhas adicionais        | Registro de incidentes de infraestrutura durante a sessão para contextualizar dados.                                                                    |

---

## 9. Desenho experimental

Esta seção detalha o tipo de desenho, a estratégia de randomização, o balanceamento entre grupos e o número de grupos/sessões planejados.

### 9.1 Tipo de desenho (completamente randomizado, blocos, fatorial, etc.)

O experimento adotará um **desenho quase-experimental com grupos paralelos e blocos por turma**. As duas turmas da disciplina de Medição e Experimentação em Engenharia de Software funcionarão como blocos naturais, refletindo eventuais diferenças de contexto (horário, dinâmica de professor-aluno, coesão da turma). Dentro de cada turma (bloco), os estudantes serão divididos em dois grupos correspondentes aos tratamentos definidos na Seção 8:

- **T1 – Grupo Documentação Textual (controle)**.
- **T2 – Grupo OpenAPI + Codegen (tratamento experimental)**.

Não haverá medidas repetidas nem _cross-over_ de tratamentos: cada participante será exposto a **apenas um tratamento** e realizará **uma única tarefa principal** de implementação do cliente REST durante a sessão experimental. Esse desenho é adequado ao contexto acadêmico (duas turmas, tempo de laboratório limitado) e ao objetivo de comparar, de forma direta, o impacto dos tratamentos sobre esforço e qualidade, reduzindo a complexidade operacional.

### 9.2 Randomização e alocação

A variável principal a ser randomizada são os **sujeitos (estudantes)**, em termos de qual tratamento (T1 ou T2) cada um receberá dentro de sua respectiva turma. A tarefa experimental (implementação de um cliente REST para uma mesma API de teste) **não será randomizada** entre participantes: todos executarão a mesma tarefa, com os mesmos requisitos e mesma API, diferenciando-se apenas pelo tipo de documentação/apoio fornecido (Fator Doc).

O procedimento proposto é:

1. Em cada turma, confirmar a lista de presentes no início da sessão experimental.
2. Aplicar rapidamente um pequeno formulário de perfil em Google Forms, coletando variáveis como: experiência prévia com REST/HTTP, experiência com OpenAPI/_Swagger_ e tempo de atuação profissional em TI.
3. Calcular, para cada estudante, um indicador simples de experiência a partir da média de duas questões em escala _Likert_ de 1 a 5 (autodeclaração de experiência com REST/HTTP e autodeclaração de experiência com OpenAPI/_Swagger_).
4. Ordenar a lista de estudantes por esse indicador e, em seguida, realizar uma **alocação aleatória estratificada**: alternar estudantes entre T1 e T2, utilizando sorteio inicial (por exemplo, moeda ou gerador aleatório) para decidir qual tratamento recebe o primeiro estudante da lista.
5. Registrar a alocação final (por exemplo, em planilha ou formulário) para uso posterior na análise.

Com isso, a randomização concentra-se na atribuição de tratamentos, mantendo a mesma tarefa e ordem de execução para todos, o que simplifica o controle de variáveis de confusão relacionadas a variações de tarefa ou sequência.

### 9.3 Balanceamento e contrabalanço

O **balanceamento entre grupos** será perseguido principalmente em dois eixos:

- **Tamanho dos grupos:** dentro de cada turma, buscar que T1 e T2 tenham números de participantes tão próximos quanto possível.
- **Perfil de experiência:** usar o procedimento de alocação estratificada descrito acima para distribuir de forma equilibrada participantes com maior e menor experiência entre T1 e T2.

Como cada participante executará apenas uma tarefa em um único momento, não haverá efeitos de ordem de tratamentos. Eventuais efeitos de horário serão minimizados pelo mesmo roteiro e duração para todos e, se necessário, registrados para inspeção posterior.

### 9.4 Número de grupos e sessões

Considerando duas turmas com cerca de 60 estudantes cada (total aproximado de 120 participantes), o plano é formar **quatro grupos analíticos principais**:

- **Turma A – T1A (Documentação Textual)** e **T2A (OpenAPI + Codegen)**.
- **Turma B – T1B (Documentação Textual)** e **T2B (OpenAPI + Codegen)**.

Em cada turma haverá uma sessão experimental principal durante o horário regular da disciplina, cobrindo apresentação, execução da tarefa de implementação do cliente REST, execução da suíte de testes e preenchimento do questionário pós-tarefa. Cada participante participará de uma única sessão, e os dados poderão ser analisados agregando as turmas ou considerando o efeito de turma como fator de bloqueio.

---

## 10. População, sujeitos e amostragem

### 10.1 População-alvo

A população-alvo é formada por desenvolvedores que implementam clientes REST para consumir APIs em aplicações web de pequeno e médio porte. Os estudantes participantes são considerados uma aproximação dessa população, por atuarem ou se prepararem para atuar em contextos de desenvolvimento de serviços web e clientes REST.

### 10.2 Critérios de inclusão de sujeitos

Serão incluídos estudantes:

- regularmente matriculados na disciplina de Medição e Experimentação em Engenharia de Software (ou equivalente);
- que já tenham cursado disciplinas básicas de programação e desenvolvimento de software;
- com conhecimento introdutório de HTTP e REST;
- presentes na sessão de laboratório, que aceitem participar voluntariamente;
- com disponibilidade para permanecer durante toda a sessão experimental.

### 10.3 Critérios de exclusão de sujeitos

Serão excluídos sujeitos que:

- não concluírem parte relevante da sessão de laboratório;
- tiverem participado previamente do desenho detalhado do experimento, da API de teste, da especificação OpenAPI ou da suíte de testes;
- apresentarem dificuldade de compreensão das instruções mesmo após esclarecimentos;
- não atenderem a requisitos éticos ou administrativos definidos pela instituição.

### 10.4 Tamanho da amostra planejado (por grupo)

O experimento deverá envolver duas turmas com cerca de 60 estudantes cada, resultando em uma amostra total planejada entre 80 e 120 sujeitos presentes e participantes. Em cada turma, os estudantes serão distribuídos de forma aproximadamente equilibrada entre T1 (Documentação Textual) e T2 (OpenAPI + OpenAPI Generator), com cerca de 20 a 30 participantes por tratamento, o que é considerado suficiente para análises descritivas e testes estatísticos com poder moderado.

### 10.5 Método de seleção / recrutamento

Será utilizada amostra de conveniência, composta pelos estudantes matriculados nas turmas da disciplina em que a atividade experimental será realizada. O recrutamento ocorrerá por convite em sala e comunicação nos canais da disciplina. No início da sessão, os presentes que aceitarem participar serão alocados a T1 ou T2 conforme o procedimento descrito na Seção 9.2, sem seleção adicional fora desse conjunto.

### 10.6 Treinamento e preparação dos sujeitos

Antes da execução, os participantes terão passado por atividades regulares da disciplina que fornecem base conceitual sobre programação, desenvolvimento de software e uso de HTTP/REST. Além disso, será realizado, em aula anterior ou no início da sessão experimental, breve _tutorial_ com: (i) visão geral da tarefa de integração de cliente REST com a API; (ii) descrição do ambiente (JavaScript, VS Code, ferramentas de apoio); (iii) apresentação sucinta da API de teste; e (iv) explicação em alto nível de especificações OpenAPI e do papel de ferramentas de geração de código. Durante a sessão, haverá instruções escritas e esclarecimentos pontuais, desde que não impliquem na solução direta da tarefa ou na quebra da distinção entre os tratamentos.

---

## 11. Instrumentação e protocolo operacional

### 11.1 Instrumentos de coleta (questionários, logs, planilhas, etc.)

Serão utilizados, principalmente:

- **Questionário de perfil em Google Forms:** coleta experiência prévia, uso de REST, familiaridade com OpenAPI e com o OpenAPI Generator, além de dados básicos para caracterização da amostra.
- **Questionário pós-tarefa em Google Forms:** registra esforço percebido, clareza da documentação e confiança na integração (VD4, VD5, VD6).
- **Registros de tempo:** anotação de início e término da atividade por participante (VD1), em planilha eletrônica.
- **Resultados da suíte de testes em Playwright:** número de testes falhos e mensagens de erro (VD2) e apoio à identificação de erros de contrato.
- **Checklist de erros de contrato:** registro estruturado de categorias de erro de contrato (VD3), em planilha ou formulário padronizado.
- **Planilha de consolidação:** integração de todas as medidas, com identificadores anônimos ou pseudoanônimos.

### 11.2 Materiais de suporte (instruções, guias)

Serão preparados: (i) guia de instruções para participantes (objetivo da atividade, ambiente, tarefa e critérios de término), (ii) guia rápido para administradores (roteiro operacional da sessão), (iii) slides introdutórios, (iv) material de apoio sobre o ambiente técnico (por exemplo, `README` do projeto base) e (v) modelos padronizados de formulários e planilhas.

### 11.3 Procedimento experimental (protocolo – visão passo a passo)

O protocolo seguirá, em linhas gerais, as etapas: (i) preparação prévia (infraestrutura, projeto base, API, especificação OpenAPI, OpenAPI Generator e instrumentos de coleta), (ii) abertura da sessão (apresentação do experimento, reforço de voluntariedade, questionário de perfil), (iii) alocação dos participantes a T1 e T2, (iv) apresentação da tarefa e distribuição dos materiais de cada tratamento, (v) implementação do cliente, com registro de tempos e apoio apenas em dúvidas de infraestrutura, (vi) execução da suíte de testes e preenchimento do checklist de erros de contrato, (vii) aplicação do questionário pós-tarefa e (viii) consolidação inicial dos dados em planilha.

### 11.4 Plano de piloto (se haverá piloto, escopo e critérios de ajuste)

Antes da execução em turmas completas, está previsto um **piloto em pequena escala** com um subconjunto de participantes, preferencialmente um grupo reduzido de estudantes da disciplina (4 a 8) ou monitores/colegas com perfil semelhante. O piloto terá como escopo validar clareza de instruções e materiais, estimar o tempo necessário para a tarefa, testar o fluxo de testes e registros e avaliar a adequação dos questionários e planilhas. Com base nesse retorno, poderão ser feitos ajustes pontuais em enunciados, tempo de sessão, instruções de uso da ferramenta de geração de código e correção de problemas técnicos.

---

## 12. Plano de análise de dados (pré-execução)

### 12.1 Estratégia geral de análise (como responderá às questões)

Serão produzidas análises descritivas (médias, medianas, dispersões, gráficos simples) e comparações entre T1 e T2, alinhadas ao modelo GQM da Seção 3. Para Q1–Q3, serão comparadas as distribuições de tempo (VD1), defeitos de integração (VD2) e erros de contrato (VD3); para Q4, serão comparadas as percepções de esforço, clareza da documentação e confiança (VD4, VD5, VD6). Os resultados serão interpretados à luz das hipóteses da Seção 7 e do contexto de turmas como blocos.

### 12.2 Métodos estatísticos planejados

Inicialmente serão usadas estatísticas descritivas e inspeção gráfica para VD1, VD2 e VD3 em T1 e T2. Para comparação entre grupos, pretende-se utilizar teste _t_ para amostras independentes quando as premissas forem razoavelmente atendidas e, em caso contrário, o teste de Mann–Whitney ou equivalente não paramétrico. As variáveis em escala _Likert_ (VD4, VD5, VD6) serão analisadas por medidas descritivas e testes não paramétricos entre grupos. Quando houver evidência de diferenças entre turmas, poderão ser realizadas análises estratificadas ou modelos simples com turma como fator de bloqueio.

### 12.3 Tratamento de dados faltantes e outliers

Casos com falhas graves de registro ou interrupções por problemas externos poderão ser excluídos de análises inferenciais principais, sendo descritos separadamente. Respostas em branco em questionários serão tratadas como ausentes, sem imputação. Valores extremos em VD1, VD2 e VD3 serão identificados por inspeção gráfica; quando decorrentes de erro de registro, serão corrigidos ou descartados daquela análise, e, quando refletirem situações reais mas raras, serão mantidos com decisão explícita sobre sua inclusão ou não em testes estatísticos.

### 12.4 Plano de análise para dados qualitativos (se houver)

Comentários abertos eventualmente coletados em campos dos questionários serão analisados de forma exploratória, por leitura e agrupamento em categorias informais (por exemplo, tipos de dificuldade ou percepções recorrentes sobre documentação e ferramentas). Essas categorias e frequências serão usadas apenas para complementar a discussão dos resultados quantitativos e sugerir hipóteses ou melhorias para estudos futuros.

---

> [!NOTE] > **Vídeo explicativo disponível:** Esta seção conta com um vídeo complementar que apresenta uma explicação detalhada sobre a avaliação de validade deste experimento, incluindo discussão das principais ameaças e estratégias de mitigação. [Assista ao vídeo aqui](./VÍDEO.mp4).

## 13. Avaliação de validade (ameaças e mitigação)

### 13.1 Validade de conclusão

A validade de conclusão pode ser ameaçada por tamanho de amostra limitado, violações de premissas estatísticas e medidas imprecisas de tempo, defeitos ou percepções. Para mitigação, pretende-se maximizar a participação, adotar testes não paramétricos quando necessário, padronizar medições e reportar tamanhos de efeito e análises descritivas, mesmo quando a significância estatística for limitada.

### 13.2 Validade interna

As principais ameaças de validade interna incluem diferenças pré-existentes entre participantes, eventos específicos da sessão (problemas de infraestrutura, atrasos, ruídos de ambiente) e contaminação entre grupos (troca de materiais ou soluções). As estratégias de controle são alocação estratificada por perfil às condições T1 e T2, uso de roteiro de sessão e infraestrutura padronizados, orientação explícita para não compartilhar materiais/soluções e registro de incidentes relevantes de infraestrutura.

### 13.3 Validade de constructo

Há risco de as medidas não representarem adequadamente os constructos de interesse, por exemplo tempo de conclusão influenciado por problemas de ambiente, número de testes falhos não capturando todos os aspectos de qualidade e escalas _Likert_ pouco precisas. Para reduzir essas ameaças, as métricas foram definidas explicitamente nas Seções 3.4 e 8.5, os instrumentos serão revisados em piloto (Seção 11.4) e serão feitas análises de consistência entre indicadores (por exemplo, defeitos vs. erros de contrato, esforço vs. tempo).

### 13.4 Validade externa

A generalização dos resultados é limitada pelo contexto acadêmico, pelo uso de uma única API de teste, de uma linguagem e de um ambiente específicos, além do perfil de estudantes. Assim, os achados podem não se transferir diretamente para organizações com equipes seniores, domínios de alta criticidade ou arquiteturas diferentes. Para mitigar, o plano descreve em detalhe contexto, sujeitos e materiais, facilitando a avaliação de similaridade e futuras replicações.

### 13.5 Resumo das principais ameaças e estratégias de mitigação

As ameaças mais críticas concentram-se em tamanho de amostra, diferenças prévias de experiência, influência de fatores externos de laboratório e restrição do contexto a uma disciplina específica. As estratégias de mitigação incluem maximizar adesão e documentar perdas de dados, usar alocação estratificada e dados de perfil, padronizar instrumentos e protocolo, registrar incidentes de infraestrutura e documentar o contexto em detalhe para apoiar replicações.

---

## 14. Ética, privacidade e conformidade

### 14.1 Questões éticas (uso de sujeitos, incentivos, etc.)

O experimento envolve estudantes em atividade de aula, o que pode gerar sensação de pressão para participar ou receio de impacto em notas. Para mitigar, a participação será voluntária, desvinculada de avaliação formal (ou com alternativa equivalente) e não haverá penalidade para quem optar por não participar ou interromper a atividade. Não são previstos riscos físicos ou psicológicos relevantes além do esforço típico de uma prática de laboratório.

### 14.2 Consentimento informado

Antes do início da coleta de dados, os estudantes receberão explicação clara sobre objetivos do estudo, tipos de dados coletados, forma de uso (apenas para fins acadêmicos e de pesquisa) e possibilidade de recusa ou retirada sem prejuízo. Quando requerido pela instituição, será utilizado termo de consentimento específico; caso contrário, o consentimento será registrado por aceite em formulário inicial, com reforço verbal em sala.

### 14.3 Privacidade e proteção de dados

Serão coletadas apenas informações necessárias para caracterização da amostra e análise dos resultados (por exemplo, experiência prévia, respostas de questionários, tempos e resultados de testes). Os dados serão armazenados com identificadores anônimos ou pseudoanônimos, sem associação direta a nomes ou matrículas. O acesso bruto aos dados identificáveis, quando houver, será restrito ao professor responsável e a membros autorizados da equipe. Os dados serão mantidos pelo tempo necessário à conclusão da disciplina e de eventuais publicações acadêmicas, seguindo diretrizes internas da instituição.

### 14.4 Aprovações necessárias (comitê de ética, jurídico, DPO, etc.)

Antes da execução, será verificado se o experimento se enquadra em exigências de submissão a comitê de ética em pesquisa com seres humanos ou a instâncias internas (coordenação de curso, comissões de pesquisa, _Data Protection Officer (DPO)_). Quando aplicável, o plano e os instrumentos serão submetidos para aprovação, e o experimento só será realizado após parecer favorável ou dispensa formal.

---

## 15. Recursos, infraestrutura e orçamento

### 15.1 Recursos humanos e papéis

- **Professor orientador:** responsável pelo desenho do experimento, aprovação final do plano, condução das sessões em laboratório, supervisão da coleta e análise de dados e comunicação de resultados.
- **Estudante pesquisador:** responsável pela preparação de materiais (API de teste, especificação OpenAPI, projeto base, testes, questionários), apoio à condução das sessões, consolidação inicial dos dados e rascunho de relatórios.
- **Monitores ou auxiliares (se houver):** apoio operacional em laboratório (organização de participantes, registro de tempos, suporte a problemas de infraestrutura) e auxílio na verificação de consistência dos dados coletados.

### 15.2 Infraestrutura técnica necessária

- Laboratório de informática (ou ambiente virtual equivalente) com estações de trabalho padronizadas, acesso à internet e permissões adequadas.
- Acesso à API Swagger Petstore (`https://petstore3.swagger.io`) a partir do laboratório.
- Repositório de código Git hospedado no GitHub (conta `lucaazalim`) com o projeto base do cliente em JavaScript e a suíte de testes em Playwright.
- Ferramenta de geração de código **OpenAPI Generator** instalada globalmente via NPM (`openapi-generator-cli`).
- Ferramentas auxiliares para registro de dados (planilhas, formulários em Google Forms, sistema de controle de versão Git).

### 15.3 Materiais e insumos

- Documentação textual da API e especificação OpenAPI em formato digital.
- Questionários de perfil e pós-tarefa (em meio digital ou impresso).
- Modelos de planilhas para registro de tempos, resultados de testes e erros de contrato.
- Slides e guias de instrução para participantes e administradores.

### 15.4 Orçamento e custos estimados

Espera-se que os custos diretos sejam reduzidos, pois o experimento utiliza infraestrutura já disponível na instituição. Os principais custos envolvem tempo de preparação e análise do professor orientador e do estudante pesquisador, tratados como parte de carga horária de disciplina ou projeto de pesquisa, além de eventuais custos marginais (por exemplo, impressão de materiais).

---

## 16. Cronograma, marcos e riscos operacionais

### 16.1 Macrocronograma (até o início da execução)

| Fase                        | Descrição resumida                                                                                                                       | Janela típica               |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | --------------------------- |
| Planejamento do experimento | Conclusão e revisão deste plano com o professor orientador.                                                                              | Início do semestre          |
| Preparação técnica          | Configuração da API de teste, especificação OpenAPI, projeto base, suíte de testes e questionários.                                      | Semanas 1–3                 |
| Piloto                      | Execução de piloto em pequena escala, com coleta de feedback sobre materiais, tempo de tarefa e fluxo de coleta de dados.                | Semana 3 ou 4               |
| Congelamento de materiais   | Definição das versões estáveis de API, especificação OpenAPI, projeto base, testes e instrumentos a serem usados nas turmas.             | Logo após o piloto          |
| Execução nas turmas         | Realização das sessões experimentais nas turmas da disciplina, preferencialmente na mesma semana ou em semanas imediatamente adjacentes. | Semana definida em conjunto |

### 16.2 Dependências entre atividades

| Atividade afetada        | Dependência principal                                                                                                                        | Observações                                                                               |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| Preparação técnica       | Aprovação conceitual do plano pelo professor orientador                                                                                      | Sem aprovação, API, testes e instrumentos não devem ser considerados "definitivos".       |
| Piloto                   | Disponibilidade de laboratório/ambiente virtual com ferramentas instaladas (incluindo OpenAPI Generator) e, se exigido, parecer ético prévio | Sem essas condições, o piloto deve ser adiado.                                            |
| Execução nas turmas      | Conclusão satisfatória do piloto e aplicação dos ajustes identificados                                                                       | Alterações maiores após o piloto exigem nova checagem rápida antes da execução principal. |
| Coleta de dados completa | Alinhamento com o calendário da disciplina e comunicação prévia aos estudantes                                                               | Evitar sobreposição com provas ou eventos que reduzam presença ou tempo disponível.       |

### 16.3 Riscos operacionais e plano de contingência

| Risco principal                                          | Impacto potencial                                                     | Ação de mitigação/contingência                                                                                  |
| -------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Indisponibilidade do professor orientador ou pesquisador | Adiamento ou cancelamento da sessão planejada                         | Definir substituto com antecedência ou reservar janela alternativa no calendário da disciplina.                 |
| Atrasos na preparação técnica                            | Materiais ou ferramentas incompletos na data planejada                | Iniciar preparação cedo, adotar checkpoints semanais e priorizar itens críticos (API, testes, especificação).   |
| Conflitos com calendário acadêmico                       | Baixa presença ou tempo insuficiente para execução                    | Planejar datas em coordenação com a disciplina e ajustar cronograma em caso de choque identificado.             |
| Problemas de infraestrutura no dia (laboratório/rede)    | Impossibilidade de executar tarefa ou coletar dados de parte da turma | Ter laboratório alternativo previamente identificado ou remarcar sessão em curto prazo, registrando o ocorrido. |

---

## 17. Governança do experimento

### 17.1 Papéis e responsabilidades formais

| Papel                                 | Responsabilidades principais                                                                                      |
| ------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Professor orientador                  | Aprovar o plano, decidir sobre mudanças de escopo, conduzir ou supervisionar as sessões e a análise de dados.     |
| Estudante pesquisador                 | Detalhar e manter o plano, preparar materiais, apoiar a condução das sessões e consolidar/analisar os dados.      |
| Monitores/auxiliares                  | Apoiar a operação em laboratório (organização, registro de tempos, suporte técnico básico) e checar consistência. |
| Coordenação da disciplina/curso       | Ser informada sobre objetivos, cronograma e eventuais mudanças relevantes que afetem a disciplina.                |
| Comitês/instâncias éticas (se houver) | Avaliar e aprovar o plano quando necessário, garantindo conformidade ética e institucional.                       |

### 17.2 Ritos de acompanhamento pré-execução

Antes da execução principal, estão previstos: (i) reunião inicial de alinhamento entre professor orientador e estudante pesquisador; (ii) checkpoints semanais curtos durante a preparação técnica; (iii) revisão após o piloto para decidir ajustes e congelar materiais; e (iv) reunião de prontidão próxima à aplicação nas turmas, verificando o atendimento aos critérios da Seção 20.

### 17.3 Processo de controle de mudanças no plano

Mudanças relevantes no desenho ou no escopo do experimento (por exemplo, tratamentos, métricas principais ou protocolo de sessão) deverão ser: propostas por escrito pelo estudante pesquisador ou pelo professor orientador, discutidas e **aprovadas formalmente pelo professor orientador** antes de implementação e registradas em histórico de revisão do plano, comunicando coordenação e instâncias éticas quando aplicável. Mudanças operacionais menores (ajustes de redação, pequenas melhorias de material) poderão ser realizadas diretamente pelo estudante pesquisador, desde que não alterem decisões experimentais centrais e sejam documentadas de forma sucinta.

---

## 18. Plano de documentação e reprodutibilidade

### 18.1 Repositórios e convenções de nomeação

Toda a documentação do experimento será mantida em repositório Git hospedado no GitHub, na conta `lucaazalim`. O plano de experimento (este `README`), os instrumentos (questionários, checklists), scripts de apoio (por exemplo, scripts para execução da suíte de testes ou consolidação de dados) e artefatos derivados (relatórios) ficarão organizados em pastas dedicadas (por exemplo, `docs/`, `instruments/`, `scripts/`, `reports/`). Para arquivos de dados coletados, serão usadas convenções de nomes que incluam data, turma e versão (por exemplo, `dados-turmaA-2025-05-v1.csv`), evitando informações pessoais diretamente nos nomes de arquivos.

### 18.2 Templates e artefatos padrão

Serão mantidos como artefatos padrão: (i) modelos de questionário de perfil e pós-tarefa; (ii) modelo de checklist de erros de contrato; (iii) modelos de planilhas para consolidação de tempos, resultados de testes e variáveis derivadas; (iv) scripts de execução automatizada da suíte de testes, quando aplicável; e (v) modelos de relatórios parciais e finais. Esses templates ficarão versionados no mesmo repositório do plano, em subpastas identificadas (por exemplo, `instruments/questionarios/`, `instruments/checklists/`, `scripts/`, `reports/templates/`).

### 18.3 Plano de empacotamento para replicação futura

Para favorecer a reprodutibilidade e a replicação, o repositório conterá: (i) este plano de experimento completo, com histórico de revisões; (ii) instruções passo a passo para preparação do ambiente (incluindo instalação/configuração da API de teste, especificação OpenAPI e OpenAPI Generator); (iii) scripts ou comandos recomendados para execução da suíte de testes e coleta de dados; (iv) exemplos anonimizados de conjuntos de dados resultantes e de análises (por exemplo, planilhas preenchidas e _notebooks_ ou scripts de análise estatística); e (v) uma breve **guia de replicação** descrevendo como adaptar o experimento a outras turmas, instituições ou tecnologias, preferindo soluções _open source_ sempre que possível.

---

## 19. Plano de comunicação

### 19.1 Públicos e mensagens-chave pré-execução

Principais públicos e mensagens:

- **Coordenação da disciplina/curso:** objetivos gerais do experimento, cronograma previsto e eventuais impactos em aulas ou avaliações.
- **Estudantes participantes:** propósito da atividade, caráter voluntário, forma de uso dos dados e datas aproximadas das sessões.
- **Equipe de infraestrutura de TI (se aplicável):** necessidades de laboratório, rede e serviços (API de teste, repositórios) e janelas de uso previstas.
- **Instâncias éticas/administrativas (quando houver):** descrição sucinta do experimento, riscos mínimos envolvidos e garantias de privacidade e consentimento.

### 19.2 Canais e frequência de comunicação

Serão utilizados principalmente: (i) **reuniões e e-mails formais** entre professor orientador e coordenação para aprovação de plano e cronograma; (ii) **avisos em sala e no ambiente virtual da disciplina** (por exemplo, Moodle ou ferramenta equivalente) para informar estudantes sobre a atividade, datas e instruções; e (iii) comunicação direta com a infraestrutura de TI por e-mail ou sistema interno de chamados, com antecedência mínima de algumas semanas. Reforços de comunicação com estudantes ocorrerão na semana anterior e no dia da atividade.

### 19.3 Pontos de comunicação obrigatórios

Serão considerados pontos obrigatórios de comunicação: (i) **aprovação do plano** pela coordenação e, quando aplicável, por instância ética; (ii) **anúncio oficial aos estudantes** da realização do experimento, com explicitação de voluntariedade; (iii) **comunicação de mudanças relevantes** de datas, escopo ou formato da atividade; (iv) **adiamentos ou cancelamentos** de sessões previamente agendadas; e (v) **divulgação posterior de resultados agregados** para estudantes e coordenação, preservando anonimato individual.

---

## 20. Critérios de prontidão para execução (Definition of Ready)

### 20.1 Checklist de prontidão (itens que devem estar completos)

Antes da execução nas turmas, devem estar concluídos e verificados, no mínimo:

- Plano de experimento revisado e aprovado pelo professor orientador (e, quando aplicável, por instância ética/administrativa).
- API de teste, especificação OpenAPI, projeto base do cliente, suíte de testes e instrumentos (questionários, checklists, planilhas) em versões estáveis.
- Ambiente de laboratório/virtual preparado e testado, com OpenAPI Generator, IDE, repositórios e permissões funcionando adequadamente.
- Materiais de comunicação preparados e enviados (coordenação informada, estudantes avisados sobre a atividade e orientações de participação).
- Agenda confirmada com coordenação da disciplina e equipe de infraestrutura, incluindo janelas de uso de laboratório e serviços.

### 20.2 Aprovações finais para iniciar a operação

O início da execução ficará condicionado ao **“ok final”** do professor orientador, que confirmará o atendimento ao checklist da Seção 20.1. Quando aplicável, também será necessária confirmação da coordenação da disciplina (sobre datas e uso de laboratório) e de instância ética/administrativa (sobre aprovação ou dispensa formal). Esses aceites poderão ser registrados por e-mail ou em ata/resumo de reunião, arquivados no mesmo repositório deste plano.

---

## Referências

LERCHER, A.; MACHO, C.; BAUER, T.; PINZGER, M. Microservice API Evolution in Practice: A Study on Strategies and Challenges. 2024. Disponível em: <https://arxiv.org/abs/2311.08175>. Acesso em: 23 nov. 2025.

LERCHER, A.; MACHO, C.; BAUER, T.; PINZGER, M. Generating Accurate OpenAPI Descriptions from Java Source Code. 2024. Disponível em: <https://arxiv.org/html/2410.23873v1>. Acesso em: 23 nov. 2025.
