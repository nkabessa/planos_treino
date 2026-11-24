# Calendar Hack PT

Aplicação web estática em **Português Europeu (pt-PT)** para planeamento de treinos de corrida e exportação direta para calendários pessoais (`.ics` / iCalendar) e folhas de cálculo (`.csv`).

## Estrutura de Ficheiros

```text
/
├── index.html                  # Aplicação web principal (sem necessidade de build)
├── README.md                   # Documentação
└── plans/
    ├── index.yaml              # Catálogo dos planos apresentados na dropdown
    ├── 5k-6s.yaml              # Plano 5 km (6 semanas)
    ├── 10k-8s.yaml             # Plano 10 km (8 semanas)
    ├── meia-maratona-12s.yaml  # Plano Meia Maratona (12 semanas)
    ├── maratona-16s.yaml       # Plano Maratona (16 semanas)
    └── trail-curto-10s.yaml    # Plano Trail Curto (10 semanas)
```

## Como adicionar novos planos à dropdown

1. Cria um novo ficheiro `.yaml` dentro da pasta `plans/` (podes duplicar qualquer um dos existentes como base).
2. Adiciona uma entrada no ficheiro `plans/index.yaml`:
   ```yaml
   plans:
     - id: meu-novo-plano
       file: meu-novo-plano.yaml
       name: "Nome visível na Dropdown"
   ```
3. Faz *push* para o GitHub Pages ou Cloudflare Pages — o novo plano ficará imediatamente disponível.
