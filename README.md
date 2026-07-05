# Algoritmos e Programação — UNA (2026/2)

Site da disciplina construído com **MkDocs Material** e publicado no **GitHub Pages**.

🌐 **Site:** https://danhpaiva.github.io/una-algprog-mkdocs-202602

## 🚀 Rodando localmente

```bash
python -m venv venv
.\venv\Scripts\activate      # Windows
# source venv/bin/activate   # Linux/Mac
pip install -r requirements.txt
mkdocs serve
```

Acesse `http://127.0.0.1:8000`. Para validar como no CI, use `mkdocs build --strict`.

## 📦 Publicação (GitHub Pages)

O deploy é automático via GitHub Actions (`.github/workflows/ci.yml`):

- **Somente a branch `main` publica** em produção. A branch `develop` apenas
  valida o build (`mkdocs build --strict`), sem publicar.
- O workflow é dividido em dois jobs (`build` e `deploy`), o que evita o erro
  *"Multiple artifacts named github-pages"* ao re-executar o deploy.

> [!IMPORTANT]
> **Configuração obrigatória (uma vez por repositório):**
> em **Settings → Pages → Build and deployment → Source**, escolha
> **"GitHub Actions"** — **não** use *"Deploy from a branch"*.
> Esta é a causa mais comum do erro *"Deployment failed, try again later"*.

Também confira em **Settings → Actions → General → Workflow permissions** se está
marcado **"Read and write permissions"**.

## 🗂️ Estrutura

```text
docs/
├── index.md         # Página inicial e cronograma
├── aulas/           # Conteúdo das aulas
├── listas/          # Listas de exercícios
└── setup.md         # Guia do professor
mkdocs.yml           # Configuração do site
requirements.txt     # Dependências (pinadas)
```
