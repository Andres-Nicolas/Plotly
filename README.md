<h1>Guía para Principiantes: Plotly</h1>

<p>Plotly es una biblioteca de Python para crear gráficos interactivos de alta calidad, útil para análisis de datos y visualización. Esta guía te ayudará a comenzar con los conceptos básicos.</p>

<h2>Instalación</h2>
<pre>
<code>
pip install plotly    # Instala la biblioteca Plotly
</code>
</pre>

<h2>Primeros Pasos</h2>
<p>Importa la biblioteca y crea un gráfico básico:</p>
<pre>
<code>
import plotly.express as px

# Datos de ejemplo
data = {
    "Nombres": ["A", "B", "C", "D"],
    "Valores": [10, 15, 7, 12]
}

# Crear un DataFrame
import pandas as pd
df = pd.DataFrame(data)

# Crear un gráfico de barras
fig = px.bar(df, x="Nombres", y="Valores", title="Gráfico de Barras Básico")
fig.show()
</code>
</pre>

<h2>Conceptos Básicos</h2>
<p>Plotly ofrece dos módulos principales para gráficos:</p>

<ul>
  <li><strong>plotly.graph_objects (go):</strong> Permite un control más detallado sobre los gráficos.</li>
  <li><strong>plotly.express (px):</strong> Simplifica la creación de gráficos comunes.</li>
</ul>

<h3>Gráficos Básicos con Plotly Express</h3>
<pre>
<code>
# Gráfico de dispersión
fig = px.scatter(df, x="Nombres", y="Valores", title="Gráfico de Dispersión")
fig.show()

# Gráfico de líneas
fig = px.line(df, x="Nombres", y="Valores", title="Gráfico de Líneas")
fig.show()
</code>
</pre>

<h3>Gráficos Personalizados con Graph Objects</h3>
<pre>
<code>
import plotly.graph_objects as go

fig = go.Figure(data=[
    go.Bar(name='Grupo 1', x=['A', 'B', 'C'], y=[10, 20, 15]),
    go.Bar(name='Grupo 2', x=['A', 'B', 'C'], y=[12, 18, 8])
])
fig.update_layout(title="Gráfico de Barras Agrupadas", barmode='group')
fig.show()
</code>
</pre>

<h2>Funciones Avanzadas</h2>
<ul>
  <li><strong>Interactividad:</strong> Los gráficos de Plotly son interactivos por defecto. Puedes hacer zoom, desplazar y guardar gráficos como imágenes.</li>
  <li><strong>Subplots:</strong> Permiten combinar varios gráficos en uno.</li>
  <li><strong>Integración:</strong> Compatible con Dash, Jupyter Notebooks y otras herramientas de visualización.</li>
</ul>

<h3>Ejemplo: Gráfico de Subplots</h3>
<pre>
<code>
from plotly.subplots import make_subplots

fig = make_subplots(rows=1, cols=2, subplot_titles=("Gráfico 1", "Gráfico 2"))

fig.add_trace(go.Bar(x=['A', 'B', 'C'], y=[10, 20, 15], name="Gráfico 1"), row=1, col=1)
fig.add_trace(go.Line(x=['A', 'B', 'C'], y=[15, 10, 20], name="Gráfico 2"), row=1, col=2)

fig.update_layout(title="Ejemplo de Subplots")
fig.show()
</code>
</pre>

<h2>Recursos Adicionales</h2>
<ul>
  <li><a href="https://plotly.com/python/">Documentación Oficial</a></li>
  <li><a href="https://dash.plotly.com/">Dash: Framework para Apps Interactivas</a></li>
  <li><a href="https://github.com/plotly/">Repositorio Oficial en GitHub</a></li>
</ul>

<h2>Contribuye o Mejora</h2>
<p>Si encuentras útil esta guía, siéntete libre de sugerir mejoras o agregar ejemplos avanzados en este repositorio. ¡Gracias por aprender con nosotros!</p>
