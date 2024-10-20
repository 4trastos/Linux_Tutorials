## Brillo de la pantalla en Debian.  🇪🇸

# No podemos cambiar el brillo de la pantalla con el teclado:

1. Abre la Terminal y escribe:
```
- xrandr --prop | grep "connected"
```

Esto nos mostrará el modelo de nuestro monitor. En mi caso es este `XWAYLAND0`:

```
XWAYLAND0 connected 1920X1200+0+0 (normal left inverted right x axis y axis) 490mm x 310mm
```

2. Ahora escribe el siguiente comando para saber cuál es el nivel de brillo actual:

```
xrandr --prop --verbose | grep -A10 "connected" | grep "Brightness"
Brightness: 0.0
```
(Brightness: 1.0 es el máximo).

3. Con este comando podemos modificar el brillo (para aumentar):

```
xrandr --output (nombre del monitor) --brightness 1.0
```

4. Con este comando podemos modificar el brillo (para disminuir:):

```
xrandr --output (nombre del monitor) --brightness 0.9

```


## Debian Screen Brightness. 🇬🇧

# We cannot change the screen brightness with the keyboard:

1. Open Terminal and type:
```
- xrandr --prop | grep " connected"
```

This will show us the model of our monitor. Which in my case is this one `XWAYLAND0`:

```
XWAYLAND0 connected 1920X1200+0+0 (normal left inverted right x axis y axis) 490mm x 310mm
```

2. Now type the following command to find out what the current brightness level is:

```
xrandr --prop --verbose | grep -A10 " connected" | grep "Brightness"
Brightness: 0.0
```
(Brightness: 1.0 is the maximum).

3. With this command we can modify the brightness (to increase):

```
xrandr --output (monitor name) --brightness 1.0
```

4. With this command we can modify the brightness (to decrease:):

```
xrandr --output (monitor name) --brightness 0.9

```
