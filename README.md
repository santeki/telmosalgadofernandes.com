# Site pessoal

O site de Telmo Salgado Fernandes, em inglês, em telmosalgadofernandes.com. A página inicial é o About. No topo, ao centro, o menu leva às páginas de cada tipo de texto, com a lista dos textos desse tipo (Essays, Short posts, Research, Op-eds); um tipo só aparece no menu quando tem textos.

## Ver o site no Mac

No Terminal, dentro desta pasta:

    hugo server

Depois abre http://localhost:1313. Cada alteração aparece logo, e os rascunhos aparecem com a etiqueta Draft.

## Escrever um artigo

1. Cria uma pasta em `content/drafts/` com o endereço do artigo, em inglês, minúsculas e hífenes. Por exemplo: `content/drafts/who-is-liable-when-ai-gets-it-wrong/`.
2. Dentro dela, cria o ficheiro `index.md`:

   ```markdown
   ---
   title: "Who is liable when AI gets it wrong?"
   category: essay
   date: 2026-11-19
   description: "One sentence. It appears on the home page and on LinkedIn."
   in_short: "Optional. The conclusion in two or three sentences, at the top of the article."
   ---

   The text, in Markdown. A footnote looks like this.[^1]

   [^1]: The text of the note.
   ```

   Em `category` vai o tipo: `essay` (texto longo), `short` (texto curto), `research` (trabalho académico) ou `op-ed` (artigo publicado noutro sítio). Os tipos estão em `hugo.toml`.

## Publicar

Quando o artigo estiver pronto, move a pasta de `content/drafts/` para `content/articles/`. A pasta `content/drafts/` nunca sai do Mac, porque o Git a ignora.

Ainda falta ligar a publicação: o domínio e o GitHub.

## Recomendar um livro

Os livros da página Readings estão em `data/readings.yaml`, um por bloco, com o título, o autor, o ano e, se quiseres, uma nota tua em inglês e um link. Um livro com `draft: true` só aparece no Mac. A página Readings só aparece no menu quando houver pelo menos um livro recomendado.

## Onde está cada coisa

- `content/articles/`: os artigos publicados.
- `content/drafts/`: os rascunhos.
- `content/_index.md`: o texto do About, que é a página inicial.
- `content/essays.md`, `short-posts.md`, `research.md`, `op-eds.md`: as páginas de cada tipo de texto.
- `data/readings.yaml`: os livros recomendados.
- `assets/images/portrait.jpg`: a imagem do canto.
- `hugo.toml`: o nome do site, o domínio e o idioma.
- `layouts/` e `assets/css/main.css`: o aspeto do site.
