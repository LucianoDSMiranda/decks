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

## Observação

O progresso da lista de compras é salvo no `localStorage` do navegador.
Isso significa que ele fica salvo naquele navegador/dispositivo.

## Preservação das compras

Atualizações do site devem manter as chaves `pokemonTCG_buy_` e os atributos `data-key` existentes. Não limpar o armazenamento nem renomear essas chaves ao editar nomes ou layout. O progresso já existente é lido diretamente, sem migração ou zeramento.

O salvamento é local ao navegador e ao endereço utilizado. Arquivo local e GitHub Pages não compartilham o mesmo armazenamento. Use **Baixar backup das compras** e **Restaurar backup** para transferir os dados ou se proteger contra a limpeza do navegador. A restauração mantém a maior quantidade entre o backup e o registro atual para cada carta/deck, sem duplicar compras, e preserva registros de cartas fora da lista atual. Não há sincronização entre dispositivos.
