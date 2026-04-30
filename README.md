# 🌍 HtmlTerra — v0.3.0

> Quiz de geografia mundial em HTML single-file. Sem instalação — jogue direto no navegador.
>
> 🔗 **[Jogar agora → roqols.github.io/HtmlTerra](https://roqols.github.io/HtmlTerra)**

---

## ✨ Novidades desta versão

### 🔤 Renomeação do projeto
- O projeto agora se chama **HtmlTerra**.
- Disponível via **GitHub Pages** — sem precisar baixar nada.

### 📱 Suporte completo a dispositivos móveis
Layout totalmente adaptado para celular e tablet via media queries:

**Mobile (≤ 600px)**
- Sidebar de países encontrados migra para uma **faixa horizontal** na base do mapa, com scroll lateral — libera espaço vertical para o mapa.
- Header compactado com fontes e espaçamentos ajustados para telas estreitas.
- Campo de digitação com `font-size: 16px` para **evitar o zoom automático do iOS**.
- Uso de `100dvh` (dynamic viewport height) para compensar a barra de endereço e o teclado virtual.
- `touch-action: none` no SVG do mapa para habilitar pinch-to-zoom e pan por toque.
- Tela de resultado com botões empilhados verticalmente.

**Tablet (601px – 900px)**
- Ajustes intermediários de fontes e largura da sidebar.

### 🗺️ Correção do fundo do mapa
- O fundo do oceano agora **cobre toda a área visível** mesmo após zoom e pan.
- A sphere e graticule foram movidas para dentro do grupo de zoom do D3, eliminando o "buraco" que aparecia nas bordas ao navegar.

### 🏝️ Porto Rico adicionado
- **Porto Rico** (ISO 630) incluído com alias `puerto rico`.

---

## 🗂️ Países no jogo

| Categoria | Qtd. |
|-----------|------|
| Com highlight no mapa | ~180 |
| Aceitos via toast (ilhas pequenas, microstados) | ~25 |
| **Total** | **~205** |

Países sem polígono no mapa 110m mas válidos: Mônaco, Vaticano, Singapura, Nauru, Maldivas, Tuvalu, Tonga, Samoa, Kiribati, Ilhas Marshall, Palau, Micronésia, Seicheles, Maurício, Comores, Cabo Verde, São Tomé e Príncipe, Dominica, Granada, São Cristóvão e Névis, Santa Lúcia, São Vicente e Granadinas, Barbados, Jamaica, Trinidad e Tobago, Liechtenstein, San Marino, Kosovo e Porto Rico.

---

## 🛠️ Stack

- **D3.js v7** — projeção Natural Earth, zoom/pan, path rendering
- **TopoJSON client v3** — `world-atlas 110m`
- **Vanilla JS + CSS** — zero frameworks, single `.html` file
- **Google Fonts** — Cinzel + Space Mono

---

## 🐛 Correções

- Fundo do mapa não cobria a área completa ao fazer zoom/pan → corrigido.
- Duplicatas na base de dados de países removidas.

---

## 🚀 Deploy

O jogo roda direto no GitHub Pages — sem backend, sem build step.

```
Repositório: https://github.com/roqols/HtmlTerra
Jogo:        https://roqols.github.io/HtmlTerra
```

Basta fazer upload do `index.html` (renomeie o `htmlterra.html` para `index.html`) e ativar o GitHub Pages nas configurações do repositório apontando para a branch `main`.

---

*Single-file game · Sem backend · Sem build step*
