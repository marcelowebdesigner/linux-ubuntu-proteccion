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


Complemento:

Chkrootkit, una solución?

Canonical, tal vez consciente de estas amenazan ha dispuesto en sus repositorios un programa que corrige o nos avisa de los posibles rootkits que habiten en nuestro sistema. La aplicación es heredada de Debian pero igualmente disponible y funcional que en la distribución madre.

Para instalarlo sólo tenemos que ir a nuestra terminal o en synaptic y escribir
  ```bash
  sudo apt-get install chkrootkit
  ```

Esto instalará el programa, la única pega que tiene es que no tiene una interfaz gráfica por lo que cada vez que se quiera usar habrá que irse a la terminal y escribir
  ```bash
  sudo chkrootkit
  ```

Esto ejecutará el análisis y os informará si vuestro equipo está o no está infectado. Si llegara a estar infectado, sólo queda la búsqueda en Google del rootkit y su solución ya que es muy difícil que un programa te solucione los rootkits, ya sea en Windows, en Mac o en Ubuntu.
