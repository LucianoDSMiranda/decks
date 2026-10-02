# Meus Decks Pokémon TCG

Site estático para acompanhar decks, comparar versões e controlar cartas a comprar.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie `index.html` e `favicon.svg` para a raiz.
3. Abra **Settings > Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/ (root)`.
6. Salve.

O site ficará disponível em um endereço parecido com:

`https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`

## Lista de compras editável

A lista inicial contém os 11 itens (15 cartas) solicitados em 02/10/2026. Digite o nome da carta, pesquise na Liga Pokémon em outra aba e informe o número completo (ex.: 128/132), quantidade desejada e preço unitário de referência. O preço é opcional, informado pelo usuário e não é atualizado automaticamente. O total pendente considera apenas as cópias ainda não compradas e não inclui frete; cartas sem preço são indicadas à parte.

É possível editar/remover itens, registrar cópias compradas e copiar as quantidades pendentes. A busca sugere nomes presentes nos decks, mas permite qualquer carta. Os nomes são enviados à Liga somente ao abrir o link de pesquisa.

## Preservação das compras

O armazenamento da lista editável usa a chave estável `pokemonTCG_shoppingList_v1`. Não trocar essa chave nem limpar o armazenamento ao atualizar o site. A lista é salva após cada alteração; falhas de leitura bloqueiam gravações para não sobrescrever dados existentes.

Os antigos registros `pokemonTCG_buy_` ficam preservados no navegador e no backup, mas não preenchem automaticamente a nova lista. A remoção das listas fixas foi solicitada pelo usuário.

Use **Baixar backup** e **Restaurar backup** para transferir ou recuperar a lista. O backup versão 2 inclui nomes, edições, quantidades, compras e preços, além dos registros antigos. Backups versão 1 continuam aceitos para preservar os registros antigos. Restaurar o mesmo arquivo não duplica os itens: a mesclagem usa IDs estáveis, mantém edições/preços atuais para itens já existentes e preserva as maiores quantidades.

Os dados ficam no navegador e endereço usados. Arquivo local e GitHub Pages não compartilham armazenamento. Não há sincronização entre dispositivos; faça backup antes de limpar os dados do navegador ou trocar de endereço.

## Numeração das cartas

As listas exibem número/total da coleção (ex.: 128/132). O campo de compras aceita esse formato e o inclui na pesquisa da Liga. Códigos antigos conhecidos, como MEG 128, são convertidos ao carregar ou restaurar; IDs, quantidades, compras e preços são mantidos. Códigos desconhecidos ficam preservados para correção manual. A chave de armazenamento não muda.

O botão Copiar para o Live mantém sigla e número no texto exportado, conforme o formato de importação do jogo. Os links do Limitless também mantêm seus identificadores internos.

## Lista solicitada em 02/10/2026

A revisão 2026-10-02-lista-1 substitui a lista anterior uma única vez em cada navegador. A chave existente armazena agora um objeto com revision e items, gravados juntos; listas antigas em array continuam sendo lidas. Atualizações futuras devem manter a revisão, salvo pedido explícito de substituição. Edições, compras, remoções e até uma lista esvaziada pelo usuário são preservadas nos próximos carregamentos. Os backups continuam usando shoppingItems como array.

## Links diretos da Liga

As 11 cartas solicitadas têm edições de arte comum verificadas na Liga Pokémon, com ofertas em português. A busca e os nomes na lista abrem a edição exata quando nome e número correspondem ao catálogo; outras edições continuam usando a pesquisa. Idioma e acabamento são selecionados na Liga, conforme a oferta. Preços continuam manuais.

A atualização preenche apenas números vazios dos itens originais com nome correspondente, mantendo a revisão existente, quantidades, compras, preços, alterações e remoções. Não recria itens excluídos.

## Transição do Dragapult

O alvo tem 20 Pokémon, 32 Treinadores e 8 Energias. O deck atual permanece como referência: 49 cartas ficam e 11 são trocadas. Budew, Fezandipiti ex e Energias sem edição informada usam as edições do deck atual. A lista de compras contém apenas a diferença positiva (11 cartas em 7 itens), sem presumir cartas livres de outros decks.

A revisão `2026-10-02-dragapult-alvo-1` substitui a lista anterior uma vez, por solicitação explícita do usuário. Depois disso, compras, preços, edições e remoções permanecem salvos. Os links da Liga foram estendidos às novas cartas; preços continuam manuais.

## Alvo Zoroark e compras unificadas

O alvo do Zoroark tem 17 Pokémon, 35 Treinadores e 8 Energias. Entram 1 Munkidori, 1 Yveltal e 2 Cyrano; saem 2 Darumaka do N e 2 Darmanitan do N. O atual continua preservado.

A revisão `2026-10-02-dragapult-zoroark-alvos-1` adiciona essa diferença uma vez à revisão de compras do Dragapult, unificando nome/número e preservando compras, preços, alterações e remoções anteriores. Instalações novas recebem 15 cartas em 9 itens para ambos os alvos. Carregamentos seguintes preservam as edições do usuário.

## Troca parcial do Dragapult

Registradas as sete entradas e sete saídas informadas: sai a linha Duskull (5 cartas), 1 Ultra Bola e 1 Torre de Vigia da Equipe Rocket; entram 1 Budew, 1 Dunsparce, 1 Dudunsparce, 1 Ruínas Arriscadas, 1 Juiz e 2 Martelo Esmagador. O atual fica em 19 Pokémon, 33 Treinadores e 8 Energias. Faltam 1 Munkidori, 2 Martelo Esmagador e 1 Ruínas Arriscadas para o alvo.

A revisão `2026-10-02-dragapult-troca-7-1` marca os itens originais da troca como adquiridos uma vez, usando o maior entre o progresso existente e o informado, limitado à quantidade do item. Preserva preços, remoções e as compras do Zoroark. Os itens adquiridos continuam no histórico da lista; totais pendentes e cópia descontam essas cartas.
