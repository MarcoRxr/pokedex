# 🚀 Proceso de Despliegue – PokeDex Angular

## 1. 📁 Creación del Repositorio

Se creó un repositorio en GitHub para alojar el proyecto PokeDex Angular.

---

## 2. ⚙️ Configuración del Proyecto

Se verificó que el proyecto Angular contara con:

* Archivo `package.json`
* Script de build:

```bash
npm run build
```

---

## 3. ☁️ Despliegue en Azure Static Web Apps

Se utilizó Azure Static Web Apps para desplegar la aplicación.

### Configuración del archivo YAML:

```yaml
app_location: "pokedex-angular"
api_location: ""
output_location: "dist/pokedex-angular"
app_build_command: "npm run build"
```

---

## 4. 🔧 Problemas Encontrados y Soluciones

### ❌ Error: No se encontraba el build

**Causa:** Ruta incorrecta en YAML
**Solución:** Ajustar `app_location` y `output_location`

---

### ❌ Error: Node incompatible

**Causa:** Azure usaba Node 22
**Solución:**

```json
"engines": {
  "node": "18.x"
}
```

---

### ❌ Error: No encontraba package.json

**Causa:** Proyecto en subcarpeta
**Solución:** Configurar correctamente la ruta en YAML

---

## 5. 🔐 Implementación de Seguridad

Se creó el archivo:

```bash
staticwebapp.config.json
```

Con los siguientes encabezados:

```json
{
  "globalHeaders": {
    "Content-Security-Policy": "default-src 'self'; img-src 'self' data: https:; script-src 'self' 'unsafe-inline' https:; style-src 'self' 'unsafe-inline' https:; font-src 'self' https: data:; connect-src 'self' https:;",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Content-Type-Options": "nosniff",
    "X-Frame-Options": "DENY",
    "Referrer-Policy": "no-referrer",
    "X-XSS-Protection": "1; mode=block"
  }
}
```

---

## 6. 🧪 Validación de Seguridad

Se utilizó la herramienta:

👉 https://securityheaders.com/

Resultado esperado: A o A+

---

## 7. ✅ Verificaciones Finales

* Aplicación accesible desde internet ✔
* HTTPS activo ✔
* Sin errores en consola ✔
* Buen puntaje en seguridad ✔

---

## 🎯 Conclusión

El despliegue de la aplicación fue exitoso, logrando una implementación funcional y segura. Se aplicaron buenas prácticas de DevOps y seguridad web, asegurando la protección de la aplicación frente a posibles vulnerabilidades.
