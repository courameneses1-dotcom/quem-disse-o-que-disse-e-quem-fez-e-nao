# QUEM DISSE O QUE DISSE E QUEM FEZ E NÃO 🇧🇷

Repositório completo do projeto **"QUEM DISSE E QUEM FEZ? — Lula vs Flávio"**: jogo de flashcards do 2º turno das eleições 2026 (25 de outubro), feito para virar voto — com declaração de voto antes/depois, parte educativa sobre a história do voto, e **toda resposta com fonte**.

## Estrutura

```
quem-disse-o-que-disse-e-quem-fez-e-nao/
├── inputs/                      # TUDO o que foi pedido pelo usuário na conversa
│   ├── 01-brief-original.md     # pedido original transcrito + acordos editoriais
│   └── 02-revisoes.md           # revisões pedidas ao longo das iterações
├── outputs/                     # TUDO o que foi produzido
│   ├── app/                     # O APP (PWA — navegador, Android, iOS)
│   │   ├── index.html           # aplicação completa, sem dependências
│   │   ├── manifest.webmanifest # instalação como app
│   │   ├── sw.js                # funcionamento offline
│   │   ├── FONTES.md            # todas as fontes do deck
│   │   └── icons/
│   ├── testes/                  # screenshots das validações
│   └── RELATORIO.md             # síntese da conversa: pedidos → entregas
├── README.md                    # este arquivo
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
