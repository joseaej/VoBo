# VoBo

**VoBo** es una aplicación móvil diseñada para la generación, firma y gestión de certificados oficiales, con un enfoque inicial validado en los **Certificados de Instalación de Gas (IRG)** en España.

## 🎯 Propuesta de Valor
Permitir a los instaladores autorizados generar certificados IRG desde su móvil, firmarlos digitalmente en pantalla y exportarlos a PDF en menos de 60 segundos. Ideal para enviar al cliente o subir directamente a las áreas privadas de distribuidoras (como Nedgia).

## 🛠️ Stack Tecnológico (Arquitectura Base)
La aplicación cuenta con una arquitectura robusta, diseñada para funcionar offline y ser fácilmente escalable a otros oficios en el futuro (electricidad, fontanería, etc.).

- **Framework:** Flutter (Dart) - Código unificado para Android e iOS.
- **Gestión de Estado:** Riverpod o BLoC.
- **Base de Datos:** Drift (SQLite) o Isar. Funcionamiento **100% local-first**, garantizando el acceso sin conexión.
- **Firma Digital:** Paquete `signature` (captura y exportación en PNG/SVG).
- **Motor PDF:** Paquetes `pdf` y `printing` en Dart puro (documentos vectoriales, sin pérdida de calidad).
- **Compartición Nativas:** `share_plus` para envío rápido por WhatsApp, Email o guardado en dispositivo.
- **Monetización:** RevenueCat (Modelo Freemium: uso gratuito limitado mensual + Plan Pro ilimitado).

## 💡 Por qué el nicho de Certificados IRG
Tras analizar el mercado y descartar los "partes de trabajo genéricos" por alta saturación, se eligió el nicho de gas por sus excelentes características:
1. **Barrera de entrada normativa máxima:** Solo un instalador habilitado e inscrito en el Registro Integrado Industrial puede firmar.
2. **Competencia inexistente en España:** Las apps actuales están orientadas a normativa británica (Gas Safe) o a climatización (F-gas/RITE).
3. **Fuera del alcance Verifactu:** Al ser un documento técnico y no una factura con valor fiscal, se evita la carga de homologación normativa de Hacienda (obligatoria en 2026/2027 para software de facturación).
