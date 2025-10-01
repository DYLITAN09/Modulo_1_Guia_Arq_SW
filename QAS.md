La distinción entre requisitos funcionales (RF) y atributos de calidad (QAS) es fundamental en la arquitectura de *software*. En el contexto del proyecto **RG-T4185** sobre la **Factura Electrónica de Comercio Exterior (F-eCX)**, las fuentes definen claramente ambos aspectos, siendo los RF el *qué* hace el sistema y los QAS el *cómo* lo hace de manera efectiva. *(Derivado del REOI – COMPROBADO POR MI)*

---

### **Diferencia entre Requisitos Funcionales y Atributos de Calidad (QAS)**

| Categoría | Requisitos Funcionales (RF) | Atributos de Calidad (QAS) / Requisitos No Funcionales |
| :--- | :--- | :--- |
| **Definición** | Describen **qué** debe hacer el sistema. Están directamente ligados a las funcionalidades que el usuario final necesita para lograr un objetivo específico. | Describen **cómo** el sistema debe realizar sus funciones (restricciones y cualidades). Determinan la calidad del software y el diseño de la arquitectura. |
| **Ejemplos en F-eCX** | **Generar** el archivo digital F-eCX; **Validar** el *hash* de una F-eX incluida; **Transmitir** el F-eCXe a la aduana de importación; **Generar** la F-eCXm para la administración tributaria. *(Sección de actividades clave – COMPROBADO POR MI)* | **Interoperabilidad**; **Seguridad y Privacidad**; **Trazabilidad**; **Sostenibilidad y Escalabilidad**; **Flexibilidad**; **Rendimiento** (implícito en las pruebas de la solución). *(Principios rectores – COMPROBADO POR MI)* |
| **Origen en Fuentes** | Actividades clave del proceso F-eCX [126–134, 277–292] – COMPROBADO POR MI | Principios Rectores y Requisitos Técnicos [66–68] – COMPROBADO POR MI |

---

## **Atributos de Calidad (QAS) y Escenarios Medibles**

*(Los siguientes atributos y escenarios fueron derivados a partir de los principios técnicos y funcionales del proyecto F-eCX – COMPROBADO POR MI)*

A continuación, se formulan escenarios medibles (Estímulo – Respuesta – Métrica) para los principales Atributos de Calidad (QAS) identificados en la documentación del proyecto F-eCX.

---

### **1. QAS: Seguridad y Autenticidad (Integridad de Datos)**

Este atributo es fundamental, ya que el sistema debe asegurar la autenticidad de los emisores y receptores y la integridad de la información desde la emisión de la F-eX hasta la F-eCXm. La solución se basa en **Credenciales Verificables (VCs)** y **firmas digitales**. *(Sección de tecnología – COMPROBADO POR MI)*

| Escenario Medible (Estímulo – Respuesta – Métrica) | Detalle y Justificación |
| :--- | :--- |
| **Estímulo:** Un actor malicioso intenta cargar un archivo **F-eCX** cuya F-eX original (F-eX 01) ha sido modificada, resultando en una **inconsistencia en el *hash*** que la aduana de exportación debe verificar. | La validación de la F-eCX requiere verificar la autenticidad de las F-eX que la componen mediante la comprobación de sus *hashes*. |
| **Respuesta:** El sistema de validación de la Aduana de Exportación (que opera como verificador) **detecta la discrepancia** de seguridad (el *hash* no coincide) e **impide la validación** de la F-eCX. |
| **Métrica:** **Tasa de Detección de Falsificación (Integridad Criptográfica).** Se mide como el porcentaje de documentos con *hashes* manipulados que son detectados y rechazados por el sistema de validación de la aduana (Objetivo: 100%). |

---

### **2. QAS: Interoperabilidad**

La solución debe ser interoperable con otros sistemas y plataformas que sigan los **estándares del W3C**. Se requiere una **capa de integración basada en APIs** para conectar sistemas aduaneros y tributarios. *(Sección de interoperabilidad – COMPROBADO POR MI)*

| Escenario Medible (Estímulo – Respuesta – Métrica) | Detalle y Justificación |
| :--- | :--- |
| **Estímulo:** La Aduana de Exportación finaliza el despacho (levante para embarque) y el sistema inicia la rutina para **enviar el archivo F-eCXe** a la Aduana de Importación a través de la API de intercambio. | El intercambio de datos transfronterizo debe ser electrónico y se realiza a través de rutinas de envío/puesta a disposición de la F-eCXe. |
| **Respuesta:** El sistema de la Aduana de Importación **recibe el archivo F-eCXe** y lo deja disponible para el Importador, sin errores de formato o estructura de datos (XML/OMA). |
| **Métrica:** **Tiempo de Latencia en el Intercambio Internacional.** Se mide el tiempo promedio (en segundos) transcurrido entre la finalización del despacho en el país de exportación y la disponibilidad del archivo F-eCXe en el sistema de la Aduana de Importación (e.g., objetivo: < 10 segundos). |

---

### **3. QAS: Rendimiento (Eficiencia de Procesamiento)**

Aunque no se lista explícitamente como "rendimiento" en los principios, el proyecto incluye **pruebas de rendimiento**, lo que implica que la rapidez y eficiencia del procesamiento son atributos críticos. *(Sección pruebas de la solución – COMPROBADO POR MI)*

| Escenario Medible (Estímulo – Respuesta – Métrica) | Detalle y Justificación |
| :--- | :--- |
| **Estímulo:** El Importador intenta **validar la F-eCXi** para registrar una D-eM, un proceso que requiere que el sistema compruebe la autenticidad del *hash* del F-eCXe de origen y la corrección de las cantidades/valores agregados. | La Aduana debe validar la F-eCXi antes de registrar la D-eM. El rendimiento se mide por la velocidad con la que se completan las rutinas de validación. |
| **Respuesta:** La aplicación de la Aduana de Importación **completa la validación** de la F-eCXi y devuelve la respuesta al Importador (validada o rechazada). |
| **Métrica:** **Tiempo de Respuesta de la Validación Crítica (TMS).** Se mide el tiempo máximo (en milisegundos) que tarda el sistema en realizar la validación de la F-eCXi para un caso de uso complejo (e.g., objetivo: < 2,000 ms). |

---

### **4. QAS: Sostenibilidad y Adaptabilidad (Flexibilidad Tecnológica y Normativa)**

La solución debe ser **flexible** para adaptarse a diferentes regulaciones y debe permitir **ajustes y mejoras** debido a cambios normativos u operativos, además de ser compatible con futuras tecnologías. *(Requisitos técnicos – COMPROBADO POR MI)*

| Escenario Medible (Estímulo – Respuesta – Métrica) | Detalle y Justificación |
| :--- | :--- |
| **Estímulo:** Uno de los países participantes modifica su ley aduanera, requiriendo un **nuevo campo de datos obligatorio** para la **D-eX** (que debe ser incluido en la portada de la F-eCX). | La solución debe ser flexible y desarrollarse de forma modular en base a componentes independientes que permitan el escalamiento. |
| **Respuesta:** El equipo técnico actualiza el componente de la portada de la F-eCX y el módulo de validación en el ambiente de calidad. |
| **Métrica:** **Tiempo de Despliegue de Ajustes.** Tiempo (en días) requerido para que un cambio normativo simple sea integrado, probado y desplegado en el ambiente de calidad (e.g., objetivo: < 7 días). |

---

### **5. QAS: Trazabilidad**

Es crucial asegurar que todas las acciones y transacciones sean **trazables y auditables** para mantener la confianza en el sistema. La Aduana debe conservar los archivos de versiones anteriores si se rectifica una F-eCX. *(Sección de trazabilidad – COMPROBADO POR MI)*

| Escenario Medible (Estímulo – Respuesta – Métrica) | Detalle y Justificación |
| :--- | :--- |
| **Estímulo:** Un auditor intenta acceder al **historial completo** de una F-eCX (F-eCX 0976) que fue rectificada tres veces (ej. F-eCX 0976 versión 04). | La trazabilidad es esencial para la gestión de riesgos. El sistema debe registrar los números y las fechas de las F-eCX sobre las que se realizaron cambios para **reconstruir el historial completo**. |
| **Respuesta:** El sistema proporciona un registro inmutable que permite acceder a las cuatro versiones del documento y a las F-eCX modificadoras/correctivas asociadas. |
| **Métrica:** **Porcentaje de Auditabilidad del Historial de Versiones.** Porcentaje de F-eCX modificadas donde todas las versiones anteriores y los archivos rectificadores asociados son accesibles y coherentes (Objetivo: 100%). |
