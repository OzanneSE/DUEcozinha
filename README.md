# DUE Restaurante · Ferramentas Ozanne

> **Técnica · Território · Resultado**

Kit de ferramentas de gestão gastronômica desenvolvido para o **DUE Restaurante** — Jardim Europa, Aracaju/SE.  
Chef Curador: **François R. Vargas Ozanne** · Ozanne Consultoria · Maio 2026

---

## Ferramentas Disponíveis

### 01 · [Grimório de Bases](grimorio.html)
Fichas técnicas completas das 44 bases de produção do DUE.

| | |
|---|---|
| **Fichas** | 44 |
| **Categorias** | 8 (Massa Fresca, Crocantes, Sobremesas, Fundos, Bases Transversais, Proteínas, Purês & Guarnições, Cremes & Emulsões) |
| **Flags** | D-1 Obrigatório · Assinatura DUE · Novas |
| **Funcionalidades** | Busca por texto, filtro por flag, sidebar de navegação, fichas expansíveis |

**Categorias de bases:**
- `B01–B07` Massa fresca e crocantes
- `B08–B10` Sobremesas (Torta Basca, Namelaka 70°, Passion)
- `B11–B15` Fundos e caldos
- `B16–B33` Bases transversais (azeites, emulsões, molhos, massas)
- `B34–B38` Proteínas (Polvo, Costela, Carne de Sol, Confit de Pato, Charque)
- `B39–B42` Purês e guarnições
- `B43–B44` Cremes e emulsões

---

### 02 · [Fichas de Pratos & CMV Dashboard](cmv.html)
Gestão de CMV por prato com dashboard em tempo real.

| | |
|---|---|
| **Pratos** | 11 (D01–D11) |
| **Categorias** | Entrada · Massa · Principal · Sobremesa |
| **Dashboard** | CMV% por prato e por categoria, métricas de receita/custo/lucro |
| **Exportação** | CSV (separador `;`, UTF-8 BOM) · XLSX (3 abas) |
| **Persistência** | Dados salvos no `localStorage` do navegador |

**Pratos do cardápio:**
| Cód | Prato | Categoria | Bases |
|-----|-------|-----------|-------|
| D01 | Tartar do Sertão | Entrada | B32·B16·B03·B36 |
| D02 | Croqueta de Polvo DUE | Entrada | B34·B27 |
| D03 | Toast de Costela DUE | Entrada | B35·B22 |
| D04 | Pappardelle de Costela | Massa | B01·B35·B22·B12 |
| D05 | Rigatone DUE | Massa | B35·B22·B23 |
| D06 | Filé do Sertão | Principal | B36·B12·B42·B38 |
| D07 | Confit de Pato DUE | Principal | B37·B40·B30 |
| D08 | Arroz de Polvo DUE | Principal | B34·B33·B43·B25 |
| D09 | Torta Basca | Sobremesa | B08 |
| D10 | Namelaka 70° | Sobremesa | B09·B05·B30 |
| D11 | Passion | Sobremesa | B10 |

**Código de cores CMV:**
- 🟢 Verde — CMV dentro do target
- 🟡 Âmbar — CMV até 15% acima do target
- 🔴 Vermelho — CMV acima de 15% do target

---

## Estrutura do Repositório

```
/
├── index.html        ← Hub principal (esta página)
├── grimorio.html     ← Grimório de Bases v5.0
├── cmv.html          ← Fichas de Pratos & CMV Dashboard
└── README.md
```

## Como Usar

**Localmente:** Abra `index.html` em qualquer navegador. Não requer servidor.

**GitHub Pages:** Vá em `Settings → Pages → Source: main branch → / (root)`. O site fica disponível em `https://[usuario].github.io/[repositório]`.

**CMV Dashboard:** Os dados de custos e preços são salvos no `localStorage` do navegador — persistem entre sessões mas ficam no dispositivo local. Para compartilhar dados, use o export XLSX.

---

## Dependências Externas (CDN)

O grimório não tem dependências. O CMV Dashboard carrega via CDN:

| Biblioteca | Versão | Uso |
|---|---|---|
| React | 18 | Interface |
| Recharts | 2.12.7 | Gráficos CMV |
| SheetJS (xlsx) | 0.18.5 | Export XLSX |
| Babel Standalone | latest | Compilação JSX no navegador |
| Google Fonts | — | Tipografia (Cormorant Garamond · DM Sans · IBM Plex Mono) |

---

## Em Desenvolvimento

- **03 · POPs de Cozinha** — Procedimentos Operacionais Padrão para as 4 funções da brigada
- **04 · Matriz de Precificação** — CMV progressivo em 3 fases com simulações

---

## Identidade Visual

```
Obsidian   #111009   ██  Fundo principal
Gold       #C8A030   ██  Destaque / acentos
Terracota  #8C4A2F   ██  Itálicos / alertas
Cream      #F8F6F0   ██  Fundo claro
```

Tipografia: **Cormorant Garamond** (display) · **DM Sans** (corpo) · **IBM Plex Mono** (dados/códigos)

---

*DUE Restaurante · Jardim Europa · Aracaju · Sergipe*  
*Ozanne Consultoria © 2026 · Chef François R. Vargas Ozanne*
