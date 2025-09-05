# Template de Testes de API com Postman

Um template leve para projetos de testes de API usando **Postman** e **Newman**.  
Fornece uma estrutura de pastas organizada para começar, executar e compartilhar testes automatizados rapidamente.

---

## Estrutura do projeto

- `collections/` – armazena as collections do Postman com todos os scripts de pré-requisição e testes incluídos.
- `environments/` – armazena os arquivos de ambiente do Postman (dev, staging, prod, etc.).
- `reports/` – pasta de saída para relatórios gerados pelo Newman (HTML, JSON, etc.).
- `docs/` – documentação adicional, screenshots ou notas relacionadas aos testes de API.

---

## Como usar

1. **Clone ou use este template** para criar um novo projeto:

```bash
git clone https://github.com/seuusuario/postman-api-tests-template.git
````

2. Importe sua collection e ambiente no Postman.

3. Ajuste quaisquer variáveis ou configurações de ambiente conforme necessário.

4. Execute os testes localmente com Newman:

```bash
newman run collections/sua_collection.json \
  -e environments/seu_ambiente.json \
  -r cli,html \
  --reporter-html-export reports/report.html
````

5. Confira os relatórios na pasta reports/.
