# mapeado_naive

práctica de mapeadfo naive, actualizando el mapa suponiendo que se conoce perfectamente la posición del robot

## Instalación

Si no tienes un *workspace* de ROS creado, créalo ahora:

```bash
mkdir rob_mov_ws
cd rob_mov_ws
mkdir src
cd src
```
puedes copiar el repositorio actual como un *package* dentro de la carpeta `src` del *workspace* creado:

```bash
git clone https://github.com/ottocol/mapeado_naive
```
y ahora compila el *workspace* y actualiza las variables de entorno para incluirlo

```bash
cd .. #ahora deberías estar en el directorio base del workspace (rob_mov_ws)
catkin_make
source devel/setup.bash
```
## Uso

Para poner en marcha el simulador `stage` junto con `rviz` para visualizar sistemas de coordenadas y mapa:

```bash
roslaunch mapeado_naive mapeado_naive.launch  
```
El mundo simulado en stage está definido en `worlds/ejemplo.world`. Se puede modificar el error de odometría cambiando la línea que comienza por `odom_error`. Los valores numéricos son las desviaciones típicas del error en `x`, `y`, `z`  y orientación
