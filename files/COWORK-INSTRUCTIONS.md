# Academic Website — Nícolas Goulart

## O que é este projeto
Site acadêmico pessoal em GitHub Pages. HTML/CSS estático, 3 páginas (CV, Research, Teaching). Paleta inspirada na Bain (vermelho #CC0000, preto #1A1A1A, branco). Estrutura inspirada no site do Pedro Sant'Anna (Jekyll AcademicPages) mas implementado em HTML puro.

## Stack
- HTML + CSS puro (style.css compartilhado)
- Sem framework, sem build step, sem JavaScript exceto toggle de abstracts
- GitHub Pages para deploy
- Fontes: Source Serif 4 (display) + DM Sans (body) via Google Fonts

## Disciplina de trabalho

### Mudanças cirúrgicas
- Este site já está no ar. Cada mudança deve ser mínima.
- Ao adicionar um paper: copiar o bloco `.paper` existente, trocar o conteúdo. Não reformatar CSS.
- Ao adicionar uma disciplina: copiar o bloco `.course` existente.
- Não mudar a paleta de cores, fontes, ou layout sem pedir.
- Não adicionar JavaScript desnecessário.
- Não adicionar dependências (React, Tailwind, etc.) — manter HTML/CSS puro.

### Simplicidade
- Cada página é um .html independente com link para style.css
- Sem componentes, sem templates, sem build
- Adicionar conteúdo = editar HTML diretamente

## Paleta de cores (não mudar)
- --red: #CC0000 (primária)
- --red-dark: #8B0000 (hover)
- --black: #1A1A1A (texto)
- --gray-mid: #6B6B6B (texto secundário)
- --gray-bg: #F7F7F7 (fundo de cards)
- --white: #FFFFFF (fundo)

## Estrutura de arquivos
```
nicolasgoulart.github.io/
├── index.html      (CV page — home)
├── research.html   (Research page)
├── teaching.html   (Teaching page)
├── style.css       (shared styles)
├── files/          (PDFs: CV, papers, problem sets)
└── images/         (profile photo, etc.)
```

## Como adicionar conteúdo

### Novo paper em Research
Copiar este bloco e preencher:
```html
<div class="paper">
  <div class="paper-title">TÍTULO</div>
  <div class="paper-authors">with <a href="URL">Coautor</a></div>
  <div class="paper-venue">Journal, Year</div>
  <div class="paper-links">
    <a href="URL">Working Paper</a>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">▶</span> Abstract
  </button>
  <div class="abstract-text">
    ABSTRACT TEXT
  </div>
</div>
```

### Nova disciplina em Teaching
Copiar este bloco e preencher:
```html
<div class="course">
  <div class="course-title">NOME DA DISCIPLINA</div>
  <div class="course-detail">
    Professor: <a href="URL">Nome</a> · Período<br>
    Tópicos<br>
    <a href="URL">Material (PDF)</a>
  </div>
</div>
```

### Novo item no CV
Copiar este bloco:
```html
<div class="cv-item">
  <div>
    <div class="title">CARGO/TÍTULO</div>
    <div class="detail">Instituição</div>
  </div>
  <div class="date">ANO</div>
</div>
```
