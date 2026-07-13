# Consola Z

**Instrumento de cálculo para ingeniería eléctrica**, pensado para resolver a mano (pero sin errores de aritmética) los problemas típicos de circuitos, fasores y sistemas nodal/mallas.

Todo corre en un único archivo HTML, sin instalación ni backend: se abre en el navegador y ya.

[![Ver demo en vivo](https://img.shields.io/badge/demo-en%20vivo-6EFFC0?style=for-the-badge)](https://jesusp2702.github.io/consola_z/Consola%20Z_V2.html)
![HTML](https://img.shields.io/badge/HTML-100%25-orange?style=flat-square)
![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square)
![Sin build](https://img.shields.io/badge/build-no%20requerido-6EFFC0?style=flat-square)

### 🔗 [Abrir Consola Z](https://jesusp2702.github.io/consola_z/Consola%20Z_V2.html)

---

## Contenido

- [Módulos](#-módulos)
- [Notación soportada](#-notación-soportada)
- [Stack técnico](#️-stack-técnico)
- [Cómo usarlo](#-cómo-usarlo)
- [Diseño responsivo](#-diseño-responsivo)
- [Autor](#-autor)

---

## ✨ Módulos

| Módulo | Qué hace |
|---|---|
| **Números complejos** | Operaciones binarias (+, −, ×, ÷) entre dos complejos, en modo rectangular o polar, con diagrama de Argand del resultado. |
| **Impedancias serie/paralelo** | Combina una lista de impedancias en serie o paralelo; incluye un submódulo para evaluar una **expresión de red completa** (`(Z1+Z2)∥Z3 + (Z4+Z5)∥Z6`). |
| **Componentes (f, L, C → jX)** | Traza paso a paso "estilo libro de texto": cada R, L o C se convierte en su impedancia según la frecuencia de trabajo y se va acumulando en serie/paralelo con lo anterior. |
| **Fasores V/I** | Suma fasorial de tensiones o corrientes con diagrama vectorial y suma punta-cola. |
| **Regulación / Máquina** | Cálculo de regulación de voltaje con su triángulo de caída en el diagrama fasorial. |
| **Matrices complejas** | Operaciones entre matrices A y B, y resolución de sistemas **Y·V = I** (nodal) o **Z·I = V** (mallas) de orden n×n, con verificación del resultado. |

Todos los módulos comparten el mismo parser de números complejos y aceptan celdas con **expresiones**, no solo literales: `13-5j+10`, `5∠30 + 2∠-45`, `(3+4j)*2`, `10∥(5+5j)`.

## 🧮 Notación soportada

- Rectangular: `3+4j`, `3-4i`, `-5j`, `2`
- Polar libre en un solo campo: `5∠30`, `5∠30°`, `5<30`
- `i` y `j` son intercambiables como unidad imaginaria
- Operador de paralelo: `∥`, `//` o `||`

## 🛠️ Stack técnico

- **React 18** (UMD, vía CDN)
- **Babel Standalone** — compila el JSX directamente en el navegador, sin paso de build
- **math.js** — aritmética compleja, matrices y determinantes
- Un solo archivo `.html`: sin `npm install`, sin bundler, sin backend

## 🚀 Cómo usarlo

**La forma más simple:** entra directo a la demo en vivo, sin instalar nada:

👉 **https://jesusp2702.github.io/consola_z/Consola%20Z_V2.html**

**Localmente:** descarga o clona el repo y abre el archivo en tu navegador:

```bash
git clone https://github.com/jesusp2702/consola_z.git
cd consola_z
```

Luego abre `Consola Z_V2.html` con doble clic, o sirviéndolo con cualquier servidor estático:

```bash
python3 -m http.server 8000
# y visita http://localhost:8000
```

> Necesita conexión a internet la primera vez, ya que React, Babel y math.js se cargan desde CDN.

## 📱 Diseño responsivo

La interfaz es horizontal en escritorio y se reorganiza en columna vertical (pestañas, grillas y filas de campos) en pantallas menores a 760px, para uso cómodo desde el celular.

## 👤 Autor

Hecho por **Jesús Peña** — UNEFA LARA.
Instrumento hecho con apoyo de Anthropic (Claude).
