# Como escrever texto científico na área de Informática

**Com base nas orientações de Lesandro Ponciano (2024)**

As diretrizes a seguir reúnem práticas amplamente aceitas em veículos científicos da área de Ciências Exatas e Computação. Ao preparar um texto para um veículo específico (conferência, periódico, simpósio etc.), sempre verifique o estilo exigido por ele.

---

## 1. Voz e estilo

- Evite **primeira pessoa do singular**. Prefira a **linguagem impessoal**:  
  _“Neste trabalho, investiga-se...”_.
- Primeira pessoa do plural é aceita, mas menos recomendada:  
  _“Neste trabalho, nós investigamos...”_.

---

## 2. Uso de termos estrangeiros

- Palavras de outros idiomas não incorporadas ao português devem estar em _itálico_.  
  Ex.: _warm-up_, _workflow_, _benchmark_.

---

## 3. Definição de siglas

- **Toda sigla deve ser definida no primeiro uso**, incluindo as muito conhecidas (IDE, API, XML).
- Nunca repita o significado por extenso após a primeira ocorrência.

---

## 4. Forma correta de apresentar siglas

- Primeiro escreva o termo por extenso, depois a sigla:  
  _Unidade Central de Processamento (UCP)_.
- Se a sigla for derivada de outro idioma, indique isso:  
  _Internet Protocol (IP, do inglês Internet Protocol)_.

---

## 5. Referências bibliográficas

- Cada tipo de publicação exige campos obrigatórios específicos (artigo, livro, link etc.).
- Siga exatamente o padrão requerido (SBC, ACM, IEEE, ABNT).
- Links devem incluir **data de acesso**.

---

## 6. Uso correto do BibTeX

- Preencha cada entrada com o tipo apropriado (`@article`, `@inproceedings` etc.).
- Garanta que todos os campos necessários estejam presentes (autor, título, ano, editora etc.).
- Se o arquivo `.bib` estiver incorreto, a referência será exibida de forma incorreta.

---

## 7. Clareza acima de estilo

- O objetivo central é **clareza e precisão**, não “escrever bonito”.
- Evite coloquialismos, frases rebuscadas e comentários vagos.
- Use termos técnicos, mas explique aqueles que não são amplamente conhecidos.

---

## 8. Evite adjetivos subjetivos

- Expressões como _“muito interessante”, “ótimo desempenho”, “extraordinário”, “bacana”_ devem ser evitadas.
- Textos científicos devem descrever, não julgar.

---

## 9. Cuidado com termos técnicos usados de forma imprecisa

- Palavras como _exponencial_, _significância_, _hipótese_, _transversal_ têm sentidos rigorosos em ciência.
- Só as utilize quando o contexto realmente corresponder ao significado técnico.

---

## 10. Uso correto de “et al.”

- “_Et al._” significa _“e outros”_.
- Usado quando há **mais de três autores** (regra pode variar pelo veículo).
- Indica que apenas o sobrenome do primeiro autor foi mantido.

---

## 11. Evite “etc.”

- O termo é impreciso e prejudica a reprodutibilidade.
- Liste explicitamente todos os elementos necessários.

---

## 12. Prefira citações indiretas

- Reescreva com suas palavras:  
  _“Há cinco perfis de engajamento [Ponciano e Brasileiro 2014]”_.
- Evite citações literais, exceto quando indispensável.

---

## 13. Como citar dentro do texto

- Indicação de autor/ano não deve interromper o fluxo textual:  
  ✔ _“Há cinco perfis [...] [Ponciano e Brasileiro 2014]”_  
  ✘ _“Segundo [Ponciano e Brasileiro, 2014] ...”_
- Também é aceitável:  
  _“Segundo Ponciano e Brasileiro (2014) ...”_.

---

## 14. Quando citar

- Sempre cite quando algo **não foi definido por você**:
  - definições formais;
  - resultados alheios;
  - motivação baseada em estudos anteriores;
  - conceitos criados por outros autores.
- Ausência de citação implica autoria sua.

---

## 15. Coerência entre citações e referências

- Todo item citado deve aparecer na lista de referências.
- Nenhum item deve aparecer na lista sem ser citado no texto.
- No LaTeX com BibTeX isso é garantido automaticamente.

---

## 16. Estruturação de seções e subseções

- Se existe a subseção **2.1**, deve existir **2.2**.
- Não crie uma seção com apenas uma subseção.

---

## 17. Construção de parágrafos

- Um parágrafo nunca deve ter apenas uma frase.
- Deve apresentar a ideia inicial e desenvolvê-la em sentenças posteriores.
- Avalie se não faz mais sentido unir parágrafos muito curtos.

---

## 18. Comprimento das frases

- Evite frases com mais de duas linhas.
- Prefira frases curtas e diretas.

---

## 19. Comprimento dos parágrafos

- Evite parágrafos muito curtos (< 4 linhas) ou muito longos (> 10 linhas).
- Ideal: **7 a 10 linhas**.

---

## 20. Regras gramaticais essenciais

- Nunca separe sujeito e verbo com vírgula:  
  ✘ _“O algoritmo, é eficiente.”_  
  ✔ _“O algoritmo é eficiente.”_
- O mesmo vale para citações no início da frase:  
  ✔ _“Almeida et al. (2020) fizeram...”_

---

## 21. Figuras, tabelas, algoritmos e equações

- Todo elemento deve ser citado no texto pelo número:  
  _“Como mostra a Figura 1...”_.
- Nenhum elemento deve aparecer sem ser referenciado.

---

## 22. Nomenclatura correta desses elementos

- São substantivos próprios:  
  _Figura 1_, _Tabela 2_, _Algoritmo 1_, _Equação 4_.

---

## 23. Tempo verbal

- Predominância do **presente**.
- Passado em algumas seções é permitido; futuro raramente é usado.
- Exemplos:
  - Introdução: _“O objetivo é investigar...”_
  - Trabalhos relacionados: _“Os trabalhos analisados apresentam...”_
  - Materiais e métodos: _“Emprega-se o algoritmo...”_

---

## 24. “Este/Neste” vs. “Esse/Nesse”

- **Este/Neste**: refere-se ao próprio trabalho ou ao que ainda será dito.
- **Esse/Nesse**: refere-se a algo já mencionado ou a outro trabalho.
- Exemplos:
  - _“Neste trabalho, investiga-se...”_
  - _“Ponciano et al. (2014) caracterizam... Nesse estudo...”_

---

## 25. Revisão após contribuições do orientador

- Certifique-se de que as alterações não criaram inconsistências.
- A responsabilidade final pelo texto é do autor.
