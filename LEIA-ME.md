# Deck COGERH no GitHub Pages + votação pelo celular

## Parte A. Publicar o deck (5 min)
1. No GitHub, crie um repositório (ex.: `deck`), público.
2. Envie os 4 arquivos desta pasta: `index.html`, `config.js`, `firebase-rules.json` (opcional) e este `LEIA-ME.md`.
   (Add file > Upload files > Commit.)
3. Settings > Pages > Source: "Deploy from a branch" > branch `main`, pasta `/ (root)` > Save.
4. Em 1 a 2 min o deck abre em `https://SEUUSUARIO.github.io/deck/`.

## Parte B. Ligar a votação pelo celular (10 min, plano grátis)
1. Acesse console.firebase.google.com e crie um projeto (pode desativar o Google Analytics).
2. Menu Build > **Realtime Database** > Create database > escolha a região > modo **bloqueado** (locked).
3. Aba **Rules**: apague tudo, cole o conteúdo de `firebase-rules.json` e clique **Publish**.
4. Copie o endereço do banco que aparece no topo da aba Data
   (ex.: `https://deck-cogerh-default-rtdb.firebaseio.com`).
5. No GitHub, abra `config.js` (lápis para editar) e preencha:
   - `fb`: o endereço do passo 4
   - `live`: `https://SEUUSUARIO.github.io/deck/`
   Commit. Aguarde 1 min.

## Como usar na apresentação
- Você abre o deck pelo link do Pages (ou pelo arquivo offline com o mesmo config.js na mesma pasta).
- Abre um dilema ou o quiz. Aparece um QR no canto do painel e a etiqueta "AO VIVO".
- O público escaneia e vota no celular, sem login. A cada pergunta nova a tela do celular troca sozinha.
- Os votos do celular somam com a sua contagem manual (teclas A–D). Enter revela.

## Limites e cuidados
- Qualquer pessoa com o link do banco pode ler e gravar votos (é uma enquete aberta). Não coloque dados sensíveis.
- Quem abrir o deck sem `#votar` age como apresentador: se abrir um dilema, troca a pergunta do público.
  Divulgue só o QR, não o link do deck, durante a votação.
- Para zerar votos antigos: Firebase > Data > apague o nó `votes`.
- Sem `config.js` preenchido, o deck funciona normalmente com contagem manual.

## Assistente tira-dúvidas (personagem no canto inferior direito)
1. No ChatGPT, abra o projeto "Identidade_Estrategica" e copie o endereço da barra do navegador.
2. Cole em `bot` no `config.js` e salve. Pronto: clicar na personagem abre o projeto em outra aba.
3. Para conversar por voz, use o ícone de voz do ChatGPT dentro do projeto (app ou site).
Obs.: o ChatGPT não permite ficar dentro do deck. O clique abre uma aba, e você volta ao deck depois.
