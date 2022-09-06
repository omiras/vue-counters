# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)

## Que hacemos ?

- Vamos a crear una aplicación que dispone de varios contadores. Cada contador tiene un número determinado. Cada vez que hacemos click en el contador, decrece el número. Cuando llega a 0, el contador ha acabado.
- Vamos a tener varios contadores gobernados por un "padre", que se va a dar cuenta cuando es que todos sus hijos han acabado el trabajo (han llegado a 0)
- Me gustaría saber de todos mis hijos, el número de ellos que han acabado de 'descontar'-