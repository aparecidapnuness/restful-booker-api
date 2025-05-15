# restful-booker-api

Este repositório contém testes automatizados da API [Restful Booker](https://restful-booker.herokuapp.com/) utilizando o Postman e o Newman, com integração ao GitHub Actions.

## 🧪 Ferramentas utilizadas

- [Postman](https://www.postman.com/)
- [Newman](https://www.npmjs.com/package/newman)
- [Newman Reporter HTML Extra](https://www.npmjs.com/package/newman-reporter-htmlextra)
- [GitHub Actions](https://docs.github.com/pt/actions)

## 📂 Estrutura

restful-booker-api/
├── restful-booker.postman_collection.json
├── restful-booker_test.postman_environment.json
├── .github/
│ └── workflows/
│ └── newman.yml
└── testArtifacts/
└── report.html (gerado automaticamente)

yaml
Copiar código

## 🚀 Como funciona

Sempre que um push for feito na branch `main`, o GitHub Actions executa:

1. Instala o Newman e o reporter HTML Extra.
2. Executa os testes da collection Postman.
3. Gera um relatório HTML no diretório `testArtifacts/`.
4. Faz o upload do relatório como artefato da execução.

## 📄 Relatório de Testes

Você pode visualizar o relatório acessando a aba **Actions** no GitHub, clicando na execução mais recente e baixando o artefato chamado **Report**. O arquivo gerado estará em HTML e mostrará o resultado detalhado dos testes.

## ✅ Exemplo de execução esperada

Todos os testes devem retornar status 200 ou 201, e os dados devem ser validados conforme os scripts definidos na collection Postman.

---

Feito com 💙 por [Aparecida Nunes]
