# Code review
<!-- .slide: class="page-title" -->



### Code review

<div class="row ">
    <div class="col-lg-5">
<img src="ressources/wtf.png" alt="">
    </div>
    <div class="col-lg-7">
<ul><li>Examen du code produit par un regard extérieur </li>
<li>Préférer une revue de code *synchrone*<!-- .element: class="highlight highlight-cyan" --> à de longs commentaires écrits</li>
<li>Le processus de review ne doit pas être inutilement complexe</li>
<li>Un code écrit en pair ou mob programming est un code déjà revu</li></ul>

<div class="picto picto-warning mtl">
  <div class="picto-content picto-content-xs">
    La revue de code n'est utile que si les *défauts* <!-- .element: class="highlight highlight-pink" --> constatés sont *corrigés* <!-- .element: class="highlight highlight-pink" -->
  </div>
</div>
    </div>
</div>



# Types de code review
<!-- .slide: class="page-title" -->



## Asynchronous code review

> After the coder is finished with coding, she makes the code available for review and starts her next task

<div class="row mtl">
    <div class="col-lg-6">
      <div class="picto picto-great">
        <div class="picto-content picto-content-xl">
          <h4>Pas de dépendance directe</h4>
          <p>Développeur et reviewer travaillent sur des tâches indépendantes, les revues et corrections sont faites en fonction de l'emploi du temps de chacun</p>
        </div>
      </div>
    </div>
    <div class="col-lg-6">
      <div class="picto picto-ko">
        <div class="picto-content picto-content-xl">
          <h4>L'inconvénient des tâches segmentées</h4>
          <ul><li>Les délais d'attente avant validation / correction peuvent se retrouver allongés.</li>
          <li>Les échanges désynchronisés peuvent laisser la place à des incompréhensions</li></ul>
        </div>
      </div>
    </div>
</div>



## Synchronous code review

> The reviewer joins the coder at her desk and they look at the same screen while reviewing, discussing and improving the code together.

<div class="row mtm">
    <div class="col-lg-6">
      <div class="picto picto-target">
        <div class="picto-content">
          <h4>Mutualiser les connaissances</h4>
          <p>Le reviewer obtient le même niveau de connaissances que le coder au fur et à mesure que la discussion avance</p>
        </div>
      </div>
      <div class="picto picto-great">
        <div class="picto-content picto-content-xl">
          <h4>Montée en compétence technique</h4>
          <p>Les améliorations sont effectuées en commun entre reviewer et coder</p>
        </div>
      </div>
    </div>
    <div class="col-lg-6">
      <div class="picto picto-warning">
        <div class="picto-content picto-content-xl">
          <h4>Changements de contexte forcés</h4>
          <p>Le travail du reviewer peut être impacté, car celui-ci doit se rendre disponible au bon moment</p>
        </div>
      </div>
    </div>
</div>



## Instant code review: pair programming

> While one developer is hitting the keyboard to produce the code the other developer is reviewing the code right on the spot,
> paying attention to potential issues and giving ideas for code improvement on the go.

<div class="row mtm">
    <div class="col-lg-6">
      <div class="picto picto-target">
        <div class="picto-content picto-content-xl">
          <h4>Tacler les problèmes complexes</h4>
          <ul><li>Une assistance en directe pour les problèmes techniques.</li>
          <li>Meilleure reflexion sur les problèmes métiers : scénarios possibles, cas limites ...</li></ul>
        </div>
      </div>
    </div>
    <div class="col-lg-6">
      <div class="picto picto-warning">
        <div class="picto-content picto-content-xl">
          <h4>Fonctionnement unidirectionnel</h4>
          <p>Mettre en place des rotations régulières, </p>
        </div>
      </div>
    </div>
</div>



## Code review once in a while: Mob programming



## Faciliter la code review

- automatiser ce qui peut l'être : editorconfig / linter / analyse statique ...
  - pylint
- ? commencer par les tests ?



## code sale / code propre ?



## Les code smells



## Importance d'un référentiel commun

- CDD


