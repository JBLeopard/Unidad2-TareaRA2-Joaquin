# 1. Documentación sobre el trazado de la vulnerabilidad

En esta documentación se realiza el **trazado completo de una vulnerabilidad**, navegando por las distintas listas y organismos oficiales de ciberseguridad.  
Así pues, se trata de:  

- Conocer las principales listas de información sobre ciberseguridad (CVE, NVD, CWE, CAPEC, etc.).
- Aprender a realizar el **trazado de una vulnerabilidad** desde una fuente informativa inicial hasta sus patrones de ataque.
- Analizar el impacto, criticidad y debilidades asociadas a una vulnerabilidad real.

**Vulnerabilidad analizada**

- **Producto afectado:** GoAnywhere MFT  
- **Fabricante:** Fortra  
- **Tipo:** Omisión de autenticación  
- **Gravedad:** Crítica

La vulnerabilidad permite a un atacante no autenticado acceder a funcionalidades internas de la aplicación.

---

## 1.1 Inicio del trazado (INCIBE)

El trazado comienza a partir de un artículo publicado por INCIBE, donde se informa de una vulnerabilidad crítica que afecta a GoAnywhere MFT.  
En dicho artículo se describe de forma general el problema y se proporcionan referencias externas para ampliar la información.

![INCIBE 1](./imagenes/1.png)
![INCIBE 2](./imagenes/2.png)

---

## 1.2 Web oficial del fabricante (Fortra)

Desde el artículo de INCIBE se accede a la web oficial del fabricante, donde se publica el aviso de seguridad correspondiente.

En esta página se detallan:
- La descripción técnica de la vulnerabilidad
- Las versiones afectadas
- Las medidas de mitigación y parches disponibles

![FORTRA 1](./imagenes/3.png)
![FORTRA 2](./imagenes/4.png)

---

## 1.3 Identificación del CVE y análisis

En la información proporcionada por el fabricante se identifica el identificador CVE asignado a la vulnerabilidad.  
Este identificador permite realizar el seguimiento oficial del fallo de seguridad en las diferentes bases de datos.  
Accedemos a la página oficial de **cve.org**, donde se muestra la información básica del CVE:

- Descripción de la vulnerabilidad  
- Referencias oficiales  
- Fecha de publicación  

![CVE 1](./imagenes/5.png)
![CVE 2](./imagenes/6.png)

---

## 1.4 Consulta en la NVD (NIST)

A continuación se consulta la **National Vulnerability Database (NVD)** mantenida por el NIST, donde se amplía la información técnica.

![NVD 1](./imagenes/7.png)

En la NVD se muestra la puntuación **CVSS**, que indica el nivel de riesgo de la vulnerabilidad.

- **Puntuación CVSS:** 9.8 Crítica  
- **Vector CVSS:** Permite analizar los factores utilizados para calcular la puntuación  

![NVD 2](./imagenes/8.png)

También podemos ver las versiones de softwate a las que afecta:  

![NVD 3](./imagenes/9.png)
![NVD 4](./imagenes/10.png)

---

## 1.5 Análisis de la CWE

Desde la NVD se identifican las **debilidades (CWE)** explotadas por la vulnerabilidad.  
Accedemos a la página oficial de **cwe.mitre.org** para analizar en detalle la debilidad principal.  
En esta sección se describe:  
- En qué consiste la debilidad  
- Lenguajes y tecnologías afectadas  
- Posibles mitigaciones  

![CWE 1](./imagenes/11.png)

Se observa la relación de la debilidad con otras CWE, mostrando jerarquías de debilidades padre e hijas.

![CWE 2](./imagenes/12.png)

También una lista de CVE relacionadas.

![CWE 3](./imagenes/13.png)

Patrones de ataque (CAPEC)  
Desde la información de la CWE se accede a los **patrones de ataque (CAPEC)** que pueden explotar esta debilidad.  

![CWE 4](./imagenes/14.png)

---

## 1.6 Análisis del patrón de ataque CAPEC

En la web oficial de **capec.mitre.org** se analiza el patrón de ataque identificado.  
Se detallan:  
- Descripción del ataque  
- Flujo de ejecución  
- Requisitos previos  
- Consecuencias  
- Posibles mitigaciones  

![CWE 4](./imagenes/14.png)

---

## 1.7 Descarga del registro CVE en formato JSON

Finalmente, desde **cve.org** se accede al **registro CVE en formato JSON**, utilizado para el tratamiento automatizado de la información de vulnerabilidades.  
Este registro contiene información estructurada sobre:  
- CVE  
- CWE  
- CPE  
- CAPEC  
- Referencias oficiales

``` sql
{"dataType":"CVE_RECORD","dataVersion":"5.1","cveMetadata":{"cveId":"CVE-2024-0204","assignerOrgId":"df4dee71-de3a-4139-9588-11b62fe6c0ff","state":"PUBLISHED","assignerShortName":"Fortra","dateReserved":"2024-01-03T00:12:28.436Z","datePublished":"2024-01-22T18:05:13.194Z","dateUpdated":"2025-05-30T14:22:31.288Z"},"containers":{"cna":{"affected":[{"defaultStatus":"affected","product":"GoAnywhere MFT","vendor":"Fortra","versions":[{"lessThan":"7.4.1","status":"affected","version":"6.0.1","versionType":"semver"}]}],"credits":[{"lang":"en","type":"finder","user":"00000000-0000-4000-9000-000000000000","value":"Mohammed Eldeeb & Islam Elrfai, Spark Engineering Consultants"}],"descriptions":[{"lang":"en","supportingMedia":[{"base64":false,"type":"text/html","value":"Authentication bypass in Fortra's GoAnywhere MFT prior to 7.4.1 allows an unauthorized user to create an admin user via the administration portal."}],"value":"Authentication bypass in Fortra's GoAnywhere MFT prior to 7.4.1 allows an unauthorized user to create an admin user via the administration portal."}],"impacts":[{"capecId":"CAPEC-1","descriptions":[{"lang":"en","value":"CAPEC-1 Accessing Functionality Not Properly Constrained by ACLs"}]}],"metrics":[{"cvssV3_1":{"attackComplexity":"LOW","attackVector":"NETWORK","availabilityImpact":"HIGH","baseScore":9.8,"baseSeverity":"CRITICAL","confidentialityImpact":"HIGH","integrityImpact":"HIGH","privilegesRequired":"NONE","scope":"UNCHANGED","userInteraction":"NONE","vectorString":"CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H","version":"3.1"},"format":"CVSS","scenarios":[{"lang":"en","value":"GENERAL"}]}],"problemTypes":[{"descriptions":[{"cweId":"CWE-425","description":"CWE-425 Direct Request ('Forced Browsing')","lang":"en","type":"CWE"}]}],"providerMetadata":{"orgId":"df4dee71-de3a-4139-9588-11b62fe6c0ff","shortName":"Fortra","dateUpdated":"2024-02-02T17:06:23.244Z"},"references":[{"tags":["vendor-advisory"],"url":"https://www.fortra.com/security/advisory/fi-2024-001"},{"tags":["permissions-required"],"url":"https://my.goanywhere.com/webclient/ViewSecurityAdvisories.xhtml"},{"url":"http://packetstormsecurity.com/files/176683/GoAnywhere-MFT-Authentication-Bypass.html"},{"url":"http://packetstormsecurity.com/files/176974/Fortra-GoAnywhere-MFT-Unauthenticated-Remote-Code-Execution.html"}],"solutions":[{"lang":"en","supportingMedia":[{"base64":false,"type":"text/html","value":"Upgrade to version 7.4.1 or higher. The vulnerability may also be eliminated in non-container deployments by deleting the&nbsp;InitialAccountSetup.xhtml file in the install directory and restarting the services. For container-deployed instances, replace the file with an empty file and restart. For additional information, see&nbsp;<a target=\"_blank\" rel=\"nofollow\" href=\"https://my.goanywhere.com/webclient/ViewSecurityAdvisories.xhtml\">https://my.goanywhere.com/webclient/ViewSecurityAdvisories.xhtml</a>&nbsp;(registration required).<a target=\"_blank\" rel=\"nofollow\" href=\"https://my.goanywhere.com/webclient/ViewSecurityAdvisories.xhtml\"></a>"}],"value":"Upgrade to version 7.4.1 or higher. The vulnerability may also be eliminated in non-container deployments by deleting the InitialAccountSetup.xhtml file in the install directory and restarting the services. For container-deployed instances, replace the file with an empty file and restart. For additional information, see  https://my.goanywhere.com/webclient/ViewSecurityAdvisories.xhtml https://my.goanywhere.com/webclient/ViewSecurityAdvisories.xhtml  (registration required).  https://my.goanywhere.com/webclient/ViewSecurityAdvisories.xhtml"}],"source":{"advisory":"XXX-YYY","discovery":"UNKNOWN"},"title":"Authentication Bypass in GoAnywhere MFT","workarounds":[{"lang":"en","supportingMedia":[{"base64":false,"type":"text/html","value":"Users are encouraged to apply defense-in-depth tactics to limit access to the administrative console. Do not expose the console to the internet and apply web application controls such as a WAF, monitoring, and access controls.&nbsp;"}],"value":"Users are encouraged to apply defense-in-depth tactics to limit access to the administrative console. Do not expose the console to the internet and apply web application controls such as a WAF, monitoring, and access controls."}],"x_generator":{"engine":"Vulnogram 0.1.0-dev"}},"adp":[{"providerMetadata":{"orgId":"af854a3a-2127-422b-91ae-364da2661108","shortName":"CVE","dateUpdated":"2024-08-01T17:41:15.984Z"},"title":"CVE Program Container","references":[{"tags":["vendor-advisory","x_transferred"],"url":"https://www.fortra.com/security/advisory/fi-2024-001"},{"tags":["permissions-required","x_transferred"],"url":"https://my.goanywhere.com/webclient/ViewSecurityAdvisories.xhtml"},{"url":"http://packetstormsecurity.com/files/176683/GoAnywhere-MFT-Authentication-Bypass.html","tags":["x_transferred"]},{"url":"http://packetstormsecurity.com/files/176974/Fortra-GoAnywhere-MFT-Unauthenticated-Remote-Code-Execution.html","tags":["x_transferred"]}]},{"metrics":[{"other":{"type":"ssvc","content":{"timestamp":"2025-05-08T15:41:03.677995Z","id":"CVE-2024-0204","options":[{"Exploitation":"none"},{"Automatable":"yes"},{"Technical Impact":"total"}],"role":"CISA Coordinator","version":"2.0.3"}}}],"title":"CISA ADP Vulnrichment","providerMetadata":{"orgId":"134c704f-9b21-4f2e-91b3-4a467353bcc0","shortName":"CISA-ADP","dateUpdated":"2025-05-30T14:22:31.288Z"}}]}}
```

[CVE-2024-0204.json](https://github.com/JBLeopard/Unidad2-TareaRA2-Joaquin/blob/main/docs/CVE-2024-0204.json)

---

