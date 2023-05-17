# BaufestGPT
Homemade LLMs :)

Agregar la OpenAI APIKey a la linea 22 de baufest_llm_v0.py


Encender la app: streamlit run baufest_llm_v0.py

## Steps:

1) Importar las bibliotecas necesarias: El código importa varias bibliotecas y módulos que se utilizarán en el script. Estos incluyen os para interactuar con el sistema operativo, OpenAI para utilizar el modelo de lenguaje de OpenAI, streamlit para crear la interfaz de usuario, PyPDFLoader para cargar y dividir documentos PDF, Chroma para almacenar y buscar vectores, y varias herramientas para trabajar con el almacén de vectores.

2) Establecer la clave API de OpenAI: El código establece la clave API de OpenAI como una variable de entorno. Esta clave se utiliza para autenticar las solicitudes a la API de OpenAI.

3) Crear una instancia del modelo de lenguaje de OpenAI: El código crea una instancia del modelo de lenguaje de OpenAI con una temperatura de 0.1 (que afecta a la aleatoriedad de las respuestas del modelo) y habilita la salida detallada.

4) Cargar y dividir el documento PDF: El código crea una instancia de PyPDFLoader con el nombre del archivo PDF, luego carga y divide el documento en páginas.

5) Cargar los documentos en Chroma: El código carga las páginas del documento en una instancia de Chroma, que es un tipo de almacén de vectores. Esto permite buscar eficientemente las páginas que son similares a una consulta dada.

6) Crear un objeto VectorStoreInfo: Este objeto contiene metadatos sobre el almacén de vectores, incluyendo su nombre, una descripción y la instancia de Chroma.

7) Crear un VectorStoreToolkit: Este toolkit se utiliza para interactuar con el almacén de vectores.

8) Crear un VectorStoreAgent: Este agente utiliza el modelo de lenguaje y el toolkit para generar respuestas basadas en la entrada del usuario.

9) Configurar la interfaz de usuario de Streamlit: El código crea un título para la aplicación, una caja de texto para la entrada del usuario y una sección para mostrar la respuesta del modelo de lenguaje. También hay un expander que muestra la página más relevante del documento basándose en la entrada del usuario.

10) Responder a la entrada del usuario: Cuando el usuario introduce una consulta, el código pasa la consulta al modelo de lenguaje para generar una respuesta y realiza una búsqueda de similitud en el almacén de vectores para encontrar la página más relevante. Luego muestra la respuesta y el contenido de la página en la interfaz de usuario.
