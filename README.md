# Tráfico en Avenida
Autor: Lizbeth Maribel Melendez Delgado A01232559
## Descripción
Simulación de una avenida de dos carriles (sentido contrario), que cuenta con un paso peatonal en el cual hay un semáforo que permite a los peatones detener el trafico. Este semáforo se mantiene en verde hasta que el peatón presiona un botón, después pasa a amarillo y luego a rojo por cierto periodo de tiempo.


## Funcionamiento
### Simulación con AgentPy
Código:

En la simulación se cuenta con dos agentes: auto y semáforo.
| Agentes | Propiedades | 
|---------|-------------|
| Auto    | direccion, posicion, velocidad, estado |
| Semáforo | direccion, posicion, estado |

Se modelan como agentes reactivos, por lo tanto sus acciones estan definidas por la situación en la que se encuentran. Reaccionan de la siguiente manera dependiendo de la situación:

| Situación | Acción |
|-----------|--------|
|Si hay un auto delante |El auto se detiene|
|Si más adelante hay un auto|El auto  frena|
|Si el semáforo esta en amarillo y se encuentro cerca del semáforo|El auto acelera|
|Si el semáforo está en amarillo y se encuentra lejos del semáforo|El auto frena|
|Si el semáforo esta en rojo|El auto se detiene|

### Aplicación gráfica con Three.js
Código:
Para la interfaz gráfica donde se visualizan los resultados de la simulación se toma en cuenta lo siguiente. Se cuenta con clases que representan los elementos de como:
- Cámara
- Piso
- Ejes
- Semáforo
- Carro
- Edificios
- Carretera, banqueta y cruce
- Escenario

Cuenta con un menús que permiten al usuario modificar ciertos parametros de los componentes:
1. Menu de escena  
![1_scene_menu](https://user-images.githubusercontent.com/57516503/143173005-83a425a4-7493-44c7-aa2a-2535f9b59970.gif)

2. Menu de camara  
![2_camara_menu](https://user-images.githubusercontent.com/57516503/143173070-f1deae15-76ad-46e4-a39c-28fd74116a06.gif)

3. Menu de modelo  
![3_model_menu](https://user-images.githubusercontent.com/57516503/143173077-580c0579-545e-45ca-b2e1-50014d8acca3.gif)

## Resultados
Como resultado de la simulación con AgentPy se obtiene un archivo json con la información de los agentes y en la aplicación gráfica se obtiene como resultado la visualización de esos datos. 
![4_result](https://user-images.githubusercontent.com/57516503/143173362-7a97ce63-0cec-4b03-9390-a286df3c78a0.gif)



