Este proyecto implementa y evalúa una red inalámbrica experimental basada en la tecnología de Espacios en Blanco de Televisión (TVWS), utilizando dispositivos Innonet configurados en una topología MASTER-SLAVE. El objetivo principal es validar la funcionalidad de esta tecnología, comprender sus requerimientos técnicos y regulatorios, y demostrar su potencial para proporcionar conectividad en zonas rurales o con baja infraestructura.

## Objetivos
### Objetivo General
Evaluar el funcionamiento y la configuración de una red inalámbrica experimental basada en tecnología TVWS, utilizando dispositivos Innonet en una arquitectura punto-a-punto.

### Objetivos Específicos
- Diseñar e implementar un enlace inalámbrico TVWS mediante la configuración de nodos Master y Slave.
- Configurar parámetros técnicos como potencia, canal, ancho de banda y direcciones IP.
- Verificar la conectividad y calidad de la señal transmitida.

### Tecnología TVWS
Los Espacios en Blanco de Televisión (TVWS) son segmentos del espectro radioeléctrico (470–698 MHz en Colombia) que quedaron disponibles tras la transición de la televisión analógica a digital. Esta tecnología destaca por su capacidad de propagación a largas distancias y atravesar obstáculos, lo que la hace ideal para zonas rurales.

### Componentes del Sistema
- **Nodo MASTER**: Punto principal de conexión a internet (IP: 192.168.100.1).
- **Nodo SLAVE**: Receptor que redistribuye la señal a usuarios finales (IP: 192.168.1.1).
- **Antenas direccionales**: Utilizadas para transmisión a larga distancia.
- **Sistema de gestión web (LuCI/OpenWrt)**: Interfaz para configurar parámetros de red.
- 
### Hardware Utilizado
- Dos dispositivos Innonet TVWS (uno como Master y otro como Slave).
- Antenas monopolo de 900 MHz (compatibles con UHF).

### Software Implementado
- Interfaz web LuCI basada en OpenWrt.
- Protocolo DHCP para asignación automática de direcciones IP.

**Configuración del Nodo MASTER**:
   - Conexión física y asignación de IP estática (192.168.100.1).
   - Acceso a la interfaz LuCI para configurar modo Master.

**Configuración del Nodo SLAVE**:
   - Cambio de modo a Slave y ajuste de parámetros para coincidir con el Master (mismo SSID y canal).

3. **Verificación del Enlace**:
   - Monitoreo de LEDs y métricas como RSSI (-76 en Master, -61 en Slave).
   - Pruebas de conectividad.
