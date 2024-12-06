<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Uso de Plotly en Google Colab</title>
</head>
<body>
    <h1>Uso de Plotly en Google Colab</h1>
    <p>Esta guía explica cómo instalar y utilizar <strong>Plotly</strong> en <strong>Google Colab</strong> para crear gráficos interactivos desde cero.</p>

    <h2>¿Qué es Plotly?</h2>
    <p>Plotly es una biblioteca de Python que permite crear gráficos interactivos y visualizaciones de datos atractivas, ideales para análisis exploratorio o presentación de resultados.</p>

    <hr>

    <h2>Guía paso a paso</h2>

    <h3>1. Abre Google Colab</h3>
    <ol>
        <li>Ve a <a href="https://colab.research.google.com/" target="_blank">Google Colab</a>.</li>
        <li>Crea un nuevo cuaderno haciendo clic en <strong>"Nuevo cuaderno"</strong>.</li>
    </ol>

    <h3>2. Instala Plotly</h3>
    <p>En la primera celda de tu cuaderno, ejecuta el siguiente comando para instalar Plotly:</p>
    <pre><code>!pip install plotly</code></pre>

    <h3>3. Importa Plotly</h3>
    <p>Importa las bibliotecas necesarias con el siguiente código:</p>
    <pre><code>import plotly.express as px
import plotly.graph_objects as go
</code></pre>

    <h3>4. Crea tu primer gráfico</h3>
    <p>Prueba un gráfico básico de dispersión usando el dataset de iris integrado en Plotly:</p>
    <pre><code># Datos de ejemplo
data = px.data.iris()

# Gráfico de dispersión interactivo
fig = px.scatter(data, x="sepal_width", y="sepal_length", color="species",
                 title="Gráfico de dispersión - Iris Dataset")
fig.show()
</code></pre>
    <p>Al ejecutar este código, verás un gráfico interactivo donde puedes hacer zoom, desplazarte y explorar datos.</p>

    <h3>5. Prueba gráficos avanzados</h3>
    <p>Aquí tienes un ejemplo de gráfico de barras con personalización:</p>
    <pre><code># Gráfico de barras
fig = go.Figure(data=[
    go.Bar(name='Producto A', x=['Enero', 'Febrero', 'Marzo'], y=[20, 14, 23]),
    go.Bar(name='Producto B', x=['Enero', 'Febrero', 'Marzo'], y=[12, 18, 29])
])

# Personalización
fig.update_layout(title="Ventas Mensuales", barmode='group')
fig.show()
</code></pre>

    <h3>6. Guarda o comparte tu gráfico</h3>
    <p>Si deseas descargar tu gráfico como un archivo HTML:</p>
    <pre><code>fig.write_html("grafico.html")</code></pre>
    <p>Para descargarlo en tu dispositivo:</p>
    <pre><code>from google.colab import files
files.download("grafico.html")
</code></pre>

    <hr>

    <h2>Recursos adicionales</h2>
    <ul>
        <li><a href="https://plotly.com/python/" target="_blank">Documentación oficial de Plotly</a></li>
        <li><a href="https://colab.research.google.com/" target="_blank">Google Colab</a></li>
    </ul>

    <hr>
    <p>¡Comienza a explorar y crea gráficos interactivos increíbles con Plotly en Google Colab! 🎉</p>
</body>
</html>
