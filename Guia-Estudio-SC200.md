# Base de conocimientos SC-200

Base de conocimientos SC-200 · Preparada el 5 de octubre de 2026 a partir del banco de 468 ejercicios. Estudia el razonamiento, no solo la letra de una respuesta. Los ejemplos KQL son didácticos: adáptalos al esquema y a los datos de tu entorno.

El PDF contiene nombres y herramientas de versiones anteriores. Azure AD se denomina Microsoft Entra ID; Microsoft 365 Defender, Microsoft Defender XDR; Azure Security Center, Microsoft Defender for Cloud; Microsoft Cloud App Security, Microsoft Defender for Cloud Apps. La guía oficial consultada ya presenta objetivos para el 21 de octubre de 2026, una fecha posterior a la preparación de esta base. Los conceptos del bloque Actualizaciones del temario son complementos del temario publicado; verifica la versión que corresponda a la fecha e idioma de tu examen.

[Guía oficial y fecha de objetivos](https://learn.microsoft.com/es-es/credentials/certifications/resources/study-guides/sc-200)

## Cómo estudiar

Marca un concepto como dominado cuando puedas explicarlo, resolver su autoevaluación y justificar la elección en una pregunta nueva. El progreso personal no predice una puntuación de examen.

1. Fundamentos e ingesta: explica el flujo desde el origen hasta la tabla y resuelve fallos de recopilación.
2. KQL: escribe filtros, agregaciones, relaciones y consultas de evidencia sin mirar soluciones.
3. Detecciones y automatización: elige regla, ventana, entidades, permisos y acción para cada escenario.
4. Defender e identidades: reconstruye un ataque y distingue investigar, contener y remediar.
5. Correo, Purview y Cloud: relaciona el problema con el servicio y el tipo de evidencia adecuados.
6. Repaso: vuelve a las preguntas que fallaste y explica por qué cada alternativa incorrecta no cumple el requisito.

## Método para resolver escenarios

Identifica el objetivo y las restricciones → localiza la fuente de datos → elige servicio o tabla → comprueba permisos y ámbito → evalúa efectos → descarta opciones que no cumplen alguna condición. En selección múltiple, cada respuesta debe aportar una parte necesaria de la solución. En ordenaciones, respeta dependencias; en asociaciones, comprueba ambos lados.

## 1. SIEM, XDR y SOAR — Fundamentos del SOC

Sentinel centraliza y analiza señales de muchas fuentes. Defender XDR correlaciona señales de los productos Defender. SOAR añade orquestación y respuesta automática.

- SIEM: recopilación, búsqueda y detección entre fuentes.
- XDR: investigación y respuesta entre dispositivos, identidades, correo y aplicaciones.
- SOAR: automatizar un flujo de respuesta con condiciones, acciones y permisos.

**Error frecuente:** Un panel de visualización no ejecuta por sí mismo una respuesta.

**Autoevaluación:** Debes bloquear una IP tras investigar un incidente: ¿basta un workbook?

**Respuesta razonada:** No. El workbook sirve para visualizar; una automatización o una acción de respuesta debe ejecutar el bloqueo.

Ejercicios relacionados del banco: 10 (pregunta PDF 10, pág. 78), 18 (pregunta PDF 18, pág. 94), 55 (pregunta PDF 55, pág. 169), 78 (pregunta PDF 78, pág. 215), 99 (pregunta PDF 99, pág. 273,274,275,276,277,278,279), 124 (pregunta PDF 124, pág. 336), 132 (pregunta PDF 132, pág. 352), 174 (pregunta PDF 174, pág. 436).

## 2. Evento, alerta, incidente y entidad — Fundamentos del SOC

Un evento registra actividad. Una alerta señala una condición que merece atención. Un incidente reúne alertas y evidencias relacionadas para investigar un posible ataque.

- Entidad: usuario, dispositivo, IP, archivo u otro objeto de investigación.
- Reconstruye la secuencia temporal y las relaciones entre entidades.
- Documenta clasificación, responsable, acciones y evidencias al cerrar.

**Error frecuente:** Varias alertas no implican necesariamente varios ataques independientes.

**Autoevaluación:** ¿Qué investigarías si una alerta de correo precede una ejecución sospechosa?

**Respuesta razonada:** El incidente completo: mensaje, destinatario, URL o adjunto, proceso ejecutado, dispositivo y actividad posterior.

Ejercicios relacionados del banco: 1 (pregunta PDF 1, pág. 60), 3 (pregunta PDF 3, pág. 64), 4 (pregunta PDF 4, pág. 66), 6 (pregunta PDF 6, pág. 70), 8 (pregunta PDF 8, pág. 74), 13 (pregunta PDF 13, pág. 84), 23 (pregunta PDF 23, pág. 104), 25 (pregunta PDF 25, pág. 108).

## 3. Triage, severidad y clasificación — Fundamentos del SOC

El triage decide qué ocurrió, a quién afecta y qué hacer primero. La severidad técnica y la prioridad operativa pueden diferir.

- Valida evidencia, alcance, exposición y criticidad del activo.
- Distingue ataque real, actividad legítima que activó una detección y detección errónea.
- Contén cuando corresponda; conserva evidencia y verifica la recuperación.

**Error frecuente:** Cerrar una alerta sin revisar las entidades relacionadas puede ocultar un ataque de varias etapas.

**Autoevaluación:** ¿Una alerta de severidad baja puede requerir atención inmediata?

**Respuesta razonada:** Sí, si afecta un activo crítico o forma parte de una cadena de ataque mayor.

Ejercicios relacionados del banco: 50 (pregunta PDF 50, pág. 159), 83 (pregunta PDF 83, pág. 225), 188 (pregunta PDF 188, pág. 464), 199 (pregunta PDF 199, pág. 488), 222 (pregunta PDF 222, pág. 534).

## 4. AMA, Azure Arc y DCR — Ingesta en Sentinel

AMA recopila telemetría; una DCR define qué recopilar y dónde enviarlo. Azure Arc incorpora servidores externos a la administración de Azure.

- Comprueba instalación, asociación de DCR, destino y permisos.
- Arc y AMA cumplen funciones distintas: administrar una máquina no garantiza recibir sus registros.
- El agente Log Analytics heredado MMA/OMS se retiró el 31 de agosto de 2024.

**Error frecuente:** Las respuestas antiguas del PDF sobre MMA no son una recomendación para una implementación nueva.

**Autoevaluación:** ¿Basta instalar Azure Arc para recibir eventos de seguridad?

**Respuesta razonada:** No. Debes configurar la recopilación correspondiente, por ejemplo AMA y su DCR.

Ejercicios relacionados del banco: 12 (pregunta PDF 12, pág. 82), 49 (pregunta PDF 49, pág. 157), 64 (pregunta PDF 65, pág. 187), 70 (pregunta PDF 70, pág. 199), 71 (pregunta PDF 71, pág. 201), 72 (pregunta PDF 72, pág. 203), 75 (pregunta PDF 75, pág. 209), 79 (pregunta PDF 79, pág. 217).

[Documentación de referencia](https://learn.microsoft.com/en-us/azure/sentinel/ama-migrate)

## 5. Eventos de Windows y filtros XPath — Ingesta en Sentinel

El conector y la regla de recopilación determinan qué eventos de Windows llegan al workspace. XPath permite seleccionar eventos en origen.

- 4624: inicio de sesión correcto; 4625: intento fallido.
- Comprueba el canal, los EventID y los filtros solicitados.
- WEF centraliza eventos de varias máquinas en un recopilador; luego necesitas la integración con Sentinel.

**Error frecuente:** Filtrar en una consulta reduce resultados; filtrar en la recopilación reduce lo ingerido.

**Autoevaluación:** Necesitas únicamente intentos fallidos: ¿qué identificador buscarías?

**Respuesta razonada:** EventID 4625. Comprueba también el alcance y la configuración del conector.

Ejercicios relacionados del banco: 18 (pregunta PDF 18, pág. 94), 49 (pregunta PDF 49, pág. 157), 55 (pregunta PDF 55, pág. 169), 88 (pregunta PDF 88, pág. 235), 95 (pregunta PDF 95, pág. 258), 132 (pregunta PDF 132, pág. 352), 193 (pregunta PDF 193, pág. 474), 235 (pregunta PDF 235, pág. 560).

## 6. Syslog, CEF y CommonSecurityLog — Ingesta en Sentinel

Syslog transporta mensajes; CEF aporta un formato de eventos de seguridad. Muchos dispositivos de red se integran mediante un recopilador Linux.

- Selecciona facility y nivel de severidad conforme al requisito.
- Comprueba el envío del dispositivo, el servicio del recopilador, AMA y la DCR.
- Syslog y CommonSecurityLog son tablas distintas: identifica dónde llegó el evento.

**Error frecuente:** Instalar el agente sin configurar el emisor y la recopilación no completa el flujo.

**Autoevaluación:** ¿Dónde buscarías normalmente eventos CEF de un firewall?

**Respuesta razonada:** En CommonSecurityLog, después de comprobar la configuración del conector.

Ejercicios relacionados del banco: 268 (pregunta PDF 268, pág. 627), 343 (pregunta PDF 342, pág. 784), 364 (pregunta PDF 363, pág. 830), 371 (pregunta PDF 370, pág. 844), 380 (pregunta PDF 379, pág. 865), 381 (pregunta PDF 380, pág. 867), 382 (pregunta PDF 381, pág. 869), 438 (pregunta PDF 437, pág. 1031).

## 7. Conectores, soluciones y diagnóstico — Ingesta en Sentinel

Un conector incorpora datos. Una solución de Content Hub puede aportar conectores, reglas, consultas, workbooks y automatizaciones.

- Instalar una solución no activa necesariamente todas sus conexiones y reglas.
- AzureActivity describe operaciones del plano de administración; SigninLogs y AuditLogs sirven para actividad de identidad según el conector.
- Los registros de recursos pueden requerir configuración de diagnóstico hacia Log Analytics.

**Error frecuente:** Una suscripción conectada no implica que cada servicio ya envíe todos sus registros.

**Autoevaluación:** ¿Por qué una tabla puede estar vacía después de instalar una solución?

**Respuesta razonada:** El conector no está configurado, no hay actividad, faltan permisos o la ingesta aún no se ha completado.

Ejercicios relacionados del banco: 18 (pregunta PDF 18, pág. 94), 65 (pregunta PDF 65, pág. 189), 86 (pregunta PDF 86, pág. 231), 96 (pregunta PDF 96, pág. 260), 100 (pregunta PDF 100, pág. 281,282,283,284,285,286,287), 132 (pregunta PDF 132, pág. 352), 151 (pregunta PDF 151, pág. 390), 167 (pregunta PDF 167, pág. 422).

## 8. Retención, planes y costes — Ingesta en Sentinel

Distingue volumen ingerido, retención, plan de tabla y capacidades de consulta. La alternativa más barata debe seguir cumpliendo los requisitos de detección e investigación.

- Analiza qué datos requieren detección rápida y cuáles se consultan ocasionalmente.
- Un nivel de compromiso afecta la facturación; no equivale a borrar datos.
- Un límite diario puede interrumpir la recopilación y reducir la visibilidad.

**Error frecuente:** No memorices una duración o precio antiguo sin revisar el plan y las condiciones del enunciado.

**Autoevaluación:** ¿Reducirías costes cortando la ingesta de eventos esenciales?

**Respuesta razonada:** No si esos eventos son necesarios para las detecciones exigidas. Revisa selección, volumen, retención y plan.

Ejercicios relacionados del banco: 8 (pregunta PDF 8, pág. 74), 122 (pregunta PDF 122, pág. 332), 271 (pregunta PDF 271, pág. 633), 275 (pregunta PDF 275, pág. 641), 339 (pregunta PDF 338, pág. 775), 392 (pregunta PDF 391, pág. 895), 415 (pregunta PDF 414, pág. 976), 448 (pregunta PDF 447, pág. 1054).

## 9. Reglas programadas y NRT — Detecciones

Una regla programada ejecuta una consulta a intervalos. NRT permite detección con menor demora, dentro de las capacidades y restricciones admitidas.

- Frecuencia: cada cuánto corre; ventana: qué intervalo examina.
- Configura umbral, entidades, agrupación y creación de incidentes.
- Considera retrasos de ingesta y duplicados al elegir frecuencia y ventana.

**Error frecuente:** Una ventana demasiado corta puede omitir eventos que llegan tarde.

**Autoevaluación:** ¿Frecuencia de cinco minutos significa analizar solo cinco minutos?

**Respuesta razonada:** No. La ventana de búsqueda se configura aparte y puede ser mayor.

Ejercicios relacionados del banco: 49 (pregunta PDF 49, pág. 157), 52 (pregunta PDF 52, pág. 163), 58 (pregunta PDF 58, pág. 175), 64 (pregunta PDF 65, pág. 187), 69 (pregunta PDF 69, pág. 197), 71 (pregunta PDF 71, pág. 201), 72 (pregunta PDF 72, pág. 203), 76 (pregunta PDF 76, pág. 211).

## 10. Entidades, agrupación y MITRE ATT&CK — Detecciones

El mapeo de entidades convierte columnas del resultado en objetos investigables. La agrupación decide cómo se presentan alertas e incidentes relacionados.

- Usa identificadores adecuados para usuarios, dispositivos e IP.
- MITRE relaciona detecciones con tácticas y técnicas del adversario.
- Revisa si agrupar por entidad y tiempo ayuda a reconstruir un mismo ataque.

**Error frecuente:** Una técnica MITRE describe comportamiento; no prueba por sí sola que exista compromiso.

**Autoevaluación:** ¿Por qué mapear la cuenta en una detección de fallos de acceso?

**Respuesta razonada:** Para correlacionar, investigar y automatizar acciones sobre la cuenta correcta.

Ejercicios relacionados del banco: 3 (pregunta PDF 3, pág. 64), 63 (pregunta PDF 63, pág. 185), 66 (pregunta PDF 67, pág. 191), 78 (pregunta PDF 78, pág. 215), 117 (pregunta PDF 117, pág. 322), 173 (pregunta PDF 173, pág. 434), 175 (pregunta PDF 175, pág. 438), 202 (pregunta PDF 202, pág. 494).

## 11. UEBA, anomalías e inteligencia de amenazas — Detecciones

UEBA busca comportamiento anómalo de usuarios y entidades. La inteligencia de amenazas aporta indicadores y contexto. La correlación de señales ayuda a detectar ataques de varias etapas.

- Una anomalía requiere validación contra contexto y actividad habitual.
- Para correlacionar debes disponer de las fuentes necesarias.
- Un indicador debe revisarse por tipo, vigencia, confianza y coincidencia.

**Error frecuente:** Una lista de indicadores no sustituye una regla que compare esos indicadores con tus eventos.

**Autoevaluación:** ¿Una IP conocida como maliciosa en tus registros confirma automáticamente un ataque?

**Respuesta razonada:** No. Revisa dirección del tráfico, momento, vigencia del indicador, entidad y evidencia adicional.

Ejercicios relacionados del banco: 99 (pregunta PDF 99, pág. 273,274,275,276,277,278,279), 175 (pregunta PDF 175, pág. 438), 240 (pregunta PDF 240, pág. 570), 255 (pregunta PDF 255, pág. 600), 260 (pregunta PDF 260, pág. 610), 273 (pregunta PDF 273, pág. 637), 291 (pregunta PDF 291, pág. 675), 296 (pregunta PDF 296, pág. 685).

## 12. Detecciones personalizadas en Defender — Detecciones

Una consulta de Advanced Hunting puede convertirse en detección. Debe conservar identificadores que permitan relacionar el resultado con el evento y la entidad.

- Para eventos de Endpoint, DeviceId y ReportId resultan relevantes para identificar el evento.
- Revisa los requisitos actuales de columnas y entidades según la tabla.
- Las detecciones continuas tienen restricciones de tablas y operadores; no toda consulta es apta.

**Error frecuente:** No apliques a todas las tablas una lista antigua de columnas o una ventana temporal memorizada.

**Autoevaluación:** ¿Qué riesgo tiene resumir eventos y eliminar sus identificadores?

**Respuesta razonada:** La detección puede no disponer de los datos necesarios para identificar evidencia o ejecutar acciones.

Ejercicios relacionados del banco: 1 (pregunta PDF 1, pág. 60), 10 (pregunta PDF 10, pág. 78), 34 (pregunta PDF 34, pág. 127), 115 (pregunta PDF 115, pág. 318), 124 (pregunta PDF 124, pág. 336), 152 (pregunta PDF 152, pág. 392), 161 (pregunta PDF 161, pág. 410), 288 (pregunta PDF 288, pág. 669).

[Documentación de referencia](https://learn.microsoft.com/en-us/defender-xdr/custom-detection-rules)

## 13. Supresión, ajuste y bloqueo — Detecciones

Ajustar o suprimir una detección reduce ruido. Bloquear modifica lo que puede ocurrir. Son decisiones con objetivos distintos.

- Investiga falsos positivos antes de crear una excepción.
- Limita la excepción por condiciones concretas y revisa su vigencia.
- Una regla de supresión no es una medida de contención.

**Error frecuente:** Silenciar una alerta sobre actividad maliciosa no elimina la amenaza.

**Autoevaluación:** ¿Qué harías con una herramienta legítima que activa una alerta repetidamente?

**Respuesta razonada:** Validaría su uso y ajustaría la detección con una excepción específica y documentada.

Ejercicios relacionados del banco: 1 (pregunta PDF 1, pág. 60), 31 (pregunta PDF 31, pág. 120), 34 (pregunta PDF 34, pág. 127), 62 (pregunta PDF 62, pág. 183), 63 (pregunta PDF 63, pág. 185), 66 (pregunta PDF 67, pág. 191), 69 (pregunta PDF 69, pág. 197), 97 (pregunta PDF 97, pág. 262).

## 14. Automation rules frente a playbooks — Automatización y permisos

La regla de automatización decide cuándo y bajo qué condiciones actuar. Un playbook, basado en Logic Apps, ejecuta un flujo de acciones e integraciones.

- Piensa en desencadenador → condiciones → acciones.
- Revisa orden, caducidad y alcance de reglas.
- Workbooks visualizan; playbooks ejecutan procesos.

**Error frecuente:** Crear un playbook no garantiza que Sentinel pueda invocarlo.

**Autoevaluación:** ¿Cómo etiquetar y notificar automáticamente ante un incidente concreto?

**Respuesta razonada:** Define condiciones en una regla de automatización y usa sus acciones o un playbook para la notificación.

Ejercicios relacionados del banco: 49 (pregunta PDF 49, pág. 157), 57 (pregunta PDF 57, pág. 173), 59 (pregunta PDF 59, pág. 177), 68 (pregunta PDF 69, pág. 195), 69 (pregunta PDF 69, pág. 197), 73 (pregunta PDF 73, pág. 205), 88 (pregunta PDF 88, pág. 235), 94 (pregunta PDF 94, pág. 256).

[Documentación de referencia](https://learn.microsoft.com/en-us/azure/sentinel/automation/run-playbooks)

## 15. Roles de Sentinel y ejecución de playbooks — Automatización y permisos

Reader permite consultar; Responder permite gestionar incidentes; Contributor permite configurar recursos y contenido de Sentinel. La ejecución de playbooks incorpora permisos adicionales.

- Playbook Operator permite ejecución manual según el ámbito otorgado.
- Automation Contributor se usa para autorizar a la identidad de servicio de Sentinel sobre los recursos de automatización.
- Configurar Logic Apps y ejecutar o administrar incidentes son capacidades diferentes.

**Error frecuente:** Comprueba tanto el rol como el ámbito: workspace, grupo de recursos y playbook no son intercambiables.

**Autoevaluación:** Puede ver incidentes pero no administrarlos: ¿qué capacidad falta?

**Respuesta razonada:** La de responder y gestionar incidentes, por ejemplo Sentinel Responder en el ámbito adecuado.

Ejercicios relacionados del banco: 6 (pregunta PDF 6, pág. 70), 7 (pregunta PDF 7, pág. 72), 9 (pregunta PDF 9, pág. 76), 10 (pregunta PDF 10, pág. 78), 12 (pregunta PDF 12, pág. 82), 19 (pregunta PDF 19, pág. 96), 20 (pregunta PDF 20, pág. 98), 21 (pregunta PDF 21, pág. 100).

[Documentación de referencia](https://learn.microsoft.com/en-us/azure/sentinel/roles)

## 16. Identidad administrada, Key Vault y mínimo privilegio — Automatización y permisos

Una identidad administrada permite a un recurso autenticarse sin incrustar secretos. Después necesita autorización para la operación concreta.

- Distingue autenticación, autorización y acceso de red.
- Concede permisos sobre el recurso y las operaciones necesarias.
- Verifica el modelo de acceso de Key Vault que indica el escenario.

**Error frecuente:** Que exista la identidad no implica que pueda leer un secreto o modificar un recurso.

**Autoevaluación:** La autenticación funciona pero leer un secreto falla: ¿qué revisarías?

**Respuesta razonada:** Permisos sobre secretos, ámbito, modelo de autorización y restricciones de red.

Ejercicios relacionados del banco: 28 (pregunta PDF 28, pág. 114), 45 (pregunta PDF 45, pág. 149), 56 (pregunta PDF 56, pág. 171), 96 (pregunta PDF 96, pág. 260), 99 (pregunta PDF 99, pág. 273,274,275,276,277,278,279), 104 (pregunta PDF 104, pág. 295), 160 (pregunta PDF 160, pág. 408), 166 (pregunta PDF 166, pág. 420).

## 17. Seleccionar la tabla correcta — KQL y hunting

La tabla se elige por el tipo de evidencia. Una consulta correcta sobre una tabla equivocada no responde la pregunta.

- DeviceProcessEvents: procesos; DeviceNetworkEvents: conexiones; DeviceFileEvents: archivos.
- DeviceLogonEvents: accesos en dispositivos; IdentityLogonEvents: autenticación de identidad.
- EmailEvents: correo; EmailAttachmentInfo: adjuntos; UrlClickEvents: clics; CloudAppEvents: actividad de aplicaciones.

**Error frecuente:** Una tabla sin datos puede indicar falta de servicio, ingesta o permisos, además de ausencia de actividad.

**Autoevaluación:** Quieres ver qué proceso abrió una conexión: ¿con qué tablas empezarías?

**Respuesta razonada:** DeviceNetworkEvents y, para ampliar el contexto del proceso, DeviceProcessEvents.

Ejercicios relacionados del banco: 1 (pregunta PDF 1, pág. 60), 7 (pregunta PDF 7, pág. 72), 34 (pregunta PDF 34, pág. 127), 40 (pregunta PDF 40, pág. 139), 115 (pregunta PDF 115, pág. 318), 121 (pregunta PDF 121, pág. 330), 145 (pregunta PDF 145, pág. 378), 149 (pregunta PDF 149, pág. 386).

[Documentación de referencia](https://learn.microsoft.com/en-us/defender-xdr/advanced-hunting-schema-tables)

## 18. Filtrar y proyectar — KQL y hunting

KQL transforma resultados mediante operadores separados por la barra vertical. Lee cada paso como una transformación de la tabla anterior.

- where filtra filas; project selecciona columnas.
- extend calcula columnas; distinct elimina combinaciones repetidas.
- Filtra temprano por tiempo y condiciones para reducir el conjunto de trabajo.

**Error frecuente:** project puede eliminar columnas que necesitarás después.

```kql
DeviceProcessEvents
| where Timestamp > ago(24h)
| where FileName =~ "powershell.exe"
| project Timestamp, DeviceName, ProcessCommandLine, DeviceId, ReportId
```

**Autoevaluación:** ¿Qué operador usarías para crear una columna calculada?

**Respuesta razonada:** extend.

Ejercicios relacionados del banco: 6 (pregunta PDF 6, pág. 70), 21 (pregunta PDF 21, pág. 100), 33 (pregunta PDF 33, pág. 125), 40 (pregunta PDF 40, pág. 139), 96 (pregunta PDF 96, pág. 260), 108 (pregunta PDF 108, pág. 303), 114 (pregunta PDF 114, pág. 316), 135 (pregunta PDF 135, pág. 358).

[Documentación de referencia](https://learn.microsoft.com/en-us/kusto/query/)

## 19. Tiempo, texto y tipos — KQL y hunting

Los nombres de columnas y los tipos importan. En muchos registros de Sentinel se usa TimeGenerated; en tablas de Defender se usa Timestamp.

- ago(1d) expresa un momento relativo; between limita un intervalo.
- has busca términos; contains busca subcadenas. Elige según el requisito.
- == distingue mayúsculas; =~ compara texto sin distinguirlas; convierte tipos cuando corresponda.

**Error frecuente:** No reemplaces automáticamente Timestamp por TimeGenerated en cualquier consulta.

**Autoevaluación:** Quieres buscar el ejecutable sin depender de mayúsculas: ¿qué comparación usarías?

**Respuesta razonada:** Por ejemplo FileName =~ "powershell.exe", sobre la columna y tabla correctas.

Ejercicios relacionados del banco: 20 (pregunta PDF 20, pág. 98), 40 (pregunta PDF 40, pág. 139), 68 (pregunta PDF 69, pág. 195), 134 (pregunta PDF 134, pág. 356), 145 (pregunta PDF 145, pág. 378), 150 (pregunta PDF 150, pág. 388), 161 (pregunta PDF 161, pág. 410), 207 (pregunta PDF 207, pág. 504).

## 20. summarize, count, dcount, bin y arg_max — KQL y hunting

summarize agrega registros. count cuenta filas; dcount estima valores distintos; bin agrupa en intervalos; arg_max devuelve la fila asociada al valor máximo.

- Usa by para definir grupos de agregación.
- Una serie por hora requiere bin del campo temporal.
- arg_max es útil para el último estado conocido de cada entidad.

**Error frecuente:** Contar eventos y contar usuarios únicos responde preguntas distintas.

```kql
SecurityEvent
| where TimeGenerated > ago(1d) and EventID == 4625
| summarize Intentos=count() by Account, bin(TimeGenerated, 1h)
| order by Intentos desc
```

**Autoevaluación:** Quieres el registro más reciente de cada equipo: ¿qué función ayuda?

**Respuesta razonada:** summarize arg_max(Timestamp, *) by DeviceId.

Ejercicios relacionados del banco: 6 (pregunta PDF 6, pág. 70), 21 (pregunta PDF 21, pág. 100), 108 (pregunta PDF 108, pág. 303), 135 (pregunta PDF 135, pág. 358), 161 (pregunta PDF 161, pág. 410), 248 (pregunta PDF 248, pág. 586), 316 (pregunta PDF 315, pág. 726), 370 (pregunta PDF 369, pág. 842).

## 21. join frente a union — KQL y hunting

join relaciona filas por claves. union combina conjuntos de filas. Debes controlar duplicados y el tipo de relación.

- inner: coincidencias; leftouter: conserva todas las filas izquierdas.
- leftanti: filas izquierdas sin coincidencia.
- innerunique deduplica el lado izquierdo; usa un tipo explícito si esa conducta cambia tu resultado.

**Error frecuente:** Un join puede multiplicar filas cuando hay varias coincidencias por clave.

**Autoevaluación:** Quieres dispositivos que no estén en una lista permitida: ¿qué relación usarías?

**Respuesta razonada:** Una exclusión por clave, por ejemplo join kind=leftanti con la lista de dispositivos permitidos.

Ejercicios relacionados del banco: 21 (pregunta PDF 21, pág. 100), 33 (pregunta PDF 33, pág. 125), 40 (pregunta PDF 40, pág. 139), 114 (pregunta PDF 114, pág. 316), 135 (pregunta PDF 135, pág. 358), 145 (pregunta PDF 145, pág. 378), 149 (pregunta PDF 149, pág. 386), 159 (pregunta PDF 159, pág. 406).

## 22. JSON, arrays y mv-expand — KQL y hunting

Muchos eventos contienen propiedades dentro de campos dinámicos. Primero interpreta el contenido y luego extrae o expande lo que necesitas.

- parse_json interpreta JSON; tostring convierte una propiedad a texto.
- mv-expand crea filas a partir de elementos de un array.
- extract permite capturar patrones de texto con una expresión regular.

**Error frecuente:** Expandir un array altera el número de filas y puede inflar un recuento posterior.

**Autoevaluación:** Un evento contiene tres destinatarios en un array: ¿qué ocurre al expandirlo?

**Respuesta razonada:** Puede producir tres filas. Debes ajustar la agregación si necesitas contar eventos originales.

Ejercicios relacionados del banco: 412 (pregunta PDF 411, pág. 962).

## 23. Series temporales y anomalías — KQL y hunting

Una serie temporal permite observar cambios y desviaciones a lo largo del tiempo. Define grupos, intervalo y tratamiento de valores ausentes.

- make-series construye una serie de valores por tiempo.
- Las funciones de análisis de series ayudan a detectar desviaciones.
- render representa el resultado; no genera por sí mismo una alerta.

**Error frecuente:** Un pico estadístico no equivale automáticamente a un ataque.

**Autoevaluación:** ¿Cómo validarías un pico de fallos de acceso?

**Respuesta razonada:** Compararía su contexto temporal, cuentas, origen, actividad habitual y otras señales.

Ejercicios relacionados del banco: 117 (pregunta PDF 117, pág. 322), 118 (pregunta PDF 118, pág. 324), 119 (pregunta PDF 119, pág. 326), 129 (pregunta PDF 129, pág. 346), 182 (pregunta PDF 182, pág. 452), 191 (pregunta PDF 191, pág. 470), 192 (pregunta PDF 192, pág. 472), 209 (pregunta PDF 209, pág. 508).

## 24. Watchlists e inteligencia de amenazas — KQL y hunting

Una watchlist aporta datos de referencia como activos críticos o listas permitidas. Los indicadores de amenazas aportan contexto de actividad potencialmente maliciosa.

- _GetWatchlist obtiene una lista para usarla en consultas.
- SearchKey es la clave elegida para relacionar datos de la lista.
- Revisa vigencia y tipo de los indicadores antes de correlacionarlos.

**Error frecuente:** Una watchlist cargada no bloquea automáticamente una IP.

**Autoevaluación:** ¿Cómo dar prioridad a incidentes de servidores críticos?

**Respuesta razonada:** Relaciona sus identificadores con una lista de activos críticos y aplica la lógica de prioridad.

Ejercicios relacionados del banco: 178 (pregunta PDF 178, pág. 444), 180 (pregunta PDF 180, pág. 448), 378 (pregunta PDF 377, pág. 861), 383 (pregunta PDF 382, pág. 871), 386 (pregunta PDF 385, pág. 879), 388 (pregunta PDF 387, pág. 884), 397 (pregunta PDF 396, pág. 909).

## 25. ASIM y normalización — KQL y hunting

ASIM normaliza eventos de distintas fuentes mediante esquemas y parsers. Así una consulta puede analizar un mismo tipo de actividad sin depender de un fabricante.

- Distingue el esquema normalizado de la tabla original.
- Usa parámetros de filtrado del parser cuando existan.
- Confirma que las fuentes y campos necesarios estén disponibles.

**Error frecuente:** Un parser no crea eventos si no existe una fuente de datos.

```kql
_Im_Dns(starttime=ago(1d), endtime=now(), responsecodename='NXDOMAIN')
| summarize Total=count() by SrcIpAddr
```

**Autoevaluación:** ¿Qué ventaja aporta normalizar DNS de varios proveedores?

**Respuesta razonada:** Permite consultar campos comunes con menor dependencia del formato de cada origen.

Ejercicios relacionados del banco: 99 (pregunta PDF 99, pág. 273,274,275,276,277,278,279), 176 (pregunta PDF 176, pág. 440), 244 (pregunta PDF 244, pág. 578), 313 (pregunta PDF 313, pág. 720), 349 (pregunta PDF 348, pág. 797), 389 (pregunta PDF 388, pág. 887), 394 (pregunta PDF 393, pág. 901), 397 (pregunta PDF 396, pág. 909).

[Documentación de referencia](https://learn.microsoft.com/en-us/azure/sentinel/normalization-schema-dns)

## 26. Hunting, bookmarks, workbooks y notebooks — KQL y hunting

Hunting investiga una hipótesis. Un bookmark conserva hallazgos y contexto. Un workbook presenta información. Un notebook combina análisis programático y consultas.

- Formula una hipótesis y define qué evidencia la apoyaría.
- Guarda resultados relevantes y relaciónalos con entidades o incidentes.
- Elige notebook cuando necesitas enriquecer o procesar datos con código adicional.

**Error frecuente:** Una consulta de hunting guardada no se convierte automáticamente en detección continua.

**Autoevaluación:** Quieres preservar un hallazgo para investigarlo después: ¿qué utilizarías?

**Respuesta razonada:** Un bookmark con contexto y entidades, y su asociación al incidente cuando corresponda.

Ejercicios relacionados del banco: 49 (pregunta PDF 49, pág. 157), 88 (pregunta PDF 88, pág. 235), 187 (pregunta PDF 187, pág. 462), 238 (pregunta PDF 238, pág. 566), 239 (pregunta PDF 239, pág. 568), 251 (pregunta PDF 251, pág. 592), 252 (pregunta PDF 252, pág. 594), 265 (pregunta PDF 265, pág. 620).

## 27. Onboarding, grupos y niveles de automatización — Defender for Endpoint

Onboarding permite que Endpoint reciba señales del dispositivo. Los grupos ayudan a controlar acceso y comportamiento de respuesta.

- Comprueba estado del sensor y conectividad.
- Revisa reglas de pertenencia y prioridad cuando un equipo coincide con varios grupos.
- El nivel de automatización determina qué remediaciones requieren aprobación.

**Error frecuente:** Un grupo de dispositivos no sustituye la incorporación del sensor.

**Autoevaluación:** El equipo aparece pero no aporta señales recientes: ¿qué revisarías?

**Respuesta razonada:** Estado del sensor, comunicación, configuración y vigencia de la telemetría.

Ejercicios relacionados del banco: 2 (pregunta PDF 2, pág. 62), 9 (pregunta PDF 9, pág. 76), 20 (pregunta PDF 20, pág. 98), 31 (pregunta PDF 31, pág. 120), 37 (pregunta PDF 37, pág. 133), 38 (pregunta PDF 38, pág. 135), 49 (pregunta PDF 49, pág. 157), 57 (pregunta PDF 57, pág. 173).

## 28. AIR y disrupción automática de ataques — Defender for Endpoint

AIR investiga y propone o ejecuta remediaciones según configuración. La disrupción automática busca frenar ataques en curso a partir de señales correlacionadas.

- Consulta acciones pendientes y completadas en el centro de acciones.
- Revisa aprobaciones, permisos y alcance antes de concluir que una remediación ocurrió.
- Después de contener, confirma si persisten procesos, accesos o movimiento lateral.

**Error frecuente:** Una recomendación de remediación no es evidencia de ejecución.

**Autoevaluación:** ¿Dónde comprobarías si una acción automática se ejecutó?

**Respuesta razonada:** En el centro de acciones y en la evidencia del recurso afectado.

Ejercicios relacionados del banco: 42 (pregunta PDF 42, pág. 143), 147 (pregunta PDF 147, pág. 382), 160 (pregunta PDF 160, pág. 408), 287 (pregunta PDF 287, pág. 667), 335 (pregunta PDF 334, pág. 765), 356 (pregunta PDF 355, pág. 812), 453 (pregunta PDF 452, pág. 1066), 464 (pregunta PDF 463, pág. 1088).

## 29. Aislar, recopilar evidencia y Live Response — Defender for Endpoint

Aislar limita la comunicación del dispositivo. El paquete de investigación recopila información. Live Response permite investigar y actuar mediante una sesión remota autorizada.

- getfile recupera un archivo; putfile coloca un archivo de la biblioteca; run ejecuta un script autorizado.
- Comprueba disponibilidad, permisos y requisitos de la característica.
- Conserva evidencia y valida el resultado de cada acción.

**Error frecuente:** Recopilar un paquete no contiene la amenaza; aislar no equivale a borrar un archivo.

**Autoevaluación:** Necesitas obtener un archivo sospechoso del dispositivo: ¿qué acción encaja?

**Respuesta razonada:** Una acción de recuperación de archivo, como getfile en Live Response, con los permisos necesarios.

Ejercicios relacionados del banco: 20 (pregunta PDF 20, pág. 98), 134 (pregunta PDF 134, pág. 356), 163 (pregunta PDF 163, pág. 414), 266 (pregunta PDF 266, pág. 622), 269 (pregunta PDF 269, pág. 629), 279 (pregunta PDF 279, pág. 649), 287 (pregunta PDF 287, pág. 667), 292 (pregunta PDF 292, pág. 677).

## 30. Indicadores, bloqueos y excepciones — Defender for Endpoint

Los indicadores pueden permitir, alertar o bloquear según el tipo y las capacidades disponibles. Su alcance y caducidad deben responder al escenario.

- Distingue hash, IP, URL, dominio y certificado.
- Comprueba requisitos de protección y acción admitida.
- Limita el alcance a los dispositivos y el periodo necesarios.

**Error frecuente:** No todos los tipos aceptan las mismas acciones ni cualquier formato, como rangos de red arbitrarios.

**Autoevaluación:** ¿Por qué usar caducidad en un indicador temporal?

**Respuesta razonada:** Para no conservar una medida excepcional cuando ya no corresponde.

Ejercicios relacionados del banco: 8 (pregunta PDF 8, pág. 74), 10 (pregunta PDF 10, pág. 78), 24 (pregunta PDF 24, pág. 106), 37 (pregunta PDF 37, pág. 133), 38 (pregunta PDF 38, pág. 135), 122 (pregunta PDF 122, pág. 332), 124 (pregunta PDF 124, pág. 336), 139 (pregunta PDF 139, pág. 366).

## 31. ASR, antivirus y EDR — Defender for Endpoint

Antivirus, reglas de reducción de superficie de ataque y EDR cubren necesidades relacionadas pero distintas: prevención, reducción de conductas riesgosas y detección/respuesta.

- ASR en Audit observa; en Block impide la conducta según la regla.
- El modo del antivirus influye en su actividad; EDR en modo de bloqueo tiene requisitos propios.
- Al modificar políticas, comprueba si agregas valores o sustituyes una configuración existente.

**Error frecuente:** Auditar una regla no proporciona la misma protección que bloquearla.

**Autoevaluación:** Quieres evaluar impacto de una regla ASR antes de aplicarla: ¿qué modo ayuda?

**Respuesta razonada:** Audit, revisando los eventos antes de decidir el bloqueo.

Ejercicios relacionados del banco: 17 (pregunta PDF 17, pág. 92), 20 (pregunta PDF 20, pág. 98), 38 (pregunta PDF 38, pág. 135), 131 (pregunta PDF 131, pág. 350), 134 (pregunta PDF 134, pág. 356), 143 (pregunta PDF 143, pág. 374), 266 (pregunta PDF 266, pág. 622), 304 (pregunta PDF 304, pág. 702).

## 32. Vulnerabilidades y remediación — Defender for Endpoint

La gestión de vulnerabilidades combina inventario, debilidades, exposición y recomendaciones para priorizar acciones.

- CVE identifica una vulnerabilidad; CVSS expresa severidad técnica.
- Considera activos afectados, exposición y amenazas activas.
- Una solicitud de remediación coordina trabajo; comprueba que el cambio se completó.

**Error frecuente:** La vulnerabilidad con mayor puntuación no siempre es la primera prioridad operativa.

**Autoevaluación:** ¿Qué puede elevar la prioridad de una vulnerabilidad de menor severidad?

**Respuesta razonada:** Exposición externa, explotación activa o presencia en un activo crítico.

Ejercicios relacionados del banco: 9 (pregunta PDF 9, pág. 76), 60 (pregunta PDF 60, pág. 179), 107 (pregunta PDF 107, pág. 301), 123 (pregunta PDF 123, pág. 334), 156 (pregunta PDF 156, pág. 400), 199 (pregunta PDF 199, pág. 488), 299 (pregunta PDF 299, pág. 692).

## 33. Decepción y señuelos — Defender for Endpoint

La decepción introduce señuelos para detectar interacciones sospechosas. Su valor depende de que la actividad sobre ellos sea poco habitual en el uso legítimo.

- Reconoce diferencias entre objetos de señuelo y credenciales o pistas que atraen interacción.
- Ajusta el despliegue al entorno y a las capacidades contratadas.
- Investiga entidad, origen y actividad posterior cuando se activa un señuelo.

**Error frecuente:** Una alerta de señuelo requiere investigación; no describe por sí sola toda la cadena de ataque.

**Autoevaluación:** ¿Por qué una interacción con una cuenta señuelo merece atención?

**Respuesta razonada:** Porque normalmente no debería formar parte de la actividad legítima y puede revelar reconocimiento o acceso indebido.

Ejercicios relacionados del banco: 300 (pregunta PDF 300, pág. 694), 357 (pregunta PDF 356, pág. 814), 435 (pregunta PDF 434, pág. 1024), 450 (pregunta PDF 449, pág. 1059).

## 34. Defender for Identity y Active Directory — Identidades y aplicaciones

Defender for Identity analiza señales de identidad para detectar reconocimiento, abuso de credenciales y movimiento lateral en entornos compatibles.

- Identifica sensores, controladores de dominio y fuentes que requiere el caso.
- Correlaciona autenticación, consultas al directorio y actividad de la cuenta.
- Distingue administración legítima de patrones de reconocimiento anómalos.

**Error frecuente:** Una alerta sobre una cuenta no determina automáticamente qué dispositivo inició toda la actividad.

**Autoevaluación:** ¿Cómo investigarías reconocimiento del directorio?

**Respuesta razonada:** Revisaría cuenta, origen, consultas, sensores y actividad posterior relacionada.

Ejercicios relacionados del banco: 139 (pregunta PDF 139, pág. 366), 175 (pregunta PDF 175, pág. 438), 331 (pregunta PDF 330, pág. 757), 350 (pregunta PDF 349, pág. 799), 359 (pregunta PDF 358, pág. 818), 365 (pregunta PDF 364, pág. 832), 409 (pregunta PDF 408, pág. 949), 417 (pregunta PDF 416, pág. 981).

## 35. Riesgo de usuario, riesgo de inicio y acceso condicional — Identidades y aplicaciones

El riesgo de inicio de sesión se refiere a un intento concreto. El riesgo de usuario evalúa la posibilidad de compromiso de la identidad. Acceso condicional aplica controles según condiciones.

- Distingue remediar un intento mediante MFA de remediar una cuenta comprometida.
- Evalúa sesión, origen, método de autenticación y señales de riesgo.
- Comprueba licencias y permisos cuando el escenario los especifica.

**Error frecuente:** Restablecer una contraseña y exigir MFA no son acciones intercambiables en cualquier caso.

**Autoevaluación:** ¿Qué riesgo puede mantenerse aunque el último inicio parezca normal?

**Respuesta razonada:** El riesgo de usuario, si hay evidencia de compromiso de la identidad.

Ejercicios relacionados del banco: 13 (pregunta PDF 13, pág. 84), 118 (pregunta PDF 118, pág. 324), 127 (pregunta PDF 127, pág. 342), 302 (pregunta PDF 302, pág. 698), 344 (pregunta PDF 343, pág. 786), 346 (pregunta PDF 345, pág. 791), 359 (pregunta PDF 358, pág. 818), 441 (pregunta PDF 440, pág. 1038).

## 36. Cloud Discovery, conectores y OAuth — Identidades y aplicaciones

Cloud Discovery ayuda a identificar uso de aplicaciones. Los conectores de aplicaciones aportan actividad y controles según el servicio. OAuth introduce permisos delegados o de aplicación.

- Revisa aplicaciones usadas, usuarios, tráfico y nivel de riesgo.
- Una aplicación sancionada o no sancionada expresa una decisión de gobierno.
- Investiga permisos concedidos, editor, alcance y uso de una aplicación OAuth sospechosa.

**Error frecuente:** Marcar una aplicación como no sancionada no garantiza bloqueo sin la integración de aplicación de políticas.

**Autoevaluación:** ¿Qué revisarías ante consentimiento OAuth sospechoso?

**Respuesta razonada:** Identidad que lo otorgó, permisos, aplicación, actividad posterior y opciones de revocación.

Ejercicios relacionados del banco: 11 (pregunta PDF 11, pág. 80), 12 (pregunta PDF 12, pág. 82), 14 (pregunta PDF 14, pág. 86), 32 (pregunta PDF 32, pág. 122,123), 93 (pregunta PDF 93, pág. 254), 113 (pregunta PDF 113, pág. 313,314), 125 (pregunta PDF 125, pág. 338), 126 (pregunta PDF 126, pág. 340).

## 37. Políticas de sesión y control de descargas — Identidades y aplicaciones

Los controles de sesión pueden supervisar o limitar acciones durante el acceso a una aplicación compatible. No son lo mismo que bloquear el inicio de sesión.

- Relaciona acceso condicional con el control de sesión necesario.
- Para descargas, comprueba aplicación, dispositivo, contenido y condiciones.
- Distingue monitorizar, bloquear una descarga y exigir autenticación adicional.

**Error frecuente:** Un control de MFA no equivale a inspeccionar y bloquear un archivo descargado.

**Autoevaluación:** Quieres permitir acceso pero impedir descargar información sensible: ¿qué enfoque estudiarías?

**Respuesta razonada:** Un control de sesión con la política y las condiciones de contenido adecuadas.

Ejercicios relacionados del banco: 4 (pregunta PDF 4, pág. 66), 6 (pregunta PDF 6, pág. 70), 7 (pregunta PDF 7, pág. 72), 13 (pregunta PDF 13, pág. 84), 14 (pregunta PDF 14, pág. 86), 21 (pregunta PDF 21, pág. 100), 50 (pregunta PDF 50, pág. 159), 77 (pregunta PDF 77, pág. 213).

## 38. Safe Links, Safe Attachments y ZAP — Correo y Purview

Safe Links protege frente a vínculos maliciosos; Safe Attachments analiza adjuntos; ZAP puede actuar sobre mensajes ya entregados cuando se identifican como maliciosos.

- Distingue prevención en entrega, protección al abrir un vínculo y actuación posterior.
- Investiga remitente, destinatario, URL, adjunto y acciones de entrega.
- Relaciona el mensaje con actividad posterior del dispositivo.

**Error frecuente:** Que un correo se haya entregado no significa que la protección haya terminado.

**Autoevaluación:** Una amenaza se reconoce después de la entrega: ¿qué función debes distinguir?

**Respuesta razonada:** ZAP, para la actuación posterior sobre mensajes según las capacidades y políticas aplicables.

Ejercicios relacionados del banco: 5 (pregunta PDF 5, pág. 68), 16 (pregunta PDF 16, pág. 90), 120 (pregunta PDF 120, pág. 328), 130 (pregunta PDF 130, pág. 348).

## 39. Explorer, investigación y remediación de correo — Correo y Purview

La investigación del correo busca entender entrega, destinatarios y comportamiento de la amenaza. La remediación debe ajustarse al alcance identificado.

- Busca mensajes relacionados por indicadores y campaña.
- Confirma si hubo entrega, clic, descarga o ejecución.
- Verifica permisos y resultado al realizar acciones sobre mensajes.

**Error frecuente:** Un mismo asunto no identifica inequívocamente todos los mensajes de una campaña.

**Autoevaluación:** ¿Qué sigue después de identificar una URL maliciosa en un correo?

**Respuesta razonada:** Buscar otros mensajes y destinatarios afectados y revisar clics, dispositivos e incidentes asociados.

Ejercicios relacionados del banco: 5 (pregunta PDF 5, pág. 68), 7 (pregunta PDF 7, pág. 72), 9 (pregunta PDF 9, pág. 76), 16 (pregunta PDF 16, pág. 90), 22 (pregunta PDF 22, pág. 102), 26 (pregunta PDF 26, pág. 110), 29 (pregunta PDF 29, pág. 116), 33 (pregunta PDF 33, pág. 125).

## 40. Audit, búsqueda de contenido y DLP — Correo y Purview

Audit responde qué actividad se registró. La búsqueda de contenido localiza información. DLP detecta y controla tratamiento de información sensible según políticas.

- Elige por el objetivo: actividad, contenido o prevención de pérdida.
- Comprueba roles, ubicaciones y periodo disponibles.
- Interpreta resultados junto con identidad y contexto del incidente.

**Error frecuente:** Encontrar un archivo no equivale a probar que se descargó o exfiltró.

**Autoevaluación:** Quieres saber quién accedió o realizó una operación: ¿dónde empezarías?

**Respuesta razonada:** En los registros de auditoría disponibles para esa actividad.

Ejercicios relacionados del banco: 16 (pregunta PDF 16, pág. 90), 25 (pregunta PDF 25, pág. 108), 29 (pregunta PDF 29, pág. 116), 110 (pregunta PDF 110, pág. 307), 130 (pregunta PDF 130, pág. 348), 140 (pregunta PDF 140, pág. 368), 151 (pregunta PDF 151, pág. 390), 157 (pregunta PDF 157, pág. 402).

## 41. Registros de Microsoft Graph — Correo y Purview

Los registros de actividad de Graph pueden ayudar a investigar operaciones de aplicaciones e identidades sobre la API.

- Relaciona identidad, aplicación, URI, método, momento y resultado.
- 401 suele señalar un problema de autenticación; 403 indica una denegación de acceso que requiere revisar autorización y contexto.
- Correlaciona solicitudes con concesiones OAuth y otros registros.

**Error frecuente:** Una respuesta HTTP aislada no explica por sí sola la causa completa ni confirma ataque.

**Autoevaluación:** Una aplicación autenticada recibe 403: ¿qué revisarías?

**Respuesta razonada:** Permisos, consentimiento, políticas, recurso solicitado y contexto de la solicitud.

Ejercicios relacionados del banco: 52 (pregunta PDF 52, pág. 163), 190 (pregunta PDF 190, pág. 468), 241 (pregunta PDF 241, pág. 572), 280 (pregunta PDF 280, pág. 651), 314 (pregunta PDF 314, pág. 722), 317 (pregunta PDF 316, pág. 728), 319 (pregunta PDF 318, pág. 732), 380 (pregunta PDF 379, pág. 865).

## 42. CSPM frente a protección de cargas — Defender for Cloud

CSPM evalúa postura y configuraciones. La protección de cargas detecta amenazas sobre recursos. Secure Score ayuda a priorizar mejoras de postura.

- Recomendación: debilidad o mejora sugerida; alerta: actividad potencialmente maliciosa.
- Cumplimiento regulatorio agrupa controles; no sustituye investigación de alertas.
- Asocia cada plan de protección al tipo de recurso requerido.

**Error frecuente:** Mejorar Secure Score no demuestra que se eliminó un ataque activo.

**Autoevaluación:** Necesitas corregir un recurso mal configurado: ¿buscas una recomendación o una alerta?

**Respuesta razonada:** Una recomendación de postura, aunque también debes revisar si existen alertas relacionadas.

Ejercicios relacionados del banco: 24 (pregunta PDF 24, pág. 106), 27 (pregunta PDF 27, pág. 112), 31 (pregunta PDF 31, pág. 120), 44 (pregunta PDF 44, pág. 147), 46 (pregunta PDF 46, pág. 151), 49 (pregunta PDF 49, pág. 157), 50 (pregunta PDF 50, pág. 159), 51 (pregunta PDF 51, pág. 161).

## 43. Recursos híbridos, AWS y GCP — Defender for Cloud

Los entornos externos requieren conexión, permisos y componentes adecuados para aportar postura o telemetría.

- Conector de nube, incorporación del recurso y recopilación son capas distintas.
- Evalúa los planes necesarios para servidores, contenedores u otras cargas.
- Comprueba permisos y ámbito tanto en Azure como en el proveedor externo.

**Error frecuente:** Un conector de nube no implica automáticamente que cada máquina tenga todos los agentes y extensiones.

**Autoevaluación:** Un servidor externo está visible pero sin telemetría: ¿qué capas revisarías?

**Respuesta razonada:** Conexión de administración, incorporación a la protección y recopilación de datos requerida.

Ejercicios relacionados del banco: 24 (pregunta PDF 24, pág. 106), 52 (pregunta PDF 52, pág. 163), 64 (pregunta PDF 65, pág. 187), 70 (pregunta PDF 70, pág. 199), 71 (pregunta PDF 71, pág. 201), 75 (pregunta PDF 75, pág. 209), 79 (pregunta PDF 79, pág. 217), 86 (pregunta PDF 86, pág. 231).

## 44. Automatización de recomendaciones y alertas — Defender for Cloud

Las automatizaciones de flujo pueden responder a alertas o recomendaciones, según desencadenador y condiciones.

- Define el evento que inicia el flujo.
- Configura integración, permisos y acciones de Logic Apps.
- Distingue respuesta a una amenaza de corrección de una configuración.

**Error frecuente:** La existencia de una recomendación no significa que su corrección sea automática.

**Autoevaluación:** Quieres abrir un ticket al detectar cierta recomendación: ¿qué necesitas?

**Respuesta razonada:** Una automatización con el desencadenador y filtros adecuados y una integración autorizada con el sistema de tickets.

Ejercicios relacionados del banco: 46 (pregunta PDF 46, pág. 151), 49 (pregunta PDF 49, pág. 157), 57 (pregunta PDF 57, pág. 173), 59 (pregunta PDF 59, pág. 177), 68 (pregunta PDF 69, pág. 195), 69 (pregunta PDF 69, pág. 197), 73 (pregunta PDF 73, pág. 205), 88 (pregunta PDF 88, pág. 235).

## 45. DevOps e infraestructura como código — Defender for Cloud

La seguridad de infraestructura como código busca detectar configuraciones inseguras antes de desplegar recursos. El formato de la plantilla determina la herramienta compatible.

- Reconoce ARM/Bicep frente a Terraform.
- Distingue análisis de código, postura del recurso desplegado y detección de amenazas en ejecución.
- En preguntas antiguas, identifica la función de la herramienta citada y comprueba su vigencia antes de usarla.

**Error frecuente:** Una herramienta compatible con un formato no es necesariamente la respuesta para todos los repositorios.

**Autoevaluación:** ¿Qué dato debes identificar antes de elegir un analizador de IaC?

**Respuesta razonada:** El lenguaje o formato del código y el tipo de análisis que exige el escenario.

Ejercicios relacionados del banco: 80 (pregunta PDF 80, pág. 219), 87 (pregunta PDF 87, pág. 233), 93 (pregunta PDF 93, pág. 254), 96 (pregunta PDF 96, pág. 260), 219 (pregunta PDF 219, pág. 528), 228 (pregunta PDF 228, pág. 546), 233 (pregunta PDF 233, pág. 556), 237 (pregunta PDF 237, pág. 564).

## 46. Data lake, KQL jobs, summary rules y search jobs — Actualizaciones del temario

Estas capacidades amplían el análisis de datos históricos y de grandes volúmenes en Sentinel.

- KQL jobs: consultas asíncronas, puntuales o programadas, sobre el data lake, incluidas relaciones entre tablas.
- Summary rules: agregan datos y guardan resúmenes en tablas de análisis.
- Search jobs: buscan grandes conjuntos de una sola tabla para facilitar investigación posterior.

**Error frecuente:** KQL jobs requieren incorporación al data lake; no todas estas opciones comparten alcance y operadores.

**Autoevaluación:** Quieres generar resúmenes periódicos de registros voluminosos: ¿qué opción encaja?

**Respuesta razonada:** Summary rules.

[Documentación de referencia](https://learn.microsoft.com/en-us/azure/sentinel/datalake/kql-jobs-summary-rules-search-jobs)

## 47. Grafos, alcance y movimiento lateral — Actualizaciones del temario

Investigar relaciones entre identidades y recursos ayuda a evaluar el alcance de un incidente y posibles rutas hacia activos importantes.

- Separa evidencia de actividad observada de caminos potenciales de ataque.
- Valida relaciones con eventos y contexto temporal.
- Prioriza activos críticos y medidas de contención según evidencia.

**Error frecuente:** Una ruta posible en un grafo no prueba que el atacante ya la recorrió.

**Autoevaluación:** ¿Qué diferencia hay entre alcance confirmado y alcance potencial?

**Respuesta razonada:** El confirmado tiene evidencia; el potencial muestra recursos o rutas que podrían verse afectados.

[Documentación de referencia](https://learn.microsoft.com/en-us/defender-xdr/investigate-incidents)

## 48. Security Copilot y validación del análisis — Actualizaciones del temario

Los asistentes de seguridad pueden apoyar resumen, investigación y análisis dentro de experiencias compatibles. El analista sigue validando evidencia y acciones.

- Comprueba permisos y datos a los que puede acceder la experiencia.
- Contrasta el resumen con alertas, consultas y registros originales.
- Antes de ejecutar una acción, confirma entidad, alcance y efecto.

**Error frecuente:** Un resumen generado no sustituye la evidencia del incidente.

**Autoevaluación:** ¿Cómo usarías un resumen de incidente para tomar decisiones?

**Respuesta razonada:** Como ayuda inicial; comprobaría cada conclusión relevante en la evidencia antes de actuar.

[Documentación de referencia](https://learn.microsoft.com/en-us/copilot/security/experiences-security-copilot)

## 49. Etiquetas de sensibilidad y protección de información — Correo y Purview

Una etiqueta de sensibilidad clasifica información y puede aplicar protección, como cifrado, restricciones y marcas visuales. Su política de publicación determina quién puede utilizarla.

- Distingue crear la etiqueta, configurar sus efectos y publicarla.
- Una etiqueta de retención gobierna conservación; no equivale a una etiqueta de sensibilidad.
- En escenarios antiguos de Azure Information Protection, identifica servicio, activación y dependencias antes de ordenar pasos.

**Error frecuente:** Clasificar información no implica automáticamente cifrarla: depende de la configuración.

**Autoevaluación:** Quieres identificar información confidencial y restringir su lectura: ¿qué comprobarías?

**Respuesta razonada:** Etiqueta de sensibilidad, configuración de cifrado y permisos, publicación y compatibilidad de la aplicación.

Ejercicios relacionados del banco: 2 (pregunta PDF 2, pág. 62), 14 (pregunta PDF 14, pág. 86), 22 (pregunta PDF 22, pág. 102), 29 (pregunta PDF 29, pág. 116), 89 (pregunta PDF 89, pág. 237,238,239,240,241), 105 (pregunta PDF 105, pág. 297), 116 (pregunta PDF 116, pág. 320), 128 (pregunta PDF 128, pág. 344).

[Documentación de referencia](https://learn.microsoft.com/en-us/purview/purview-security)

## 50. Microsoft Entra Internet Access y roles — Identidades y aplicaciones

Microsoft Entra Internet Access y Private Access forman parte de Global Secure Access. La administración utiliza roles de Microsoft Entra que debes distinguir de los roles de Azure sobre recursos.

- Global Secure Access Administrator administra estas capacidades.
- Otras tareas, como editar acceso condicional, pueden necesitar un rol adicional.
- Un permiso de lectura no equivale a permiso para configurar el servicio.

**Error frecuente:** No deduzcas permisos solo del nombre del departamento o del rol Azure Contributor.

**Autoevaluación:** ¿Un usuario que lee registros necesariamente puede configurar Internet Access?

**Respuesta razonada:** No. Comprueba la asignación del rol administrador pertinente y las capacidades de la tarea.

Ejercicios relacionados del banco: 451 (pregunta PDF 450, pág. 1061).

[Documentación de referencia](https://learn.microsoft.com/en-us/entra/global-secure-access/reference-role-based-permissions)
