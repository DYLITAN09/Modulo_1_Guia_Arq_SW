El proyecto **RG-T4185** (Apoyo a la Gestión Digital Fiscal y Aduanera en LAC) busca implementar un piloto de la Factura Electrónica de Comercio Exterior (F-eCX) utilizando tecnología de credenciales verificables. La identificación de riesgos es esencial para la gestión del proyecto. **(Sección ii. Introducción - ARCHIVO REOI)** - COMPROBADO POR MI  

A continuación, se identifican los riesgos principales clasificados en técnicos, normativos y operativos, seguidos de preguntas propuestas para los talleres.

---

## Identificación de Riesgos

### 1. Riesgos Técnicos

Los riesgos técnicos se centran en la implementación de la nueva solución digital y su integración con los sistemas existentes:

| Riesgo Técnico | Detalle y Justificación | Citas |
| :--- | :--- | :--- |
| **Dependencia y Complejidad de la Tecnología (VCs/DIDs)** | La solución está obligada a utilizar **Credenciales Verificables (VCs) e Identificadores Descentralizados (DIDs)**, siguiendo los **estándares de la W3C**. Esto introduce complejidad y dependencia de protocolos nuevos en el ámbito de la gestión fiscal/aduanera. | **(Sección 6. Principios Rectores - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Fallo de Interoperabilidad con Sistemas Legados** | La solución debe tener un **impacto mínimo** en las plataformas tecnológicas actuales y se requiere una **capa de integración basada en APIs**. Existe el riesgo de que los sistemas aduaneros y tributarios existentes no se ajusten o integren sin problemas con la F-eCX, o que la traducción de datos entre modelos sea ineficiente. | **(Sección 11. Requisitos Técnicos - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Problemas de Seguridad y Autenticidad** | El sistema debe garantizar la **autenticidad y validez** de los archivos digitales, así como la **integridad de la información** desde la F-eX hasta la F-eCXm. Existe el riesgo de que fallen los mecanismos de verificación descentralizada (como la comprobación de *hashes*) si los documentos F-eX originales no incluyen elementos de seguridad adecuados. | **(Sección 9. Modelo Conceptual - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Sostenibilidad a Largo Plazo** | Riesgo de que la solución desarrollada no sea **sostenible en el tiempo**, a pesar de que el proyecto busca mitigarlo utilizando **código abierto**. | **(Sección 6. Principios Rectores - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Inconsistencia del Modelo de Datos** | El **Modelo de Datos de la OMA** es la referencia, pero es **insuficiente para los intereses del control fiscal interno**. Riesgo de que la definición de la estructura de datos F-eCX no contemple adecuadamente los **datos de interés nacional**. | **(Sección 9. Modelo Conceptual - ARCHIVO REOI)** - COMPROBADO POR MI |

---

### 2. Riesgos Normativos

Los riesgos normativos están relacionados con el marco legal y regulatorio necesario para habilitar la F-eCX, especialmente en el contexto regional:

| Riesgo Normativo | Detalle y Justificación | Citas |
| :--- | :--- | :--- |
| **Inconsistencia Jurídica Internacional** | La solución F-eCX requiere **acueros de cooperación internacional** que permitan el **intercambio electrónico de información a nivel masivo y en tiempo real**. Riesgo de que la **consistencia jurídica plena** entre el marco normativo doméstico y los acuerdos internacionales no se establezca o que los acuerdos no permitan el uso de la información en **procesos administrativos o judiciales**. | **(Sección 13. Riesgos Identificados - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Modificaciones Legales Obligatorias** | Es necesario que cada país participante realice un **análisis exhaustivo de su marco normativo** para definir si los acuerdos actuales contemplan todas las facultades necesarias o si se requieren **cambios normativos**. El riesgo es el retraso o la imposibilidad de lograr dichos cambios. | **(Sección 13. Riesgos Identificados - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Modelo de F-eX Preexistente** | El modelo conceptual **presupone la existencia de la emisión de la F-eX** en una fase previa al despacho de exportación (antes del registro de la D-eX). Los países que no dispongan de una F-eX podrían experimentar una **reducción de los beneficios de integración**. | **(Sección 9. Modelo Conceptual - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Exclusiones del Piloto** | El piloto simplifica o elimina procedimientos complejos como el **tratamiento de las divergencias** y ciertas **rectificaciones posteriores al despacho de exportación**. Esto implica un riesgo regulatorio, ya que el piloto no abordará las complejidades legales de la gestión completa de discrepancias y ajustes en el mundo real. | **(Sección 9. Modelo Conceptual - ARCHIVO REOI)** - COMPROBADO POR MI |

---

### 3. Riesgos Operativos

Estos riesgos se relacionan con la ejecución del proyecto, la gobernanza y la aceptación institucional:

| Riesgo Operativo | Detalle y Justificación | Citas |
| :--- | :--- | :--- |
| **Falta de Colaboración Interinstitucional (Apropiación)** | Existe un riesgo significativo de que los productos (modelos, soluciones) logren **escasa apropiación por parte de los países** o que haya una falta de **colaboración y coordinación interinstitucional** entre las autoridades de tributos internos y aduanas. | **(Sección 13. Riesgos Identificados - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Cambios Políticos y de Autoridades** | Existen **riesgos de implementación asociados a cambios de autoridades y/o a potenciales cambios en el clima político y social** dentro los países participantes. Esto puede afectar la continuidad y el apoyo al proyecto. | **(Sección 13. Riesgos Identificados - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Limitación del Alcance del Piloto** | El piloto se ejecuta con **datos ficticios** en **ambientes de calidad** y con una **muestra limitada de 2 o 3 países y empresas**. Riesgo de que las lecciones aprendidas no escalen adecuadamente a un despliegue real con mayor volumen de datos y complejidad operativa. | **(Sección 9. Modelo Conceptual - ARCHIVO REOI)** - COMPROBADO POR MI |
| **Capacidad y Adaptación del Personal** | Las administraciones tributarias enfrentan desafíos de **fuerza laboral** y necesitan personal con **nuevas habilidades** para utilizar la tecnología y los datos disponibles. Existe el riesgo de que la solución técnica supere la capacidad operativa del personal de las ATyA. | **(Sección 13. Riesgos Identificados - ARCHIVO REOI)** - COMPROBADO POR MI |

---

## Propuesta de Preguntas para Talleres

Los talleres son clave para la **difusión y transferencia de conocimiento** (Componente 2) y para la **coordinación** y deben ser organizados para discutir la innovación, soluciones digitales y uso de datos con **autoridades y actores del sector privado**. Las preguntas propuestas deben estar diseñadas para mitigar los riesgos identificados y obtener la retroalimentación necesaria de los *stakeholders*. **(Sección 14. Implementación de Talleres - ARCHIVO REOI)** - COMPROBADO POR MI  

### **Taller 1: Coordinación Interinstitucional y Gobernanza (Riesgo Operativo)**

Objetivo: Establecer un mecanismo de gobernanza integrado y asegurar la **apropiación** y **coordinación** entre las Administraciones Tributarias (AT) y Aduaneras (A).

1.  **Gobernanza:** ¿Cómo se asegurará la **participación sostenida** y el **liderazgo de alto nivel** de ambas administraciones (AT y A) en el Comité de Dirección Técnica (CDT) para impulsar la **armonización de los datos y la eliminación de redundancias**? **(Sección 11. Requisitos Técnicos - ARCHIVO REOI)** - COMPROBADO POR MI  
2.  **Mecanismos de Intercambio:** ¿Cuál es la **rutina de llenado y presentación** de la F-eCX que generará el **menor impacto** en los procesos actuales del exportador e importador, y quién será el **responsable final** del mantenimiento de los traductores de datos entre los modelos fiscales y aduaneros? **(Sección 9. Modelo Conceptual - ARCHIVO REOI)** - COMPROBADO POR MI  
3.  **Trazabilidad:** ¿Qué **bloques de información** de las F-eCX son prioritarios para el **control del IVA** en las transacciones internacionales, y cómo se garantizará la **trazabilidad** de esos datos específicos a lo largo del ciclo de exportación e importación? **(Sección 13. Riesgos Identificados - ARCHIVO REOI)** - COMPROBADO POR MI  

---

### **Taller 2: Marco Normativo y Jurídico (Riesgo Normativo)**

Objetivo: Evaluar la preparación legal para la F-eCX y definir la ruta para los acuerdos de cooperación internacional.

1.  **Evaluación Legal:** De acuerdo con el análisis normativo preliminar, ¿Qué **modificaciones a los marcos normativos domésticos** (tributarios y aduaneros) son imprescindibles para permitir la operación de la F-eCX como **archivo digital precursor** de las declaraciones D-eX/D-eM y para el uso de **Credenciales Verificables**? **(Sección 13. Riesgos Identificados - ARCHIVO REOI)** - COMPROBADO POR MI  
2.  **Cooperación Internacional:** ¿Qué **alcance jurídico** debe tener el **protocolo bilateral de intercambio de información** para que los datos de la F-eCXe puedan ser utilizados por la Aduana de Importación para **gestión de riesgos** y, si fuera necesario, como **evidencia en procesos judiciales o administrativos**? **(Sección 13. Riesgos Identificados - ARCHIVO REOI)** - COMPROBADO POR MI  
3.  **Divergencias y Rectificaciones:** Dada la complejidad de las **rectificaciones post-despacho** y el **tratamiento de divergencias** (Sección 13), ¿Cuál es el procedimiento legalmente admisible en su jurisdicción para notificar y procesar un **cambio de datos** que afecte el valor o la clasificación arancelaria después de la liberación de la mercancía? **(Sección 9. Modelo Conceptual - ARCHIVO REOI)** - COMPROBADO POR MI  

---

### **Taller 3: Tecnología y Estándares (Riesgo Técnico)**

Objetivo: Definir la arquitectura, asegurar la interoperabilidad y abordar los desafíos de la implementación de la identidad digital descentralizada.

1.  **Implementación de VCs/DIDs:** ¿Cómo se manejará la **emisión y verificación** de las **Credenciales Verificables (VCs)** en el entorno del piloto para asegurar la **portabilidad y transferencia** de los documentos F-eCX sin la necesidad de conexión constante con el emisor original (Decisión de Diseño)? **(Sección 6. Principios Rectores - ARCHIVO REOI)** - COMPROBADO POR MI  
2.  **Integración de Datos:** Si el Modelo OMA es insuficiente para el control fiscal, ¿Cómo se integrarán los **códigos SKU** u otros **datos de interés nacional** en el diseño del archivo **F-eCXm** de manera que se facilite la **auditoría de inventario** de la Administración Tributaria, sin sobrecargar los requisitos de la Aduana? **(Sección 9. Modelo Conceptual - ARCHIVO REOI)** - COMPROBADO POR MI  
3.  **Seguridad de la F-eX:** En el caso de países donde la **F-eX no incluye un *hash* basado en contenido** que garantice su integridad, ¿Qué **elemento de seguridad alternativo** se propone para la validación descentralizada de la F-eCX, o qué modificaciones en el proceso de emisión de la F-eX son necesarias antes del registro de la F-eCX? **(Sección 11. Requisitos Técnicos - ARCHIVO REOI)** - COMPROBADO POR MI  
