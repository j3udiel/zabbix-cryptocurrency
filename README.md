# Plantilla de Zabbix para la Monitorización de Criptomonedas

Esta plantilla de Zabbix está diseñada para monitorizar diversas métricas relacionadas con criptomonedas. Utiliza la API de diversas plataformas de intercambio y datos financieros para obtener información actualizada y precisa sobre los precios, volúmenes de transacción y otros datos relevantes de criptomonedas.

## Requisitos

- Zabbix Server 5.0 o superior
- Acceso a la API de la plataforma de intercambio de criptomonedas
- Python 3.6 o superior (si se utiliza un script externo para la integración con la API)

## Contenidos de la Plantilla

### Items Monitorizados

La plantilla incluye los siguientes ítems para monitorizar:

1. **Precio actual del Bitcoin (BTC)**
2. **Precio actual de Ethereum (ETH)**
3. **Volumen de transacción de las últimas 24 horas (BTC)**
4. **Volumen de transacción de las últimas 24 horas (ETH)**
5. **Capitalización de mercado total (BTC)**
6. **Capitalización de mercado total (ETH)**

Nota: si cambias la macro {$CURRENCY} y pon las currency que quieras de coingekko para que se auto descubran las que quieras.

### Triggers

La plantilla incluye triggers para alertar sobre:

- Caídas significativas en el precio de BTC y ETH
- Incrementos significativos en el volumen de transacción
- Disminución en la capitalización de mercado

### Gráficos y Pantallas

Se han configurado gráficos y pantallas para visualizar:

- Evolución del precio de BTC y ETH
- Volumen de transacción a lo largo del tiempo
- Capitalización de mercado

## Instalación

1. **Importar la Plantilla en Zabbix:**
   - Acceda a la interfaz web de Zabbix.
   - Vaya a **Configuración** > **Plantillas**.
   - Haga clic en **Importar**.
   - Seleccione el archivo `zbx_export_templates.yaml` y haga clic en **Importar**.

2. **Configurar Macros:**
   - Una vez importada la plantilla, configure las macros necesarias para acceder a la API de la plataforma de intercambio de criptomonedas. Esto incluye la clave API y cualquier otro parámetro requerido.

3. **Asociar la Plantilla a un Host:**
   - Vaya a **Configuración** > **Hosts**.
   - Seleccione el host al que desea asociar la plantilla.
   - En la pestaña **Plantillas**, haga clic en **Seleccionar** y elija la plantilla de criptomonedas.

## Uso

- **Monitoreo Automático:** La plantilla comenzará a recopilar datos automáticamente una vez asociada a un host.
- **Alertas:** Configure sus preferencias de notificación en Zabbix para recibir alertas vía email, SMS u otros métodos.
- **Visualización:** Utilice los gráficos y pantallas preconfigurados para una visualización intuitiva de las métricas.

## Personalización

Si necesita monitorizar otras criptomonedas o añadir métricas adicionales, puede modificar la plantilla YAML y añadir los nuevos ítems y triggers según sus necesidades.

## Soporte

Para soporte adicional, por favor visite el [foro de Zabbix](https://www.zabbix.com/forum) o contacte al autor de la plantilla.
