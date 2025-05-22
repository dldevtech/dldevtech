# Guía de Refactorización y Buenas Prácticas

## 📚 Introducción

Este archivo pretende ser una referencia para las primeras tareas en un proyecto real. En el abordaremos las distintas recomendaciones que se deben aplicar a la hora de realizar una tarea compleja. Por lo general, nos encontramos con un problema, lo mejor que podemos hacer como desarrolladores de software sería dividir esos problemas en partes muy pequeñas, una vez establecidas todas las variantes, casuísticas, necesidades, estamos preparados para generar nuestro puzzle desde el problema inicial.

Para nosotros el orden, la organización y la asimilación de los conceptos es muy importante ya que es la esencia de tu trabajo de cara a mundo laboral. A través de la refactorización, esa herramienta que nos sirve para modularizar problemas y separarlo en módulos o responsabilidades más pequeñas, conseguimos establecer un patrón fácil de reconocer para futuros lectores de nuestro código.

---
## 👩‍💻​ Analogía Refactorización

Imaginemos que cada uno de nuestros trabajadores esta en uno de los puestos, a pesar de que podría parecer que funcionaria, si nuestro encargado de despiezar tiene que hacer una tortilla, tiene que ir a por los huevos, partirlos, batirlos y ya con eso pasárselo al encargado de los fuegos. El problema es que además de eso nos han pedido una lubina, unas patatas fritas y una ensaladilla rusa.

---
## 🛠️ Paso a paso para modularizar un componente complejo

A diferencia del mundo real, en el mundo digital nosotros podemos "Crear" sin límite a estos trabajadores. 
### 1.- Analizar, detectar responsabilidades y dividir

Podemos dividir aun mucho mas las tareas si contamos con trabajadores ilimitados:

- Despiezar ( )
- Cocinar ( )
- Sazonar ( )
- BuscarAlimentos ( )
- ReponerComida ( )
- TemperaturaFuego ( )
- ControlDeCocción ( )
- RecuperarComidaPreparada ( )
- Emplatar ( )
- ComandasPendientes ( )
- ComandasCompletadas ( )

Desde luego necesitamos más personas, pero los ordenadores trabajan de una forma mucho más rápida de lo que un proceso físico requiere. Aquí las responsabilidades están divididas mucho más de tal manera que el flujo no se detenga porque el que despieza los alimentos tenga que ir a reponerlos.

En esto consiste la refactorización, en ir modularizando todas funciones y responsabilidades de nuestro código para que cuando alguien que no ha elaborado el código pueda ver el flujo de una forma transparente y visual.

### 2.- Crear Carpetas según las funcionalidades

Pero incluso en nuestro ejemplo, si tuviéramos cada una de las funciones en un archivo único podríamos perecer al leer todo el código. Por eso debemos organizar todo ello en secciones que sean intuitivas a simple vista:

- Cocineros
	- Despiezar ( )
	- Sazonar ( )
	- Cocinar ( )
	- TemperaturaFuego ( )
	- ControlDeCocción ( )
	
- Vajilla
	- RecuperarComidaPreparada ( )
	- Emplatar ( )
	- LimpiarPlatos ( )
	- ReponerPlatos ( )
	
- CoordinadorCocina
	- ComandasPendientes ( )
	- ComandasCoompletadas ( )


### 3.- Testear cambios de forma progresiva

Cuando hagamos estos cambios no podemos hacerlo de forma brusca, primero podemos separar a los Cocineros y comprobar que todo sigue funcionando.

Con esta estructura somos capaces de ver de un vistazo que cada ente digital tiene una tarea y un área asignada. Podemos imaginar el flujo como Coordinadores --> Cocineros --> Vajilla --> Coordinadores para finalmente completar y mandar nuevamente.

A pesar de todo esto es una forma de hacerlo pero podríamos dividir aun más las secciones y decir que los que reponen los platos y los que reponen los alimentos tiene una formación parecida, modularizando aun más y diciendo que hay un área de reposición en los que unos reponen platos y otros alimentos.

---
## 🧼 Buenas prácticas generales

### Nombres claros

Cuando realizamos estas modularizaciones tenemos que tener en cuenta tanto el flujo como el propósito de nuestras funciones, de cara a comprender nuestro código o el de otros. Si le ponemos a uno de nuestros cocineros Despiezar, esperamos que se encargue de todos los cortes de los alimentos, pero no seria muy intuitivo llamar a este "ente digital" ElaboracionDeLosDistintosCortesEnLosAlimentos ( ), puede que sea muy descriptivo pero no sintetiza.

### Componentes pequeños, reutilizables y no duplicados 

Este punto depende mucho de las funciones que tengamos dentro del proyecto o de como este estructurado el mismo. No obstante, podemos ver de forma intuitiva que a lo mejor la función de reponerAlimentos y ReponerPlatos tienen ciertas similitudes. De ello se podría tener a un único reponedor que pueda estar pendiente de si le llaman los Cocineros o los de Vajilla.

---

## 💾​ Conclusión

Hemos visto un ejemplo con pseudocódigo, no tiene nada de lógica y debemos de tener en cuenta que las distintas herramientas con las que trabajamos a veces nos obligan a tomar ciertas estructuras. A pesar de todo lo más importante en nuestro trabajo es mantener una actitud crítica y analítica. No dejar de cuestionarnos sobre el código:

- ¿Podemos dividir esta tarea en subtareas pequeñas?

- ¿Las subtareas podrían reducirse a un núcleo aún más pequeño?

- ¿Hemos nombrado bien a nuestros "entes digitales"?

Es un trabajo complicado al principio, pero siguiendo patrones, ejemplos en nuestro propio código y distintas guías disponibles en Internet podemos afilar nuestra mente hasta que sea una experta "Despiezadora" como el cocinero de nuestro ejemplo.

