Código Node-Red del dispositivo IoT embarcado en el vehículo.

Los flujos están escritos desde el nulo conocimiento inicial de Node-Red y el escaso tiempo disponible por lo que por favor disculpe si no son "elegantes" ni eficientes ( seguramente hay formas más elegantes y eficientes de hacer lo mismo).

Esta versión está configurada (por facilidad en el desarrollo y depuración) para PC Windows, siendo migrable de forma muy sencilla a cualquier dispositivo
capaz de ejecutar Node-red (como Raspberry pi) sin más que cambiar la configuración de nodos que gestionan los puertos serie.

Se ha obtado por lo anterior en lugar de emplear el M5Stick al no disponer este de conectividad Bluetooth ( sí dispone, pero requiere un cambio de
firmware no compatible con UIFlow). Adicionalmente, la unidad GPS facilitada para el concurso no funcionaba* y se optó por obtener las coordenadas 
geográficas, etc a través de una App Android corriendo en un teléfono móvil.
La unidad GPS facilitada para el concurso aunque respondía con la fecha-hora, no devolvía datos de posición geográfica. Se intentó no sólo con 
M5Stick, sino también con Raspberry-Pi, conectando los pines del puerto serie (TX-RX-GND) del módulo GPS a los correspondientes (RX-TX-GND) en Raspberry-Pi,
con el mismo resultado: las sentencias NMEA devueltas no contenían latitud, longitud,... 

Se trata de una versión "Prueba de Concepto" con código no refinado y con simulación de datos en lugar de emplear dispositivos OBD-II ELM-327 o similares (pero implementando la 
adquisición de datos del vehículo mediante el (sencillísimo) protocolo serie que implementan.
