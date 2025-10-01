El proyecto **RG-T4185, "Apoyo a la Gestión Digital Fiscal y Aduanera en LAC"**, es una Cooperación Técnica (CT) no reembolsable del Banco Interamericano de Desarrollo (BID) que se enfoca en la modernización del comercio exterior mediante la digitalización.

A continuación, se presenta el resumen de los objetivos, el alcance y las restricciones regulatorias de este proyecto.

***

### **Objetivos del Proyecto RG-T4185**

El objetivo general es **contribuir y acelerar el desarrollo y la implementación de la Factura Electrónica de Comercio Exterior (F-eCX)**, mediante el diseño, implementación y pilotaje del modelo. Esto busca contribuir a la eficiencia en la recolección de tributos, disminuir el fraude y la evasión, y promover el comercio regional e internacional en un contexto de trazabilidad e integridad.

**Objetivos Estratégicos Clave (Justificación):**

*   **Control Fiscal y Aduanero:** Mejorar la recaudación tributaria y aduanera, perfeccionando la gestión de riesgo. Específicamente, es fundamental para lograr un **control efectivo del Impuesto sobre el Valor Añadido (IVA)** de exportación e importación.
*   **Integración:** Diseñar un modelo que permita:
    *   **Integrar los controles** de la administración tributaria y aduanera a nivel nacional en el país de exportación.
    *   **Interconectar los controles aduaneros** entre los países de exportación e importación.
    *   **Integrar los controles aduaneros y fiscales** en el país de importación.
*   **Facilitación del Comercio:** Simplificar el proceso regulatorio y facilitar el cumplimiento tributario y aduanero a los operadores económicos, promoviendo **ahorros de tiempo y recursos financieros** para el sector privado.
*   **Armonización:** Promover el desarrollo de lineamientos regionales y el diseño de la F-eCX en aras de la **armonización, estandarización y digitalización** en la región.

### **Alcance del Proyecto RG-T4185**

El alcance principal es el desarrollo e implementación de un **piloto de una solución digital** para la emisión y gestión de la F-eCX que se apalanca en el uso de credenciales verificables (VCs).

**Componentes y Entregables (Componente 1 - US$395,000):**

1.  **Desarrollo de Lineamientos Regionales:** Desarrollo de lineamientos, estrategias, guías, y el **diseño del modelo conceptual y operativo regional** de F-eCX armonizado. Esto incluye el relevamiento y compilación de los marcos regulatorios y normativos.
2.  **Solución Digital y Pilotaje:** Diseño e implementación de una solución digital de interoperabilidad que incorpore criterios modernos de seguridad y ciberseguridad.
    *   El piloto debe ser adaptable a las necesidades de los países exportadores e importadores participantes.
    *   El alcance del piloto deberá contemplar la participación de las administraciones aduaneras y tributarias de **2 o 3 países participantes** (Brasil, Colombia, Guatemala, República Dominicana y Uruguay son los países beneficiarios).
    *   También incluirá la participación de **2 o 3 empresas** seleccionadas para validar la funcionalidad y eficacia de la solución.
    *   La implementación de la prueba piloto se ejecutará en etapas, iniciando con la integración de la factura de exportación y la declaración de exportación, y concluyendo con la integración de la declaración de importación con la factura de importación.
    *   El piloto se ejecutará con **datos ficticios** en **ambientes de calidad** para simular operaciones reales, **sin efectos jurídicos**.

**Tecnología Mandatoria:**

*   La solución debe apalancarse obligatoriamente en el uso de **Credenciales Verificables (VCs)** e **Identificadores Descentralizados (DIDs)**, siguiendo los **estándares de la W3C**.
*   El desarrollo se realizará en **código abierto** (OpenSource), según los requisitos del BID.
*   El modelo de datos se basará en el **Modelo de Datos de la Organización Mundial de Aduanas (OMA)**, adaptado a las necesidades específicas de la F-eCX y de las administraciones nacionales.

### **Restricciones Regulatorias y de Diseño**

Las restricciones provienen del marco normativo y de las simplificaciones aplicadas para el piloto:

| Restricción Regulatoria/Diseño | Detalle y Justificación | Secciones Citadas |
| :--- | :--- | :--- |
| **Análisis Normativo Requerido** | Es necesario que los países realicen un **análisis exhaustivo de su marco normativo doméstico e internacional** para definir si los acuerdos actuales contemplan las facultades necesarias para ejecutar las operaciones definidas o si se requieren **cambios normativos**. | |
| **Base Normativa Interna** | El modelo propuesto **presupone la existencia de la emisión de la F-eX** (Factura Electrónica de Exportación) en una fase previa al despacho de exportación (antes del registro de la D-eX). La falta de una F-eX reduce los beneficios de integración entre ATyA. | |
| **Modelo de Datos (OMA)** | El Modelo de Datos de la OMA es la referencia, pero puede ser **insuficiente para los intereses del control fiscal interno**; por lo tanto, no debe ser una limitación para que la F-eCX mantenga **datos de interés nacional**. | |
| **Impacto Normativo Mínimo** | La solución debe buscar el **menor impacto** en los procesos actuales de la administración tributaria y aduanera, recomendando el uso de **traductores de datos** como alternativa para minimizar cambios estructurales en los modelos de datos existentes. | |
| **Simplificación de la Rectificación (Piloto)** | Para simplificar el piloto, las rectificaciones de la F-eCX (antes de la D-eX) se harán mediante **cancelación y emisión de una nueva F-eCX**. Esto elimina la necesidad de operar los estados de F-eCX modificadora, complementaria o correctiva durante el piloto en esa etapa. | |
| **Exclusión de Rectificaciones Post-Exportación (Piloto)** | El piloto **no tratará las rectificaciones** de la F-eCXe que se produzcan después de la finalización del despacho de exportación, lo que elimina la posibilidad de operar la F-eCXi modificadora. | |
| **Exclusión de Tratamiento de Divergencias (Piloto)** | Los procedimientos de la sección 13 del documento de diseño conceptual, relativos al **tratamiento de las divergencias entre el exportador y el importador**, **no se procesarán en el piloto**. | |