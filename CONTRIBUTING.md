# Contribuciones

### Por dónde comenzar?

**1.** Hacer el _fork_ del proyecto.

**2.** [Entender nuestro flujo](#fluxo).

**3.** [Lea y pratique las buenas prácticas](#boas-pr%C3%A1ticas).

### Flujo

Es muy facil contribuir para el proyecto. Cualquier tipo de ayudad (sea grande o pequeña) es bienvenida. Si encuentras cualquier parte del libro que pueda ser mejorada, esa es una gran oportunidad para participar
([aqui](https://github.com/braziljs/eloquente-javascript/issues?q=is%3Aopen+is%3Aissue+label%3Amelhorias) es un excelente lugar para encontrar cosas que puedan ser mejoradas. Caso no sepas por donde comenzar:

**1.** Luego del _fork_ hacer una referencia al repositorio oficial del proyecto

```
git remote add upstream git@github.com:leodufer/eloquente-javascript.git
```

**2.** Antes de iniciar el proceso de colaboración, cree una nueva rama para hacer tus modificaciones

Algunos ejemplos:

- Para traducciones: `git checkout -b traduccionCapX`
- Para revision: `git checkout -b revisionCapX`
- Para errores: `git checkout -b correcionCapX`

> Use cualquier nombre que sea coherente con la colaboración que está siendo hecha.
> `X` representa el numero de capítulo.

**3.** Luego de realizar las alteraciones, e hora de hacer un commit com un mensaje coherente con lo que fue hecho. Ejemplo:

```
git add --all
git commit -am ‘Añadir traduccion/revision/mejoria capítulo X linea/lineas Y’
git push origin traduccionCapX
```

**4.** Envie um _Pull Request_ com las alteraciones hechas, haciendo referencia para el `master` del repositorio oficial.

**5.** Su contrubución será analizada por la comunidad. Em algunos casos pediremos algunas alteraciones antes de dar merge.

Después del merge:

- Delete el branch utilizado:

```
git checkout master
git push origin :traducionCapX
git branch -D traducionCapX
```

- Actualice su repositorio com el repositorio oficial:

```
git fetch upstream
git rebase upstream/master
git push -f origin master
```

**6.** Cuando inicies una nueva contribución, repita el processo inciando por el paso 2.

### Buenas prácticas

- **No traduzcas terminos técnicos e bloques de código**
- Antes de enviar su contribción, certifique-se de que está enviando apenas un **único** commit que represente lo que fue hecho. Caso tengas varios commits, [aplastelos](http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html) antes de hacer el _Pull Request_.
- Caso tengas cualquier tipo de duda, habra una _Issue_ que haremos lo possible para ajudarte.
- No adicione comentarios en las issues de "log" “log”. Ellas tiemen la finalidad de almacenar referencias al trabajo de cada capítulo.
- Colabore con las discusiones.
- Delimitación para títulos de obras: Utilizar el travesaño (—) para el inicio de la frase, nombre del autor y luego después el nombre de la obra, sin alterar ningun valor. Ejemplo:

> — Master Yuan-Ma, The Book of Programming

- Estrangerismo: Utilizar el formato itálico. Ejemplo: _bug_
- Sentido Figurado: Siempre destacar com comillas dobles.
- Citación: Comillas dobles con el signo de >. Ejemplo:

> “Foo bar”

- Marcación para código: Utilizar um apóstrofe (\`) para indicar un pedazo de código en medio de um texto (`var foo = undefined`). O tres apóstrofes con el nomnbre del lenguaje de programación en frente (\`\`\`js), para indicar um bloco de código:

```js
var foo;
foo = undefined;
```

### Dudas en traducciones de términos, palabras, expresiones etc…

Cuando estes en una situación en que no sabes exatamente como traducir una palabra, término ou expresión, recomendamos que sigas los seguintes passos:

**1.** Habra una _Issue_ con un título descriptivo como por ejemplo: “_Como traducir la palavra/término “x”?_” y coloque una descripción haciendo referencia a la linea e y el capítulo que estes trabayando.

**2.** Adicione una tag `[TODO: ref #<número-de-issue-dae-discusión>]<palabra/término no traducido>[/TODO]` y continue trabayando en el archivo mientras no haya uaa conclusión en la _Issue_. Esse processo é importante para facilitar o acesso a itens pendentes e ter uma referência clara onde está ocorrendo a discussão.

**3.** Após a conclusão da discussão na _Issue_, feche a mesma. Em seguida, remova a tag adicionada no passo 2 e atualize a palavra/termo não traduzido.

**4.** Como mantemos um arquivo de [glossário](https://github.com/braziljs/eloquente-javascript/blob/master/glossario.md), faça um _Pull Request_ adicionando o novo termo, colocando a referência `#<número-da-issue>` no termo/palavra em questão para fácil acesso no futuro.

***

Obrigado! :heart: :heart: :heart:

