# Source: https://vilcagamarracf.github.io/posts/02_formulas_metric

Tabla de Contenidos

- [¿Qué es LaTeX?](https://vilcagamarracf.github.io/posts/02_formulas_metric/#qu%c3%a9-es-latex)
- [Representando fórmulas en la web con MathJax](https://vilcagamarracf.github.io/posts/02_formulas_metric/#representando-f%c3%b3rmulas-en-la-web-con-mathjax)
- [Ejemplos](https://vilcagamarracf.github.io/posts/02_formulas_metric/#ejemplos)
 - [Índice de calidad del suelo ponderado (SQIw)](https://vilcagamarracf.github.io/posts/02_formulas_metric/#%c3%adndice-de-calidad-del-suelo-ponderado-sqiw)
 - [Funciones de puntuación (normalización de indicadores)](https://vilcagamarracf.github.io/posts/02_formulas_metric/#funciones-de-puntuaci%c3%b3n-normalizaci%c3%b3n-de-indicadores)
 - [Autocorrelación espacial](https://vilcagamarracf.github.io/posts/02_formulas_metric/#autocorrelaci%c3%b3n-espacial)
 - [Interpolación espacial](https://vilcagamarracf.github.io/posts/02_formulas_metric/#interpolaci%c3%b3n-espacial)
 - [Semivariograma empírico](https://vilcagamarracf.github.io/posts/02_formulas_metric/#semivariograma-emp%c3%adrico)
 - [Kriging de regresión](https://vilcagamarracf.github.io/posts/02_formulas_metric/#kriging-de-regresi%c3%b3n)
 - [Ponderación por distancia inversa (IDW)](https://vilcagamarracf.github.io/posts/02_formulas_metric/#ponderaci%c3%b3n-por-distancia-inversa-idw)
 - [Métricas de validación cruzada](https://vilcagamarracf.github.io/posts/02_formulas_metric/#m%c3%a9tricas-de-validaci%c3%b3n-cruzada)
 - [Hidrología y Teledetección: Modelo METRIC](https://vilcagamarracf.github.io/posts/02_formulas_metric/#hidrolog%c3%ada-y-teledetecci%c3%b3n-modelo-metric)
 - [Balance de energía superficial](https://vilcagamarracf.github.io/posts/02_formulas_metric/#balance-de-energ%c3%ada-superficial)
 - [Radiación neta en la superficie](https://vilcagamarracf.github.io/posts/02_formulas_metric/#radiaci%c3%b3n-neta-en-la-superficie)
 - [Flujo de calor del suelo](https://vilcagamarracf.github.io/posts/02_formulas_metric/#flujo-de-calor-del-suelo)
 - [Flujo de calor sensible](https://vilcagamarracf.github.io/posts/02_formulas_metric/#flujo-de-calor-sensible)
 - [Cálculo de la evapotranspiración](https://vilcagamarracf.github.io/posts/02_formulas_metric/#c%c3%a1lculo-de-la-evapotranspiraci%c3%b3n)
- [Conclusiones](https://vilcagamarracf.github.io/posts/02_formulas_metric/#conclusiones)
- [Referencias](https://vilcagamarracf.github.io/posts/02_formulas_metric/#referencias)

## ¿Qué es LaTeX?[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#qu%C3%A9-es-latex)

LaTeX es un sistema de composición de textos de alta calidad, utilizado mayormente en documentos técnicos o científicos de todo tipo de tamaños y empleandose en cualquier formato editorial.

Es muy utilizado para la composición de artículos académicos, tesis y libros técnicos, donde la calidad tipográfica son comparables a la de una editorial científica de primera línea. Es considerado un programa profesional para creación de documentos donde su principal ventaja es que siempre generar un único resultado, el cual puede ser exportado a numerosos formatos. Tiene a su vez en cuenta numerosos aspectos tipográficos editables.

A pesar de ello, lo que nos trae aquí es una parte pequeña de ese universo, las fórmulas. Cuando redactamos un documento técnico científico hay momentos donde debemos presentar una fórmula. Usualmente se trabaja con Word ya que es el más común de todos al ser popular en el sistema Windows. A continuación te presento una forma sencilla de cómo usar la IA de ChatGPT para generar la fórmula y usarla en Word.

![alt text](https://vilcagamarracf.github.io/posts/02_formulas_metric/Prueba-2.gif)

Solo fue necesario copiarlo en una sección de ecuación y dar enter para obtener la fórmula en Word sin problemas. Ahora presentaré las fórmulas renderizadas en esta misma página.

## Representando fórmulas en la web con MathJax[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#representando-f%C3%B3rmulas-en-la-web-con-mathjax)

MathJax permite renderizar fórmulas LaTeX en la web, con la funcionalidad adicional de poder copiar la expresión para reutilizarla. Si necesitas usar la fórmula en Word o en un documento LaTeX, solo la copias y pegas donde lo necesites.

Si se tiene el código LaTeX para generar la fórmula del Root Mean Square Error (RMSE):

```latex
$$
\mathrm{RMSE} = \sqrt{\frac{1}{n}\sum_{i=1}^{n}(y_i - \hat{y}_i)^2}
$$
```

copiar

y su versión renderizada

RMSE\=1n∑i\=1n(yi−y^i)2

Para poder utilizar esta fórmula puedes dar click derecho sobre la fórmula renderizada, el cual abrirá un menú donde nos interesa el `Copy to Clipboard > TeX Commands`.

![alt text](https://vilcagamarracf.github.io/posts/02_formulas_metric/image-1.png#center)

## Ejemplos[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#ejemplos)

### Índice de calidad del suelo ponderado (SQIw)[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#%C3%ADndice-de-calidad-del-suelo-ponderado-sqiw)

Índice de Calidad del Suelo ponderado (weighted additive approach):

SQIw\=∑i\=1nWiNi

donde n es el número total de variables, Wi es el peso asignado a cada indicador (derivado del Análisis de Componentes Principales ACP), y Ni es el puntaje normalizado del indicador. El índice resultante se clasifica en cinco categorías con intervalos iguales de 0.2:

| Clase | Rango SQIw |
| --- | --- |
| Muy pobre | < 0.20 |
| Pobre | 0.20 – 0.40 |
| Aceptable | 0.40 – 0.60 |
| Bueno | 0.60 – 0.80 |
| Óptimo | ≥ 0.80 |

Expresión específica del SQIw para el valle de Bella Unión:

SQIw\=0.212SECe+0.204SpH+0.177SKav+0.160SSand+0.123SOM+0.123SPav

donde Si representa el puntaje normalizado (0.1–1) de cada indicador.

#### Funciones de puntuación (normalización de indicadores)[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#funciones-de-puntuaci%C3%B3n-normalizaci%C3%B3n-de-indicadores)

Función “más es mejor” (_more is better_):

M(x)\={0.1si x<x10.1+0.9x−x1x2−x1si x1≤x≤x21si x\>x2

Función “menos es mejor” (_less is better_):

L(x)\={1si x<x11−0.9x−x1x2−x1si x1≤x≤x20.1si x\>x2

donde M(x) y L(x) son las funciones de puntuación, con valores restringidos entre 0.1 y 1.0. x es el valor medido del indicador, y x1, x2 son los valores umbral (puntos de inflexión) de la curva.

### Autocorrelación espacial[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#autocorrelaci%C3%B3n-espacial)

Índice I de Moran (Moran, 1950):

I\=n∑i\=1n∑j\=1nwij⋅∑i\=1n∑j\=1nwij(yi−y¯)(yj−y¯)∑i\=1n(yi−y¯)2

donde n es el número de observaciones, wij es el peso espacial entre las muestras i y j, yi es el valor muestreado en la localización i, y y¯ es la media aritmética de todos los valores muestreados. I∈\[−1,+1\]: valores positivos indican agrupamiento espacial, valores cercanos a cero indican distribución aleatoria, y valores negativos indican dispersión.

### Interpolación espacial[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#interpolaci%C3%B3n-espacial)

#### Semivariograma empírico[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#semivariograma-emp%C3%ADrico)

γ(h)\=12E\[z(x)−z(x+h)\]2

donde E representa la varianza esperada, y z(x), z(x+h) son pares de valores separados por la distancia h.

#### Kriging de regresión[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#kriging-de-regresi%C3%B3n)

Predicción por kriging de regresión en la localización S0:

Z(S0)\=m(S0)+e(S0)\=∑k\=1pβkqk(S0)+∑i\=1Nλie(Si)

donde βk son los coeficientes de regresión asociados a p covariables qk, λi son los pesos de kriging, N es el número de observaciones, y e(Si) son los residuos de la regresión en cada punto Si.

#### Ponderación por distancia inversa (IDW)[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#ponderaci%C3%B3n-por-distancia-inversa-idw)

y^p\=∑i\=1nyidir∑i\=1n1dir

donde y^p es el valor predicho en el punto no muestreado p; yi es el valor observado en el punto muestreado i; di es la distancia entre los puntos p e i; r es el parámetro de potencia (fijado en r\=2); y n es el número de puntos vecinos usados para la interpolación (máximo 12).

### Métricas de validación cruzada[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#m%C3%A9tricas-de-validaci%C3%B3n-cruzada)

Raíz del error cuadrático medio (RMSE):

RMSE\=1n∑i\=1n(yi−y^i)2

Error absoluto medio (MAE):

MAE\=1n∑i\=1n|yi−y^i|

Coeficiente de determinación (R2):

R2\=1−∑i\=1n(yi−y^i)2∑i\=1n(yi−y¯)2

Error medio (ME, sesgo):

ME\=1n∑i\=1n(yi−y^i)

donde yi es el valor observado en la localización i, y^i es el valor predicho mediante validación cruzada, y y¯ es la media de todos los valores observados.

### Hidrología y Teledetección: Modelo METRIC[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#hidrolog%C3%ADa-y-teledetecci%C3%B3n-modelo-metric)

Mapping evapotranspiration at high resolution with internalized calibration (METRIC) es un modelo de procesamiento de imágenes satelitales para calcular la evapotranspiración (ET) como residuo del balance energético superficial (Allen et al., 2007). Este modelo tiene fórmulas interesantes de representar. A continuación presentaré algunas de las más importantes:

#### Balance de energía superficial[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#balance-de-energ%C3%ADa-superficial)

LE\=Rn−G−H

#### Radiación neta en la superficie[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#radiaci%C3%B3n-neta-en-la-superficie)

Rn\=(1−α)RS↓+(RL↓−RL↑)−(1−ε0)RL↓

donde:

- Rn : Flujo de radiación neta
- α : Albedo de superficie \[−\]
- RS↓ : Radiación de onda corta entrante
- RL↓ : Radiación de onda larga entrante
- RL↑ : Radiación de onda larga saliente
- ϵ0 : Emisividad del ancho de banda en la superficie

El término (1−ϵ0)RL↓ representa la fracción de radiación entrante de onda larga (incoming long-wave radiation) reflejada desde la superficie. Todas las radiaciones se miden en Wm−2.

#### Flujo de calor del suelo[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#flujo-de-calor-del-suelo)

GRn\=(Ts−273.15)(0.0038+0.0074α)(1−0.98NDVI4)(26)

donde:

- Ts : Temperatura de la superficie \[K\]
- α : Albedo de la superficie \[−\]

#### Flujo de calor sensible[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#flujo-de-calor-sensible)

H\=ρairCpdTrah

donde:

- ρair: Air density \[kgm−3\]
- Cp: Air specific heat
- dT: Temperature difference (T1 - T2) between two heights (z1 and z2)
- rah: Aerodynamic resistance to heat transport

#### Cálculo de la evapotranspiración[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#c%C3%A1lculo-de-la-evapotranspiraci%C3%B3n)

ET instantánea en el momento de la imagen satelital:

ETinst\=3600⋅LEλρw

Calor latente de vaporización:

λ\=(2.501−0.00236(Ts−273.15))×106

## Conclusiones[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#conclusiones)

El disponer estas fórmulas en este blog permite reutilizarlas en futuros trabajos que requieran dichos análisis permitiendo agilizar con los detalles finales. Invito al lector a aprender un poco más sobre LaTeX ya que es una forma de obtener resultados de estilo publicación, el cual le da una mejor presentación.

## Referencias[#](https://vilcagamarracf.github.io/posts/02_formulas_metric/#referencias)

Sitios web

- The LaTeX Project: An introduction to LaTeX. [Enlace](https://www.latex-project.org/about/)
- Universidad de Alicante: Herramientas para la investigación - ¿Qué es LaTeX?. [Enlace](https://desarrolloweb.dlsi.ua.es/cursos/2015/herramientas-investigacion/que-es-latex)
- MathJax - Beautiful and accessible math in all browsers. [Enlace](https://www.mathjax.org/)

Artículos científicos

- Poma-Chamana, R., Vilca-Gamarra, C., Hermoza, N., Mercado, R., Mejía, S., Rengifo, R., & Quispe, K. (2025). Estimation and mapping of soil fertility index in arid agricultural environments of the Tambo Valley using regression kriging. _Frontiers in Soil Science_, 5, 1706974. [Enlace](https://doi.org/10.3389/fsoil.2025.1706974)
- Poma-Chamana, R., Vilca-Gamarra, C., Linares-Escapa, S., Puma-Huacani, K., Carrillo, A., Villalta-Soto, M., & Quispe, K. (2026). Soil Quality in Olive Orchards of Southern Peru Using a Weighted Soil Quality Index (SQIw): Constraints by Salinity, Organic Matter and Sustainable Management Approach. _Frontiers in Soil Science_, 6, 1724235. [Enlace](https://doi.org/10.3389/fsoil.2026.1724235)
- Allen, R. G., Tasumi, M., & Trezza, R. (2007). Satellite-based energy balance for mapping evapotranspiration with internalized calibration (METRIC)—Model. _Journal of irrigation and drainage engineering_, 133(4), 380-394. [Enlace](https://www.researchgate.net/publication/228615269_Satellite-Based_Energy_Balance_for_Mapping_Evapotranspiration_With_Internalized_Calibration_METRIC_-_Model)

---

Muchas gracias por leer. Te invito a revisar los demás posts mediante los tags aquí abajo.