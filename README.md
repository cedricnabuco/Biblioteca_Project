# Biblioteca_Project
Projeto de app de biblioteca. Desenvolvido para a disciplina Engenharia de Software.

Aplicativo pessoal para cadastro e avaliação da minha biblioteca de livros, com geração de gráficos sobre autores, editoras e gêneros. Uso individual, single-device (celular, via navegador/PWA).

## Objetivo

- Cadastrar livros da biblioteca pessoal, com avaliação (nota) e anotações
- Buscar dados do livro automaticamente via ISBN (capa, autor, editora, data de publicação)
- Importar uma planilha Excel existente para popular o banco
- Exportar um novo Excel a partir dos dados atualizados no app
- Gerar gráficos e estatísticas (autores, editoras, gêneros, progresso de leitura)
- Acessar pelo celular como se fosse um app (PWA), sem depender de servidores externos

## Stack

| Camada | Tecnologia |
|---|---|
| Linguagem | Python |
| Banco de dados | SQLite (`sqlite3`) |
| Interface | Flask |
| Excel | `pandas` + `openpyxl` |
| Dados externos de livros | Google Books API / Open Library |
| Requisições HTTP | `requests` |
| Gráficos | `matplotlib` ou `plotly` |
| Experiência mobile | PWA (manifest.json + "Adicionar à Tela de Início" no iOS) |

## Funcionalidades

- [ ] Cadastro de livro (título, autor, editora, gênero, ISBN)
- [ ] Avaliação (nota) e anotações pessoais
- [ ] Busca automática de dados via ISBN (capa, data de publicação, etc.)
- [ ] Importação de planilha Excel existente
- [ ] Exportação de planilha Excel atualizada
- [ ] Gráficos: livros por autor, por editora, por gênero
- [ ] Interface web acessível pelo celular (mesma rede Wi-Fi)

## Plano de desenvolvimento (blocos)

- [x] **Bloco 0** — Preparação do ambiente (Python, venv, editor)
- [ ] **Bloco 1** — Schema do banco de dados (tabelas e relações)
- [ ] **Bloco 2** — CRUD via terminal (sem interface)
- [ ] **Bloco 3** — Integração com API externa de livros (busca por ISBN)
- [ ] **Bloco 4** — Importação/exportação de Excel
- [ ] **Bloco 5** — Interface web (Flask)
- [ ] **Bloco 6** — Gráficos e estatísticas
- [ ] **Bloco 7** — Experiência tipo app (PWA para iOS)

## Estrutura do projeto

```
Biblioteca_Project/
├── src/            # código do app (schema, CRUD, etc. — a partir do Bloco 1)
├── venv/           # ambiente virtual (ignorado pelo git)
├── requirements.txt
├── .gitignore
└── README.md
```

O código do projeto fica na pasta `src/` (pacote Python).

## Dependências

As dependências são instaladas **por bloco**, conforme cada etapa precisa delas,
e o `requirements.txt` é atualizado à medida que novas libs entram. O Bloco 1
usa apenas `sqlite3`, que já vem embutido no Python, então nenhuma instalação
extra é necessária ainda.

## Estrutura do banco (visão inicial)

Tabelas previstas: `livros`, `autores`, `editoras`, `generos`, `anotacoes`.
Relações e campos exatos a definir no Bloco 1.

## Observações

- Projeto de aprendizado: prioridade em entender cada peça antes de avançar, não em velocidade.
- Cada bloco é desenvolvido e testado isoladamente antes de integrar ao restante.
