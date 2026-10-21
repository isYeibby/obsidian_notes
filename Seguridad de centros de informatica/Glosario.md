**Alumno:** Yhosmar Beltrán Martínez Hernández  
**Materia:** Seguridad de centros de informática  
**Grupo:** 906

# SEGURIDAD DE LA INFORMACIÓN

- Seguridad de la información: Protección de la información y de los sistemas de información frente al acceso, uso, divulgación, interrupción, modificación o destrucción no autorizados de atacates, desastres naturales, condiciones ambientales adversas, fallos en el suministro eléctrico, robos o actos de vandalismo, u otras situaciones indeseables.

- **Brecha de Seguridad (Breach):** Evento en el cual se compromete la confidencialidad, integridad o disponibilidad de los datos o transacciones.

## A. La Tríada CIA (CIA Triad)

Modelo tradicional centrado en la protección de los datos. También conocido en algunas publicaciones como **CAI** o expresado en su forma negativa como **DAD** (_Disclosure, Alteration, Denial_).

- **Confidencialidad (Confidentiality):** Capacidad de proteger la información para que no sea vista ni accedida por personas o procesos no autorizados. Es un componente necesario de la privacidad.
    
- **Integridad (Integrity):** Capacidad de evitar que los datos sean modificados o eliminados de manera no autorizada o no deseada. Incluye tanto prevenir cambios indebidos como la capacidad de revertir o deshacer modificaciones autorizadas pero indeseadas (p. ej., mediante _rollbacks_ en bases de datos).
    
- **Disponibilidad (Availability):** Garantía de que los usuarios autorizados puedan acceder a los datos y sistemas cuando lo necesiten. Su pérdida puede deberse a fallas de energía, errores de software, problemas de red o ataques externos.

## B. La Hexada de Parker (Parkerian Hexad)

Modelo ampliado propuesto por Donn Parker en _Fighting Computer Crime_. Añade tres principios adicionales a la tríada CIA:

- **Posesión o Control (Possession or Control):** Refiere a la disposición y tenencia física del soporte/medio en el que se almacenan los datos. Permite categorizar incidentes donde se pierde el medio físico sin que necesariamente se comprometa la confidencialidad (ej. perder cintas de respaldo que están fuertemente cifradas).
    
- **Autenticidad (Authenticity):** Garantía sobre la atribución correcta de la autoría o propiedad de la información o comunicación (ej. verificar que un e-mail realmente proviene de quien dice ser mediante firmas digitales).
    
- **Utilidad (Utility):** Nivel o grado de utilidad que tienen los datos para un propósito específico. A diferencia de los otros principios, no es estrictamente binario. Por ejemplo, unos datos robados que están cifrados tienen baja utilidad para un atacante, pero alta utilidad para el dueño si posee la clave.
    
- **No Repudio (Non-repudiation):** Concepto vinculado a la autenticidad que impide que un emisor o usuario niegue haber realizado una acción o enviado un mensaje determinado.

- DLP: La prevención de perdida de datos (Data Loss Prevention) es la disciplina que consiste en proteger los datos confidenciales del robo, la pérdida y el uso indebido mediante estrategias, procesos y tecnologías de ciberseguridad.

## 3. Categorías de Ataques

- **Intercepción (Interception):** Ataque dirigido principalmente contra la **confidencialidad**. Ocurre cuando un usuario no autorizado accede a datos, aplicaciones o entornos (ej. espiar llamadas, leer e-mails, visualizar o copiar archivos no autorizados).
    
- **Interrupción (Interruption):** Ataque dirigido principalmente contra la **disponibilidad** (y en ocasiones contra la integridad). Hace que un activo quede inaccesible o inservible de forma temporal o permanente (ej. un ataque DoS o la alteración de un proceso de base de datos).
    
- **Modificación (Modification):** Ataque dirigido principalmente contra la **integridad** (aunque puede afectar la disponibilidad y confidencialidad). Consiste en alterar o manipular indebidamente un activo, como modificar un archivo de datos o un archivo de configuración de un servidor web.
    
- **Fabricación (Fabrication):** Ataque dirigido principalmente contra la **integridad** (y potencialmente contra la disponibilidad). Consiste en generar datos, comunicaciones o procesos espurios dentro de un sistema (ej. insertar registros falsos en una base de datos, enviar correo basura con malware o satura un servicio con tráfico falso).

## 4. Gestión del Riesgo y sus Componentes

- **Amenaza (Threat):** Cualquier elemento, evento o entidad que tiene el **potencial de causar daño** a los activos. Las amenazas suelen ser específicas para determinados entornos (ej. un virus diseñado para Windows no suele amenazar a un entorno Linux).
    
- **Vulnerabilidad (Vulnerability):** Debilidad, falla o hueco presente en un sistema o entorno que puede ser explotado por una amenaza para causar daño (ej. software sin parchear, falta de generadores eléctricos, diseño físico inadecuado).
    
- **Riesgo (Risk):** La **probabilidad** de que una amenaza explote exitosamente una vulnerabilidad y cause un impacto negativo. Para que exista riesgo, deben coincidir la amenaza y la vulnerabilidad explotable.
    
- **Impacto (Impact):** Factor considerado por organizaciones (como la NSA) que mide la gravedad del daño o la pérdida del valor de un activo en caso de que una amenaza se materialice.   

## 5. Tipos de Controles de Seguridad

Medidas implementadas para mitigar el riesgo y contrarrestar las amenazas:

- **Controles Físicos (Physical Controls):** Medidas que protegen el entorno físico donde residen los sistemas y datos, controlando el acceso a las instalaciones.
    
    - _Ejemplos:_ Cajas fuertes, cerrojos, cercas, guardias, cámaras, sistemas de aire acondicionado, extinción de incendios y generadores de energía de respaldo.
        
- **Controles Lógicos o Técnicos (Logical / Technical Controls):** Mecanismos basados en tecnología que protegen las redes, sistemas informáticos y datos en tránsito, proceso o almacenamiento.
    
    - _Ejemplos:_ Contraseñas, cifrado, firewalls, listas de control de acceso (ACL), e IDS/IPS.
        
- **Controles Administrativos (Administrative Controls):** Reglas, políticas, procedimientos, directrices y normativas en formato documental ("de papel") que establecen el comportamiento esperado de las personas.
    
    - _Requisito clave:_ Para ser efectivos, la organización debe tener la **capacidad de hacer cumplir su cumplimiento** (_enforce compliance_); de lo contrario, generan una falsa sensación de seguridad.
        

## 6. Estrategia de Defensa en Profundidad y Capas

- **Defensa en Profundidad (Defense in Depth):** Estrategia de seguridad (derivada de la táctica militar) que consiste en estructurar **múltiples capas de defensas independientes**. Su objetivo no es garantizar la impenetrabilidad absoluta, sino retrasar al atacante y dar tiempo a la organización para detectar la agresión y responder activamente antes de que alcance los activos críticos.
    
- **Capas de Protección Lógica:**
    
    1. **Red Externa (External Network):** Primera línea defensiva expuesta al exterior (ej. DMZ, VPN, análisis de vulnerabilidades).
        
    2. **Perímetro de Red (Network Perimeter):** Frontera entre la red interna y externa (ej. Firewalls, inspección de paquetes con estado / Stateful Packet Inspection, servidores Proxy).
        
    3. **Red Interna (Internal Network):** Red corporativa local (ej. IDS/IPS internos, registro de logs, auditorías).
        
    4. **Host / Equipo (Host):** Protección a nivel de servidor o estación de trabajo (ej. Antivirus, hashing de contraseñas, autenticación).
        
    5. **Aplicación (Application):** Seguridad integrada en el software (ej. Validación de datos de entrada, filtrado de contenido, Single Sign-On / SSO).
        
    6. **Datos (Data):** Capa central que contiene la información misma (ej. Cifrado, controles de acceso rigurosos, copias de seguridad / Backups).
        
- **Pruebas de Penetración (Penetration Testing):** Método transversal para identificar brechas evaluando las defensas mediante la simulación de técnicas reales empleadas por un atacante.

# PREVENCIÓN DE PÉRDIDA DE DATOS (DLP)

## 1. Conceptos Fundamentales de DLP

- **Prevención de Pérdida de Datos / Data Loss Prevention (DLP):** Disciplina de ciberseguridad orientada a proteger la información confidencial contra el robo, la pérdida y el uso indebido mediante la combinación de estrategias, procesos y tecnologías de monitoreo y aplicación de políticas.

- **Solución DLP:** Herramienta tecnológica que inspecciona los paquetes de datos mientras circulan por la red para detectar el uso de información confidencial (como tarjetas de crédito o propiedad intelectual) y aplicar controles de acceso de manera automatizada.

## 2. Estados de los Datos

Para proteger adecuadamente la información, las políticas de DLP evalúan los datos en tres estados principales:

- **Datos en Uso (_Data in Use_):** Información que se encuentra activa mientras es accedida, procesada, actualizada, modificada o eliminada por un usuario o sistema (por ejemplo, documentos editados o datos usados para análisis).

- **Datos en Movimiento / En Tránsito (_Data in Motion / In Transit_):** Información que se desplaza a través de una red o entre diferentes redes (por ejemplo, mediante aplicaciones de mensajería o transmisiones de servidores). Es considerado el estado más vulnerable.

- **Datos en Reposo (_Data in Repose_):** Información almacenada de forma estática en unidades de disco duro locales, repositorios en la nube o archivos (por ejemplo, respaldos o documentos guardados). Aunque son más fáciles de proteger, siguen expuestos a robos físicos de medios de almacenamiento.

## 3. Incidentes y Tipos de Pérdida de Datos

Aunque a menudo se usan indistintamente, el documento diferencia tres tipos de eventos relacionados con la pérdida de información:

- **Filtración de Datos (_Data Breach_):** Incidente de seguridad en el que partes no autorizadas obtienen acceso a información confidencial o sensible a través de un ataque cibernético u otra vulneración.

- **Fuga de Datos (_Data Leak_):** Exposición accidental de información confidencial al público debido a errores de procedimiento, fallas técnicas u omisiones (tanto de naturaleza digital como física).

- **Exfiltración de Datos (_Data Exfiltration_):** Robo deliberado de datos en el que un atacante copia o extrae la información hacia un dispositivo o entorno bajo su propio control. (Toda exfiltración requiere una filtración previa, pero no toda filtración deriva necesariamente en un robo de datos).

## 4. Tipos de Datos y Activos Críticos

- **Información de Identificación Personal / Personally Identifiable Information (PII):** Datos altamente valiosos para los delincuentes que permiten identificar a un individuo (incluye números de identificación fiscal, correos electrónicos, teléfonos y direcciones particulares).

- **Propiedad Intelectual / Intellectual Property (IP):** Registros, secretos comerciales y activos creativos o tecnológicos exclusivos de una organización que representan una ventaja competitiva.





# PLAN DE CONTINUIDAD DE NEGOCIO VS. RECUPERACIÓN ANTE DESASTRES (BCDR)

## 1. Conceptos Estratégicos Principales

- **Plan de Continuidad de Negocio / Business Continuity Plan (BCP):** Plan detallado y de enfoque amplio que describe los pasos y tácticas que tomará una organización para mantener o volver a sus funciones comerciales normales antes, durante y después de un desastre o interrupción.
    
      
    
- **Plan de Recuperación ante Desastres / Disaster Recovery Plan (DRP):** Plan de contingencia más específico y reactivo enfocado en proteger y restaurar de manera directa los sistemas de TI, la infraestructura y los datos críticos de la empresa tras una interrupción.
    
      
    
- **BCDR (Business Continuity and Disaster Recovery):** Enfoque unificado moderno que combina la continuidad de negocio y la recuperación ante desastres, impulsando a los ejecutivos a trabajar ambas disciplinas de forma coordinada en lugar de aislada.
    
      
    

## 2. Métricas y Objetivos de Rendimiento

- **Objetivo de Tiempo de Recuperación / Recovery Time Objective (RTO):** Cantidad máxima de tiempo que se requiere para restaurar los procesos comerciales y la operatividad de los sistemas tras un incidente no planeado.
    
      
    
- **Objetivo de Punto de Recuperación / Recovery Point Objective (RPO):** Cantidad máxima de datos que una empresa puede permitirse perder durante un desastre sin comprometer su viabilidad de recuperación (define la tolerancia de antigüedad de las copias de seguridad).
    
      
    

## 3. Análisis y Evaluaciones de Riesgo

- **Análisis de Impacto en el Negocio / Business Impact Analysis (BIA):** Evaluación inicial que ayuda a las organizaciones a comprender las amenazas a las que se enfrentan, detallando sus vulnerabilidades, estimando la probabilidad de ocurrencia y priorizando las respuestas de protección correspondientes.
    
      
    

## 4. Tipos de Planes Específicos (Ejemplos Estables)

- **Plan de Gestión de Crisis:** Documento detallado que indica cómo administrar de forma táctica y hora a hora una amenaza específica (como un corte de energía, delito cibernético o desastre natural).
    
      
    
- **Plan de Comunicaciones:** Estrategia coordinada con especialistas en relaciones públicas para abordar y gestionar las comunicaciones y la reputación de la organización ante el público durante un incidente imprevisto.
    
      
    
- **Plan de Recuperación de Red:** Plan enfocado en restaurar con rapidez servicios esenciales de conectividad y comunicación (Internet, datos móviles, redes LAN y WAN).
    
      
    
- **Plan de Recuperación del Centro de Datos:** Protocolo orientado a salvaguardar la infraestructura de TI y respaldar de forma segura los repositorios de datos ante fallas de energía o ciberataques.
    
      
    
- **Plan de Recuperación Virtualizado:** Estrategia basada en el uso de máquinas virtuales (VM) e instancias de alta disponibilidad (HA) para reactivar aplicaciones críticas en cuestión de minutos tras una interrupción.
    
      
    

## 5. Clasificación de Activos (Inventario DRP)

- **Activos Críticos:** Elementos de hardware, software o infraestructura de los cuales depende totalmente la organización para sus operaciones comerciales normales.
    
      
    
- **Activos Importantes:** Recursos utilizados al menos una vez al día cuya interrupción afectaría considerablemente las operaciones críticas (aunque no las paralice por completo).
    
      
    
- **Activos Sin Importancia:** Bienes que posee la compañía pero que no se emplean con la frecuencia suficiente para ser esenciales en las operaciones cotidianas.


### Roles y Responsabilidades Clave en un Plan (BCDR)

- **Informante de Incidentes (_Incident Informer_):** Persona encargada de mantener actualizada la información de contacto de las partes interesadas y de comunicarse con los líderes empresariales y _stakeholders_ tan pronto como ocurre un evento que afecta al negocio.
    
      
    
- **Supervisor de DRP (_DR Supervisor_):** Responsable de verificar y asegurar que los miembros del equipo ejecuten de manera correcta las tareas que les fueron asignadas durante un incidente.
    
      
    
- **Gestor de Activos (_Asset Manager_):** Persona cuyo trabajo consiste en asegurar, proteger y salvaguardar los activos críticos de la organización cuando se desencadena un desastre.
    
      
    

### Causas Comunes de Interrupción e Incidentes

El artículo destaca que los planes BCDR se diseñan para mitigar una gran variedad de escenarios adversos que pueden paralizar una organización, entre los cuales se incluyen:

- **Cortes masivos de energía (_Power outages_):** Fallas eléctricas prolongadas que afectan la infraestructura física y los centros de datos.

- **Desastres naturales (_Natural disasters_):** Eventos ambientales imprevistos que dañan las instalaciones físicas y alteran las operaciones normales.
 
- **Ataques de ransomware y malware:** Incidentes cibernéticos maliciosos diseñados para cifrar información, bloquear sistemas y extorsionar a las organizaciones.

































- **Malware:** Término genérico que engloba cualquier software malicioso (como virus, gusanos o troyanos) diseñado para infiltrarse, dañar o comprometer sistemas informáticos y redes.
    
- **Ransomware:** Tipo específico de malware que cifra los archivos o bloquea el acceso a un sistema informático, exigiendo el pago de un rescate económico a cambio de restaurar el acceso a la información.
    
- **Phishing:** Técnica de ingeniería social basada en el envío de correos electrónicos o mensajes fraudulentos que imitan a entidades legítimas para engañar a los usuarios y robar sus credenciales, contraseñas o información personal.
    
- **Exploits:** Fragmentos de código, secuencias de comandos o técnicas diseñadas para aprovechar una vulnerabilidad específica en un sistema o aplicación con el fin de obtener acceso no autorizado o provocar un comportamiento imprevisto.
