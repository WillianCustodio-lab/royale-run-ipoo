# 👑 RoyaleRun

> Um jogo de ação top-down inspirado no universo do Clash Royale, desenvolvido em **Greenfoot 3.9.0** como projeto final da disciplina de IPOO.

**Integrantes:** Lucas Rodrigues · Willian Custódio

---

## 🎮 Sobre o Jogo

Você controla um **Goblin Dardo** infiltrado no reino inimigo. Seu objetivo é sobreviver aos ataques de torres, derrotar inimigos, coletar coroas e escapar por cada fase antes de ser eliminado.

O jogo possui **3 fases progressivas**, cada uma com inimigos, obstáculos e mecânicas novas, culminando em uma batalha contra o **Mega Cavaleiro**, o chefão final.

---

## 🕹️ Controles

| Tecla | Ação |
|-------|------|
| `W` `A` `S` `D` | Movimentar o personagem |
| `Espaço` | Atirar na direção do mouse |
| `Enter` | Confirmar / Avançar de tela |

---

## 📋 Como Jogar

1. Abra o projeto no **Greenfoot 3.9.0**
2. Clique em **Run** para iniciar a tela inicial
3. Clique em **Start** para ver as instruções ou iniciar o jogo
4. Colete coroas para acumular pontuação
5. Ao atingir **100 pontos**, a Torre do Rei se abre
6. Nas fases 2 e 3, colete também a **Chave** para liberar a saída
7. Entre na torre para avançar à próxima fase

---

## 🗺️ Fases

### Fase 1 — O Reino
Fase introdutória. Inimigos básicos e mecânica de tiro.

- **Inimigos:** Bárbaros (surgem periodicamente) + Princesa nas torres
- **Obstáculos:** Vinhas, Rio (bloqueiam passagem)
- **Objetivo:** Acumule 100 pontos e escape pela Torre do Rei

### Fase 2 — O Inverno
Cenário congelado com novos desafios de movimentação.

- **Inimigos:** Bárbaros + Golem de Gelo + Mago de Gelo nas torres
- **Obstáculos:** Gelo (reduz velocidade ao pisar), Blocos de Ice
- **Itens extras:** Elixir Negro (aumento de velocidade), Chave
- **Objetivo:** 100 pontos + coletar a Chave + escapar

### Fase 3 — O Chefão
Batalha final contra o Mega Cavaleiro.

- **Inimigos:** Mega Cavaleiro (chefão) + Canhoneiro nas torres
- **Mecânica especial:** O chefe lança luvas do céu — fique de olho nas sombras!
- **Obstáculos:** Lápides, Vinhas
- **Itens extras:** Elixir Negro, Chave
- **Objetivo:** Derrotar o Mega Cavaleiro + 100 pontos + coletar a Chave + escapar

---

## 🧩 Itens Coletáveis

| Item | Efeito |
|------|--------|
| 👑 **Coroa** | +10 pontos |
| ⚗️ **Elixir Negro** | Aumenta a velocidade temporariamente (~3 segundos) |
| 🗝️ **Chave** | Libera a saída da fase (fases 2 e 3) |

---

## 👾 Inimigos

| Inimigo | Tipo | Comportamento |
|---------|------|---------------|
| Bárbaro | Terrestre | Move-se pelo mapa, persegue o jogador e coroas |
| Princesa | Torre | Atira proj éteis para baixo periodicamente |
| Golem de Gelo | Terrestre | Lento, 3 pontos de vida; ao morrer, cria bloco de gelo |
| Mago de Gelo | Torre | Atira projéteis de gelo periodicamente |
| Canhoneiro | Torre | Dispara projéteis mais rápidos |
| Mega Cavaleiro | Chefão | Lança luvas do céu; 10 pontos de vida; barra de vida visível |

---

## 🏗️ Arquitetura do Projeto

O projeto segue os princípios de **Orientação a Objetos**, com herança, encapsulamento e alta coesão entre as classes.

```
World
├── FaseBase          ← base de todas as fases
│   ├── Fase1
│   ├── Fase2
│   └── Fase3
├── TelaInicial
├── TelaInstruções
├── TelaVitoria
└── TelaDerrota

Actor
├── JogadorBase       ← base do personagem jogável
│   ├── JogadorFase1
│   ├── JogadorFase2
│   └── JogadorFase3
├── InimigoBase       ← base dos inimigos terrestres
│   ├── Barbaro
│   └── GolemDeGelo
├── InimigoTorre      ← base dos inimigos fixos
│   ├── Princesa
│   ├── MagoDeGelo
│   └── Canhoneiro
├── ItemBase          ← base dos itens coletáveis
│   ├── ItemCoroa
│   ├── ItemChave
│   └── ElixirNegro
├── Obstaculo         ← base dos obstáculos
│   ├── Agua, Gelo, Vines, Torre, TorreRei ...
└── MegaCavaleiro

Utilitários (sem herança de Actor)
├── ControleAnimacao
├── ControleDeTiro
├── MovimentoInimigo
├── ComportamentoInimigo
├── GeradorItemBase → GeradorCoroa, GeradorChave, GeradorElixirNegro
├── GerarBarbaros
├── ConstruirCenarioBase → ConstruirCenarioFase1/2/3
├── CronometroGlobal
└── Pontuacao
```

---

## ⚙️ Requisitos

- **Java** 11 ou superior
- **Greenfoot 3.9.0** — [Download oficial](https://www.greenfoot.org/download)

---

## ▶️ Como Executar

1. Clone ou baixe o repositório
2. Abra o **Greenfoot 3.9.0**
3. Vá em `Scenario > Open` e selecione a pasta do projeto
4. Clique em **Compile** (se necessário)
5. Clique em **Run**

---

## 📁 Estrutura de Arquivos Relevantes

```
RoyaleRun/
├── *.java          # Código-fonte das classes
├── *.ctxt          # Metadados do BlueJ/Greenfoot
├── images/         # Sprites e imagens do jogo
├── sounds/         # Efeitos sonoros e músicas
└── README.md
```

---

## 👥 Créditos

Desenvolvido por **Lucas Rodrigues** e **Willian Custódio** como projeto final da disciplina de Introdução à Programação Orientada a Objetos (IPOO).

O tema e os personagens são inspirados no universo do jogo **Clash Royale** (Supercell), utilizados apenas para fins educacionais.
