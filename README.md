# VisionGuard-dev
App de navegacion IA para personas con discapacidad visual

## Build y subida a Google Play (EAS)

Pasos rápidos:

1. Instalar EAS CLI:

```bash
npm install -g eas-cli
```

2. Iniciar sesión en Expo:

```bash
eas login
```

3. Construir AAB para Play (perfil `production` ya configurado):

```bash
eas build --platform android --profile production
```

4. (Opcional) Subir a Google Play con una cuenta de servicio:

 - Crea la cuenta de servicio en Google Play Console → Settings → API access → Create service account.
 - Descarga el JSON y guárdalo en la raíz del proyecto como `service-account.json`.
 - Ejecuta:

```bash
eas submit --platform android --profile production --service-account-json ./service-account.json
```

Notas:
- Si EAS pregunta por credenciales (keystore), permite que EAS las gestione automáticamente a menos que tengas una propia.
- Para pruebas rápidas en tu móvil, puedes usar el perfil `preview`:

```bash
eas build --platform android --profile preview
```

No compartas el JSON o contraseñas por chat; guárdalos localmente y ejecuta los comandos en tu máquina.
