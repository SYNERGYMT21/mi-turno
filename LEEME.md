# Mi Turno · App Android (APK)

App de finanzas para conductores (Uber, Cabify, DiDi, inDrive). Los datos se guardan en el teléfono.
Se usa el Excel para respaldar e importar/exportar (pestaña Ajustes).

## Opción A · Sin instalar nada (GitHub, recomendada)
1. Crea un repositorio en github.com y sube TODO el contenido de esta carpeta
   (incluida la carpeta oculta `.github`; si usas arrastrar y soltar y no se sube, usa "git push").
2. Entra a la pestaña **Actions** → **Build APK** → **Run workflow**.
3. Cuando termine (3-6 min) abre la ejecución y descarga el archivo **MiTurno-APK** (contiene `app-debug.apk`).
4. Pasa el APK al celular, ábrelo y permite "instalar apps de orígenes desconocidos" cuando te lo pida.

## Opción B · En tu computador
Requisitos: Node 18+, JDK 17 y Android Studio.
```
npm install
npx cap add android
npm run sync
npx cap open android      # en Android Studio: Build > Build APK(s)
```
El APK queda en `android/app/build/outputs/apk/debug/app-debug.apk`.

## Notas
- Es un APK de pruebas (debug), perfecto para uso personal. Para publicar en Play Store hay que firmarlo (release).
- Los datos viven en el teléfono: si desinstalas la app se pierden. Usa **Ajustes → Exportar Excel** como respaldo.
- Para pasar datos entre el teléfono y tu Excel: Exportar Excel (app) y Importar Excel (app) con el archivo Finanzas_Conductor_v2.xlsx.
