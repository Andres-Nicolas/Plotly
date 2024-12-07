<h1 style="text-align:center;">🐍✨Plotly 🚀✨</h1>

<p style="text-align:center;">Plotly es una poderosa biblioteca de Python para crear gráficos interactivos. Esta guía paso a paso te ayudará a comenzar con tus propias visualizaciones como todo un profesional. 🚀</p>

<h2>🚀 Instalación</h2>
<pre>
<code>
pip install plotly    # Instala la biblioteca Plotly
</code>
</pre>

<h2>🐍 Primeros Pasos</h2>
<p>Importa la biblioteca y crea tu primer gráfico interactivo. ¡Es más fácil de lo que imaginas! 🌟</p>
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

<h2>✨ Conceptos Básicos</h2>
<p>Plotly ofrece dos módulos principales para crear gráficos interactivos:</p>

<ul>
  <li><strong>plotly.graph_objects (go):</strong> 🛠️ Para control detallado y gráficos personalizados.</li>
  <li><strong>plotly.express (px):</strong> 🚀 Para gráficos simples y rápidos con menos código.</li>
</ul>

<h3>🌟 Gráficos Básicos con Plotly Express</h3>
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

<h3>🛠️ Gráficos Personalizados con Graph Objects</h3>
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

<h2>✨ Funciones Avanzadas</h2>
<ul>
  <li>🌟 <strong>Interactividad:</strong> Los gráficos son interactivos por defecto. Haz zoom, desplaza y guarda tus gráficos como imágenes.</li>
  <li>🚀 <strong>Subplots:</strong> Combina varios gráficos en uno.</li>
  <li>🐍 <strong>Integración:</strong> Compatible con Dash, Jupyter Notebooks y otras herramientas de visualización.</li>
</ul>

<h3>🌟 Ejemplo: Gráfico de Subplots</h3>
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

<h2>🌟 Recursos Adicionales</h2>
<ul>
  <li>📖 <a href="https://plotly.com/python/" target="_blank">Documentación Oficial</a></li>
  <li>🚀 <a href="https://dash.plotly.com/" target="_blank">Dash: Framework para Apps Interactivas</a></li>
  <li>⭐ <a href="https://github.com/plotly/" target="_blank">Repositorio Oficial en GitHub</a></li>
</ul>

