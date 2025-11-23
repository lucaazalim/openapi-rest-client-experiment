## 1. Tema do experimento

> **Tema:** Efeito do uso de especificações OpenAPI na produtividade e qualidade da implementação de clientes REST.

Ideia geral: comparar dois jeitos de implementar a integração com uma API REST:

- **Grupo A:** recebe apenas documentação textual da API (ex.: página HTML/PDF).
- **Grupo B:** recebe a mesma API descrita em **OpenAPI** + ferramenta de geração de cliente (OpenAPI Generator/NSwag/etc).

---

## 2. Planejamento do experimento (conteúdo para a folha A4)

Você pode organizar a folha com pequenos blocos/títulos assim:

### Título do experimento

> **Impacto do uso de OpenAPI na implementação de clientes REST**

---

### Objetivo

Avaliar se o uso de uma especificação OpenAPI, combinada com geração automática de código cliente, **reduz o tempo de implementação** e **diminui defeitos** na integração com APIs REST, em comparação ao uso apenas de documentação textual.

---

### Escopo

- APIs REST de pequeno/médio porte (ex.: CRUD de pedidos, produtos, usuários).
- Foco na **implementação do cliente** (consumo da API), não no desenvolvimento da própria API.
- Participantes: estudantes de Engenharia de Software com experiência básica em REST.

---

### Variáveis

- **Variável independente (fator):**

  - Forma de documentação/apoio:

    - Nível 1: Documentação textual tradicional.
    - Nível 2: Especificação OpenAPI + geração automática de cliente.

- **Variáveis dependentes (o que será medido):**

  1. **Tempo de conclusão** da tarefa (em minutos).
  2. **Número de defeitos** encontrados em uma suíte de testes automatizada.
  3. **Erros de contrato** (campos faltando, tipos errados, endpoints incorretos).
  4. **Percepção subjetiva de esforço** (questionário curto Likert: facilidade, clareza da documentação, confiança na integração).

- **Possíveis variáveis de controle:**

  - Linguagem de programação utilizada.
  - IDE/ambiente de desenvolvimento.
  - Nível de experiência prévia com REST (coletado em um questionário inicial).

---

### Materiais e instrumentos necessários

- 1 API REST pronta (mock ou real), com:

  - Documentação textual (ex.: Swagger UI impresso/exportado em HTML).
  - Arquivo de especificação **OpenAPI** (YAML ou JSON).

- Ferramenta de **codegen** (ex.: OpenAPI Generator, NSwag, etc).
- Computadores com IDE configurada.
- Repositório com:

  - Projeto base do cliente (sem implementação).
  - Suíte de testes automatizada para validar a integração.

- Cronômetro ou software para registrar o tempo.
- Questionários impressos ou formulário online (pré e pós-experimento).
- Planilha ou ferramenta para registrar medidas (tempo, defeitos, respostas de questionário).

---

### Pessoas envolvidas

- **Pesquisador principal:** aluno.
- **Orientador:** professor.
- **Participantes:** ~8–20 estudantes desenvolvedores (podem ser colegas de período).
- **Auxiliar/observador (opcional):** ajudar a coletar tempos e organizar os grupos.

---

### Passo a passo (procedimento)

1. **Preparação**
   1.1. Definir a API de teste e criar a especificação OpenAPI correspondente.
   1.2. Configurar o projeto base (cliente sem implementação) e a suíte de testes.
   1.3. Elaborar os questionários de perfil (experiência) e pós-uso (percepção).

2. **Seleção e divisão dos participantes**
   2.1. Convidar voluntários e aplicar questionário de perfil.
   2.2. Dividir aleatoriamente em dois grupos de tamanho semelhante:

   - Grupo A: Documentação textual.
   - Grupo B: OpenAPI + codegen.

3. **Execução da tarefa**
   3.1. Apresentar rapidamente o objetivo da atividade (sem induzir o resultado).
   3.2. Entregar a cada grupo o material correspondente.
   3.3. Solicitar que implementem a integração do cliente com a API até passar em todos os testes.
   3.4. Registrar o **tempo gasto** por cada participante.

4. **Coleta de resultados**
   4.1. Rodar a suíte de testes e contar **falhas/defeitos** por participante.
   4.2. Registrar erros de contrato específicos (mapeamento errado de campos, endpoints etc.).
   4.3. Aplicar o **questionário de percepção** de esforço e qualidade da documentação.

5. **Análise**
   5.1. Comparar média de tempo, número de defeitos e respostas de questionário entre os grupos.
   5.2. Verificar se o grupo com OpenAPI obteve resultados significativamente melhores.

---

### Tempo necessário (estimado)

- Preparação de materiais: ~1–2 semanas (fora do experimento em si).
- Execução do experimento com participantes:

  - Explicação + organização: 15–20 min.
  - Implementação da tarefa: 60–90 min.
  - Questionários finais: 10–15 min.

---

### Custo estimado

- Uso de laboratórios da universidade: custo indireto (infraestrutura já disponível).
- Softwares/ferramentas: preferencialmente **open source** ou versões comunitárias → custo zero direto.
- Possível custo de impressão de folhas (questionários, instruções): baixo.

---

### Sugestão de desenho/fluxograma para a folha

Você pode desenhar um fluxograma simples:

1. **Definir API + OpenAPI** →
2. **Dividir participantes em Grupo A / Grupo B** →
3. **Cada grupo implementa o cliente** →
4. **Rodar testes automatizados** →
5. **Aplicar questionário** →
6. **Comparar resultados (tempo, defeitos, percepção)**.
