# linux-ubuntu-protección

Este repositorio te muestra cómo agregar Canonical Livepatch como protección para tu sistema operativo Linux Ubuntu.

## Instalación de Canonical Livepatch en Linux

Para instalar Canonical Livepatch en tu sistema Linux, sigue estos pasos:

1. Abre la aplicación de Linux (Ubuntu Software).

2. Busca "livepatch" y selecciona "Canonical-Livepatch". Haz clic en "Instalar".

3. O desde la consola, ejecuta el siguiente comando para instalar:

  ```bash
   sudo snap install canonical-livepatch
   ```
Dirígete a https://ubuntu.com/livepatch, regístrate de forma gratuita y obtén un token.

Copia el comando siguiente, reemplazando <YOUR_TOKEN> con el token que obtuviste:
  
  ```bash
  sudo canonical-livepatch enable <YOUR_TOKEN>
   ```
Abre una terminal y pega el comando que copiaste en el paso anterior.

Para verificar el estado del servicio Livepatch, ejecuta el siguiente comando:

  ```bash
  sudo canonical-livepatch status
  ```
Esto mostrará el estado actual del servicio Livepatch. Si ves alguna falla, continúa con los siguientes pasos para solucionarla.

Si es necesario, reinicia el servicio Livepatch con el siguiente comando:

  ```bash
  sudo systemctl restart snap.canonical-livepatch.canonical-livepatchd
  ```
Vuelve a verificar el estado del servicio para asegurarte de que esté funcionando correctamente:

  ```bash
  sudo ua status
  ```

¡Listo! Ahora deberías tener Canonical Livepatch instalado y funcionando en tu sistema Linux.
