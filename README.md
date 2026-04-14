# 🧩 PokeDex Angular - Despliegue Seguro en la Nube

## 📌 Descripción del Proyecto

Este proyecto consiste en el despliegue de una aplicación web tipo PokeDex desarrollada en Angular, la cual permite visualizar información de diferentes Pokémon.

El objetivo principal es realizar un despliegue funcional en la nube aplicando buenas prácticas de seguridad web mediante encabezados HTTP.

---

## 🌐 URL de la Aplicación

👉 ( [Pokédex | Angular](https://thankful-rock-05c1e000f.7.azurestaticapps.net/)  )

---

## ⚙️ Tecnologías Utilizadas

* Angular 14
* Node.js
* Azure Static Web Apps
* GitHub Actions
* JSON (configuración de seguridad)

---

## 🔐 Seguridad Implementada

Se implementaron encabezados HTTP de seguridad mediante el archivo:

```bash
staticwebapp.config.json
```

### 🔒 Encabezados aplicados:

* **Content-Security-Policy (CSP):** Previene ataques XSS restringiendo recursos.
* **Strict-Transport-Security (HSTS):** Obliga el uso de HTTPS.
* **X-Content-Type-Options:** Evita interpretación incorrecta de archivos.
* **X-Frame-Options:** Protege contra clickjacking.
* **Referrer-Policy:** Protege información del usuario.
* **X-XSS-Protection:** Activa protección contra scripts maliciosos.

---

## 🧪 Validación de Seguridad

Se utilizó la herramienta:

👉 https://securityheaders.com/

Resultado esperado: **A o A+**

(Agregar captura aquí)

---

## 🧠 Reflexión Técnica

### 1. ¿Qué vulnerabilidades previenen los encabezados implementados?

Los encabezados de seguridad HTTP implementados permiten mitigar diversas vulnerabilidades comunes en aplicaciones web. Por ejemplo, el encabezado Content-Security-Policy (CSP) ayuda a prevenir ataques de tipo Cross-Site Scripting (XSS), ya que restringe las fuentes desde donde se pueden cargar scripts y otros recursos.

El encabezado Strict-Transport-Security (HSTS) obliga a que todas las conexiones se realicen mediante HTTPS, evitando ataques de tipo Man-in-the-Middle (MITM).

Por otro lado, X-Content-Type-Options: nosniff evita que el navegador interprete incorrectamente los tipos de archivos, reduciendo riesgos de ejecución de código malicioso.

El encabezado X-Frame-Options: DENY protege contra ataques de clickjacking, impidiendo que la aplicación sea cargada dentro de iframes externos.

Finalmente, Referrer-Policy: no-referrer evita la exposición de información sensible.

---

### 2. ¿Qué aprendiste sobre la relación entre despliegue y seguridad web?

Aprendí que el despliegue de una aplicación no solo implica hacerla accesible, sino también protegerla. Una aplicación sin medidas de seguridad puede ser vulnerable a ataques.

También entendí que la seguridad se puede mejorar mediante configuraciones externas como encabezados HTTP sin modificar el código base.

El uso de herramientas de análisis permite validar el nivel de seguridad y mejorar continuamente.

---

### 3. ¿Qué desafíos encontraste en el proceso?

Uno de los principales desafíos fue la configuración del entorno de despliegue en Azure, especialmente la correcta ubicación de los archivos en el repositorio.

También hubo dificultades con errores de build y compatibilidad de versiones de Node.js.

Finalmente, la configuración de los encabezados de seguridad requirió pruebas para no afectar el funcionamiento de la aplicación.

---

## ✅ Conclusión

El despliegue seguro es fundamental en el desarrollo web moderno. No basta con que una aplicación funcione correctamente, también debe garantizar la seguridad de los usuarios y sus datos.
