# Interface recuperada — Status Demo

Projeto estático em HTML, CSS e JavaScript puro, reconstruído a partir das 11 capturas fornecidas. Abra `index.html` para começar. Não é necessário instalar dependências ou executar build.

## O que foi reconstruído

Quatro páginas representam a sequência completa; as últimas capturas são trechos do mesmo painel com rolagem.

| Referência | Implementação |
| --- | --- |
| 015447 | `index.html`: cabeçalho, título, duas opções e rodapé |
| 015505 | `acesso.html`: formulário, botão, três avisos e faixa de preferência |
| 015533 e 015543 | `processando.html`: animação, progresso e log em diferentes momentos |
| 015607 | `painel.html#conversas`: faixa verde e lista de conversas |
| 015622 | `painel.html#midias`: áudios e galeria |
| 015632 | `painel.html#palavras`: palavras-chave e contadores |
| 015643 | `painel.html#locais`: mapa e botão |
| 015653 | `painel.html#plano`: plano e benefícios |
| 015707 | `painel.html`: carrossel de depoimentos e perguntas frequentes |
| 015715 | `painel.html`: perguntas, área de garantia e botão fixo |

As referências foram reproduzidas em estrutura, cores, dimensões aproximadas, espaçamento e ordem. Não há promessa de igualdade pixel a pixel: as capturas têm larguras e recortes diferentes e não fornecem fontes, DOM ou CSS originais. A fonte local de fallback é Arial. Textos, marca e fotografias foram substituídos por conteúdo demonstrativo conforme solicitado.

## Fluxo

1. Em `index.html`, escolha uma das opções; ambas levam ao formulário.
2. Em `acesso.html`, informe um nome opcional e abra a demonstração.
3. Em `processando.html`, acompanhe aproximadamente 6,5 segundos de preparação local ou use “Pular apresentação”.
4. Em `painel.html`, explore os cards e seus diálogos.

O menu das primeiras telas também oferece acesso direto às quatro páginas. No fim do painel é possível voltar ao início ou reiniciar.

## Interações incluídas

- Menu lateral com fechamento por clique, Escape e foco de teclado controlado.
- Formulário opcional com nome guardado somente na sessão do navegador.
- Preferência de aviso salva em `sessionStorage`, com fallback quando indisponível.
- Progresso animado e logs fictícios, sem qualquer chamada externa.
- Conversas de exemplo em janelas modais.
- Galeria com seis fotos locais e ampliação.
- Quatro áudios WAV sintéticos curtos para testar o componente de áudio.
- Palavras-chave e mapa ilustrativo com diálogos.
- Carrossel manual com cinco depoimentos explicitamente fictícios.
- FAQ expansível.
- CTA fixo que navega até o plano; o botão do plano apenas abre uma explicação.
- Fechamento de diálogos por botão, Escape ou clique fora; áudio interrompido ao fechar.

## Estrutura dos arquivos

| Arquivo/pasta | Função |
| --- | --- |
| `index.html` | Primeira etapa |
| `acesso.html` | Formulário demonstrativo |
| `processando.html` | Estado de preparação |
| `painel.html` | Painel completo e componentes finais |
| `styles.css` | Aparência compartilhada, tokens e regras responsivas |
| `app.js` | Ícones, componentes compartilhados e interações |
| `assets/` | Fotos, mapa, favicon e áudios locais |
| `ASSETS.md` | Origem das imagens |
| `CONTINUAR_NO_CODEX.md` | Orientação pronta para continuar o desenvolvimento |

## Personalizar

- Textos principais e ordem dos blocos: nos arquivos HTML.
- Dados das conversas, galeria e depoimentos: em `app.js`.
- Cores, largura dos cards, tipografia e espaçamento: em `styles.css`.
- O token `--stage-offset` recria a área vazia à esquerda nas referências de desktop. Use `0px` para centralizar todo o conteúdo.
- Abaixo de 1280 px a interface usa o espaço disponível; no celular a galeria passa a duas colunas. O botão fixo preserva margens laterais.
- Troque a marca demonstrativa “Status” pela marca real no componente `brand` de `app.js`.

## Desenvolvimento local opcional

Com Python instalado, execute dentro da pasta:

```sh
python -m http.server 8080
```

Depois abra `http://localhost:8080`. Também funciona abrindo `index.html` diretamente, sem servidor.

## Limites desta entrega

Esta entrega é o front-end demonstrativo. Não inclui backend, autenticação, APIs, acesso ao WhatsApp, rastreamento, pagamento ou publicação. O mapa é uma ilustração local. Os números, planos, depoimentos e mensagens são fictícios. O preço de R$ 20,00 serve apenas para preservar a composição visual do componente.

Não há dependências externas em tempo de execução: os recursos estão na pasta. O navegador pode restringir preferências de sessão ao abrir via `file://`; isso não impede a navegação.

Verificação: sintaxe JavaScript, 107 verificações de DOM/links/interações em jsdom, seis fotografias e quatro áudios íntegros. Foram verificados menu, formulário, progresso, diálogos, carrossel e referências locais. A inspeção visual em navegador não estava disponível neste ambiente; vale revisar as quatro páginas no navegador-alvo antes de integrar ao produto.
