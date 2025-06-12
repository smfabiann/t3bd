README - Tarea 3 INF-239 (2025-1)

Integrantes:
- Fabian San Martin 202304650-7
- Maximiliano Yáñez - 202304626-4

IMPORTANTE
Se uso Docker Desktop, MongoCompass, Mongosh y Nootebook Jupiter.
Este trabajo se realizo en Windows 11 junto con Ubuntu WSL. Cualquier ejecucion
fuera de este ambiente no se garantiza que funcione.

Aplicaciones
- Docker Desktop
- Mongo MongoCompass
- Mongosh
- Nootebook Jupiter

Archivos:
- deploy-202304626-4-202304650-7.yml
- pymongo-202304626-4-202304650-7.ipynb
- uarxiv-202304626-4-202304650-7.json
Los datos completos del .json estan aqui https://discord.com/channels/@me/1354242253203443772/1382861610498003014
El .json de la tarea solo tiene los cambios que hicimos.


Intrucciones:
1. Tener las aplicaciones mencionadas arriba instaladas. Tambien como un WSL de Linux Ubuntu.
2. En la carpeta donde se armará el trabajo, en una terminal, colocar este comando (con Docker Desktop abierto):
    ´´´
    docker-compose -f deploy-202304626-4-202304650-7.yml up -d
    ´´´
2. Una vez montado el MongoDB con Docker, insertaremos los datos. Para ello, abrir MongoCompass y colocar como URL esto:
    ´´´
    mongodb://mongo1:30001,mongo2:30002,mongo3:30003/?replicaSet=my-replica-set&readPreference=primary&ssl=false
    ´´´  
    Dar a conectar y deberia haber conectado sin problemas. En el caso contrario cambiar "mongo1", "mongo2" y "mongo3" por "localhost".
    Y ya deberia estar funcionando.
3. Ahora se puede usar el Jupiter Notebook correctamente. Para facilitar el uso, se usará directamente en Visual Studio Code.
4. Todas las pruebas de ejecucion estaran adrento del Jupiter Notebook

No usamos el Script especial dada por la tarea para insertar datos porque se nos crasheaba a cada rato, asi que tuvimos que insertar los 
datos por MongoCompass. Los unicos datos faltaran son las urls de los "pdf-source".
En la consulta que nos piden los links de los urls (la .c) hicimos que pida los link al momento de insertar los datos en vez de la sacarlos
directamente de MongoBD por el problema mencionado anteriormente.