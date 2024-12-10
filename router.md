# Router

## Context

- SPA (Single Page Aplication): aplicació qe carrega una única pàgina HTML i actualitza el contingut de forma dinàmica mitjançant JavaScript.

## Explicació router

- Un router és un component que gestiona la navegació entre les diferents parts de l'aplicació.
- El router és responsable de determinar quina ruta s'ha de seguir per mostrar el contingut corresponent.
- El router pot ser implementat de diverses maneres, com per exemple, utilitzant la biblioteca `vue-router` per a aplicacions Vue.js o bé implementant un router personalitzat utilitzant JavaScript i HTML.
- El router pot ser configurat per mostrar contingut dinàmicament en funció de la ruta actual, permetent a l'usuari navegar entre les diferents parts de l' aplicació.

```JavaScript
//main.js
import './assets/main.css'

import  { createApp } from 'vue'
import App from './App.vue'
import router from './router'

const app= createApp(App)
app.use(router)
app.mount('#app')

```

```JavaScript
//index.js
import { createRouter, createWebHistory } from 'vue-router'
import Home from '../views/Home.vue'

const router = createRouter({
    history: createWebHistory(process.env.BASE_URL),
    routes: [
        {
            path: '/',
            name: 'home
            component: Home
        }
    ]
})
export default router

```

- **RouterLink:**  Crea enllaços que es connecten amb el router. Permet a Vue canviar l'URL de la pàgina sense actualitzar la pàgina.

- **Router View:**  és un component que mostra el contingut corresponent a la ruta actual.

- **Router-Rutes :**  són les rutes que defineixen les diferents parts de l'aplicació. Cada ruta té un nom, un camí i un component associat.

- **Router-Lazy routes:** permet carregar els components només quan són necessaris, millorant la càrrega de la pàgina.

## Diferencias useRoute() y useRouter()

- **useRouter()**:  és una funció que retorna l'objecte router. Permet accedir a les propietats i mètodes del router des de qualsevol component de la nostra aplicació.

- **useRoute()**:  és una funció que retorna l'objecte de la ruta actual. Permet accedir a les propietats de la ruta actual des de qualsevol component de la nostra aplicació.
