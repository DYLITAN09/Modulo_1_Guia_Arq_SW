El proyecto **RG-T4185** se enfoca en el desarrollo e implementación de un piloto de la **Factura Electrónica de Comercio Exterior (F-eCX)**. A continuación, se presenta la extracción de los actores clave, sus roles, las dependencias institucionales y los supuestos subyacentes.

***

## 1. Stakeholders (Interesados) y Roles

Los interesados del proyecto se dividen en entidades ejecutoras/financieras, beneficiarios directos (países y entidades) y operadores clave:

| Stakeholder | Rol en el Proyecto / Función Principal | Citas |
| :--- | :--- | :--- |
| **Banco Interamericano de Desarrollo (BID)** | **Agencia Ejecutora (AE)**, Proveedor de financiamiento (Bien Público Regional - BPR). Es responsable de la supervisión, el desembolso, la propiedad intelectual de los productos y la coordinación regional. | |
| **División de Gestión Fiscal (IFD/FMM)** | **Unidad Ejecutora y Líder del Equipo del Proyecto**. Supervisa la consultoría y es responsable del desembolso de fondos. | |
| **Mónica Calijuri** | **Jefe/Líder de Equipo** (IFD/FMM). Supervisa la consultoría y debe **aprobar por escrito todos los entregables**. | |
| **Firmas Consultoras / Consultores Individuales** | Contratados para realizar la revisión de literatura, desarrollar lineamientos, elaborar el diseño conceptual, desarrollar el **prototipo**, y ejecutar el pilotaje de la solución F-eCX. | |
| **Países Beneficiarios (Brasil, Colombia, R. Dominicana, Guatemala, Uruguay)** | Son los destinatarios del proyecto. Proveen una **contrapartida local en especie** (tiempo dedicado a la revisión de insumos técnicos, participación en el piloto, coorganización de reuniones). | |
| **ATyA (Administraciones Tributarias y Aduaneras)** | **Beneficiarios directos del modelo**. Deben validar la información y gestionar el flujo de la F-eCX/D-eX/D-eM. Su rol es la integración y el control de las operaciones de comercio exterior. | |
| **Comité de Dirección Técnica (CDT)** | Conformado por representantes de los países. Su función principal es **analizar el desarrollo del programa de trabajo, revisar los términos de referencia y facilitar el desarrollo de las actividades**. | |
| **Exportador** | **Genera la F-eCX** a partir de una o más **F-eX validadas** y la transmite a la Aduana de Exportación, solicitando el registro de la D-eX. | |
| **Importador** | **Genera la F-eCXi** a partir de la F-eCXe recibida y solicita el registro de la Declaración de Importación (D-eM). | |
| **Sector Privado (Empresas)** | Participan en la validación de la funcionalidad y eficacia de la solución (2 o 3 empresas seleccionadas). Son el objetivo de la **facilitación del comercio** y el cumplimiento tributario. | |
| **Socios Estratégicos** | Incluyen al **CIAT, FAD del FMI y la OMA**. Colaboran, coordinan con el equipo del BID y proporcionan lineamientos (OMA). | |

## 2. Dependencias Institucionales

Las dependencias clave reflejan la necesidad de **coordinación** para lograr la integración regional y nacional, tanto en el desarrollo del piloto como en su futura operatividad.

*   **Aprobación y Financiamiento:** La ejecución del proyecto (CT RG-T4185) y el pago a consultores dependen del **BID** y, específicamente, de la **aprobación escrita** de la Especialista Líder de Sector, Mónica Calijuri.
*   **Gobernanza Nacional:** El proyecto requiere la creación de un **Comité de Dirección Técnica (CDT)** con representantes de los países para guiar el programa de trabajo.
*   **Cooperación ATyA Nacional:** Para el correcto funcionamiento del modelo F-eCX, es indispensable una **voluntad de cooperación y coordinación interinstitucional** entre las autoridades de tributos internos y las aduanas dentro de cada país. Se debe **designar un equipo coordinador mixto** de ambas administraciones.
*   **Integración Documental (Exportación):** La F-eCX (creada por el Exportador) es el archivo digital preparatorio para la D-eX. La Aduana de Exportación depende de que la F-eCX esté validada para poder generar la D-eX.
*   **Integración Documental (Importación):** El Importador requiere el archivo **F-eCXe** (proporcionado por la Aduana de Exportación/Importación) para poder generar la F-eCXi, la cual es la base para la D-eM.
*   **Marco Normativo:** La implementación final de la F-eCX requiere que los países realicen un **análisis exhaustivo de su marco normativo doméstico e internacional** para asegurar que los acuerdos actuales contemplen las facultades necesarias, o que se realicen los cambios normativos requeridos.
*   **Interoperabilidad:** La solución digital requiere una **capa de integración basada en APIs** para conectarse con los sistemas aduaneros y tributarios existentes, así como con la **VUCE**.

## 3. Supuestos Explícitos e Implícitos

El diseño y la viabilidad del proyecto se basan en varios supuestos tecnológicos, funcionales y de gobernanza:

### A. Supuestos Explícitos (Definidos en el Alcance o Diseño Conceptual)

1.  **Modelo F-eX Preexistente:** El modelo conceptual propuesto **presupone la existencia de la emisión de la F-eX** en una fase previa al despacho de exportación, antes del registro de la D-eX. La falta de una F-eX reduce los beneficios de la integración.
2.  **Tecnología de Identidad Descentralizada:** La solución se desarrollará obligatoriamente utilizando **Credenciales Verificables (VCs) e Identificadores Descentralizados (DIDs)**, siguiendo los **estándares de la W3C**.
3.  **Tecnología de Código Abierto:** Todos los componentes de la solución deben estar **basados en código abierto** (Open Source), según los requerimientos del BID.
4.  **Modelo de Datos de Referencia:** El modelo de datos adoptado es el de la **Organización Mundial de Aduanas (OMA)**.
5.  **Exclusiones del Piloto:** Para simplificar la prueba piloto, ciertas funcionalidades complejas (como la rectificación de la F-eCXe después del despacho o el tratamiento de las divergencias entre exportador e importador) **serán eliminadas o simplificadas**.

### B. Supuestos Implícitos (Condiciones necesarias para el éxito o el avance)

1.  **Voluntad Política Sostenida:** Se asume que la **renovada voluntad de cooperación** entre las ATyA de ALC para el intercambio de información se mantendrá durante todo el periodo de ejecución del proyecto (36 meses).
2.  **Capacidad de Intercambio Legal:** Se asume que los países **alcanzarán los acuerdos de cooperación internacional** necesarios para permitir el intercambio electrónico de información a nivel masivo y en tiempo real, así como el uso de dicha información en procesos administrativos y judiciales.
3.  **Adaptabilidad de Sistemas Legados:** Se asume que las **plataformas tecnológicas existentes** de las ATyA (los sistemas aduaneros y tributarios) pueden ajustarse, aunque sea mínimamente, o integrarse a través de APIs, con la nueva solución F-eCX. El proyecto busca el **menor impacto** en los procesos actuales, lo que supone que la funcionalidad de conversión/traducción de datos será efectiva.
4.  **Seguridad y Trazabilidad de Documentos:** Se asume que las F-eX ya validadas contienen, o pueden incorporar, elementos de seguridad (como *hashes*) que permitan a la Aduana de Exportación **verificar la autenticidad e integridad** de la F-eX de forma descentralizada.
5.  **Gobernanza Funcional:** Se asume que el mecanismo de gobernanza (equipo coordinador mixto) será efectivo para la **armonización de los datos y la eliminación de redundancias** entre los requerimientos aduaneros y fiscales.