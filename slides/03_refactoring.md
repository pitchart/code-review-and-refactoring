# Refactoring
<!-- .slide: class="page-title" -->



## Refactoring

#### Refactoring <!-- .element: class="mtl" -->
Modification du code écrit sans en changer le comportement

Relancer les tests régulièrement : ils doivent tous passer.

Cela permet de s'assurer que le refactoring n'entraine pas de regression <!-- .element: class="arrow arrow-cyan" -->



### Pourquoi refactorer ?

- Améliorer la lisibilité, l'expressivité, la maintenabilité du code
- Généraliser les comportements applicatifs
- S'assurer que le code peut évoluer sereinement
- Faciliter la mise en place des tests
- Réduire la dette technique

<div class="picto picto-target mtl">
  <div class="picto-content picto-content-xl">
    <h4>Checklist pour un bon refactoring</h4>
    <ul><li>Le code est plus propre</li>
    <li>Aucune nouvelle fonctionnalité n'a été créée</li>
    <li>Tous les tests existants sont verts, *à l'exception des tests trop bas niveaux qui peuvent être supprimés*</li>
    <li>Les points non couverts ont été décrits et mis en visibilité de l'équipe</li></ul>
  </div>
</div>



## How to ?

#### S'assurer que le code est couvert par des tests

- éviter les regressions
- éviter d'introduire de nouvelles fonctionnalités

#### Du plus simple au plus complexe <!-- .element: class="mtm" -->

- gagner en lisibilité (code standards)
- isoler les détails d'implémentation (introduce variable, extract method ...)
- s'appuyer sur les fonctionnalités de l'IDE
- utiliser des étapes intermédiaires et du code temporaire
- commiter fréquemment



## Code smells & refactoring

![](ressources/code-smells-refactoring.png) <!-- .element: style="max-height: 60vh" -->

*[Refactoring techniques @ Refactoring Guru](https://refactoring.guru/refactoring/techniques)*

<!-- .element: style="text-align:center" -->


## Refactoring legacy code 

#### Identifier les points de couture
> A Seam is a place to alter program behavior, without changing the code.

<div class="row mtm">
    <div class="col-lg-6">
        <h4>Wrap Technique</h4>
<ol>
<li>Renommer la méthode à refactorer.</li>
<li>Créer une nouvelle méthode avec le même nom et la même signature que l'ancienne</li>
<li>Appeler l'ancienne méthode depuis la nouvelle méthode</li>
<li>Ajouter la logique refactorée avant ou après cet appel et retirer l'équivalent dans l'ancienne méthode</li></ol>
    </div>
    <div class="col-lg-6">
        <h4>SPROUT TECHNIQUE</h4>
        <ol><li>Créer le nouveau code quelque part</li>
        <li>Tester le nouveau code</li>
        <li>Identifier le(s) point(s) d'insertion du nouveau code dans le code existant</li>
        <li>Utiliser le nouveau code dans le code existant</li></ol>
    </div>
</div>


## En cas d'absence de tests

<div class="row">
    <div class="col-lg-6">
        <img src="ressources/approval-testing.png" alt="">
    </div>
    <div class="col-lg-6">
        <h4>Golden master</h4>
        <p>Permet de sécuriser la refonte d’une application en appliquant une couche de test sur l’application initiale avant toute modification.</p>
        <div class="picto picto-great mtl">
          <div class="picto-content picto-content-xl">
            <h4>Enrichir le patrimoine de tests</h4>
            <p>Le nouveau code apporté doit être testé indépendamment pour permettre de retirer les tests Golden Master progressivement</p>
          </div>
        </div>
    </div>
</div>



<img src="ressources/questions.svg" class="question" />
# Avez-vous des questions ?
<!-- .slide: class="page-questions" -->
