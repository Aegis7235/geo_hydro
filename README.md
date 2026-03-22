# 🗺️ Atlas Topográfico e Hidrológico Profissional

Sistema profissional de cartografia interativa com análise hidrológica pelo método **SCS-CN**, relevo 3D, curvas de nível e delimitação automática de bacias hidrográficas.

🔗 **[Acessar o projeto](https://aegis7235.github.io/geo_hydro/)**

---

## ✨ Funcionalidades

- 🏔️ **Relevo 3D** com terrain exaggeration e hillshade
- 📏 **Curvas de nível** com cotas a cada 100 m e 500 m
- 🏢 **Edifícios 3D** extrudados por altura real
- 🛰️ **Camada de satélite** sobreposta ao mapa base
- 🌊 **Rios, lagos e oceanos** com estilos temáticos
- 🖊️ **Desenho de polígonos** interativo no mapa
- 💧 **Cálculo hidrológico** pelo método SCS-CN (Runoff Curve Number)
- 🔍 **Delimitação automática de bacias** por ponto de exutório
- 🎨 **4 temas visuais**: Pergaminho, Magma, Esmeralda e MDT

---

## 🧮 Método SCS-CN

O modelo **Soil Conservation Service Curve Number** (USDA, 1972) é utilizado para estimar o escoamento superficial a partir de dados de precipitação e uso do solo. O sistema calcula:

- Precipitação efetiva (Q)
- Volume de escoamento
- Pico de vazão (método racional)
- Classificação de risco hidrológico

Grupos hidrológicos de solo suportados: **A, B, C e D**

Tipos de uso do solo suportados: Floresta, Pastagem, Urbano, Misto e Solo Exposto

---

## 🛠️ Tecnologias utilizadas

| Tecnologia | Uso | Licença |
|---|---|---|
| [MapLibre GL JS](https://maplibre.org/) | Renderização do mapa interativo | BSD 3-Clause |
| [Turf.js](https://turfjs.org/) | Cálculos geoespaciais (área, perímetro, centroide) | MIT |
| [MapTiler](https://www.maptiler.com/) | Tiles de terreno RGB, curvas de nível, edifícios e satélite | Comercial (plano free) |
| [OpenFreeMap](https://openfreemap.org/) | Mapa base vetorial (estilo Liberty) | ODbL / MIT |
| [mghydro Watershed API](https://mghydro.com/) | Delimitação automática de bacias hidrográficas | Público / gratuito |
| [Font Awesome 6](https://fontawesome.com/) | Ícones da interface | CC BY 4.0 (free) |
| [Google Fonts](https://fonts.google.com/) | Tipografias Cinzel, EB Garamond, IM Fell English | OFL |

---

## 🔐 Configuração de chaves API

O projeto usa a API do **MapTiler**, que requer uma chave pessoal. A chave **não está exposta no repositório** — ela é injetada via GitHub Actions no momento do deploy.

Para rodar localmente, substitua `__MAPTILER_KEY__` no `index.html` pela sua chave obtida em [maptiler.com](https://www.maptiler.com/).

---

## 🚀 Deploy

O projeto é publicado automaticamente via **GitHub Actions** a cada push na branch `main`. O workflow está em `.github/workflows/deploy.yml`.

Para configurar no seu fork:

1. Crie o secret `MAPTILER_KEY` em **Settings → Secrets and variables → Actions**
2. Ative o GitHub Pages na branch `gh-pages` em **Settings → Pages**
3. Faça push na `main` — o deploy ocorre automaticamente

---

## 📄 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

---

*Desenvolvido com foco em cartografia profissional e análise hidrológica aplicada ao território brasileiro.*
