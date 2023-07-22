## Tomar en cuenta

El scroll del touchpad, de la laptop está configurado para que se comporte
con la configuración "Natural Scroll", esta configuración está pensada 
para funcionar como si fuera un dispositivo móvil, o táctil.

Se quiere evitar esta configuración quitando esta configuración.

## Solución

Modificar el archivo: /etc/X11/xorg.conf.d/30-touchpad.conf, o crearlo 
en esa ruta:

    vim /etc/X11/xorg.conf.d/30-touchpad.conf

Listo, en ahí vamos a generar la siguiente configuración correspondiente

    Section "Inputclass"
        Identifier "devname"
        Driver "libinput"
        Option "Tapping" "on"
    EndSection

Antes se encontraba la opción: `Option "NatualScrolling" "true"` 
se removió para optener lo deseado.

## Historia

En un principio me encontraba trabajando con NaturalScrolling normal, 
esto por tema que yo quería trabajar así, pero tuve que optar por trabajar 
de esa manera por la siguiente razón.

En mi trabajo como desarrollador,
me proporcionaron una computadora con sistema operativo Windows y si
bien puedo configurarlo a mi manera, al momento de que necesito ayuda
y mis compañeros quieren ayudarme, esta característica al momento de
hacer scroll con el mouse, les resulta 
incómoda. Por ese motivo tuve que adaptarme al desempeño normal del
Scroll, que Windows trae por defecto.

## Referencias

https://gist.github.com/miguelmota/c35999dbf9c15154d0aec8dace29d481


