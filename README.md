
![image](https://user-images.githubusercontent.com/73592097/161028745-44f431f3-dfff-4b74-a2e4-a3e48b3cb998.png)


# Índice #

## 1. Requisitos para la instalación de WSL 2 ##

## 2. Habilitación del Subsistema de Windows para Linux ##

## 3. Habilitación de la característica Máquina virtual ##

## 4. Descarga del paquete de actualización del kernel de Linux ##

## 5. Definición de WSL 2 como versión predeterminada ##

## 6. Instalación de la distribución de Linux que quiera ##

## 7. Instalación de docker ##

## 8. Instalación de la imagen de Laravel en docker ##


<hr>

**1. Requisitos para la instalación**

Los requisitos para instalar los programas que a continuación vamos a descibir son:

- Sistema Operativo Windows 10 sistemas x64: La versión 1903 o posterior, con la compilación 18362 o posterior.

**2. Habilitación del Subsistema de Windows para Linux**
Antes de instalar las distribuciones de Linux en Windows, habilitaremos las características opcional "Subsistema de Windows para Linux".

Para ello localizamos y ejecutamos PowerShell como administrador, y ejecutamos  el siguiente comando:

> dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart 

![image](https://user-images.githubusercontent.com/73592097/161030977-ae12abc0-7872-4f6d-a05d-5b39bedf0d92.png)

**3. Habilitación de la característica Máquina virtual**

Antes de instalar WSL 2, debe habilitar la característica opcional Plataforma de máquina virtual. La máquina necesitará funcionalidades de virtualización para usar esta característica para ello vamos nuevamenta a la ventana abierta PowerShell y ejecutamos el siguiente comando:

> dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

![image](https://user-images.githubusercontent.com/73592097/161034267-e7a15de9-a884-433d-a382-6e709d892018.png)


Posteriormente reiniciamos para completar la instalaciónfr WSL 2 

**4. Descarga del paquete de actualización del kernel de Linux**

Ahora descargamos la versión más reciente del kernel de Linux en WSL 2 para maquinas x64 en el siguiente [enlace](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

Seguidamente ejecutaremos el instalador y daremos siguiente a todas las ventanas, hasta finalizar con la siguiente ventana

![image](https://user-images.githubusercontent.com/73592097/161035082-f68715c5-1d94-4523-86a8-aa347634f8b6.png)

**5. Definición de WSL 2 como versión predeterminada**

En la  PowerShell, ejecutaremos el siguiente comando para establecer WSL2 como version predeterminada al instalar una nueva distribución de Liunux.

> wsl --set-default-version 2

![image](https://user-images.githubusercontent.com/73592097/161035661-9ec93512-a087-4de8-861d-3cd3dc996e11.png)

**6. Instalación de la distribución de Linux**

En este paso vamos a instalar la distribución de Linux favorita, para ello vamos a [Microsoft Store](https://aka.ms/wslstore),oh bien si no nos aparece en el buscador introducimos la palabra Linux

![image](https://user-images.githubusercontent.com/73592097/161036611-7f1be929-2b67-410e-9952-ed0be71960ee.png)

En la página de la distribución seleccionamos -> obtener 

![image](https://user-images.githubusercontent.com/73592097/161036792-defb193e-24d2-416c-827f-425859085acc.png)

Se nos abrira una ventana en la que tendremos que poner nuestro usuario y contraseña.

![image](https://user-images.githubusercontent.com/73592097/161037262-1f712667-ad70-4882-aa5d-147e2ad71628.png)

**7. Instalación de docker**
Ahora vamos a descargarnos docker desde la pagina [oficial](https://www.docker.com/get-started/)

Para ello nos descargaremos docker Desktop para windows y ejecutamos el instalador una vez descargada la aplicación, y seguimos la guia de instalación de docker

Una vez instalado reiniciamos el sistema


Ahora iniciamos docker y nos aparecerá una ventana similar a la siguiente

![image](https://user-images.githubusercontent.com/73592097/161039316-f692f9b5-68e0-45f3-b4f8-96c8096f3e9c.png)

Nos vamos a configuración que se encuentra en la barra azul

![image](https://user-images.githubusercontent.com/73592097/161039440-3bf96782-f684-4d5c-9a26-d1125855f7db.png)

Nos aparecerá la siguiente ventana 
![image](https://user-images.githubusercontent.com/73592097/161039537-84eeb99d-c4e9-4161-8899-c73ce18ee294.png)

Iremos a recursos y posteriormente a la opcion WSL INTEGRATION 

![image](https://user-images.githubusercontent.com/73592097/161039690-9f8145ab-ccc2-461f-a0e5-1f2278131a65.png)

Habilitaremnos la distribuciñon que tengamos instalada en mi caso es Ubuntu

![image](https://user-images.githubusercontent.com/73592097/161039818-23e4c0a4-4b07-4032-8b6f-f89005d170df.png)

En la terminal de la distribucion de ubuntu, nos aseguraremos que tenemos docker instalado co nel siguiente comando

![image](https://user-images.githubusercontent.com/73592097/161040133-63410695-357e-4529-889d-b5def469b3c4.png)


**8. Instalación de la imagen de Laravel en docker**

Para la instalación de la imagen de Laravel en docker introduciremos el siguiente comando que se nos descargara la imagen en docker, el comando es

> curl -s https://laravel.build/helloworld | bash

![image](https://user-images.githubusercontent.com/73592097/161041619-c7df69df-c756-4b9e-80a5-f444f33567cc.png)

Nos aparecera el proyecto creado por laravel

![image](https://user-images.githubusercontent.com/73592097/161041916-2d25d568-8d44-4530-9c77-dfd2d142de4b.png)

Entramos en la carpeta del proyecto

A continuación lanzamos el proyecto con el comando

> cd helloword/

> ./vendor/bin/sail up

![image](https://user-images.githubusercontent.com/73592097/161042945-229b07e8-1a40-416f-9fef-9029287dd25e.png)

Esto nos llevará un tiempo 

![image](https://user-images.githubusercontent.com/73592097/161043177-ef7bcd84-6037-4a0a-9de3-457f6ec4684d.png)

















