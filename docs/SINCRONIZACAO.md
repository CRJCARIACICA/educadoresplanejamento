# Sincronização entre dispositivos

## Princípio

O GitHub Pages hospeda somente o código estático do aplicativo. Os dados operacionais devem ficar em outro repositório privado, em um arquivo JSON versionado.

## Estrutura

- Código público: `CRJCARIACICA/educadoresplanejamento`
- Dados privados: `CRJCARIACICA/educadoresplanejamento-dados`
- Backup: `dados/backup-oficial.json`
- Portal: `sync.html`

## Uso diário

1. No primeiro dispositivo, abra `sync.html`.
2. Trabalhe no aplicativo incorporado.
3. Ao terminar, clique em **Enviar para o GitHub**.
4. No segundo dispositivo, abra `sync.html`.
5. Antes de editar, clique em **Baixar do GitHub**.
6. Após terminar, envie novamente.

## Token

Crie um token fine-grained restrito ao repositório privado de dados, com permissão `Contents: Read and write`. O token deve ser digitado em cada dispositivo e não pode ser colocado dentro do arquivo HTML ou enviado ao repositório.

## Conflitos

Evite editar simultaneamente em dois dispositivos. O fluxo é manual e segue a regra: baixar antes de começar e enviar ao terminar. O histórico de commits do arquivo JSON permite recuperar versões anteriores.

## Dados pessoais

O GitHub Pages é público. Cadastros de jovens, contatos, listas de presença, fotografias, avaliações e demais informações pessoais ou sensíveis nunca devem ser incluídos no repositório público do código.