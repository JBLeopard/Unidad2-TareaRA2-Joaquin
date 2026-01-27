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

**Código comentado en Visual Studio Code**  

![Comentarios en lavadero.py](./imagenes/1.png)
![Comentarios en lavadero.py](./imagenes/2.png)
![Comentarios en lavadero.py](./imagenes/3.png)
![Comentarios en lavadero.py](./imagenes/4.png)
![Comentarios en lavadero.py](./imagenes/5.png)
![Comentarios en lavadero.py](./imagenes/6.png)
![Comentarios en lavadero.py](./imagenes/7.png)
![Comentarios en lavadero.py](./imagenes/8.png)
![Comentarios en lavadero.py](./imagenes/9.png)
![Comentarios en lavadero.py](./imagenes/10.png)
![Comentarios en lavadero.py](./imagenes/11.png)
![Comentarios en lavadero.py](./imagenes/12.png)
![Comentarios en lavadero.py](./imagenes/13.png)
![Comentarios en lavadero.py](./imagenes/14.png)
![Comentarios en lavadero.py](./imagenes/15.png)



**Archivo lavadero.py (estado final corregido):**  

[lavadero.py](https://github.com/JBLeopard/Unidad1-TareaRA1-Joaquin/blob/main/src/lavadero.py)

---

## 1.2 Documentación mediante Jupyter Notebook (estado inicial lavadero.py)

Como apoyo adicional, se ha creado un cuaderno Jupyter Notebook donde se explica:

- Pruebas unitarias de la aplicación
- Simulación

Este formato facilita una comprensión más visual y didáctica del programa.

**Notebook visualizado en el navegador**  

![Notebook Lavadero](./imagenes/notebook.png)

**Notebook del proyecto:**  

[notebook_lavadero.ipynb](./notebook_lavadero.ipynb)

---
