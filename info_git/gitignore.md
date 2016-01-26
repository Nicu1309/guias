# .gitignore

.gitignore es un archivo especial para git (De la misma forma que
Makefile lo es para make), que indica a git un conjunto de archivos
que no tiene que seguir (track en la literatura inglesa).

Esto nos permite definir, por ejemplo, que git ignore archivos
intermedios de compilación, copias de seguridad personales, archivos
de notas que guardamos en nuestro repositorio local pero no queremos
que estén disponibles para nuestros colaboradores, archivos con claves
sensibles, etc...

Un ejemplo de archivo .gitignore típico para un proyecto en C sencillo
sería:

```
# Ignorar archivos de compilacion intermedios
**/*.[ao]
# Ignorar copias de seguridad locales
**/*~
```

Tal y como esta descrito en el propio archivo (líneas en blanco se
ignoran, y líneas que empiecen en # son comentarios), este archivo
hará que git ignore cualquier fichero que acabe en .o, .a o ~, lo
cual evitará que nuestro repositorio en red se llene de ficheros
objeto o librerías compiladas.

Los patrones que admite .gitignore son los llamados patrones glob
(glob patterns en la literatura inglesa), que en nuestro caso sería
suficiente con entender que son los patrones de expansión que entiende
la consola. La excepción son los patrones de la forma

```
**/*~
```

Que indican que se ignore cualquier fichero terminado en ~ en el
directorio actual y en cualquiera de los subdirectorios.

GitHub ofrece ejemplos de archivos para diferentes lenguajes de
programacion en el repositorio https://github.com/github/gitignore

En caso de que se tenga más curiosidad, se puede obtener más
información en el libro adjunto proGit, paginas 50 y 51
