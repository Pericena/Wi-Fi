# Wi-Fi 

Cualquier sistema operativo guarda un registro de contraseñas usadas. No están a simple vista, pero si sabemos dónde buscar, las encontraremos. Lo mismo ocurre con las claves WiFi, que quedan registradas y que te permiten no tener que configurarla cada vez que te conectas. Sin embargo, si no la usas durante un tiempo puede que te la vuelva a pedir y tengas que acudir a este artículo.
![](https://2.bp.blogspot.com/-XFgUd3Et6iU/XHNZ8hJAllI/AAAAAAAANtY/hTHDTTM3dbgPz5__p2MfhdYT57BmRFyvACLcBGAs/s1600/Screenshot_1.png)

- MAS  https://lpericena.blogspot.com/2018/10/wifi.html

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
![](https://4.bp.blogspot.com/-Oduj_bdJat8/XHNZ9wzeWWI/AAAAAAAANtk/4BR1t5jiqXI9m0vTRQSDXxI_auMsZVNnwCLcBGAs/s1600/Screenshot_4.png)
visita la pagina web para que puedas ver el proceso de la instalaci¨®n y el uso
https://lpericena.blogspot.com/2018/10/wifi.html

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


## Licencia ??

Este proyecto est¨® bajo la Licencia (Licencia publica general de GNU) - mira el archivo [LICENSE.md](LICENSE.md) para detalles

---
Por [Pericena](https://github.com/Pericena)
