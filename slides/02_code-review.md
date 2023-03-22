# Code review
<!-- .slide: class="page-title" -->



### Code review

<div class="row ">
    <div class="col-lg-5">
<img src="ressources/wtf.png" alt="">
    </div>
    <div class="col-lg-7">
<h4>Examen du code produit par un regard extérieur </h4>
<ul>
<li>Favorise la qualité du code (lisibilité, maintenabilité, généricité)</li>
<li>Réduit le nombre de bugs</li>
<li>Diffuse les connaissances dans l'équipe</li></ul>

<div class="picto picto-warning mtl">
  <div class="picto-content picto-content-xs">
    Le processus de review ne doit pas être inutilement complexe
  </div>
</div>
<div class="picto picto-ko mtl">
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



## Mob code review

#### Identifier des parties de code à refactorer
- Un développeur présente une portion de code qu'il a récemment rencontré
- Les autres développeurs proposent des axes d'amélioration en termes de structuration, de design, ou suggèrent des portions du code ayant des comportements similaires.

<br class="mtl">

#### Homogénéiser les standards de l'équipe <!-- .element: class="mtl" -->
- Les développeurs présentent tour à tour une portion de code qu'ils ont récemment écrit
- Les autres développeurs procèdent à la revue du code et s'accordent sur leur pratique de la code review



## Faciliter la code review

#### Avant : *automatiser* <!-- .element: class="highlight highlight-cyan" -->

- standards de code (editorconfig / linter)
- analyse statique (complexité, duplication)

<div class="row mvl">
    <div class="col-lg-8">
<h4 class="pts">Privilégier de petits apports de code</h4>
<p>Facilite la compréhension et la concentration du reviewer</p>
    </div>
    <div class="col-lg-4">
<img src="ressources/short-term-memory.png" alt="">
    </div>
</div> 

#### Commencer par la revue des tests

- lecture du code en condition de consommateur, permet de se concentrer sur les interfaces (méthodes publiques) ou le design.
- Tests = spécifications exécutables



## A votre tour

#### Qu'est-ce que du code sale ? <!-- .element: class="mtl" -->
#### Qu'est-ce que du code propre ? <!-- .element: class="mtl" -->
#### Comment passer de l'un à l'autre ? <!-- .element: class="mtl" -->



## Les code smells

Terme inventé par *Kent Beck* <!-- .element: class="highlight highlight-cyan" --> et popularisé par *Martin Fowler* <!-- .element: class="highlight highlight-cyan" -->

> If it stinks, change it
> <br> *– Kent Beck*

Une notion intuitive rendue plus précise et objective par la littérature existante  
[Code smells & refactorings @ Refactoring Guru](https://refactoring.guru/refactoring/smells)

<!-- .element: class="arrow arrow-pink mtm" -->

#### De même que les design patterns : <!-- .element: class="mtl" -->
- Fournissent un vocabulaire standard
- Donnent des critères d'applicabilité
- Proposent des solutions : refactoring
- Recensent des variations
- Certains sont évidents, d'autres moins



## Importance d'un référentiel commun

<div class="row mtl">
    <div class="col-lg-8">
      <img src="ressources/crappy-driven-development.png" alt="">
    </div>
    <div class="col-lg-4">
      <h4>Objectif</h4>
      <p>Rendre le code si sale que personne ne sera capable de le comprendre facilement</p>
      <h4 class="mtl">Résultat</h4>
      <ul><li>Une liste d'anti-patterns à traquer en code review</li>
      <li>Un standard d'équipe connu de tous</li></ul>
    </div>
</div>


