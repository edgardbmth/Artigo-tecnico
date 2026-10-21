# 🚀 Normalização de Banco de Dados: Garantindo Integridade e Consistência

Página web e artigo técnico desenvolvidos para a disciplina de **Modelagem de Banco de Dados** (Braz Cubas)[cite: 1]. O projeto aborda o processo sistemático de normalização de dados, eliminação de redundâncias e aplicação das Formas Normais (1FN, 2FN e 3FN) para evitar anomalias em sistemas relacionais.

📍 **URL da Página Publicada:** [https://jbettuz211.github.io/desnormalizacao-db](https://edgardbmth.github.io/Artigo-tecnico/)

---

## 👥 Autores

| Foto | Nome | Curso / Semestre | Links |
| :---: | :--- | :--- | :---: |
| <img src="https://github.com/jbettuz211.png" width="60" style="border-radius:50%"> | **José Bettuz** | ADS — 2º Semestre | [<img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white"/>](https://github.com/jbettuz211) |
| <img src="https://github.com/higorsantos23.png" width="60" style="border-radius:50%"> | **Higor Aparecido** | Ciência da Computação — 2º Semestre | [<img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white"/>](https://github.com/higorsantos23) [<img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white"/>](https://www.linkedin.com/in/higor-santos-a86048246/) |
| <img src="https://github.com/edgardbmth.png" width="60" style="border-radius:50%"> | **Edgard Aparecido** | Ciência da Computação — 1º Semestre | [<img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white"/>](https://github.com/edgardbmth) [<img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white"/>](https://www.linkedin.com/in/edgard-figueiredo-91397b225/?isSelfProfile=true) |
| <img src="https://github.com/adrianomuniz410-sketch.png" width="60" style="border-radius:50%"> | **Adriano Muniz** | ADS — 1º Semestre | [<img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white"/>](https://github.com/adrianomuniz410-sketch) [<img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white"/>](https://linkedin.com) |

---

## 📌 Quadro de Observação e Decisões do Projeto

### Referências Analisadas
1. **Fundamentos de Modelagem Relacional:** Estudo das regras de Codd e das dependências funcionais aplicadas a projetos transacionais (OLTP).
2. **Literatura Acadêmica de Banco de Dados:** Análise do impacto prático de tabelas não normalizadas na integridade e surgimento de anomalias de escrita.

### Decisões do Grupo
- **Decisão 1:** Adotamos o PostgreSQL para exemplificar a modelagem relacional restrita e a aplicação de chaves primárias e estrangeiras.
- **Decisão 2:** Focamos a estruturação didática nas três primeiras formas normais (1FN, 2FN e 3FN) acompanhadas de exemplos práticos de código SQL.

---

## 🛠️ Como Rodar os Scripts SQL Localmente

### Pré-requisitos
- **PostgreSQL** instalado (v15 ou superior).
- Um cliente SQL (DBeaver, pgAdmin ou terminal `psql`).

### Passo a Passo
1. Clone o repositório em sua máquina:
   ```bash
   git clone [https://github.com/edgardbmth/Artigo-tecnico.git](https://github.com/edgardbmth/Artigo-tecnico.git)
   cd Artigo-tecnico
