# Visualización de distancias genéticas: Heatmap y Clustermap

Este repositorio contiene los scripts utilizados para generar gráficos de **heatmap** y **clustermap** a partir de una matriz de distancias genéticas obtenida mediante **MEGA**.  
Los códigos forman parte del análisis visual desarrollado en la tesis de pregrado *“[Título de la tesis]”* y permiten reproducir los gráficos utilizados en la sección de Resultados.

---

# Contenido del repositorio

- **`heatmap_clustermap.ipynb`**  
  Notebook de Python que procesa la matriz de distancias y genera gráficos de heatmap y clustermap.

- **`GeneticDistanceMatrix.csv`** (opcional)  
  Ejemplo de la matriz de distancias genéticas exportada desde MEGA.

- **`figures/`**  
  Carpeta donde se almacenan las imágenes generadas.

---

# Datos de entrada

Los scripts utilizan como insumo una matriz de distancias genéticas exportada desde **MEGA** en formato `.csv`.  
El archivo debe presentar:

- Filas y columnas con los nombres de las muestras.
- Valores de distancia genética.
- Celdas superiores o inferiores vacías (MEGA genera una matriz triangular); el código reconstruye una matriz simétrica.

Ejemplo de formato:
,Sample1,Sample2,Sample3,...
Sample1,0,0.12,0.18,...
Sample2,,0,0.15,...
Sample3,,,0,...


---

## 🛠️ Dependencias

Los códigos están escritos en Python 3 e incluyen las siguientes librerías:

- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`

Puedes instalarlas con:

```bash
pip install pandas numpy seaborn matplotlib
