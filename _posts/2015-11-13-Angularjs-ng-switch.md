---
layout: post
title:  "Ejemplo de ng-switch en Angularjs"
date:   2015-11-13 15:00:00
categories: Post
author: Jonathan Lara Bustos
tags: Angularjs JavaScript ng-switch
comments: true
---

#Presentación
Buenas tardes, mi nombre es Jonathan Lara y estaré publicando todos los jueves en el blog de MoSyt. Actualmente me encuentro estudiando Ingeniería en Tecnologías de la información y trabajando en esta empresa que es Mobile System Technologies, estoy realizando las funciones de diseño visual de las aplicaciones, programación en frond end y apoyando en el área de diseño. Le estaré compartiendo ejemplos,  cosas relacionadas con el fron end o algún dato interesante.

###Comencemos

#####Nuestro controlador llevaría lo siguiente:
```javascript
  $scope.opciones = ['1', '2', '3'];
  $scope.selection = $scope.opciones[0];
```
- La primera línea son las opciones que contendrá nuestro select.
- la segunda line es en la posición que iniciara nuestro select.

#####Contenido de la vista:

```html
  <select class="form-control inputSize" ng-model="selection" ng-options="item for item in opciones">
  </select>
  <hr/>
  <div class="animate-switch-container" ng-switch on="selection">
      <div class="animate-switch" ng-switch-when="1"> 
      Opcion 1 seleccionada
      </div>
      <div class="animate-switch" ng-switch-when="2">
        Opcion 2 seleccionada
      </div>
      <div class="animate-switch" ng-switch-default>
        Opcion 3 seleccionada
      </div>
  </div>
```

- La directiva ng-options se encarga de mostrar todas las opciones que es en opciones y guardarlas en item.
- La directiva ng-model mustrar el primer valor. Este valor se especificó en el controlador.
- La directiva ng-switch on detecta el cambio que ocurre en el select.
- La directiva ng-switch-when decida el contenido que se cargara dependiendo del valor que tenga.


Dependiendo de valor seleccionada es lo que se cargara en el div que tiene la class animate-switch-container

Ejemplo: [Aqui!](http://plnkr.co/edit/trgVzA2mYx05TGT2cEnn?p=preview)

Dejo mi correo por cualquier cosa: jonathanlara@mosyt.org

