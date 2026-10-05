# Animação de Loading gov.br para Typebot

Animação de validação de dados com temática do gov.br, otimizada para embed mobile no Typebot.

## Funcionalidades

- **Fase 1 (6 segundos)**: Spinner circular com "Confirmando dados..." e barra de progresso
- **Fase 2 (permanente)**: Ícone de check verde com "Dados validados com sucesso!"
- Não retorna ao estado inicial após completar
- Design responsivo otimizado para mobile
- Cores oficiais do gov.br (azul, amarelo, verde, vermelho)

## Deploy no Railway

### Opção 1: Via GitHub

1. Faça upload deste projeto para um repositório GitHub
2. Acesse [railway.app](https://railway.app)
3. Clique em "New Project" > "Deploy from GitHub repo"
4. Selecione o repositório
5. O Railway detectará automaticamente o Node.js e fará o deploy
6. Após o deploy, copie a URL gerada

### Opção 2: Via Railway CLI

```bash
# Instalar Railway CLI
npm install -g @railway/cli

# Login
railway login

# Criar novo projeto
railway init

# Deploy
railway up
```

## Usar no Typebot

Após obter a URL do Railway, use no Typebot como embed:

### Opção 1: Bloco de Embed
1. Adicione um bloco "Embed" no Typebot
2. Cole a URL do Railway
3. Configure as dimensões (recomendado: 320x400px)

### Opção 2: Bloco de Imagem/Mídia
1. Use um bloco de texto com HTML customizado
2. Adicione um iframe:
```html
<iframe src="SUA_URL_RAILWAY" width="100%" height="300" frameborder="0"></iframe>
```

## Personalização

Você pode ajustar os seguintes parâmetros no arquivo `index.html`:

- **Tempo de loading**: Altere `LOADING_TIME` (em milissegundos)
- **Cores**: Modifique as variáveis CSS no início do arquivo
- **Textos**: Altere as mensagens no HTML e JavaScript

## Estrutura do Projeto

```
govbr-loading-animation/
├── index.html      # Página principal com animação
├── server.js       # Servidor Express
├── package.json    # Dependências Node.js
├── Procfile        # Configuração Railway
└── README.md       # Este arquivo
```

## Licença

Este projeto é de uso livre para fins governamentais e educacionais.
