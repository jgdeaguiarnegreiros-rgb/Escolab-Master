# Ecoleta

Aplicação Node.js/Express para cadastrar e pesquisar pontos de coleta de resíduos.

## Requisitos

- Node.js 20.17 ou superior
- npm

## Instalação e execução

```sh
npm ci
npm start
```

O servidor escuta a porta `3000` por padrão. Configure `PORT` para alterá-la. O
banco SQLite de runtime é `src/database/ecoleta.sqlite`; `DATABASE_PATH` pode
apontar para outro arquivo SQLite. A inicialização verifica o arquivo e cria a
tabela `places` somente quando necessário. O arquivo legado
`src/database/database.db` é preservado e não é substituído automaticamente;
faça backup e recupere-o separadamente antes de reutilizá-lo.

Abra `http://localhost:3000`. O fluxo permite pesquisar pontos por cidade,
cadastrar um ponto e consultar os resultados. O formulário de cadastro usa a
API de localidades do IBGE para carregar estados e cidades.

## Segurança

Consulte [SECURITY.md](SECURITY.md) para limitações e orientação de reporte.
