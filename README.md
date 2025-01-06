## Development

1. Clonar el repositorio
2. Crear un .env basado en el .env.template
3. Inicializar y actualizar Sub-módulos, cuando alguien clona el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos
```
git submodule update --init --recursive
```
4. Ejecutar npm i en cada uno de los submodulos
5. Ejecutar `docker-compose up --build`

## Para ver mas bonito buscar en la paletta de comando. 
Open preview

## Para crear un nuevo submodulo en el launcher
1. En github crear un nuvo repository y incluyo el readme porque no se pueden crear repositorios vbacios
2. crear todo como el paso 3 de `Pasos para crear los Git Submodules` 
3. Despues borro el readme y para crear dentro de esa carpeta misma un nuevo projecto de nest sin crear otra carpeta hago lo siguiente
  3.1 Dentro de la carpeta hago ``nest new <nombre_de_la_carpeta> --directory .``


### Pasos para crear los Git Submodules
1. Crear un nuevo repositorio en GitHub
2. Clonar el repositorio en la máquina local
3. Añadir el submodule, donde `repository_url` es la url del repositorio y `directory_name` es el nombre de la carpeta donde quieres que se guarde el sub-módulo (no debe de existir en el proyecto)
```
git submodule add <repository_url> <directory_name>
```
4. Añadir los cambios al repositorio (git add, git commit, git push)
Ej:
```
git add .
git commit -m "Add submodule"
git push
```

5. Para actualizar las referencias de los sub-módulos
```
git submodule update --remote
```


## Importante
Si se trabaja en el repositorio que tiene los sub-módulos, **primero actualizar y hacer push** en el sub-módulo y **después** en el repositorio principal. 

Si se hace al revés, se perderán las referencias de los sub-módulos en el repositorio principal y tendremos que resolver conflictos.