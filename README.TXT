# 👑 RoyaleRun

> Jogo de ação top-down inspirado no universo de Clash Royale, desenvolvido em **Greenfoot 3.9.0** como projeto final da disciplina de IPOO.

## 👥 Integrantes
- Lucas Rodrigues
- Willian Custódio

---

# 🎮 Sobre o Jogo

Você controla um **Goblin Dardo** infiltrado no reino inimigo.  
Seu objetivo é sobreviver aos ataques das torres, derrotar inimigos, coletar coroas e escapar de cada fase antes de ser eliminado.

O jogo possui **3 fases progressivas**, cada uma introduzindo novos inimigos, obstáculos e mecânicas, culminando em uma batalha contra o **Mega Cavaleiro**.

---

# 🕹️ Controles

- `W A S D` → Movimentação
- `Espaço` → Atirar na direção do mouse
- `Enter` → Confirmar / avançar telas

---

# 📋 Como Jogar

1. Abra o projeto no **Greenfoot 3.9.0**
2. Clique em **Run**
3. Inicie o jogo pela tela inicial
4. Colete coroas para ganhar pontos
5. Ao atingir **100 pontos**, a Torre do Rei será liberada
6. Nas fases 2 e 3, colete também a **Chave**
7. Entre na torre para avançar

---

# 🗺️ Fases

## Fase 1 — O Reino

Fase introdutória com mecânica básica de combate.

### Inimigos
- Bárbaros
- Princesa nas torres

### Obstáculos
- Vinhas
- Rio

### Objetivo
- Conseguir 100 pontos
- Escapar pela Torre do Rei

---

## Fase 2 — O Inverno

Mapa congelado com redução de velocidade no gelo.

### Inimigos
- Bárbaros
- Golem de Gelo
- Mago de Gelo

### Obstáculos
- Gelo
- Blocos de Ice

### Itens Extras
- Elixir Negro
- Chave

### Objetivo
- Conseguir 100 pontos
- Coletar a chave
- Escapar

---

## Fase 3 — O Chefão

Batalha final contra o Mega Cavaleiro.

### Inimigos
- Mega Cavaleiro
- Canhoneiros nas torres

### Mecânica Especial
O chefe lança luvas do céu. Observe as sombras para desviar.

### Obstáculos
- Lápides
- Vinhas

### Objetivo
- Derrotar o Mega Cavaleiro
- Conseguir 100 pontos
- Coletar a chave
- Escapar

---

# 🧩 Itens

| Item | Função |
|---|---|
| 👑 Coroa | +10 pontos |
| ⚗️ Elixir Negro | Aumenta velocidade temporariamente |
| 🗝️ Chave | Libera a saída da fase |

---

# 👾 Inimigos

| Inimigo | Descrição |
|---|---|
| Bárbaro | Persegue o jogador e as coroas |
| Princesa | Atira projéteis periodicamente |
| Golem de Gelo | Possui 3 vidas e cria gelo ao morrer |
| Mago de Gelo | Dispara projéteis congelantes |
| Canhoneiro | Dispara projéteis rápidos |
| Mega Cavaleiro | Chefão com barra de vida e ataques especiais |

---

# 🏗️ Arquitetura

## Worlds
```text
FaseBase
├── Fase1
├── Fase2
└── Fase3
```

## Actors
```text
JogadorBase
├── JogadorFase1
├── JogadorFase2
└── JogadorFase3

InimigoBase
├── Barbaro
└── GolemDeGelo
```

---

# ⚙️ Requisitos

- Java 11+
- Greenfoot 3.9.0

## Download
- https://www.greenfoot.org/download

---

# ▶️ Como Executar

```bash
git clone URL_DO_REPOSITORIO
```

Depois:

1. Abra o Greenfoot
2. Vá em `Scenario > Open`
3. Selecione a pasta do projeto
4. Clique em `Run`

---

# 📁 Estrutura do Projeto

```text
RoyaleRun/
├── images/
├── sounds/
├── *.java
├── *.ctxt
└── README.md
```

---

# 📚 Créditos

Projeto desenvolvido para a disciplina de IPOO.

Inspirado no universo de Clash Royale, da Supercell, utilizado apenas para fins educacionais.