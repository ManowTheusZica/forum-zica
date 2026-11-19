# forum-zica

Fórum do grupo em **um único arquivo HTML** — sem framework, sem build, sem backend.
Abre no navegador e funciona.

**[Abrir o fórum](https://manowtheuszica.github.io/forum-zica/)**

## O que tem dentro

- roteamento de SPA em `index.html` (hash), 6 categorias e ~15 tópicos já populados
- usuários com avatar colorido gerado a partir do nome
- reações (like, love, fire) guardadas em `localStorage`
- busca em títulos e respostas, criação de tópico e de resposta
- tema escuro/claro com persistência, layout responsivo

## Por que single-file

Era requisito: publicar no GitHub Pages sem pipeline e abrir de qualquer máquina sem
instalar nada. Tudo — CSS, JS, dados iniciais — vive no mesmo arquivo, porque o
`fetch` de JSON local quebra quando a página é aberta via `file://`.

## Limitações

O estado é local (`localStorage`): cada navegador tem o seu fórum. Sem servidor não há
como sincronizar — é o preço de rodar sem backend.
