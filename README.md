# 🎓 Sapiência

**Plataforma educacional de prática de redações para o ENEM** — construa repertório sociocultural, estude modelos dissertativo-argumentativos e treine sua escrita com autoavaliação guiada.

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-7F5D99)
![License](https://img.shields.io/badge/license-MIT-C4B5D4)
![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-6-646CFF?logo=vite&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-3-06B6D4?logo=tailwindcss&logoColor=white)

---

## ✨ Sobre o Projeto

O **Sapiência** é uma plataforma web desenvolvida para estudantes que desejam aperfeiçoar suas habilidades de redação dissertativo-argumentativa para o ENEM. O projeto combina **repertórios socioculturais curados**, **modelos didáticos** e **autoavaliação por competências** em uma interface moderna, responsiva e acessível.

> *"Escrever bem é aprender a pensar."*

🔗 **Acesse:** [sapiencia.vercel.app](https://sapiencia.vercel.app) *(em breve)*

---

## 🚀 Funcionalidades

### 🏠 Início
- Hero section com chamada para ação
- **Repertório do dia** com sorteio aleatório
- Navegação rápida para as principais seções

### 📚 Repertório Sociocultural
- **40 repertórios** curados entre filósofos, sociólogos, leis, livros, filmes, séries, pensadores, movimentos e fenômenos
- **14 eixos temáticos** (Educação, Tecnologia, Meio Ambiente, Desigualdade, Saúde Mental, etc.)
- Filtros por **pills clicáveis** com `aria-pressed` para acessibilidade
- Busca por autor, obra ou lei
- Sistema de **favoritos** persistente em `localStorage`
- Textos variados e originais com `explicacao` e `comoUsar`

### 📝 Modelos de Redação
- **Modelo dissertativo-argumentativo completo** com comentários didáticos por parágrafo
- **Esqueletos guiados** para Introdução, Desenvolvimento 1, Desenvolvimento 2 e Conclusão
- Estrutura expansível com animações suaves

### ⏱️ Treino
- **Timer com persistência** via `sessionStorage` (não perde o tempo ao trocar de aba)
- **Autoavaliação por competências** baseada nas 5 competências do ENEM
- **Situações críticas** com orientações contextuais (ex: nota baixa em Competência 3)
- Salvamento automático do treino no histórico

### 📊 Histórico
- **Busca** por tema ou anotações
- **Filtros por faixa de nota** (alto, médio, baixo, zero)
- **Ordenação** por data ou nota (ascendente/descendente)
- **Export/Import em JSON** para backup e migração entre dispositivos
- Exclusão individual de treinos

### 🎨 Design & UX
- **Shader animado** do `@paper-design/shaders-react` (Warp) como fundo
- **Splash screen educacional** no primeiro carregamento da sessão
- **Menu hambúrguer** responsivo para mobile
- **Skeleton loader** nas transições entre páginas
- **Scroll to top** automático ao trocar de rota
- Tema **claro/escuro** seguindo `prefers-color-scheme`
- Acessibilidade: `aria-pressed`, `aria-current`, `aria-expanded`, `role="status"`, respeito a `prefers-reduced-motion`

---

## 🛠️ Tecnologias

| Categoria | Tecnologia |
|-----------|-----------|
| Framework | React 18 |
| Linguagem | TypeScript 5 |
| Build Tool | Vite 6 |
| Estilização | Tailwind CSS 3 |
| Shader de fundo | `@paper-design/shaders-react` |
| Tipografia | Bricolage Grotesque + Source Serif 4 (Google Fonts) |
| Deploy | Vercel |
| PWA | `manifest.json` + ícones 192/512 |

---

## 🏗️ Estrutura do Projeto

```
sapiencia/
├── public/
│   ├── favicon.svg
│   ├── icon-192.png          # Ícone PWA 192x192
│   ├── icon-512.png          # Ícone PWA 512x512
│   ├── logo-sapiencia.png
│   ├── manifest.json         # PWA manifest
│   └── robots.txt            # SEO crawlers
├── src/
│   ├── components/
│   │   ├── layout/           # Header, Footer, Navigation
│   │   └── ui/               # SilkShaderBackground, Skeleton, SplashScreen
│   ├── data/
│   │   ├── modelos.ts        # Modelos de redação e esqueletos
│   │   ├── repertorios.ts    # 40 repertórios socioculturais
│   │   └── temas.ts          # Eixos temáticos
│   ├── hooks/
│   │   ├── useAutoEvaluation.ts
│   │   └── useTimer.ts       # Timer persistente com sessionStorage
│   ├── pages/
│   │   ├── Historico.tsx     # Histórico com busca/filtros/export
│   │   ├── Inicio.tsx        # Home com repertório do dia
│   │   ├── Modelos.tsx       # Modelos de redação
│   │   ├── Repertorio.tsx    # Catálogo de repertórios
│   │   └── Treino.tsx        # Treino com timer e autoavaliação
│   ├── services/
│   │   └── storage.ts        # localStorage wrapper + export/import
│   ├── styles/
│   │   └── globals.css       # Variáveis CSS + animações
│   ├── App.tsx               # Router + SplashScreen + transições
│   └── main.tsx              # Entry point
├── index.html                # Meta tags OG/Twitter + PWA links
├── package.json
├── tailwind.config.js
├── tsconfig.json
└── vite.config.ts
```

---

## 📦 Como Rodar Localmente

### Pré-requisitos
- **Node.js** 18+ 
- **npm** 9+

### Instalação

```bash
# Clone o repositório
git clone https://github.com/Binhu01/Sapiencia.git

# Entre na pasta do projeto
cd Sapiencia

# Instale as dependências
npm install

# Rode o servidor de desenvolvimento
npm run dev
```

O projeto estará disponível em **http://localhost:5173**

### Build para Produção

```bash
npm run build
npm run preview   # para visualizar o build localmente
```

---

## 🎨 Paleta de Cores

| Token | Hex | Uso |
|-------|-----|-----|
| `brand-purple` | `#7F5D99` | Cor primária |
| `brand-purple-deep` | `#352744` | Títulos escuros |
| `brand-purple-dark` | `#17121F` | Background dark mode |
| `brand-beige` | `#F5F0E6` | Background light mode |
| `brand-lavender` | `#C4B5D4` | Destaques e bordas |
| `brand-graphite` | `#3D3545` | Texto light mode |

---

## 🚢 Deploy

O projeto está configurado para deploy na **Vercel**:

1. Conecte o repositório `Binhu01/Sapiencia` em [vercel.com/new](https://vercel.com/new)
2. Configurações detectadas automaticamente:
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
3. Clique em **Deploy**

O Vercel também gera **previews automáticos** a cada push em branches de feature.

---

## 📄 Licença

Este projeto é desenvolvido para **fins educacionais** e não possui vínculo oficial com o INEP ou o MEC. Distribuído sob a licença MIT.

---

## 👨‍💻 Autor

Desenvolvido por **Glauber** com assistência de [Claude](https://claude.ai).

---

<div align="center">
  <sub>Feito com 💜 para estudantes do ENEM</sub>
</div>