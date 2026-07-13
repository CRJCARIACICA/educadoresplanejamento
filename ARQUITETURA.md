# Arquitetura da hospedagem

## Camada pública

O GitHub Pages publica os arquivos estáticos do repositório `CRJCARIACICA/educadoresplanejamento`.

Arquivos principais:

- `index.html`: aplicativo
- `sync.html`: portal de sincronização
- `.nojekyll`: publicação direta dos arquivos
- `README.md`: instruções gerais
- `docs/SINCRONIZACAO.md`: procedimento operacional

## Camada privada de dados

Os dados ficam em um segundo repositório privado e não são publicados no GitHub Pages.

Caminho recomendado:

- Repositório: `CRJCARIACICA/educadoresplanejamento-dados`
- Branch: `main`
- Arquivo: `dados/backup-oficial.json`

## Persistência

O aplicativo continua usando LocalStorage para operação local. O portal `sync.html` captura o LocalStorage, converte-o em JSON e envia o arquivo ao repositório privado pela API de conteúdos do GitHub. No outro dispositivo, o mesmo portal baixa e restaura o JSON.

## Limite importante

Não há edição simultânea nem mesclagem automática de registros. A rotina correta é baixar antes de editar e enviar ao terminar.