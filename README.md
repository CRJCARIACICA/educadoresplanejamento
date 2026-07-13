# Aplicativo de Acompanhamento dos Educadores — CRJ Cariacica

Aplicativo web estático para planejamento, acompanhamento, execução, evidências, instrumentais, relatórios e metas das ações do CRJ Cariacica.

## Estrutura recomendada

- **Repositório público de código:** `CRJCARIACICA/educadoresplanejamento`
  - Hospeda o aplicativo no GitHub Pages.
  - Contém apenas `index.html`, documentação e arquivos visuais sem dados pessoais.
- **Repositório privado de dados:** `CRJCARIACICA/educadoresplanejamento-dados`
  - Guarda o arquivo `dados/backup-oficial.json` versionado pelo GitHub.
  - Não deve ser publicado no GitHub Pages.

## Publicação

1. Envie `index.html`, `.nojekyll`, `README.md` e a pasta `docs` para a branch `main` do repositório público.
2. Abra **Settings > Pages**.
3. Em **Build and deployment**, escolha **Deploy from a branch**.
4. Selecione `main` e `/(root)`.
5. Salve e aguarde a publicação.

O endereço padrão será:

`https://crjcariacica.github.io/educadoresplanejamento/`

## Sincronização entre dispositivos

O aplicativo usa `LocalStorage` para funcionar rapidamente e sem servidor. Para sincronizar:

1. Crie o repositório privado `educadoresplanejamento-dados`.
2. Crie um token fine-grained com acesso somente a esse repositório e permissão **Contents: Read and write**.
3. No aplicativo, abra **Banco de Dados / Backup > Sincronização entre dispositivos pelo GitHub**.
4. Informe repositório, branch, caminho e token.
5. Use **Enviar dados para o GitHub** após trabalhar em um dispositivo.
6. No outro dispositivo, use **Baixar dados do GitHub** antes de começar.

O token fica somente na sessão da aba e não é incluído no código nem no arquivo de backup.

## Segurança

O GitHub Pages é um site público. Nunca coloque listas de presença, contatos, documentos pessoais ou cadastros de jovens no repositório público do aplicativo. Use exclusivamente o repositório privado de dados e limite o token ao menor nível de permissão possível.
