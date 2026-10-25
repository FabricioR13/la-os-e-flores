# Laços e Flores — catálogo de cestas, flores e balões

Catálogo online com presentes prontos, **Monte sua cesta** (o valor vai somando a cada item),
sacola com cálculo de frete por região, pedido enviado pelo WhatsApp e painel para a loja.
Identidade visual tirada do logo do Instagram (@lacoseflores_): verde-oliva do laço, rosa da
flor e fundo rosado.

## Como abrir

### 1. Só ver funcionando — `Demonstracao.html`
Dê dois cliques. Abre no navegador com tudo funcionando, fotos incluídas no próprio arquivo.
O painel abre pelo link **Painel da loja** na faixa escura do topo (ou com `#admin` no fim do
endereço). Senha inicial: `lacos2026`.

### 2. Publicar por link — `index.html` + pasta `img`
É a mesma página, com as fotos em arquivos separados (carrega mais rápido no celular).
Suba o `index.html`, a pasta `img` e o `.nojekyll` para o GitHub Pages (ou outra hospedagem)
e mande o link para a cliente.

## O que o cliente vê

1. **Presentes prontos** — 27 produtos tirados dos posts do Instagram, com filtro por
   categoria (Cestas, Flores e plantas, Balões, Kids, Canecas) e botão **+** para a sacola.
2. **Monte sua cesta** — primeiro o cliente escolhe os itens (flores, chocolates, bebidas,
   balões e extras). Cada item ocupa alguns **espaços** (balões e cartão vão por fora e não
   ocupam). Só depois a etapa **Escolha a cesta** é liberada, mostrando apenas as cestas cuja
   capacidade comporta todos os itens — a menor que serve aparece como **Ideal**. Se o cliente
   acrescentar itens e a cesta escolhida não comportar mais, ela é desmarcada. O resumo mostra
   cada item, a ocupação da cesta e o total na hora. Ao **Confirmar cesta**, ela vai para a
   sacola, e a mensagem do WhatsApp sai com a cesta e todos os itens agrupados por tipo,
   quantidades, valores e ocupação.
3. **Sacola** — muda quantidades, escolhe **entrega** (região → frete entra no total) ou
   **retirada na loja** (sem frete), data e período, nome de quem recebe, mensagem do cartão,
   dados e forma de pagamento.
4. **Finalizar pelo WhatsApp** — o pedido é registrado e o cliente vai para o WhatsApp da loja
   com a mensagem pronta (itens, componentes da cesta montada, frete, total, cartão).
   Nada é pago no site.

## Painel — `#admin`

- **Resumo**: entradas, saídas e saldo do mês, valor a receber, próximas entregas.
- **Pedidos**: em aberto / todos / entregues / cancelados / calendário do mês; mudar situação
  (novo, confirmado, em produção, saiu para entrega, entregue, cancelado), dar desconto,
  registrar pagamento (vira entrada no financeiro), chamar o cliente no WhatsApp e cadastrar
  **pedido manual** (encomenda feita pelo direct, telefone ou balcão).
- **Presentes prontos**: criar, editar, trocar foto (o celular reduz a foto sozinho), preço,
  categoria, destaque “Mais pedido”, ocultar do catálogo, criar categorias.
- **Monte sua cesta**: itens, preços e **espaço que cada item ocupa**; cestas com preço e
  **capacidade**; desmarcar “No site” esconde o que acabou.
- **Fretes**: regiões/cidades e valores; ligar ou desligar a retirada na loja.
- **Entradas e saídas**: lançamentos por mês.
- **Configurações**: WhatsApp que recebe os pedidos, Instagram, endereço de retirada, horário,
  aviso de antecedência, senha do painel e **cópia de segurança** (baixar/restaurar `.json`).

## Importante: é uma demonstração

Os pedidos e as alterações do painel ficam salvos **só no navegador de quem abriu**. O pedido
de um cliente chega à loja normalmente pelo WhatsApp, mas não aparece no painel do celular da
dona. Para isso o site precisa de um banco de dados (como na versão com servidor do catálogo da
Angel) — dá para fazer quando a cliente fechar.

## Para revisar com a Laços e Flores

- **Todos os preços e fretes são fictícios** (como combinado). Ajuste no painel.
- Fretes iniciais: Triunfo Centro R$ 8, demais bairros R$ 12, Polo Petroquímico R$ 18,
  Montenegro R$ 25, São Jerônimo/Charqueadas R$ 30, Nova Santa Rita R$ 30, Canoas/Esteio
  R$ 40, Porto Alegre R$ 50.
- WhatsApp cadastrado: (51) 99646-6664 (o da bio do Instagram). Endereço de retirada em
  branco — preencher em Configurações.
- Nomes e descrições dos produtos foram escritos a partir das fotos; confira com a dona.
- As fotos são os posts inteiros recortados dos prints, sem os ícones do Instagram, ampliados
  e com nitidez ajustada. Como vêm de prints, a qualidade tem limite: fotos originais da loja
  ficam bem melhores — troque pelo painel ou substitua os arquivos da pasta `img` mantendo o
  mesmo nome.
- O logo foi reconstruído a partir do post e da foto de perfil do Instagram (no Instagram ele
  aparece cortado), com contornos limpos.
- Os espaços de cada item e a capacidade das cestas são estimativas: ajuste com a dona.
- Os prints originais continuam na pasta `WhatsApp Unknown…`; não são usados pelo site.

## Onde fica cada coisa

- `index.html` — todo o site (catálogo, Monte sua cesta, sacola e painel), em um arquivo só.
  Os dados iniciais (produtos, itens da montagem, fretes, configurações) estão no começo do
  script, em `DADOS_INICIAIS`. Se mudar esses dados no arquivo, aumente `VERSAO_DADOS`
  para os navegadores carregarem a versão nova.
- `img/` — logo (`logo.png`), emblema (`emblema.png`) e fotos dos produtos.
- `Demonstracao.html` — cópia do `index.html` com as fotos embutidas.
