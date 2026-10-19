# Andarilho e suas Sombras — blog com publicação privada

O site continua público no GitHub Pages. Para publicar textos e vídeos sem editar HTML, o projeto usa o Pages CMS (editor externo conectado ao GitHub).

## Como funciona
- `content/posts.json` guarda as publicações.
- `blog.html` exibe todos os textos e vídeos marcados como publicados.
- `videos.html` exibe somente as publicações do tipo `video`.
- `.pages.yml` configura o painel de edição com título, data, tipo, categoria, resumo, texto, link do YouTube e opção de publicar.
- Só pessoas que têm permissão de escrita no repositório GitHub conseguem salvar alterações. Não adicione outras pessoas como colaboradoras se quiser ser a única pessoa que publica.

## Configurar uma vez
1. Crie um repositório **público** no GitHub para que qualquer pessoa possa ler o site.
2. Envie o conteúdo desta pasta inteira para a raiz do repositório (incluindo `.pages.yml`, `content/`, `css/`, `js/`, `img/` e `webfonts/`). Certifique-se de que arquivos e pastas ocultos, como `.pages.yml`, também sejam enviados.
3. Em **Settings → Pages**, escolha **Deploy from a branch**, selecione `main` e `/(root)`.
4. Acesse https://app.pagescms.org/ e entre com sua conta do GitHub.
5. Instale/conceda o acesso do Pages CMS **somente ao repositório deste site**. Abra o repositório no painel; o arquivo `.pages.yml` já configura o editor.
6. Confirme que somente sua conta possui acesso de escrita ao repositório. Não compartilhe senha nem token do GitHub.

## Publicar um texto
1. Entre em https://app.pagescms.org/ com a conta autorizada.
2. Abra o repositório e escolha **Publicações do blog**.
3. Adicione um item e preencha título, data, tipo `text`, categoria, resumo e texto completo.
4. Marque **Publicar no site?** como verdadeiro e salve.
5. O Pages CMS grava a alteração no GitHub. Aguarde o GitHub Pages atualizar e confira `blog.html`.

## Publicar um vídeo
1. Envie o vídeo ao YouTube (público ou não listado) e copie o link.
2. No painel, adicione uma publicação com tipo `video`, preencha título, data, descrição e cole o link no campo **Link do vídeo**.
3. Marque a publicação como publicada e salve. Ela aparecerá em `blog.html` e `videos.html`.

## Rascunhos e remoção
- Desmarque **Publicar no site?** para manter o item no arquivo sem mostrá-lo aos visitantes.
- Para retirar uma publicação, desmarque o campo e salve; ou exclua o item no editor.

## Segurança importante
- O painel não fica protegido por uma senha feita no HTML. A autenticação é feita pela conta GitHub/Pages CMS.
- O site público e os arquivos do repositório são públicos; não coloque rascunhos confidenciais, dados pessoais ou senhas em `posts.json`.
- Para manter só você como editor, não dê acesso de escrita a outras contas. A URL da área de edição pode ser vista por qualquer pessoa, mas sem permissão no repositório ela não deve conseguir salvar conteúdo.
- Os vídeos são incorporados do YouTube; o GitHub Pages não é indicado para hospedar arquivos de vídeo grandes diretamente.
