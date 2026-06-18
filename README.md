#  Painel de Monitoramento de Voos – SIROS + Supabase

##  Sobre o Projeto e LINKS

Este projeto foi desenvolvido como atividade avaliativa da disciplina, com o objetivo de implementar um pipeline de dados completo utilizando **GitHub Actions**, **Supabase** e **GitHub Pages**.

O sistema realiza a coleta automática de informações de voos através da API pública do **SIROS/ANAC**, processa os dados e os armazena em um banco de dados hospedado no Supabase. Em seguida, os dados são disponibilizados em um painel web publicado pelo GitHub Pages.

SIROS API | Online Dashboard (GitHub Pages):
 
https://sn-2026-murilosc.github.io/1-A-A-2Tri-MuriloSouzaC/

SIROS API | Online Dashboard (Vercel)

https://sirosdashboard.vercel.app/

Repositório:

https://github.com/SN-2026-MuriloSC/1-A-A-2Tri-MuriloSouzaC

---

##  Tecnologias Utilizadas

* Python 3.12
* GitHub Actions
* GitHub Pages
* Supabase
* PostgreSQL
* HTML, CSS e JavaScript
* API SIROS/ANAC

---

##  Funcionalidades

* Consulta automática de voos da API SIROS.
* Filtragem por aeroportos configurados.
* Armazenamento dos dados no Supabase.
* Atualização automática através do GitHub Actions.
* Painel web para visualização de chegadas e partidas.
* Consulta por aeroporto, data, companhia aérea e tipo de operação.
* Exibição de horários, aeronaves, assentos e origem/destino dos voos.

---

##  Arquitetura do Projeto

```text
API SIROS/ANAC
       ↓
GitHub Actions
       ↓
Supabase (PostgreSQL)
       ↓
GitHub Pages
       ↓
Painel Web
```

---

##  Estrutura do Repositório

```text
.github/workflows/
├── update-flights.yml

scripts/
├── fetch_flights.py

data/
├── airports.json

index.html
README.md
```

---

## Segurança

As credenciais sensíveis foram armazenadas utilizando os recursos de segurança do GitHub:

* `SUPABASE_URL` → GitHub Secrets
* `SUPABASE_SERVICE_KEY` → GitHub Secrets

A chave **service_role** não está presente no código público do projeto.

---

##  Utilização de Inteligência Artificial

Durante o desenvolvimento deste projeto foi utilizada a ferramenta **ChatGPT (OpenAI)** como apoio para:

* Correção de erros de configuração;
* Identificação de problemas no GitHub Actions;
* Auxílio na integração entre GitHub, Supabase e API SIROS;
* Revisão e organização do código;
* Documentação do projeto.

A IA foi utilizada como ferramenta de apoio ao aprendizado e desenvolvimento, sendo todas as decisões finais, testes e validações realizadas pelo aluno.

---


