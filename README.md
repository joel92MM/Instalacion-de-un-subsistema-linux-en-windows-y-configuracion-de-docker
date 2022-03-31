
![image](https://user-images.githubusercontent.com/73592097/161028745-44f431f3-dfff-4b74-a2e4-a3e48b3cb998.png)


# Índice #

## 1. Requisitos para la instalación ##

## 2. Habilitación del Subsistema de Windows para Linux ##

## 3. Comprobación de los requisitos para ejecutar WSL 2 ##

## 4. Habilitación de la característica Máquina virtual ##

## 5. Descarga del paquete de actualización del kernel de Linux ##

## 6. Definición de WSL 2 como versión predeterminada ##

## 7. Instalación de la distribución de Linux que quiera ##

####

<hr>

**1. Requisitos para la instalación**

Los requisitos para instalar los programas que a continuación vamos a descibir son:

- Sistema Operativo Windows 10 sistemas x64: La versión 1903 o posterior, con la compilación 18362 o posterior.

**2. Habilitación del Subsistema de Windows para Linux**
Antes de instalar las distribuciones de Linux en Windows, habilitaremos las características opcional "Subsistema de Windows para Linux".

Para ello localizamos y ejecutamos PowerShell como administrador, y ejecutamos  el siguiente comando:

> dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart 

![image](https://user-images.githubusercontent.com/73592097/161030977-ae12abc0-7872-4f6d-a05d-5b39bedf0d92.png)


