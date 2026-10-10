# QUEM DISSE E QUEM FEZ? — Lula vs Flávio 🎮

Jogo de flashcards do 2º turno de 2026 (25 de outubro). Funciona em **navegador**, **Android** e **iOS** como PWA (Progressive Web App) — sem loja de apps, sem custo.

## O que é
- **Quem disse?** — frases reais de Lula e de Flávio Bolsonaro (Deus, família, Brasil, tarifas, rachadinha, caso Master…). O jogador chuta de quem é.
- **Quem fez?** — fatos verificáveis de cada um (Bolsa Família, 29 milhões fora da pobreza × relatoria da lei anti-rave, investigação no STF, tarifaço…).
- **Desafio** — perguntas de conhecimento (condenação por golpe, números do Banco Mundial).
- Jogador coloca o **nome**, pontua, vê recorde local e **compartilha o resultado**.
- **Toda resposta traz fonte com link** (veículo + data). É isso que dá credibilidade ao jogo — quem discorda clica e confere.

## Rodar localmente
Basta abrir `index.html` no navegador. Para o PWA completo (instalação + offline), sirva por HTTP:

```bash
cd quem-disse
python -m http.server 8080
# abre http://localhost:8080
```

## Colocar no ar (para viralizar)
Qualquer hospedagem estática gratuita:
1. **Netlify Drop** (mais fácil): https://app.netlify.com/drop — arrasta a pasta `quem-disse`, ganha um link na hora.
2. **Vercel**: `npx vercel` dentro da pasta.
3. **GitHub Pages**: sobe os arquivos num repo → Settings → Pages.

Com o link no ar:
- **Android (Chrome)**: abre o link → "Adicionar à tela inicial" → vira app instalado (ícone, fullscreen, offline).
- **iPhone (Safari)**: Compartilhar → "Adicionar à Tela de Início".
- Compartilha o **resultado** nos grupos — o texto de share já chama para o jogo.

## Adicionar/editar cards
Todo o deck está no array `DECK` dentro de `index.html`. Cada card:

```js
{t:'v', cat:'frase',            // 'frase' | 'fato' | 'desafio'; t:'v' = Flávio x Lula, t:'q' = múltipla escolha
 q:'“A frase…”', a:'lula',      // ou a:'flavio'
 exp:'explicação que aparece depois do chute',
 src:'Veículo, data', url:'https://link-da-fonte'}
```

**Regra de ouro** (mantida até aqui): só entra card com fonte verificada — veículo reconhecido + data + link. Acusações judiciais sempre com o estado atual do processo (denunciado/arquivado/investigado/condenado), porque o TSE já suspendeu peça que dizia "denunciado" no presente.

## Estrutura
```
quem-disse/
├── index.html            # app completo (HTML+CSS+JS, sem dependências)
├── manifest.webmanifest  # PWA
├── sw.js                 # cache offline
├── FONTES.md             # todas as fontes do deck (veículo + data + URL)
└── icons/                # 192 / 512 / apple-touch
```
