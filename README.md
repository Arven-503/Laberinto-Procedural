Laberinto Procedural con DFS y BFS

Este proyecto implementa un videojuego de laberinto creado de forma procedimental en Python mediante la biblioteca pygame-ce. El sistema emplea dos algoritmos esenciales de búsqueda en grafos:

1. Búsqueda en Profundidad (DFS): Utilizado para construir la estructura principal del mapa garantizando que todas las áreas queden interconectadas.
2. Búsqueda en Anchura (BFS): Implementado para calcular la trayectoria óptima hasta el objetivo y ofrecer asistencia visual temporal al usuario.

Requisitos Previos

Para ejecutar este software se requiere tener instalado:

* Python 3.8 o superior.
* Biblioteca pygame-ce.

Instalación de Dependencias

Paso 1: Creación y activación del entorno virtual (Opcional, recomendado)

En sistemas Windows:
python -m venv .venv
..venv\Scripts\activate

En sistemas Linux o macOS:
python3 -m venv .venv
source .venv/bin/activate

Paso 2: Instalación de pygame-ce

Ejecute el siguiente mandato en su consola:
pip install pygame-ce

Si utiliza el gestor de paquetes uv:
uv pip install pygame-ce

Ejecución del Programa

Asegúrese de hallarse en el directorio donde se ubica el fichero principal (ejemplo: try.py) y ejecute:

python try.py

En caso de utilizar un entorno virtual sin activación previa:
..venv\Scripts\python.exe try.py

Controles de la Aplicación

* Teclas de Dirección o W, A, S, D: Desplazar al personaje por los corredores del laberinto.
* Tecla H: Activar la guía visual que traza el camino más breve (calculado por BFS) durante 3 segundos.
* Tecla R: Reiniciar la partida y generar un nuevo mapa procedimental.
* Tecla ENTER: Comenzar un nuevo nivel tras alcanzar la pantalla de victoria.

Estructura del Proyecto

* generar_laberinto(filas, cols): Ejecuta el algoritmo DFS con retroceso (backtracking) sobre una matriz bidimensional y posteriormente elimina el 10 por ciento de los muros internos para originar ciclos y rutas alternativas.
* buscar_camino_bfs(laberinto, inicio, meta): Implementa una estructura de Cola (FIFO) para explorar el mapa por niveles y reconstruir la secuencia mínima de pasos hasta el destino.
* Clase Juego: Administra la lógica de estados, detección de colisiones, temporizadores y renderizado gráfico de los componentes en pantalla.