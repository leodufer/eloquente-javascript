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

**5.** Sua contribuição será analisada pela comunidade. Em alguns casos pediremos algumas alterações antes de dar merge.

Após o merge:

- Delete a branch utilizada:

```
git checkout master
git push origin :traducaoCapX
git branch -D traducaoCapX
```

- Atualize seu repositório com o repositório oficial:

```
git fetch upstream
git rebase upstream/master
git push -f origin master
```

**6.** Quando iniciar uma nova contribuição, inicie repita o processo pelo passo 2.

### Boas práticas

- **Não traduza termos técnicos e blocos de código**
- Antes de enviar sua contribuição, certifique-se de que está enviando apenas um **único** commit que represente o que foi feito. Caso tenha feito vários commits, [esmague-os](http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html) antes de fazer o _Pull Request_.
- Caso tenha qualquer tipo de dúvida, abre uma _Issue_ que faremos o possível para te ajudar.
- Não adicione comentários nas issues de “log”. Elas tem apenas a finalidade de armazenar referências ao trabalho de cada capítulo.
- Contribua com as discussões.
- Delimitação para títulos de obras: Utilizar o travessão (—) para o início da frase, nome do autor e logo após o nome da obra, sem alterar nenhum valor. Exemplo:

> — Master Yuan-Ma, The Book of Programming

- Estrangeirismo: Utilizar o formato itálico. Exemplo: _bug_
- Sentido Figurado: Sempre destacar com aspas duplas.
- Citação: Aspas duplas com o sinal de >. Exemplo:

> “Foo bar”

- Marcação para código: Utilizar um apóstrofe (\`) para indicar um pedaço de código no meio de um texto (`var foo = undefined`). Ou três apóstrofe com o nome da linguagem de programação na frente (\`\`\`js), para indicar um bloco de código:

```js
var foo;
foo = undefined;
```

### Dúvidas em tradução de termos, palavras, expressões etc…

Quando estiver em uma situação em que você não sabe exatamente como traduzir uma palavra, termo ou expressão, nós recomendamos que siga os seguintes passos:

**1.** Abra uma _Issue_ com um título descritivo como por exemplo: “_Como traduzir a palavra/termo “x”?_” e coloque uma descrição fazendo referência à linha e o capítulo que esteja trabalhando.

**2.** Adicione uma tag `[TODO: ref #<número-da-issue-da-discussão>]<palavra/termo não traduzido>[/TODO]` e continue trabalhando no arquivo enquanto não há uma conclusão na _Issue_. Esse processo é importante para facilitar o acesso a itens pendentes e ter uma referência clara onde está ocorrendo a discussão.

**3.** Após a conclusão da discussão na _Issue_, feche a mesma. Em seguida, remova a tag adicionada no passo 2 e atualize a palavra/termo não traduzido.

**4.** Como mantemos um arquivo de [glossário](https://github.com/braziljs/eloquente-javascript/blob/master/glossario.md), faça um _Pull Request_ adicionando o novo termo, colocando a referência `#<número-da-issue>` no termo/palavra em questão para fácil acesso no futuro.

***

Obrigado! :heart: :heart: :heart:

