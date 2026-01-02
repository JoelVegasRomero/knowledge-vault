# Ciclo de vida de la ingenieria de datos 

## Conceptos Clave
La tecnologia es Secundaria, hay que en focarnos en la calidad de los datos. 

## Flujo 
Generacion --> Almacenamiento --> Ingestion --> Transformacion --> Servicio
Aparte Tenemos los **underccurrents** el cual engloba a: 
Seguridad, Gestion de Datos, Operaciones de datos, arquitectura de Datos, orquestacion de datos e ingieneria de software

**Flujo**: Ingestion de Datos -> Servicio (Esto permite que el agua se vaya moviendo por al tuberia)
**Seguridad Undercurrent**: Seguridad, Orquestacion ... (Esto hace referencia a la presion del agua los filtros de agua ... sin ello la tuberia explotaria)

## El "Por Que"
Debido a que no importa que tan bien este hecho el codigo si los datos luego no nos sirven para nada, es como hacer una **tuberia super (Tecnologia)** bonita pero luego no da **agua potable (Objetivo Final)**

**Idempotencia (Concepto Pro):** El objetivo final ("agua potable") debe ser el mismo sin importar cuántas veces abras el grifo.
**Seguridad como Undercurrent:** No es un paso final, es algo que debe estar presente desde la Generación hasta el Servicio.


## 🌐 Traducción al Ámbito Laboral (Del "Agua" al "Dato")

| Concepto de Agua | Realidad Técnica (Ingeniería de Datos) |
| :--- | :--- |
| **Agua Potable** | **Data Value:** Datos limpios, precisos y listos para tomar decisiones (ej. un reporte de ventas sin errores). |
| **Tubería Bonita** | **Pipeline / Stack:** El código (Python, SQL) y las herramientas (Airflow, Kafka) que usamos. |
| **Idempotencia** | **Retry Logic:** Si un proceso falla y lo reinicio, no duplica datos. El resultado final es siempre el mismo. |
| **Filtros / Presión** | **Transformación / Orquestación:** Limpiar el ruido del dato y asegurar que cada paso ocurre en el orden correcto. |

### 🔄 El Ciclo de Vida Real (Ejemplo de uso)
1. **Generación:** Un cliente hace click en "Comprar".
2. **Ingestión:** Capturamos ese click (log) y lo movemos hacia nuestro sistema.
3. **Almacenamiento:** Guardamos el click en un "Data Lake" (S3, Google Cloud Storage).
4. **Transformación:** Convertimos el log bruto en una fila con: `ID_Usuario`, `Precio`, `Producto`.
5. **Servicio:** El jefe de ventas ve en su pantalla que las ventas han subido un 5%.