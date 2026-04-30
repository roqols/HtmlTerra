# 🌍 Atlantis — v0.3.0

> Quiz de geografia mundial em HTML single-file, sem dependências de servidor.

---

## ✨ Novidades desta versão

### 🔤 Renomeação do projeto
- O projeto passou a se chamar **Atlantis** (anteriormente Atlas Quiz → Atlantis World → Atlantis).
- Título atualizado na aba do navegador, tela de setup e header do jogo.

### 📱 Suporte completo a dispositivos móveis
Layout totalmente refeito para celular e tablet via media queries:

**Mobile (≤ 600px)**
- Sidebar de países encontrados migra para uma **faixa horizontal** na base do mapa, com scroll lateral — libera espaço vertical para o mapa.
- Header compactado com fontes e espaçamentos ajustados para caber em telas estreitas.
- Campo de digitação com `font-size: 16px` para **evitar o zoom automático do iOS**.
- Uso de `100dvh` (dynamic viewport height) para compensar a barra de endereço e o teclado virtual.
- `touch-action: none` no SVG do mapa para habilitar pinch-to-zoom e pan por toque sem conflito com o scroll da página.
- Tela de resultado com botões empilhados verticalmente.
- Labels auxiliares ocultados para economizar espaço.

**Tablet (601px – 900px)**
- Ajustes intermediários de fontes e largura da sidebar.

### 🗺️ Correção do fundo do mapa
- O fundo do oceano agora **cobre toda a área visível** mesmo após zoom e pan.
- A sphere e a graticule foram movidas para dentro do grupo de zoom do D3, eliminando o "buraco" de cor diferente que aparecia nas bordas ao navegar pelo mapa.
- O `rect` de fundo foi expandido para `21×` as dimensões do container, garantindo cobertura total em qualquer posição.

### 🏝️ Porto Rico adicionado
- **Porto Rico** (ISO 630) incluído na base de dados com alias `puerto rico`.
- Aceito via toast "muito pequeno para aparecer no mapa" (o dataset 110m não inclui o polígono como entidade separada).

---

## 🗂️ Países no jogo

| Categoria | Qtd. |
|-----------|------|
| Com highlight no mapa | ~180 |
| Aceitos via toast (ilhas pequenas, microstados) | ~25 |
| **Total** | **~205** |

Países sem polígono no mapa 110m mas válidos no jogo incluem: Mônaco, Vaticano, Singapura, Nauru, Maldivas, Tuvalu, Tonga, Samoa, Kiribati, Ilhas Marshall, Palau, Micronésia, Seicheles, Maurício, Comores, Cabo Verde, São Tomé e Príncipe, Dominica, Granada, São Cristóvão e Névis, Santa Lúcia, São Vicente e Granadinas, Barbados, Jamaica, Trinidad e Tobago, Liechtenstein, San Marino, Kosovo e Porto Rico.

---

## 🛠️ Stack

- **D3.js v7** — projeção Natural Earth, zoom/pan, path rendering
- **TopoJSON client v3** — `world-atlas 110m`
- **Vanilla JS + CSS** — zero frameworks, single `.html` file
- **Google Fonts** — Cinzel + Space Mono

---

## 🐛 Correções

- Duplicatas na base de dados removidas (países com ISO repetido na seção de pequenos).
- Fundo do mapa não cobria a área completa ao fazer zoom/pan → corrigido.

---

## 📋 Como usar

Abra o arquivo `atlantis.html` diretamente no navegador. Nenhum servidor necessário.

```
# Desktop
Abra atlantis.html no Chrome, Firefox ou Safari

# Mobile
Sirva o arquivo via qualquer servidor HTTP local ou hospede no GitHub Pages
```

---

*Single-file game · Sem backend · Sem build step*
