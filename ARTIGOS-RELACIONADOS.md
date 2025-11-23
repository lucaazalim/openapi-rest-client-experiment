# 1. _Microservice API Evolution in Practice: A Study on Strategies and Challenges_

### **Autores**

Lercher, A.; Macho, C.; Bauer, T.; Pinzger, M.

### **Abstract**

> “Nowadays, many companies design and develop their software systems as a set of loosely coupled microservices that communicate via their Application Programming Interfaces (APIs). While the loose coupling improves maintainability, scalability, and fault tolerance, it poses new challenges to the API evolution process. Related works identified communication and integration as major API evolution challenges but did not provide the underlying reasons and research directions to mitigate them. In this paper, we aim to identify microservice API evolution strategies and challenges in practice and gain a broader perspective of their relationships. We conducted 17 semi-structured interviews with developers, architects, and managers in 11 companies and analysed the interviews with open coding used in grounded theory. In total, we identified six strategies and six challenges for REpresentational State Transfer (REST) and event-driven communication via message brokers. The strategies mainly focus on API backward compatibility, versioning, and close collaboration between teams. The challenges include change impact analysis efforts, ineffective communication of changes, and consumer reliance on outdated versions, leading to API design degradation. We defined two important problems in microservice API evolution resulting from the challenges and their coping strategies: tight organisational coupling and consumer lock-in. To mitigate these two problems, we propose automating the change impact analysis and investigating effective communication of changes as open research directions.”

### **Citação em ABNT**

LERCHER, A.; MACHO, C.; BAUER, T.; PINZGER, M. _Microservice API Evolution in Practice: A Study on Strategies and Challenges._ 2024. Disponível em: [https://arxiv.org/abs/2311.08175](https://arxiv.org/abs/2311.08175). Acesso em: 23 nov. 2025.

---

# 2. _Generating Accurate OpenAPI Descriptions from Java Source Code_

### **Autores**

Lercher, A.; Macho, C.; Bauer, T.; Pinzger, M.

### **Abstract**

> “Developers require accurate descriptions of REpresentational State Transfer (REST) Application Programming Interfaces (APIs) for a successful interaction between web services. The OpenAPI Specification (OAS) has become the de facto standard for documenting REST APIs. Manually creating an OpenAPI description is time-consuming and error-prone, and therefore several approaches were proposed to automatically generate them from bytecode or runtime information. In this paper, we first study three state-of-the-art approaches, Respector, Prophet, and springdoc-openapi, and present and discuss their shortcomings. Next, we introduce AutoOAS, our approach addressing these shortcomings to generate accurate OpenAPI descriptions. It detects exposed REST endpoint paths, corresponding HTTP methods, HTTP response codes, and the data models of request parameters and responses directly from Java source code. We evaluated AutoOAS on seven real-world Spring Boot projects and compared its performance with the three state-of-the-art approaches. Based on a manually created ground truth, AutoOAS achieved the highest precision and recall when identifying REST endpoint paths, HTTP methods, parameters, and responses. It outperformed the second-best approach, Respector, with a 39% higher precision and 35% higher recall when identifying parameters and a 29% higher precision and 11% higher recall when identifying responses. Furthermore, AutoOAS is the only approach that handles configuration profiles, and it provided the most accurate and detailed description of the data models that were used in the REST APIs.”

### **Citação em ABNT**

LERCHER, A.; MACHO, C.; BAUER, T.; PINZGER, M. _Generating Accurate OpenAPI Descriptions from Java Source Code._ 2024. Disponível em: [https://arxiv.org/html/2410.23873v1](https://arxiv.org/html/2410.23873v1). Acesso em: 23 nov. 2025.
