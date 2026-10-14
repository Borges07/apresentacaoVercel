# Publicar a demonstração na Vercel

As quatro páginas, o JavaScript, o CSS e os assets originais foram preservados. O arquivo `vercel.json` na pasta externa configura a publicação estática da subpasta `projeto-recuperado`. Não precisa de React, Next.js, instalação de dependências ou build.

## Pelo painel da Vercel

1. Envie esta pasta completa para um repositório GitHub, incluindo `vercel.json` e a subpasta `projeto-recuperado`.
2. Na Vercel, escolha **Add New → Project** e importe o repositório.
3. Use **Framework Preset: Other** e **Root Directory: raiz do repositório** (a pasta que contém `vercel.json`). Não selecione a subpasta interna.
4. Deixe o comando de build vazio. O arquivo de configuração já define **Output Directory: projeto-recuperado**.
5. Clique em **Deploy**. Não são necessárias variáveis de ambiente.

## Pelo terminal, como alternativa

Na pasta externa, onde está `vercel.json`, execute:

```powershell
npx vercel
```

Siga a autenticação e a seleção de conta/projeto. Esse comando gera uma publicação de preview. Para publicar em produção depois de revisar:

```powershell
npx vercel --prod
```

## Rotas para testar

| Caminho | Tela |
| --- | --- |
| `/` | Início |
| `/acesso` | Formulário |
| `/processando` | Preparação animada |
| `/painel` | Painel completo |
| `/painel#midias` | Galeria e áudios |
| `/painel#plano` | Plano demonstrativo |

Os links originais com `.html` continuam válidos: a Vercel redireciona para a versão sem extensão. A configuração remove barras finais para manter os caminhos relativos de CSS, JavaScript e assets funcionando. Cada rota corresponde ao seu HTML; atualizar uma página ou abri-la diretamente mantém a tela correta.

## Roteiro rápido para apresentar ao cliente

1. Abra `/` e selecione uma das opções.
2. Dê um nome opcional ao painel e clique em **Abrir Demonstração Agora**.
3. Aguarde cerca de 6,5 segundos ou clique em **Pular apresentação**.
4. No painel, abra uma conversa, uma foto, os áudios e o mapa.
5. Mostre o plano, alterne os depoimentos e abra as perguntas frequentes.
6. Confira também no celular e atualize diretamente `/acesso` e `/painel` para validar a publicação.

O site mantém as funcionalidades demonstrativas existentes. Dados, depoimentos e preço continuam ilustrativos; não há backend ou pagamento integrado.

Configuração baseada na documentação oficial: https://vercel.com/docs/project-configuration/vercel-json
