# QUEM DISSE O QUE DISSE E QUEM FEZ E NÃO 🇧🇷

Repositório completo do projeto **"QUEM DISSE E QUEM FEZ? — Lula vs Flávio"**: jogo de flashcards do 2º turno das eleições 2026 (25 de outubro), feito para virar voto — com declaração de voto antes/depois, parte educativa sobre a história do voto, e **toda resposta com fonte**.

## Links

- 🔴 **APP NO AR**: https://courameneses1-dotcom.github.io/quem-disse-o-que-disse-e-quem-fez-e-nao/
- 📦 **Repositório**: https://github.com/courameneses1-dotcom/quem-disse-o-que-disse-e-quem-fez-e-nao
- O app publicado vem da branch `gh-pages` (espelho de `outputs/app`). Para atualizar o site após mudar o app: `git push origin main` e depois `git subtree push --prefix=outputs/app origin gh-pages`.

## Estrutura — markdowns de INPUT e OUTPUT separados

```
quem-disse-o-que-disse-e-quem-fez-e-nao/
│
├── inputs/                                  # 📥 O QUE FOI PEDIDO (um .md por pedido)
│   ├── 01-brief-original.md                 # pedido original + acordos editoriais
│   ├── 02-revisao-nome-e-contexto.md        # R2: nome do jogo + contexto Vorcaro
│   ├── 03-revisao-arte-hero-e-textos.md     # R3: hero/bandeira/muro + linguagem do povo + terras raras
│   ├── 04-revisao-gamificacao-urna-fake-news.md  # R4: sons, 50/50, caveira, urna, anti-abstenção
│   └── 05-feedback-arte.md                  # feedback: arte reprovada + caminhos pra v5
│
├── outputs/                                 # 📤 O QUE FOI PRODUZIDO
│   ├── RELATORIO.md                         # síntese: pedidos → entregas → decisões
│   ├── FONTES.md                            # TODAS as fontes (mestra)
│   ├── app/                                 # O APP (PWA — navegador, Android, iOS)
│   │   ├── index.html                       # aplicação completa, sem dependências
│   │   ├── manifest.webmanifest             # instalação como app
│   │   ├── sw.js                            # funcionamento offline
│   │   ├── FONTES.md                        # cópia de trabalho (o rodapé do app linka pra cá)
│   │   └── icons/
│   └── testes/                              # screenshots das validações (v1→v4)
│
├── README.md                                # este arquivo
└── .gitignore
```

## Rodar

Abra `outputs/app/index.html` no navegador, ou sirva por HTTP para o PWA completo:

```bash
cd outputs/app
python -m http.server 8080
```

## Publicar (gerar link compartilhável)

Arraste a pasta `outputs/app` em https://app.netlify.com/drop — pronto, URL pública.
No Android (Chrome): "Adicionar à tela inicial". No iPhone (Safari): Compartilhar → Adicionar à Tela de Início.

## Versionamento (importante!)

Este repo preserva **todas as versões** — nada é sobrescrito sem histórico:

```bash
git log --oneline          # ver todas as versões
git checkout v1.0          # voltar à versão 1 (tema vermelho, sem declaração de voto)
git checkout main          # voltar para a versão atual
```

- **v1.0** — primeira versão funcional: flashcards com fonte, tema vermelho/preto.
- **v2** — nome final "QUEM DISSE E QUEM FEZ?", tema verde/amarelo, declaração de voto antes/depois, tela educativa (voto feminino, ditadura, branco/nulo), recado fixo de rodapé, reorganização em inputs/outputs, git.

## Linha editorial (regra inviolável do deck)

Só entra citação/fato **com fonte verificada** (veículo + data + link — ver `outputs/app/FONTES.md`). Acusações judiciais sempre com o estado atual do processo (denunciado / arquivado / investigado / condenado). Motivo: o próprio TSE suspendeu peça de campanha que dizia "denunciado" no presente — formulação imprecisa derruba a peça e um card falso descredibiliza o app inteiro.
