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

A lista começa vazia. Digite o nome da carta, pesquise na Liga Pokémon em outra aba e informe a edição, quantidade desejada e preço unitário de referência. O preço é opcional, informado pelo usuário e não é atualizado automaticamente. O total pendente considera apenas as cópias ainda não compradas e não inclui frete; cartas sem preço são indicadas à parte.

É possível editar/remover itens, registrar cópias compradas e copiar as quantidades pendentes. A busca sugere nomes presentes nos decks, mas permite qualquer carta. Os nomes são enviados à Liga somente ao abrir o link de pesquisa.

## Preservação das compras

O armazenamento da lista editável usa a chave estável `pokemonTCG_shoppingList_v1`. Não trocar essa chave nem limpar o armazenamento ao atualizar o site. A lista é salva após cada alteração; falhas de leitura bloqueiam gravações para não sobrescrever dados existentes.

Os antigos registros `pokemonTCG_buy_` ficam preservados no navegador e no backup, mas não preenchem automaticamente a nova lista. A remoção das listas fixas foi solicitada pelo usuário.

Use **Baixar backup** e **Restaurar backup** para transferir ou recuperar a lista. O backup versão 2 inclui nomes, edições, quantidades, compras e preços, além dos registros antigos. Backups versão 1 continuam aceitos para preservar os registros antigos. Restaurar o mesmo arquivo não duplica os itens: a mesclagem usa IDs estáveis, mantém edições/preços atuais para itens já existentes e preserva as maiores quantidades.

Os dados ficam no navegador e endereço usados. Arquivo local e GitHub Pages não compartilham armazenamento. Não há sincronização entre dispositivos; faça backup antes de limpar os dados do navegador ou trocar de endereço.
