# 4. Reflexión sobre los riesgos de las aplicaciones

La aplicación desarrollada y analizada en los apartados anteriores es una aplicación local de consola, con una funcionalidad concreta y un alcance bastante limitado. Desde el punto de vista de la seguridad, este tipo de aplicaciones presentan unos riesgos claramente inferiores a los de aplicaciones más complejas o expuestas a Internet.

Al tratarse de una aplicación local, que no realiza comunicaciones de red ni intercambia información con otros sistemas, la superficie de ataque es muy reducida. No existen muchos de los riesgos habituales en aplicaciones web, como inyecciones SQL, ataques XSS, CSRF o accesos no autorizados desde el exterior. En este sentido, la mayoría de los posibles problemas de seguridad estarían relacionados con errores de programación o fallos en la lógica de la propia aplicación.

Durante el desarrollo y análisis de la aplicación, se observa que las entradas del usuario están bastante controladas, ya que se realizan mediante opciones concretas mostradas por consola. Esto limita mucho las posibilidades de introducir datos maliciosos o inesperados. Aun así, este tipo de aplicaciones no están completamente libres de riesgos. Una validación incorrecta o un mal control del flujo del programa podría provocar comportamientos no deseados, bloqueos o resultados incorrectos.

En un entorno local, el impacto de este tipo de fallos suele ser reducido y normalmente afecta únicamente al propio usuario o al sistema donde se ejecuta la aplicación. Sin embargo, esta práctica ayuda a entender que incluso en aplicaciones sencillas es importante tener en cuenta aspectos básicos de seguridad desde el desarrollo.

Si se comparan estos riesgos con los de otros tipos de aplicaciones, las diferencias son evidentes. Por ejemplo, una aplicación bancaria suele estar expuesta a Internet y gestiona información extremadamente sensible, como datos financieros y credenciales de acceso. En este caso, una vulnerabilidad puede tener consecuencias muy graves, como pérdidas económicas, fraudes o accesos no autorizados a cuentas de usuario.

En aplicaciones del ámbito de la salud, los riesgos son todavía más críticos. Estas aplicaciones manejan datos médicos personales, por lo que un fallo de seguridad puede afectar directamente a la privacidad de los pacientes e incluso tener consecuencias legales importantes. Además, en este tipo de aplicaciones la disponibilidad de la información es fundamental, ya que un error podría impedir el acceso a datos necesarios para la atención sanitaria.

Por otro lado, las aplicaciones de redes sociales presentan riesgos diferentes, relacionados principalmente con la privacidad, la suplantación de identidad y el uso indebido de la información personal de los usuarios. Al contar con una gran cantidad de usuarios y datos, cualquier vulnerabilidad puede tener un impacto muy amplio.

Comparando todos estos casos, queda claro que los riesgos de una aplicación dependen en gran medida de sus características, su exposición y el tipo de información que gestiona. La aplicación desarrollada en esta práctica tiene un perfil de riesgo bajo, pero sirve como ejemplo para comprender cómo deben analizarse los riesgos en función del contexto.

En este sentido, el uso de estándares como OWASP ASVS resulta muy útil, ya que permite adaptar los requisitos de seguridad al tipo de aplicación que se está desarrollando. No todas las aplicaciones necesitan el mismo nivel de protección, pero todas deberían aplicar medidas de seguridad acordes a los riesgos que presentan.

Esta reflexión me ha permitido entender mejor que la seguridad no es un conjunto de reglas fijas que se aplican igual a todos los proyectos, sino un aspecto que debe evaluarse de forma realista en función del tipo de aplicación y su uso.

---

![](./imagenes/seguridad.jpg)
