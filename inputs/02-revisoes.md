# Input 02 — Revisões pedidas pelo usuário

## R1 (mesma sessão, após a v1)
- Contextualizar no enunciado das mensagens do "irmão" que o destinatário era o banqueiro Vorcaro (não só na explicação pós-resposta).
- Nome do jogo corrigido: **"Quem disse e quem fez? Lula vs Flávio"** (era "Quem disse? Flávio x Lula").
- Status: feito na v1.1.

## R2 (mesma sessão)
- **Git + GitHub**: versionar tudo, sem sobrescrever, preservando todas as versões.
- **Declaração de voto antes e depois** de jogar, com opções: branco, nulo, Lula, Flávio e não vou votar.
- **Parte educativa**: importância do voto; conquista recente do voto feminino; 21 anos de ditadura no Brasil.
- **Organização**: todos os inputs e outputs da conversa em subpastas, sob a pasta mãe "quem disse o que disse e quem fez e não".
- **Visual**: cores do app em verde e amarelo.
- **Recado fixo** no app: ideia original "NÃO VOTE PELO DIREITO DE VOTAR" → substituída por versão mais impactante (ver MOTTO no código), com alternativas.
- **Tática**: gamificação de convencimento (pré/pós = medição de virada de voto).
- Status: feito na v2.

## R3 (mesma sessão)
- **Hero artístico** na capa (desenhado em SVG, sem imagem externa): bandeira do Brasil por cima de uma bandeira rasgada dos EUA; título "QUEM (branco) DISSE (amarelo)" e "E (branco dentro de estrela vermelha) QUEM FEZ?" escritos dentro da bandeira; demais estrelas brancas/douradas; muro de tijolos quebrando com pichação "O BRASIL NÃO CABE NO QUINTAL DE NINGUÉM" (verde e amarelo); povo pulando o muro (referência The Wall/Pink Floyd); punho erguido (Muhammad Ali/Malcolm X); estátua da Liberdade segurando bandeirinha do Brasil; águia careca sendo pisoteada por um gavião; chamas; flora (folhas e flor); estrelas douradas no arredor/fundo da tela (textura CSS no body).
- **Simplificar TODOS os textos** pra "linguagem do povo", menos texto — quem quer detalhe clica em "ver fonte" (explicações foram cortadas pra 1–2 frases curtas; educativa e mensagens de virada enxutas; fonte exibida só como link).
- **Terras raras**: 1 card "Quem fez?" (Flávio oferecendo os minerais na carta a Trump) + 1 quiz explicando o que são em linguagem simples — fontes: G1 e ICL.
- Status: feito na v3.

## R4 (mesma sessão)
- **Gamificação sonora**: som de acerto (botão fica verde com fundo), som de erro, buzzer de caveira — e **bip de tecla de urna eletrônica** em TODOS os botões (Web Audio API, sem arquivos; não usar o som de "fim/confirmar" longo, só o bip curto de tecla comum — o de confirmar entrou só como bip duplo curto).
- **50/50**: metade da rodada (7/14) é múltipla escolha; outra metade "quem disse/fez".
- **Alternativas com explicação**: cada alternativa errada explica brevemente por que está errada ("why").
- **Fake news como armadilha**: alternativas marcadas como fake news documentada → clicou, fica **roxo**, caveira 💀 "VOCÊ CAIU EM UMA FAKE NEWS" surge e evapora, som de buzzer, e alerta fixo no feedback: "não compartilhe antes de checar / não acredite em tudo que vê na internet". Contador de "fake news que engoliu" no resultado. Exemplo pedido: "Qual destes políticos foi preso injustamente?" → Lula (580 dias, STF anulou), com why do Flávio ("nunca foi preso; injusto é ele estar solto"). Fake news fontadas usadas: Lula ateu (Folha), fechar igrejas (Carta 2022), banheiro unissex (Flow/PT), Aparecida padroeira (Folha).
- **Urna simulada** no final (construída no app): teclado com BRANCO/CORRIGE/CONFIRMA, número **13 = Lula / 22 = Flávio**, inválido = nulo, FIM na tela ao confirmar; bip de tecla em cada pressão. Botão pular = "não vou votar".
- **Painel anti-abstenção** no resultado: documento com foto, horário, 70+/16-17 facultativo com fila prioritária, justificativa pelo e-Título.
- Status: feito na v4.
