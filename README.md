# Como instalar FNM en Windows

1. Primeramente ponemos este comando en la terminal de Windows, ya sea CMD o PowerShell:

```(PowerShell)
winget install Schniz.fnm
```

- Este comando lo que hara sera instalar FNM en nuestra computadora, para despues usar las banderas que nos proporciona FNM.

2. Como segundo lugar tendremos que poner el seguiente comando en la terminal:

```(PowerShell)
notepad $profile
```

- Este comando lo que hara sera crear el archivo _Microsoft.PowerShell_profile_.

- Si no encuentra la ruta del archivo tendremos que poner el siguiente comando para ver o que carpeta del perfil lo debemos poner:

```(PowerShell)
notepad
```

- Ese nos dira en que carpeta debemos poner el archivo, en su mayoria es la carpeta WindowsPowerShell, entonces debemos ir a crear la carpeta que nos pide.

- **_OJO_**: Solamente crear la carpeta en el apartado que nos piden.

3. Una vez creada la carpeta podemos ingresar el siguiente comando en la terminal:

```(PowerShell)
notepad $profile
```

- Esto nos creara nuestro archivo _Microsoft.PowerShell_profile_, el cual dira que si no existe uno, si queremos crearlo, entonces, creamos uno nuevo y dentro del nuestro nuevo archivo ponemos la siguiente linea:

```(PowerShell)
fnm env --use-on-cd --shell power-shell | Out-String | Invoke-Expression
```

- Guardamos el archivo y tendriamos configurado correctamente el FNM para poder gestionar nuestra diferentes versiones de nodejs.
