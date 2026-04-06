# Política de Seguridad - VStoreApp

## 1. Protección Anti-Copyright y Anti-Plagio

### Medidas Implementadas:
- **Deshabilitación de Clic Derecho**: Previene la copia directa de contenido mediante el menú contextual.
- **Bloqueo de Selección de Texto**: Impide la selección y copia de texto mediante `user-select: none`.
- **Protección contra Arrastre**: Desactiva eventos de `dragstart` y `drop` para evitar la extracción de recursos.
- **Bloqueo de Pegado**: Desactiva eventos de `paste` para prevenir inyecciones de código.
- **Marca de Agua Digital**: Incluye marca de agua invisible en el código fuente para identificar la autoría.

## 2. Protección contra Ataques y Depuración

### Medidas Implementadas:
- **Bloqueo de Herramientas de Desarrollador**: Desactiva F12, Ctrl+Shift+I, Ctrl+U y Ctrl+S.
- **Detección de DevTools**: Monitorea intentos de acceso a las herramientas de depuración.
- **Ofuscación de Código**: El JavaScript está minificado y ofuscado para dificultar el análisis.
- **Content Security Policy (CSP)**: Restringe las fuentes de contenido y previene inyecciones XSS.

## 3. Cabeceras de Seguridad HTTP

### Configuradas:
- **Strict-Transport-Security (HSTS)**: Fuerza HTTPS en todas las conexiones.
- **X-Frame-Options**: Previene clickjacking estableciendo `DENY`.
- **X-Content-Type-Options**: Previene MIME sniffing con `nosniff`.
- **X-XSS-Protection**: Activa protección XSS del navegador.
- **Referrer-Policy**: Controla información de referencia con `strict-origin-when-cross-origin`.
- **Permissions-Policy**: Deshabilita acceso a cámara, micrófono, geolocalización y otros permisos.

## 4. Protección de Recursos

### Archivos Protegidos:
- Archivos de configuración (`.env`, `.json`, `.config`)
- Archivos de base de datos (`.sql`)
- Archivos de registro (`.log`)
- Archivos de respaldo (`.bak`, `.backup`, `.tmp`)
- Archivos ocultos (comenzando con `.`)

## 5. Optimización de Caché y Compresión

### Implementado:
- **GZIP Compression**: Comprime recursos HTML, CSS, JavaScript y JSON.
- **Cache Control**: Establece tiempos de expiración según el tipo de recurso.
- **Versioning**: Los recursos estáticos se cachean por 1 mes.
- **HTML**: Se cachea por 1 hora para permitir actualizaciones frecuentes.

## 6. Integridad de Contenido

### Verificaciones:
- **Subresource Integrity (SRI)**: Verifica la integridad de bibliotecas externas.
- **Firma Digital**: Los archivos descargables están firmados digitalmente.
- **Hash de Verificación**: Se proporciona hash SHA-256 para validación.

## 7. Privacidad y Anonimato

### Garantías:
- No se recopilan datos personales sin consentimiento explícito.
- No se utilizan cookies de seguimiento.
- No se comparte información con terceros.
- Se respeta la política de privacidad de los usuarios.

## 8. Reportar Vulnerabilidades

Si descubres una vulnerabilidad de seguridad, por favor contacta a:
**Email**: security@verificadoyseguro.github.io

Por favor, no publiques vulnerabilidades públicamente hasta que hayan sido corregidas.

## 9. Actualizaciones de Seguridad

Esta política se revisa y actualiza regularmente. La última actualización fue el 6 de abril de 2026.

---

**© 2026 VStoreApp. Todos los derechos reservados.**
