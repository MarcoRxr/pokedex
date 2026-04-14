# 🔐 Reflexión Técnica – Seguridad en el Despliegue de PokeDex

## 1. ¿Qué vulnerabilidades previenen los encabezados implementados?

Los encabezados de seguridad HTTP implementados permiten mitigar diversas vulnerabilidades comunes en aplicaciones web. Por ejemplo, el encabezado **Content-Security-Policy (CSP)** ayuda a prevenir ataques de tipo Cross-Site Scripting (XSS), ya que restringe las fuentes desde donde se pueden cargar scripts y otros recursos.

El encabezado **Strict-Transport-Security (HSTS)** obliga a que todas las conexiones se realicen mediante HTTPS, evitando ataques de tipo Man-in-the-Middle (MITM).

Por otro lado, **X-Content-Type-Options: nosniff** evita que el navegador interprete incorrectamente los tipos de archivos, reduciendo riesgos de ejecución de código malicioso.

El encabezado **X-Frame-Options: DENY** protege contra ataques de clickjacking, impidiendo que la aplicación sea cargada dentro de iframes externos.

Finalmente, **Referrer-Policy: no-referrer** evita la exposición de información sensible en las cabeceras HTTP al navegar entre sitios.

---

## 2. ¿Qué aprendiste sobre la relación entre despliegue y seguridad web?

Aprendí que el despliegue de una aplicación web no solo consiste en hacerla accesible en internet, sino también en asegurarla adecuadamente. La seguridad es una parte fundamental del proceso de despliegue, ya que una aplicación expuesta sin protección puede ser vulnerable a múltiples ataques.

Además, entendí que herramientas como los encabezados HTTP de seguridad permiten fortalecer la aplicación sin necesidad de modificar directamente el código fuente. También aprendí la importancia de validar la seguridad utilizando herramientas como escáneres web, que permiten medir el nivel de protección implementado.

En resumen, el despliegue y la seguridad están completamente relacionados: una aplicación bien desplegada debe ser funcional, accesible y segura al mismo tiempo.

---

## 3. ¿Qué desafíos encontraste en el proceso?

Durante el proceso, uno de los principales desafíos fue la configuración correcta de las rutas y archivos en el entorno de despliegue, especialmente al trabajar con servicios en la nube como Azure Static Web Apps.

También resultó complicado entender por qué ocurrían ciertos errores durante el build y despliegue, como problemas con la ubicación del proyecto o incompatibilidades de versiones de Node.js.

Otro desafío importante fue la implementación de los encabezados de seguridad, ya que era necesario comprender qué hace cada uno y cómo configurarlos correctamente sin afectar el funcionamiento de la aplicación.

Finalmente, interpretar los resultados del escaneo de seguridad y mejorar la calificación requirió ajustes y pruebas adicionales hasta lograr un nivel adecuado de protección.

---

## ✅ Conclusión

Este proceso permitió comprender que la seguridad web es un componente esencial en cualquier despliegue. No basta con que una aplicación funcione correctamente, también debe proteger la información y garantizar una experiencia segura para el usuario.
