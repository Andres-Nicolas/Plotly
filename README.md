<h1 style="text-align:center;">🐍✨ Plotly en Google Colab 🚀✨</h1>

<p style="text-align:center;">Aprende a usar Plotly en Google Colab para crear gráficos interactivos directamente desde tu navegador. 🌟</p>

<h2>🚀 Requisitos Previos</h2>
<ul>
  <li>Acceso a <a href="https://colab.research.google.com/" target="_blank">Google Colab</a> 🌐</li>
  <li>Conexión a internet para instalar bibliotecas y visualizar gráficos interactivos 📡</li>
</ul>

<h2>🌟 Paso 1: Configuración Inicial</h2>
<p>Primero, instala Plotly en tu entorno de Colab ejecutando el siguiente comando en una celda de código:</p>
<pre>
<code>
# Instalar Plotly en Google Colab
!pip install plotly
</code>
</pre>

<h2>🌟 Paso 2: Primer Gráfico con Plotly Express</h2>
<p>Crea un gráfico interactivo básico para probar la instalación. Usa los siguientes comandos:</p>
<pre>
<code>
# Importa Plotly Express
import plotly.express as px

# Crea un conjunto de datos simple
data = {
    "Nombres": ["A", "B", "C", "D"],
    "Valores": [10, 15, 7, 12]
}

# Crear un DataFrame
import pandas as pd
df = pd.DataFrame(data)

# Generar un gráfico de barras
fig = px.bar(df, x="Nombres", y="Valores", title="Gráfico de Barras Básico")
fig.show()
</code>
</pre>

<h2>🌟 Paso 3: Explorando Gráficos Adicionales</h2>
<p>Prueba otros tipos de gráficos interactivos:</p>

<h3>🚀 Gráfico de Dispersión</h3>
<pre>
<code>
fig = px.scatter(df, x="Nombres", y="Valores", title="Gráfico de Dispersión")
fig.show()
</code>
</pre>

<h3>🚀 Gráfico de Líneas</h3>
<pre>
<code>
fig = px.line(df, x="Nombres", y="Valores", title="Gráfico de Líneas")
fig.show()
</code>
</pre>

<h2>🌟 Paso 4: Personalización con Graph Objects</h2>
<p>Si necesitas personalizar más tus gráficos, puedes usar <code>plotly.graph_objects</code>. Aquí tienes un ejemplo:</p>
<pre>
<code>
import plotly.graph_objects as go

# Crear un gráfico de barras personalizado
fig = go.Figure(data=[
    go.Bar(name='Grupo 1', x=['A', 'B', 'C'], y=[10, 20, 15]),
    go.Bar(name='Grupo 2', x=['A', 'B', 'C'], y=[12, 18, 8])
])
fig.update_layout(title="Gráfico de Barras Agrupadas", barmode='group')
fig.show()
</code>
</pre>

<h2>✨ Paso 5: Exportando Gráficos</h2>
<p>Para guardar un gráfico como imagen, utiliza el siguiente código:</p>
<pre>
<code>
# Guardar el gráfico como archivo HTML
fig.write_html("grafico.html")

# Descarga directa en Google Colab
from google.colab import files
files.download("grafico.html")
</code>
</pre>

<h2>🚀 Recursos Adicionales</h2>
<ul>
  <li>📖 <a href="https://plotly.com/python/" target="_blank">Documentación Oficial de Plotly</a></li>
  <li>🌐 <a href="https://colab.research.google.com/" target="_blank">Google Colab</a></li>
  <li>⭐ <a href="https://github.com/plotly/" target="_blank">Repositorio de Plotly en GitHub</a></li>
  <li>📗 <a href="https://colab.research.google.com/drive/1xYy-example-example-id" target="_blank">Ejemplo práctico en Google Colab</a> 🚀</li>
</ul>

<h2>👨‍💻 Integrantes</h2>
<ul>
  <li>👓 Andrés Nicolás Rodríguez Bustos 🧠</li>
  <li>👓 Adrian Camilo Gonzalez Riveros 🧠</li>
  <li>👓 Giankarlo Rojas Delgado 🧠</li>
</ul>
