# .gitignore

.gitignore es un archivo especial para git (De la misma forma que
Makefile lo es para make), que indica a git un conjunto de archivos
que no tiene que seguir (track en la literatura inglesa).

Esto nos permite definir, por ejemplo, que git ignore archivos
intermedios de compilaci�n, copias de seguridad personales, archivos
de notas que guardamos en nuestro repositorio local pero no queremos
que est�n disponibles para nuestros colaboradores, archivos con claves
sensibles, etc...

Un ejemplo de archivo .gitignore t�pico para un proyecto en C sencillo
ser�a:

```
# Ignorar archivos de compilaci�n intermedios
*.[ao]
# Ignorar copias de seguridad locales
*~
```

Tal y como esta descrito en el propio archivo (l�neas en blanco y
l�neas que empiecen en # son comentarios), este archivo har� que git
ignore cualquier fichero que acabe en .o, .a o ~, lo cual evitar� que
nuestro repositorio en red se llene de ficheros objeto o librer�as
compiladas.

Los patrones que admite .gitignore son los llamados patrones glob
(glob patterns en la literatura inglesa), que en nuestro caso ser�
suficiente con entender que son los patrones de expansi�n que entiende
la consola.

En caso de que se tenga m�s curiosidad, se puede obtener m�s
informaci�n en el libro adjunto proGit, paginas 50 y 51