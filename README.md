# 🚀 Desnormalização de Banco de Dados: Performance vs Consistência

Página web e artigo técnico desenvolvidos para a disciplina de **Modelagem de Banco de Dados** (Braz Cubas)[cite: 1]. O projeto aborda quando a redundância controlada de dados é a escolha certa para otimizar a performance de leitura em sistemas de alto volume[cite: 1].

📍 **URL da Página Publicada:** [https://jbettuz211.github.io/desnormalizacao-db](https://jbettuz211.github.io/desnormalizacao-db)

---

## 👥 Autores

| Foto | Nome | Curso / Semestre | Links |
| :---: | :--- | :--- | :---: |
| <img src="https://github.com/jbettuz211.png" width="60" style="border-radius:50%"> | **José Bettuz** | ADS — 2º Semestre | [<img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white"/>](https://github.com/jbettuz211) |
| <img src="https://github.com/higor-username.png" width="60" style="border-radius:50%"> | **Higor Aparecido** | ADS — 2º Semestre | [<img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white"/>](https://github.com/higor-username) [<img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white"/>](https://linkedin.com) |
| <img src="https://github.com/edgard-username.png" width="60" style="border-radius:50%"> | **Edgard Aparecido** | ADS — 2º Semestre | [<img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white"/>](https://github.com/edgard-username) [<img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white"/>](https://linkedin.com) |
| <img src="https://github.com/adriano-username.png" width="60" style="border-radius:50%"> | **Adriano Muniz** | ADS — 2º Semestre | [<img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white"/>](https://github.com/adriano-username) [<img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white"/>](https://linkedin.com) |

---

## 📌 Quadro de Observação e Decisões do Projeto

### Referências Analisadas
1. **Modern SQL:** Analisamos a comparação entre esquemas normalizados (OLTP) e esquemas achatados/desnormalizados para relatórios analíticos.
2. **Brandur (Blog Técnico):** Observamos a abordagem realista sobre o custo computacional dos `JOIN`s em grande escala e a importância de manter a consistência com *triggers* e visões materializadas.

### Decisões do Grupo
- **Decisão 1:** Escolhemos o PostgreSQL (v15+) como SGBD padrão para demonstrar o uso de **Views Materializadas** e comparar planos de execução (`EXPLAIN ANALYZE`).
- **Decisão 2:** Focamos o artigo na separação conceitual e prática entre **OLTP (Transacional)** e **OLAP (Analítico)**.
- **Decisão 3:** Implementamos o artigo em um único template limpo, responsivo e adaptável ao modo escuro via JavaScript.

### O que decidimos NÃO fazer
- **Escopo:** Decidimos não abordar as Formas Normais Iniciais (1FN, 2FN e 3FN) em profundidade, assumindo que o leitor já possui a base teórica e quer focar na otimização de leitura[cite: 1].

---

## 🛠️ Como Rodar os Scripts SQL Localmente

### Pré-requisitos
- **PostgreSQL** instalado (v15 ou superior).
- Um cliente SQL (DBeaver, pgAdmin ou `psql`).

### Passo a Passo

1. **Clonar o Repositório:**
   ```bash
   git clone [https://github.com/jbettuz211/desnormalizacao-db.git](https://github.com/jbettuz211/desnormalizacao-db.git)
   cd desnormalizacao-db
