# Validación de Levantamiento de Flota | Milwaukee Tool & Hangcha México 🚜⚡

Aplicación web estática, interactiva y responsiva desarrollada a partir del archivo de levantamiento de planta (`Levantamiento Planta Hangcha.xlsx`). Permite al cliente revisar y validar individual o masivamente los **85 equipos de montacargas**, confirmando especificaciones de modelos, capacidades de carga, alturas de mástil, tipos de energía, voltajes de cargador y ubicaciones por planta.

---

## 🚀 Características Principales

1. **Catálogo Completo (85 Equipos)**:
   - Vista en **Tarjetas visuales** o en **Tabla compacta** tipo Excel.
   - Buscador universal en tiempo real (# de equipo, modelo, tipo, depto, planta).
   - Filtros instantáneos por:
     - **Planta**: Golden, Planta 1, Planta 2.
     - **Modelo**: DR16LI, BT45LI, FPG25 (Gas), FBT20LI, FBE25LI, OPM02LI, CBD20-WD, MJ20 (Mima).
     - **Departamento**: Warehouse, CI, Shipping, Test Lab, Relevo, EHS.
     - **Estado de Validación**: Pendientes, Aprobados, Con Cambios.

2. **Sistema de Validación con Paloma y Tacha**:
   - 🟢 **Paloma (Aprobar)**: Marca el equipo con visto bueno.
   - 🔴 **Tacha (Requiere Cambio / Rechazar)**: Abre un panel desplegable de observaciones para que el cliente especifique:
     - Etiquetas rápidas: `Capacidad Carga`, `Altura Mástil`, `Voltaje/Cargador`, `Modelo Incorrecto`, `Reubicar Planta`, `Tipo de Equipo`.
     - Campo de texto libre para detallar el requerimiento exacto (ej. *"Se requiere capacidad de 2.5T en vez de 1.6T"*).
   - Botón de **Aprobación Masiva**: Permite aprobar con un solo clic todos los equipos filtrados (ej. todas las unidades de un modelo o planta homogénea).

3. **Vista Agrupada por Familia de Modelos (8 Modelos)**:
   - Resumen consolidado de especificaciones técnicas por modelo.
   - Posibilidad de validar familias completas en un solo clic.

4. **Persistencia Automática (LocalStorage)**:
   - El cliente puede recargar la página o cerrar el navegador sin perder su avance.

5. **Múltiples Opciones de Entrega de Resultados a Hangcha**:
   - 📊 **Descargar Excel Oficial (.xlsx)**: Genera un archivo con las columnas originales del levantamiento más:
     - `ESTADO DE VALIDACIÓN` (`APROBADO (PALOMA) ✓`, `REQUIERE CAMBIO (TACHA) ✕`, `PENDIENTE`)
     - `OBSERVACIONES / CAMBIOS SOLICITADOS`
     - `MOTIVOS SELECCIONADOS`
     - `FECHA DE VALIDACIÓN`
     - `VALIDADO POR`
     - Hoja adicional con **Resumen Ejecutivo** y métricas.
   - 💬 **Enviar por WhatsApp**: Permite ingresar cualquier número de WhatsApp de destino (o dejar en blanco para elegir el contacto) con el desglose preformateado.
   - ✉️ **Enviar por Correo**: Dirigido automáticamente a **projectmilwhang@gmail.com** con el informe técnico completo redactado.
   - 📋 **Copiar Resumen**: Copia el reporte ejecutivo al portapapeles.
   - 💾 **Respaldos JSON**: Guardar y cargar sesiones en archivo `.json`.

---

## 💻 Cómo Probar la Aplicación en Local

Simplemente haz doble clic sobre el archivo `index.html` o ábrelo en cualquier navegador web moderno (Google Chrome, Safari, Microsoft Edge, Firefox). **No requiere servidor, ni instalación de software, ni conexión de base de datos.**

---

## 🌐 Cómo Subir a GitHub y Activar GitHub Pages (Paso a Paso)

Puedes publicar la aplicación en GitHub de dos maneras:

### Opción A: Desde la Terminal (Recomendado)

1. Abre tu terminal en la carpeta del proyecto:
   ```bash
   cd "/Users/flavioberlanga/Desktop/Proyecto Milwaukee-Hangcha"
   ```

2. Inicializa el repositorio Git (si aún no está inicializado):
   ```bash
   git init
   git add .
   git commit -m "feat: Aplicacion web de Hojas de Datos y Validacion Milwaukee-Hangcha con fichas tecnicas PDF"
   ```

3. Crea un nuevo repositorio en [GitHub.com](https://github.com/new) (por ejemplo llamado `validacion-milwaukee-hangcha`).

4. Conecta tu repositorio local y sube los cambios:
   ```bash
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/validacion-milwaukee-hangcha.git
   git push -u origin main
   ```

5. **Activa GitHub Pages**:
   - En tu repositorio de GitHub, ve a **Settings** (Configuración) > **Pages**.
   - En **Build and deployment** > **Source**, selecciona `Deploy from a branch`.
   - En **Branch**, selecciona `main` y carpeta `/ (root)`.
   - Haz clic en **Save** (Guardar).
   - En 1 o 2 minutos, GitHub te dará un enlace público como:
     `https://TU_USUARIO.github.io/validacion-milwaukee-hangcha/`

---

### Opción B: Directamente desde la Web de GitHub (Sin Terminal)

1. Ve a [GitHub.com](https://github.com/new) y crea un repositorio público (ej. `validacion-milwaukee-hangcha`).
2. Haz clic en **"uploading an existing file"** (subir archivos existentes).
3. Arrastra todos los archivos de esta carpeta (`index.html`, los archivos `.png`, `.pdf` y este `README.md`).
4. Haz clic en **Commit changes**.
5. Ve a **Settings** > **Pages** > selecciona rama `main` y guarda.
6. ¡Listo! Comparte el enlace generado con el cliente.

---

## 📋 Estructura de Archivos

```
Proyecto Milwaukee-Hangcha/
├── Levantamiento Planta Hangcha.xlsx  # Archivo Excel original de referencia
├── index.html                        # Aplicación web interactiva (Hojas de Datos)
├── logo-milwaukee.png                # Logotipo oficial de Milwaukee Tool
├── logo-hangcha.png                  # Logotipo oficial de Hangcha
├── *.png                             # Fotografías oficiales de cada modelo
├── *.pdf                             # Fichas técnicas oficiales descargables
└── README.md                         # Guía de uso y despliegue a GitHub
```
