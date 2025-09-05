# Template de Testes de API com Postman

Um template leve para projetos de testes de API usando **Postman** e **Newman**.  
Fornece uma estrutura de pastas organizada para começar, executar e compartilhar testes automatizados rapidamente.

---

## Estrutura do projeto

- `.github/workflows/` – exemplos de workflows GitHub Actions
- `collections/` – armazena as collections do Postman com todos os scripts de pré-requisição e testes incluídos.
- `docs/` – documentação adicional, screenshots ou notas relacionadas aos testes de API.
- `environments/` – armazena os arquivos de ambiente do Postman (dev, staging, prod, etc.).
- `reports/` – pasta de saída para relatórios gerados pelo Newman (HTML, JSON, etc.).

---

## Como usar

## Como usar

1. **Clone o repositório**

```bash
git clone https://github.com/seuusuario/postman-api-tests-template.git
cd postman-api-tests-template
```

2. **Instale Newman e o reporter HTML**

```bash
npm install -g newman newman-reporter-html
```

3. **Adicione sua collection do Postman**

- Copie sua collection para a pasta `collections/`.
- Se houver environment, coloque em `environments/` (opcional).

4. **Execute os testes localmente**

```bash
mkdir -p reports
newman run "collections/sua_collection.json" \
  -r cli,html \
  --reporter-html-export "reports/report.html"
```

- Os relatórios HTML serão gerados na pasta `reports/`.

5. **(Opcional) Configure GitHub Actions**

- Suba o workflow `.github/workflows/api-tests.yml`.
- Ajuste o nome da collection e environment.
- Use secrets para variáveis sensíveis, se necessário.

