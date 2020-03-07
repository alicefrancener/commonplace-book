# Como combinar diferentes repositórios no git

Considerando que há dois repositórios que você deseja unir (*merge*), `sub-projeto` e `projeto`:

Entre no repositório no qual você quer combinar com o outro (ex.: dentro de `projeto` irei combinar o repo `sub-projeto`).

``` bash
git remote add -f sub-projeto git@github.com:username/sub-projeto.git
```

Combine os repositórios.

``` bash
git merge sub-projeto/master --allow-unrelated-histories
```

Nesse ponto, os repositórios foram combinados.

:bulb: Uma dica para evitar conflitos entre arquivos é verificar antes os dois repositórios que serão combinados. Geralmente arquivos que estão na raiz como `.gitignore`, `LICENSE` and `README` geram conflitos, pois existem nos dois repositórios; eles podem ser renomeados ou movidos para outra pasta antes do `merge`.

---

<small>Fonte: [How to merge two or multiple git repositories into one](https://medium.com/altcampus/how-to-merge-two-or-multiple-git-repositories-into-one-9f8a5209913f)<small>
