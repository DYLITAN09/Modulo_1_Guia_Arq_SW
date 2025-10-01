La implementación del piloto de la Factura Electrónica de Comercio Exterior (F-eCX) bajo el proyecto **RG-T4185** se basa en un diseño conceptual que define el sistema, sus actores y sus interacciones.  
**(Sección i. Proyecto RG-T4185 - ARCHIVO BASE)** - COMPROBADO POR MI

A continuación, se presenta el diagrama C4 Nivel Contexto en formato estructurado, seguido de las Decisiones de Diseño Arquitectónico (ADR) iniciales con alternativas y *trade-offs*.  
**(Sección ii. Diseño Conceptual - DOCUMENTO DE REFERENCIA)** - COMPROBADO POR MI

---

## 1. Diagrama C4 Nivel Contexto (Texto Estructurado)

El Diagrama C4 Nivel Contexto muestra la **Plataforma de Solución Digital F-eCX** como el sistema central, interactuando con actores humanos y sistemas externos en el ciclo de exportación e importación.  
**(Sección iii. C4 Contexto - MODELO DE ARQUITECTURA)** - COMPROBADO POR MI

### Sistema Central (System Under Consideration)

| ID | Nombre | Descripción |
| :--- | :--- | :--- |
| **F-eCX** | **Plataforma de Solución Digital F-eCX** | **Sistema digital para la emisión, gestión y verificación del ciclo completo de la Factura Electrónica de Comercio Exterior (F-eCX)**, desde la exportación hasta el control fiscal en la importación. Se basa en **Credenciales Verificables (VCs) e Identificadores Descentralizados (DIDs)**. |  

**(Referencia: W3C Standards, Identidad Descentralizada)** - COMPROBADO POR MI

### Actores Humanos (Users)

| ID | Nombre | Descripción |
| :--- | :--- | :--- |
| **E** | **Exportador** | Crea la F-eCX a partir de una o más F-eX previamente validadas y la transmite a la Aduana de Exportación para solicitar el registro de la D-eX. |
| **I** | **Importador** | Recibe la F-eCXe, genera la F-eCXi y la transmite a la Aduana de Importación para solicitar el registro de la Declaración de Importación (D-eM). |
| **AT-E** | **Admin. Tributaria País Exportador** | Valida las F-eX. Se le pone a disposición el archivo de la F-eCX de final de despacho para sus controles. |
| **A-E** | **Aduana de Exportación** | Recibe y valida la F-eCX, genera la D-eX. **Transmite el archivo F-eCXe** a la Aduana de Importación. |
| **A-I** | **Aduana de Importación** | Recibe la F-eCXe, valida la F-eCXi, genera la D-eM, y genera la F-eCXm y N-eCX para retroalimentación y control fiscal. |
| **AT-I** | **Admin. Tributaria País Importador** | Recibe la F-eCXm (archivo de control tributario) de la Aduana de Importación para vincular las importaciones al expediente tributario del importador. |  

**(Fuente: Manual Operativo Aduanero - ARCHIVO BID)** - COMPROBADO POR MI

### Sistemas Colaboradores (External Systems)

| ID | Nombre | Descripción |
| :--- | :--- | :--- |
| **S-DEX** | **Sistema D-eX** | Sistema aduanero existente en el país exportador para el registro de la Declaración de Exportación (D-eX). |
| **S-DEM** | **Sistema D-eM** | Sistema aduanero existente en el país importador para el registro de la Declaración de Importación (D-eM). |
| **VUCE** | **Ventanilla Única de Comercio Exterior** | Sistema para gestionar la emisión de licencias, permisos y certificados (LPCO). |  

**(Referencia: Sistemas VUCE en ALC - ARCHIVO TÉCNICO)** - COMPROBADO POR MI

### Flujos Principales

1.  **E** crea la **F-eCX** (basada en F-eX validadas por **AT-E**) y la envía a la **F-eCX** (Plataforma).  
   **(Proceso de Creación F-eCX - MANUAL TÉCNICO)** - COMPROBADO POR MI
2.  La **F-eCX** (Plataforma) se integra con **S-DEX** para generar la D-eX.  
   **(Proceso D-eX - ARCHIVO SISTEMA EXPORTADOR)** - COMPROBADO POR MI
3.  **A-E** envía la **F-eCXe** a la **F-eCX** (Plataforma) después del despacho de exportación.  
   **(Transferencia Interinstitucional - INFORME BID)** - COMPROBADO POR MI
4.  La **F-eCX** (Plataforma) transmite la **F-eCXe** entre países cooperantes.  
   **(Protocolo de Intercambio Internacional)** - COMPROBADO POR MI
5.  **I** recibe la F-eCXe y genera la **F-eCXi** usando la **F-eCX** (Plataforma).  
   **(Validación Importador - ARCHIVO BID)** - COMPROBADO POR MI
6.  La **F-eCX** (Plataforma) se integra con **S-DEM** para generar la D-eM.  
   **(Proceso D-eM - SISTEMA ADUANERO)** - COMPROBADO POR MI
7.  **A-I** genera la **F-eCXm** y la transmite a **AT-I**.  
   **(Control Fiscal Importador - DOCUMENTO BASE)** - COMPROBADO POR MI

---

## 2. Decisiones de Diseño Arquitectónico (ADR) Iniciales

Las decisiones de diseño arquitectónico iniciales reflejan los requisitos obligatorios del proyecto (financiado por el BID) y las soluciones propuestas para manejar la complejidad de la interoperabilidad y la seguridad regional.  
**(Sección iv. ADR - DOCUMENTO BID)** - COMPROBADO POR MI

### ADR 1: Adopción de Tecnología de Identidad Descentralizada

| Decisión (ADR) | Alternativas | *Trade-offs* (Compensaciones) |
| :--- | :--- | :--- |
| **Implementar la solución F-eCX usando Credenciales Verificables (VCs) e Identificadores Descentralizados (DIDs), siguiendo los estándares del W3C.** | **A1:** Utilizar una Infraestructura de Clave Pública (PKI) centralizada gestionada por una entidad (ej. autoridad certificadora nacional). **A2:** Utilizar solo certificados de firma electrónica existentes. | **Ventajas:** **Seguridad y Privacidad**, **Autenticidad** y **Trazabilidad**. Permite la **verificación descentralizada**. **Desafíos:** Mayor **Complejidad Técnica** y riesgo de adopción. |  
**(Referencia: W3C, DID & VC Standards)** - COMPROBADO POR MI

### ADR 2: Estilo Arquitectónico para la Interoperabilidad

| Decisión (ADR) | Alternativas | *Trade-offs* (Compensaciones) |
| :--- | :--- | :--- |
| **Implementar una arquitectura de integración mediante una Capa de APIs.** | **A1:** Bases de datos compartidas o Data Lake central. **A2:** Protocolos punto a punto rígidos. | **Ventajas:** Desacoplamiento, modularidad, menor impacto en sistemas legados, flexibilidad. **Desafíos:** Mayor esfuerzo de mantenimiento de APIs y traductores. |  
**(Referencia: APIs para interoperabilidad - GUÍA BID)** - COMPROBADO POR MI

### ADR 3: Estándar del Modelo de Datos

| Decisión (ADR) | Alternativas | *Trade-offs* (Compensaciones) |
| :--- | :--- | :--- |
| **Adoptar el Modelo de Datos de la OMA como referencia.** | **A1:** Modelo regional nuevo basado en UBL. **A2:** Modelo basado solo en Factura Electrónica doméstica. | **Ventajas:** Armonización internacional, facilita el intercambio. **Desafíos:** Puede ser insuficiente para control fiscal interno. Requiere datos adicionales. |  
**(Referencia: OMA Data Model)** - COMPROBADO POR MI

### ADR 4: Estrategia de Armonización de Datos (Temporalidad)

| Decisión (ADR) | Alternativas | *Trade-offs* (Compensaciones) |
| :--- | :--- | :--- |
| **Utilizar traductores de datos como solución intermedia.** | **A1:** Modificación inmediata de sistemas nacionales al estándar F-eCX/OMA. | **Ventajas:** Minimiza impacto inicial, facilita adopción progresiva. **Desafíos:** Mantiene redundancia y complejidad en traducción. |  
**(Referencia: Estrategia de Armonización - ARCHIVO BID)** - COMPROBADO POR MI

### ADR 5: Enfoque de Licenciamiento de Software

| Decisión (ADR) | Alternativas | *Trade-offs* (Compensaciones) |
| :--- | :--- | :--- |
| **Desarrollar la solución con código abierto.** | **A1:** Adquirir solución propietaria. | **Ventajas:** Mitiga riesgo de sostenibilidad, permite auditoría y mejora del código. **Desafíos:** Requiere más recursos internos o consultoría para mantenimiento. |  
**(Referencia: Licenciamiento Open Source - DOCUMENTO PROYECTO)** - COMPROBADO POR MI
