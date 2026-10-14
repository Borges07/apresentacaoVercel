# Contexto para continuar o projeto

Este projeto reconstrói o layout de quatro etapas a partir de 11 capturas. A maior parte das capturas corresponde a seções sucessivas de `painel.html`. O objetivo é preservar o visual e usar conteúdo legítimo e demonstrativo como ponto de partida.

## Prompt sugerido

> Leia README.md, os quatro arquivos HTML, styles.css e app.js antes de alterar qualquer coisa. Use esta interface como referência visual para integrar ao meu projeto existente. Preserve cores, dimensões, espaçamentos, ordem dos blocos, responsividade e navegação. Se o repositório já usa React, Next, Vue ou outra stack, extraia componentes sem redesenhar as telas. Mantenha os dados de exemplo identificados até que exista uma fonte real autorizada. Primeiro entenda a estrutura do meu repositório e mapeie as rotas e componentes; depois conecte as funcionalidades que eu especificar. Não invente endpoints, regras comerciais, depoimentos, permissões ou integrações. Não implemente acesso não autorizado a contas de terceiros. Preços e áreas comerciais são apenas demonstrativos até serem substituídos por uma oferta real. Não publique automaticamente: a entrega inicial é local.

## Componentes sugeridos para extração

- AppHeader / Brand / NavigationDrawer / AppFooter
- ChoiceCard / AccessForm / SessionNotice
- LoadingPanel / ProgressLog
- ReportBanner / SectionCard / SectionArrow
- ConversationList / ConversationDialog
- MediaGallery / ImageDialog / AudioDialog
- KeywordList / LocationCard
- PricingCard / FloatingCTA
- TestimonialCarousel / FAQ / GuaranteeCard
- Modal

## Cuidados de implementação

- `app.js` centraliza comportamentos por `body[data-page]`.
- Textos recebidos do usuário devem continuar sendo inseridos com `textContent`, nunca interpolados em HTML.
- Os dados estáticos da demonstração não representam consultas a serviços externos.
- Ao criar backend, documente as rotas, o modelo de dados e os requisitos reais antes de substituir os mocks.
- Garanta navegação por teclado, nome acessível para controles, fechamento dos diálogos e interrupção de mídia.
- Uma mudança de texto pode mudar as quebras de linha; compare a composição após integrar à stack definitiva.
