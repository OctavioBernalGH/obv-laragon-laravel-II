# obv-laragon-laravel-II

Requisitos previos para crear un proyecto en Laravel:
<ul>
  <li>PHP</li>
  <li>Mysql</li>
  <li>Composer</li>
  <li>Node</li>
</ul>

Vamos a proceder a crear un nuevo proyecto en Laravel utilizando la última versión, para ello utilizaremos Laragon como localserver y composer para instalar las dependencias y crear la estructura de proyecto. Creamos un nuevo proyecto mediante el comando <b>composer create-project laravel/laravel nombre-proyecto</b>.

![image](https://user-images.githubusercontent.com/103035621/193810171-b2b096de-eb5e-47b8-8e8a-c431bf6efba4.png)

Para proseguir se ha de modificar el fichero <b>.env</b> y adaptarlo a la BBDD que disponemos, en el caso que estoy haciendo utilizo la BBDD local de Laragon:

![image](https://user-images.githubusercontent.com/103035621/193810980-74ae2e25-b477-4c5b-9693-01126de2089d.png)

A continuación aprovechando los snipets que proporciona artisan, crearemos toda la estructura base MVC, para ello utilizamos el comando <b>php artisan make:model NombreModelo -crm</b>, dicho comando creará el modelo de datos, el fichero migrations (este fichero permite definir la estructura de la BBDD, esta estructura se creará mediante <i>php artisan migrate</i> cogiéndo como estructura el fichero migrations), y el controlador:

![image](https://user-images.githubusercontent.com/103035621/193811620-7e7f21cf-6c8d-42d2-aedc-61450f6437fa.png)

Añadimos los campos deseados para la tabla en el fichero migrations creado en el anterior paso, de esta forma definimos la estructura que creará el programa:

![image](https://user-images.githubusercontent.com/103035621/193812419-5b555743-e76e-4a9d-96ed-2af4efd2a944.png)

Una vez definido aplicamos los cambios en la BBDD, para ello utilizamos el comando <b>php artisan migrate</b>.

![image](https://user-images.githubusercontent.com/103035621/193812732-6aa00de4-34e0-43a9-af1b-4687d2c1fe30.png)

Se puede observar mediante el gestor de BBDD heidi incluido en laragon que se ha creado la estructura de tabla definida en migrations:

![image](https://user-images.githubusercontent.com/103035621/193813021-2cf125de-3939-4572-8353-f44c0307b3ba.png)

Insertaremos datos en la BBDD de forma manual para comenzar a tratarlos en la aplicación, para ellos vamos al gestor y creamos las diferentes sentencias:

![image](https://user-images.githubusercontent.com/103035621/193814038-3c096c1a-5b70-4b86-b405-c241185789dd.png)
![image](https://user-images.githubusercontent.com/103035621/193814100-2c34a269-9a1c-482b-9f02-2d11db882d82.png)
