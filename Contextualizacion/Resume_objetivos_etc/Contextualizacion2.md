El proyecto **RG-T4185** se enfoca en el desarrollo e implementación de un piloto de la **Factura Electrónica de Comercio Exterior (F-eCX)**  
**(Sección ii. Introducción – ARCHIVO REOI)** – COMPROBADO POR MI.  

A continuación, se presenta la extracción de los actores clave, sus roles, las dependencias institucionales y los supuestos subyacentes.  
**(Sección iii. Marco Institucional – ARCHIVO REOI)** – COMPROBADO POR MI.  

***

## 1. Stakeholders (Interesados) y Roles

Los interesados del proyecto se dividen en entidades ejecutoras/financieras, beneficiarios directos (países y entidades) y operadores clave.  
**(Sección iv. Descripción de Servicios – ARCHIVO REOI)** – COMPROBADO POR MI.  

| Stakeholder | Rol en el Proyecto / Función Principal | Citas |
| :--- | :--- | :--- |
| **Banco Interamericano de Desarrollo (BID)** | **Agencia Ejecutora (AE)**, Proveedor de financiamiento (Bien Público Regional - BPR). Es responsable de la supervisión, el desembolso, la propiedad intelectual de los productos y la coordinación regional. | **(Sección iii. Marco Institucional – ARCHIVO REOI)** – COMPROBADO POR MI |
| **División de Gestión Fiscal (IFD/FMM)** | **Unidad Ejecutora y Líder del Equipo del Proyecto**. Supervisa la consultoría y es responsable del desembolso de fondos. | **(Sección iii. Marco Institucional – ARCHIVO REOI)** – COMPROBADO POR MI |
| **Mónica Calijuri** | **Jefe/Líder de Equipo** (IFD/FMM). Supervisa la consultoría y debe **aprobar por escrito todos los entregables**. | **(Términos de Referencia – ARCHIVO REOI)** – COMPROBADO POR MI |
| **Firmas Consultoras / Consultores Individuales** | Contratados para realizar la revisión de literatura, desarrollar lineamientos, elaborar el diseño conceptual, desarrollar el **prototipo**, y ejecutar el pilotaje de la solución F-eCX. | **(Sección iv. Descripción de Servicios – ARCHIVO REOI)** – COMPROBADO POR MI |
| **Países Beneficiarios (Brasil, Colombia, R. Dominicana, Guatemala, Uruguay)** | Son los destinatarios del proyecto. Proveen una **contrapartida local en especie** (tiempo dedicado a la revisión de insumos técnicos, participación en el piloto, coorganización de reuniones). | **(Anexo 1 – ARCHIVO REOI)** – COMPROBADO POR MI |
| **ATyA (Administraciones Tributarias y Aduaneras)** | **Beneficiarios directos del modelo**. Deben validar la información y gestionar el flujo de la F-eCX/D-eX/D-eM. Su rol es la integración y el control de las operaciones de comercio exterior. | **(Sección Técnica – ARCHIVO REOI)** – COMPROBADO POR MI |
| **Comité de Dirección Técnica (CDT)** | Conformado por representantes de los países. Su función principal es **analizar el desarrollo del programa de trabajo, revisar los términos de referencia y facilitar el desarrollo de las actividades**. | **(Sección v. Gobernanza – ARCHIVO REOI)** – COMPROBADO POR MI |
| **Exportador** | **Genera la F-eCX** a partir de una o más **F-eX validadas** y la transmite a la Aduana de Exportación, solicitando el registro de la D-eX. | **(Sección Técnica – ARCHIVO REOI)** – COMPROBADO POR MI |
| **Importador** | **Genera la F-eCXi** a partir de la F-eCXe recibida y solicita el registro de la Declaración de Importación (D-eM). | **(Sección Técnica – ARCHIVO REOI)** – COMPROBADO POR MI |
| **Sector Privado (Empresas)** | Participan en la validación de la funcionalidad y eficacia de la solución (2 o 3 empresas seleccionadas). Son el objetivo de la **facilitación del comercio** y el cumplimiento tributario. | **(Sección Alcance – ARCHIVO REOI)** – COMPROBADO POR MI |
| **Socios Estratégicos** | Incluyen al **CIAT, FAD del FMI y la OMA**. Colaboran, coordinan con el equipo del BID y proporcionan lineamientos (OMA). | **(Sección Cooperación – ARCHIVO REOI)** – COMPROBADO POR MI |

---

## 2. Dependencias Institucionales

Las dependencias clave reflejan la necesidad de **coordinación** para lograr la integración regional y nacional, tanto en el desarrollo del piloto como en su futura operatividad.  
**(Sección v. Gobernanza – ARCHIVO REOI)** – COMPROBADO POR MI.  

* **Aprobación y Financiamiento:** La ejecución del proyecto (CT RG-T4185) y el pago a consultores dependen del **BID** y de la **aprobación escrita** de la Especialista Líder de Sector, Mónica Calijuri.  
  **(Sección iii. Marco Institucional – ARCHIVO REOI)** – COMPROBADO POR MI  

* **Gobernanza Nacional:** El proyecto requiere la creación de un **Comité de Dirección Técnica (CDT)** con representantes de los países para guiar el programa de trabajo.  
  **(Sección v. Gobernanza – ARCHIVO REOI)** – COMPROBADO POR MI  

* **Cooperación ATyA Nacional:** Para el correcto funcionamiento del modelo F-eCX, es indispensable la **coordinación interinstitucional** entre autoridades tributarias y aduaneras en cada país.  
  **(Sección iv. Descripción de Servicios – ARCHIVO REOI)** – COMPROBADO POR MI  

* **Integración Documental (Exportación):** La F-eCX (creada por el Exportador) es requisito para la D-eX.  
  **(Sección Técnica – ARCHIVO REOI)** – COMPROBADO POR MI  

* **Integración Documental (Importación):** El Importador necesita la **F-eCXe** para generar la F-eCXi y la D-eM.  
  **(Sección Técnica – ARCHIVO REOI)** – COMPROBADO POR MI  

* **Marco Normativo:** Requiere análisis del marco legal nacional e internacional.  
  **(Sección Marco Legal – ARCHIVO REOI)** – COMPROBADO POR MI  

* **Interoperabilidad:** Se prevé una **capa de integración basada en APIs** conectada a los sistemas tributarios y aduaneros.  
  **(Sección Técnica – ARCHIVO REOI)** – COMPROBADO POR MI  

---

## 3. Supuestos Explícitos e Implícitos

El diseño y la viabilidad del proyecto se basan en varios supuestos tecnológicos, funcionales y de gobernanza **(Sección iii. Supuestos-ARCHIVO REOI) - COMPROBADO POR MI**.

### A. Supuestos Explícitos (Definidos en el Alcance o Diseño Conceptual)

1. **Modelo F-eX Preexistente:** El modelo conceptual propuesto presupone la existencia de la emisión de la F-eX en una fase previa al despacho de exportación, antes del registro de la D-eX. La falta de una F-eX reduce los beneficios de la integración **(Sección iii.a.1-ARCHIVO REOI) - COMPROBADO POR MI**.  
2. **Tecnología de Identidad Descentralizada:** La solución se desarrollará obligatoriamente utilizando **Credenciales Verificables (VCs) e Identificadores Descentralizados (DIDs)**, siguiendo los estándares de la W3C **(Sección iii.a.2-ARCHIVO REOI) - COMPROBADO POR MI**.  
3. **Tecnología de Código Abierto:** Todos los componentes de la solución deben estar basados en **código abierto (Open Source)**, según los requerimientos del BID **(Sección iii.a.3-ARCHIVO REOI) - COMPROBADO POR MI**.  
4. **Modelo de Datos de Referencia:** El modelo de datos adoptado es el de la **Organización Mundial de Aduanas (OMA)** **(Sección iii.a.4-ARCHIVO REOI) - COMPROBADO POR MI**.  
5. **Exclusiones del Piloto:** Para simplificar la prueba piloto, ciertas funcionalidades complejas (como la rectificación de la F-eCXe después del despacho o el tratamiento de las divergencias entre exportador e importador) serán eliminadas o simplificadas **(Sección iii.a.5-ARCHIVO REOI) - COMPROBADO POR MI**.  

### B. Supuestos Implícitos (Condiciones necesarias para el éxito o el avance)

1. **Voluntad Política Sostenida:** Se asume que la renovada voluntad de cooperación entre las ATyA de ALC para el intercambio de información se mantendrá durante todo el periodo de ejecución del proyecto (36 meses) **(Sección iii.b.1-ARCHIVO REOI) - COMPROBADO POR MI**.  
2. **Capacidad de Intercambio Legal:** Se asume que los países alcanzarán los acuerdos de cooperación internacional necesarios para permitir el intercambio electrónico de información a nivel masivo y en tiempo real, así como el uso de dicha información en procesos administrativos y judiciales **(Sección iii.b.2-ARCHIVO REOI) - COMPROBADO POR MI**.  
3. **Adaptabilidad de Sistemas Legados:** Se asume que las plataformas tecnológicas existentes de las ATyA (los sistemas aduaneros y tributarios) pueden ajustarse, aunque sea mínimamente, o integrarse a través de APIs, con la nueva solución F-eCX. El proyecto busca el menor impacto en los procesos actuales, lo que supone que la funcionalidad de conversión/traducción de datos será efectiva **(Sección iii.b.3-ARCHIVO REOI) - COMPROBADO POR MI**.  
4. **Seguridad y Trazabilidad de Documentos:** Se asume que las F-eX ya validadas contienen, o pueden incorporar, elementos de seguridad (como *hashes*) que permitan a la Aduana de Exportación verificar la autenticidad e integridad de la F-eX de forma descentralizada **(Sección iii.b.4-ARCHIVO REOI) - COMPROBADO POR MI**.  
5. **Gobernanza Funcional:** Se asume que el mecanismo de gobernanza (equipo coordinador mixto) será efectivo para la armonización de los datos y la eliminación de redundancias entre los requerimientos aduaneros y fiscales **(Sección iii.b.5-ARCHIVO REOI) - COMPROBADO POR MI**.  

