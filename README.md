# SmartPass 9.2v
Plataforma digital desenvolvida para substituir o controle analógico de saída de alunos em sala de aula. O sistema permite o monitoramento em tempo real do fluxo escolar e gera dados estruturados sobre o comportamento dos alunos, auxiliando na tomada de decisões estratégicas e na identificação de padrões atípicos de ausência em sala

# 🏫 SmartPass: Sistema Digital de Fluxo Escolar & Data Analytics

![SmartPass](https://img.shields.io/badge/Status-Em_Produção-success)
![Data Science](https://img.shields.io/badge/Foco-Ciência_de_Dados-blue)
![AI Assisted](https://img.shields.io/badge/Desenvolvimento-IA_Assistida-purple)

## 🎯 O Problema
No ambiente escolar, o controle de saída de alunos para banheiros, bebedouros ou coordenação costuma ser feito de forma analógica (crachás físicos ou anotações). Isso gera desorganização, perda de tempo de aula e, principalmente, uma total ausência de dados sobre o comportamento e a rotina dos estudantes fora da sala de aula.

## 💡 A Solução
Desenvolvido para solucionar uma dor real do chão da escola, o **SmartPass** é um sistema digital projetado para modernizar e monitorar o fluxo de estudantes. Ele substitui o modelo analógico por uma interface digital rápida rodando em tablets nas salas de aula, permitindo que a gestão e os professores tenham controle em tempo real de quem está fora de sala, bloqueando saídas em horários indevidos e criando filas de espera automáticas.

## 📊 Foco em Dados (Data Science & Analytics)
Mais do que um controlador de portas, o SmartPass atua como um gerador primário de dados para a inteligência da gestão escolar. Através dele, é possível responder a perguntas de negócio educacionais:
* **Mapeamento de Picos:** Identificação de horários de maior fluxo nos corredores.
* **Análise Comportamental:** Rastreamento de padrões de saídas recorrentes de alunos específicos, servindo de alerta precoce para a coordenação pedagógica (possíveis questões de saúde, evasão de rotina ou necessidade de intervenção).
* **Eficiência de Tempo:** Mensuração do tempo médio gasto fora de sala por aluno, turma e disciplina.

---

## 🛠️ Arquitetura e Tecnologias Utilizadas

Este projeto foi construído focando em performance, acessibilidade e baixo custo de infraestrutura, utilizando uma arquitetura *Serverless* (sem servidor dedicado) para armazenamento e estruturação de dados.

### Front-end & UI (Interface do Usuário)
* **HTML5 & CSS3 Vanilla:** Estruturação da interface sem uso de frameworks pesados, garantindo carregamento instantâneo no hardware da escola.
* **CSS Flexbox & Grid:** Utilizados para criar um layout responsivo e dinâmico, adaptando a lista de alunos perfeitamente à tela.
* **Single Page Application (SPA) Logic:** A navegação entre as telas (Login, Setup, Principal, Ocupado) é feita via manipulação de DOM (`display: none` / `flex`), criando uma experiência fluida de aplicativo nativo.
* **Otimização Touch:** Uso de `100dvh` e bloqueio de zoom/seleção (`user-select: none`, `touch-action: manipulation`) para estabilidade em tablets (iOS/Android).

### Lógica e Controle de Estado
* **JavaScript (ES6+):** Toda a regra de negócio roda de forma ágil no *Client-side*.
* **Algoritmos de Validação Curricular:** Lógicas de tempo que cruzam a hora atual com a grade curricular, bloqueando saídas automaticamente em horários críticos (ex: 1º horário e pós-intervalo).
* **Gerenciamento de Fila (Queueing):** Implementação de filas em array para gerenciar alunos que solicitam saída enquanto o sistema está ocupado.
* **Timers Assíncronos:** Uso de `setInterval` para monitoramento do tempo fora de sala e disparos de alertas visuais após 8 minutos.

### Back-end & Banco de Dados (Data Pipeline)
* **Google Apps Script (GAS):** Atua como o endpoint da API RESTful (recebendo requisições POST via a função `fetch` do JavaScript).
* **Google Sheets (Data Lake):** Utilizado como banco de dados NoSQL leve. Todos os eventos de saída (aluno, motivo, hora, duração e aula atual) são estruturados em JSON no front-end e enviados para a nuvem para posterior análise e extração de relatórios analíticos pela coordenação.

### Desenvolvimento & Produtividade
* **Inteligência Artificial (IA Generativa):** Utilização de IA como assistente de *Pair Programming* para acelerar o desenvolvimento (Rapid Prototyping). A IA foi fundamental para otimizar funções complexas em JavaScript, refatorar o código para melhor performance em dispositivos móveis e estruturar rapidamente o banco de dados local em formato JSON (processamento das grandes matrizes com a grade curricular e a lista de alunos de dezenas de turmas).

---

## 📸 Demonstração da Interface
> *(DICA: Adicione aqui 2 ou 3 prints do sistema funcionando, ou um GIF gravando a tela do sistema em uso. Lembre-se de usar dados fictícios para proteger a privacidade dos alunos!)*

---

### 👨‍💻 Autor
**Danilo Andrade Matias** *Consultor de Tecnologia Educacional e Especialista em Ciência de Dados aplicada à Educação.* [LinkedIn](https://www.linkedin.com/in/seu-link-aqui) | [Portfólio/GitHub](https://github.com/seu-usuario)
