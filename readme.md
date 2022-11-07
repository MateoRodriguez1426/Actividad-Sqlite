



### Actividad de desarrollo de base de datos en Sqlite
### Ejercicio Semanal - SQLite
#### Definir y aplicar cada uno de los siguientes conceptos

- **update**
- **estructura de la base de datos .schema**
- **date and time functions**
- **primary key constraint**
- **not null constraint**
- **unique constraint**
- **default constraint**
- **check constraint**
- **alter table**
- **delete, drop**
- **backup, restore**


### -Creacion de Base de Datos
> Una vez ya instalado el SGBD sqlite se procede a abrir el simbolo de sistema de Windows y crear la base de datos denominada ejercicio1.bd, ademas de abrirla y crear la tabla User, en la que se aplican lo temas vistos en la clase
![Creacion de Base de Datos](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.001.png)


> Continuando con el paso interior una vez se halla creado la tabla se realiza la incersion de datos
![Creacion de Base de Datos](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.002.png)

### -Update
> La sentencia Update como su nombre lo indica sirve para actualizar los datos de la tabla, a continuacion se mostrara la correcta sintaxis del comando Update

        UPDATE table
        SET column_1 = new_value_1,
            column_2 = new_value_2
        WHERE
            search_condition 
        ORDER column_or_expression
        LIMIT row_count OFFSET offset;


>Primero, especifique la tabla donde desea actualizar después de la cláusula UPDATE .
>En segundo, establezca un nuevo valor para cada columna de la tabla en la cláusula SET.
>En tercer lugar, especifique filas para actualizar usando una condición en la cláusula WHEREc. La  cláusula WHEREs opcional. Si lo omite, la declaración  UPDATE actualizará los datos en todas las filas de la tabla.
>Finalmente, use las cláusulas ORDER BY y en la declaración para especificar el número de filas para actualizar.LIMITUPDATE


- Como podemos ver se modificara la columna firstname de la primera tabla creada users
- Asi mismo se modificara la columna email

![Update](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.003.png)

![Update](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.004.png)

![Update](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.006.png)

![Update](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.007.png)


### estructura de la base de datos .schema
>El esquema de una base de datos (en inglés, database schema) describe la estructura de una base de datos, en un lenguaje formal soportado por un sistema de gestión de base de datos (DBMS). En una base de datos relacional, el esquema define sus tablas, sus campos en cada tabla y las relaciones entre cada campo y cada tabla.

El esquema es generalmente almacenado en un diccionario de datos. Aunque generalmente el esquema es definido en un lenguaje de base de datos, el término se usa a menudo para referirse a una representación gráfica de la estructura de base de datos.

### date and time functions
> Las funciones date sirven para solicitarle al sistema la fecha u hora, asi mismo dependiendo de la funcion empleada esta puede generar diversos formatos y modelos estaticos o dinamicos
> Actualmente existen 6 tipos de funciones que nos dependiendo nos pueden dar la fecha o la hora, estas son:


- date()
- time()
- datetime()
- julianday()
- unixepoch()
- strtime()


![date and time functions](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.005.png)



### primary key constraint y not null constraint
>  continuacion vamos a crear una nueva tabla denominada computadores y en ella utilizaremos los elementento primary key y not null.
- **Primary key**
Las llaves primarias son campos que nos ayudan a identificar y clasificar cada fila de una tabla, asi en este ejemplo hacemos que la columna idcomputer sea un entero y el identificador de cada registro que se realice
- **Not Null**
En este caso el comando not null es utilizado para indicar que ese campo **NO** puede estar vacio y debe tener algun tipo de dato acorde; en los ejemplos se puede ver que en caso de que queramos dejar vacio un campo siempre y cuando no tenga la instruccion not null escribiremos un null en el registro y automaticamente aparecera vacio
![primary key constraint y not null constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.008.png)

![primary key constraint y not null constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.009.png)

![primary key constraint y not null constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.010.png)

![primary key constraint y not null constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.011.png)

![primary key constraint y not null constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.012.png)

![primary key constraint y not null constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.013.png)



### Unique Constraint
> El comando Unique es utilizado para especificar que los registros que se coloquen en ese campo deben ser unicos y no se pueden repetir en otros registros, en caso de que se intente registrar un dato repetido como en la 3 imagen saldra un error
![Unique Constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.014.png)

![Unique Constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.015.png)


- Error al registrar un dato repetido en una columna unique
![Unique Constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.016.png)




### Default Constraint
>Esta instruccion nos ayuda para dejar un campo con un registro por defecto, en el ejemplo el precio del libro se deja por defecto en 100 

![Default Constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.024.png)

![Default Constraint](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.025.png)


### Alter table
> La instruccion alter table nos permite modificar y alterar informacion y datos de las tablas creadas, estos pueden ser nombres de columnas, nombres de tablas, datos de las filas, crear y eliminar filas y columnas, etc.
>En este ejemplo se renombra la tabla acudiente y se agrega la columna sexo
![Alter table](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.017.png)

![Alter table](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.018.png)


### Informacion de registros
> Hasta el momento se ha visto como ver los registros de la tabla mediante un select * from nombretabla, pero en el caso de querer ver la informacion detallada de las columnas de una tabla, se utiliza el comando **pragma table_info(nombretabla);** y apareceran las columnas tal y como se muestran en la imagen
![pragma table_info(nombretabla)](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.019.png)

### drop, delete 
> Este comando se puede utilizar tanto para eliminar tablas y columnas como para eliminar bases de datos completas, a continuacion se crearan tablas y se enseñara su posterior eliminacion mediante el comando drop


![drop, delete ](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.020.png)


### Check Constraint
>Sirve para tener un patron que de cumplirse permite la admision de datos en un registro, si no se cumple no admite el registro
![](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.021.png)

![ ](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.022.png)

![](Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.023.png)




