# Stylecourse
### Un ejemplo de Repositorio basado en el seguimiento de un curso

Bienvenido al Curso de cómo usar Git para hacer el seguimiento de un curso a través de un repositorio local y remoto.

Primero debemos de tener linkeado nuestro repositorio local desde dónde haremos todos los cambios con un repositorio remoto en **GitHub**.

Luego de crear ambos repositorios y linkearlos, podremos seguir con el curso.

En el repositorio local o remoto, deberemos crear un **README.md**, en el cual estaremos escribiendo toda la historia, ediciones y cambios tanto del curso como del repositorio.

La estructura del **README.md** debe de ser la siguiente:

```markdown
# Curso HTML5 y CSS3
### Un pequeño curso sobre como usar HTML5 y CSS3

Qué se aprenderá? Aprenderemos sobre HTML5 y CSS3, herramientas fundamentales para el desarrollo de páginas web y aplicaciones desktop.

## Inicio del Curso, Parte 1: HTML5
HTML5 es un lenguaje de marcado de texto que permite darle una estructura a las páginas web. Se trata del primer paso para realizar un sitio en internet.

El componente principal de HTML5 son sus etiquetas, que inician con un "< >" y terminan con "</>".
Ejemplo: (Agregar en bloque de codigo)

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
</html>

Esto es solo un ejemplo de como funciona HTML5 con etiquetas.
Por ahora, solo crea un nuevo archivo **index.html** en tu editor de texto favorito y copia el codigo anterior.

### Fin de la Parte 1: HTML5 del Curso de HTML5 y CSS3

## Commit Nro 1 Version Nro 0.1
### Cambios realizados (- es una unordered list)
- Archivos Nuevos:
1. index.html
- Archivos editados:
1. index.html

### Explicacion (Colocar en bloque de codigo en caso de referencias)
<!DOCTYPE html> Etiqueta super importante 
<html> y </html> Dentro de estas 2 etiquetas colocaremos todo nuestro sitio web
<head> y </head> Aqui colocamos metadatos de la pagina web como el charset o el titulo de la web
<body> y </body> Dentro del body estara todo nuestro contenido visible en la pagina web

### Fin del Commit Nro 1
(Insertar linea horizontal)

## Commit Nro 2 Version Nro 0.2

### Cambios realizados

### Explicacion
```

**Nota:** Podemos colocar tambien imagenes si requerimos de estas para un mejor entendimiento de la clase y/o de los cambios realizados en el repositorio.

## Flujo de Trabajo luego del Commit Inicial

1. Creacion de una nueva **branch** y desplazarnos a esta con: 

	```bash
	git checkout -b [branch-name]
	```

	Donde **[branch-name]** seria el nombre de la clase actual que estamos viendo.

2. **Edición** y **Adición** de los archivos siguiendo el curso.

3. Editar el archivo **README.md**  con la estructura que se presentó anteriormente.

4. Agregar al **staging** los archivos editados/creados con: 

	```bash
	git add -A
	```

5. Hacer **commit** de los archivos en **staging** con: 

	```
	git commit
	```

	**Nota:** El Mensaje del Commit debe contener lo siguiente:

	- Numero de Commit
	- Version del Proyecto
	- Cambios principales

6. **Taggear** el commit anterior con la versión respectiva referenciada tanto en el **README.md** como en el git commit.

7. Crear un **tag** con la version del repositorio mas actual y vincularlo al ultimo commit realizado con: 

	```bash
	git tag [num-version] [SHA1]
	```

	Donde **[num-verion]** es el Numero de la Version actual y **[SHA1]** es el SHA1 del ultimo Commit que se genero. 

8. Desde el Repositorio Local nos cambiamos al **branch** principal, **master** con: 

	```bash
	git checkout master
	```

9. En el **branch** master hacemos un merge del **branch** en el que estuvimos trabajando con: 

	```bash
	git merge [local-branch-name]
	```

	Donde **[local-branch-name]** es el nombre del **branch** en donde hicimos todos los cambios.

10. Hacer push del repositorio local con: 

	```bash
	git push [remote-repo-name] [local-repo-branch]
	```

	Donde **[remote-repo-name]** es el nombre del Repositorio remoto (se le coloca casi siempre **origin**), y **[local-repo-branch]** es el nombre del branch al cual queremos hacerle **push** hacia nuestro repositorio remoto, que seria la **branch** master.

11. Hacer push de los tags del repositorio local con: 

	```bash
	git push [remote-repo-name] [local-repo-branch] --tags
	```

12. Cambios al **branch** principal **master** del repositorio local con: 

	```bash
	git checkout master
	```

13. **Ir** al Paso 1.

------

De esta manera podremos tener un control tanto de los cambios en el repositorio como del seguimiento del curso.