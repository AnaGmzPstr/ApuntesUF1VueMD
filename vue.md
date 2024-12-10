# Vue

Instal·lar quasar

Iniciar un projecte

```bash
npm create @vue@latest
cd nomCarpeta
npm install
npm run dev
```

afegir en el git ignore la carpeta node_modules

## Organización carpetas de vue

- `src`: Conté tot el codi font de l'aplicació.
- `src/main.js`: S'encarrega de crear l'aplicació.
- `src/App.vue`: S'encarrega de crear la interfície gràfica
- `src/components`: Conté tots els components de l'aplicació.

## Variables

**Variable reactiva**:  Una variable que es pot canviar a través de l'aplicació (renderitza la pantalla).  Per exemple, si tenim una variable que mostra el nom de l'usuari, quan l'usuari canvia el seu nom, la variable es canvia.

## Funció ref()

La funció `ref()` permet crear una variable reactiva.

```vue
<script setup>
import { ref } from 'vue'

// variable reactiva
const contador =  ref(0)

// modifiquem el valor
const incrementar = () =>{
    contador.value++
}

// resetear valor
const reset =() =>{
  contador.value =0
}

// decrementar valor
const decremenar =() =>{
  contador.value--
}

</script>

<template>
<div>
    <p>El comptador és: {{ contador }} </p>
    <button @click="incrementar">Incrementar</button>
    <button @click="decremenar">Decrementar</button>
    <button @click="reset">Resetear cuanta</button>
</div>
</template>

```

## Directivas

### v-bind

La directiva `v-bind` permet assignar un valor a un atribut HTML.

### v-if i v-else

La directiva `v-if` permet mostrar o ocultar un element HTML en funció de una condició. La directiva `v-else` permet mostrar un element HTML quan la condició de `v-if` no és veritat.

Podem utilitzar: `<p>{{ active ? 'Actiu' : 'Inactiu' }}</p>` per mostrar un text diferent

### v-show

La directiva `v-show` permet mostrar o ocultar un element HTML en funció d 'una condició, però a diferència de `v-if` no elimina l'element del DOM.

### v-on

La directiva `v-on` permet afegir un event listener a un element HTML. Per exemple, `v-on:click` permet afegir un event listener a l'event click.

## Reactivitat a Vue.js 3 computed()

La reactivitat a Vue.js 3 es basa en el concepte de `computed()`. Aquesta funció permet crear una propietat calculada que es reactualitza  quan els seus dependents canvien.
