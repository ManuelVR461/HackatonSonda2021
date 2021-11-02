## DESAFIO SONDA HACKATHON 2021

### 3OMEGA



# INTEGRANTES
- DANIEL VERDUGO
- MANUEL RAMIREZ
- RAFAEL ALVAREZ

# Solicitud
Se requiere revisar mensaje de error al insertar documentos en la tabla tractoventadec.

# Análisis
En revisión de archivos de logs se detecta que en este caso hubo perdida del código del financiador que se tomaba de la sesión, lo que derivo en un error en el SQL que inserta los registros en tabla tractoventadec

# Solución
Se realizó cambio en la forma en que se obtiene el código del financiador, ahora se toma de la página y no de la sesión.

# Información Técnica
- [x] Instalación de código via Capistrano
- [ ] Build and install via Jenkins
- [ ] Configuración Puppet
- [ ] Cambio de configuración manual/Crontab
- [ ] Creación/Modificación de Tablas
- [ ] Creación/Modificación procedimiento almacenado

# Roll Back
Volver a la versión anterior.

# QA
Se deben realizar pruebas de emisión de bonos con seguros configurado con los atributos de Salud para Todos y hacer pruebas de adjuntar documentos.
