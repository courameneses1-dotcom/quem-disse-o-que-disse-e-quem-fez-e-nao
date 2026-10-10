# O APP — QUEM DISSE E QUEM FEZ? (Lula vs Flávio)

PWA (navegador + Android + iOS), zero dependências. Sobe com `python -m http.server 8080` nesta pasta ou publique arrastando-a em https://app.netlify.com/drop

## Fluxo do jogo (v2)
1. **Home** — declaração de voto PRÉ (Lula / Flávio / Branco / Nulo / Não vou votar) + nome → JOGAR.
2. **14 cards** — 💬 Quem disse? / ⚡ Quem fez? / 🎯 Desafio, cada resposta com fonte + link.
3. **Resultado** — pontuação, níveis, declaração de voto PÓS com comparação antes→depois e mensagem de virada; compartilhar; "Por que votar?".
4. **Por que votar?** — voto feminino (1927/1932/1934/1946/1988), 21 anos de ditadura, branco/nulo não anulam (TSE), 25/10.

## Customização rápida
- **Recado fixo (MOTTO)**: constante `MOTTO` no início do `<script>` no index.html (há 2 alternativas prontas no comentário).
- **Deck de cards**: array `DECK` no index.html — regra: só entra card com fonte (veículo + data + link). Detalhes e lista completa em FONTES.md.
- **Quantidade por rodada**: constante `ROUND` (14) e as fatias de frase/fato/desafio em `startGame()`.
