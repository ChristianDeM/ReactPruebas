# Pruebas Con react.

## iniciando react
<p> codigo  para instalar react

``npx create-react-app  `` +Nombre de la carpeta  

# scripits

``npm star ``
<p> ejecuta  el servidor 

``npm run build ``
``npm test ``
``npm run eject ``



<p> Dentro de la carpeta public se encuentra index.html

### index.html

<p>dentro del index.html  donde iria todo el demo de la aplicacion seria en la seccion 

``<div id= root> ``

<p> para esta prueba elminamos todo lo que hay dentro de src para crear y profrofundisar lo que hay en src
<p> Puedes ver los cambios en los comits de este proyecto de purebas. 


## index.js

importando react y react-dom

No requiere instalacion por qque ya las tiene dentro de react.

React

sirve para  utlizar jsx un lenguaje parecido a HTML pero es javascript.

para esto creamos un ``document.getElementById("root")``  dentro de  ``ReactDom.render{};`` para realizar la prueba 

Codigo dentro de index.js
```
ReactDom.render(
    <div> Hola mundo</div>,
    document.getElementById("root")
);
```

Teniendo en cuenta que en el index.html  se encuentra ``<div id=root>`` nos mostrara ahora en pantalla Hola mundo 


## APP.jsx

creamos un archivo app.jsx podemo crear app.js pero con la extencios jsx damos a entender que es un componente especial para React.

Ahora dentro de ``app.jsx`` importaremos a react nuevamente y luego gcrearemos una funcion  llamada app  donde retornara un mensaje  el cual pueda ser ledio en  el index.js

```
import react  from 'react';

export function app(){
    return(<div>Este div esta dendtro de app.jsx</div>)
};
```

ahora en nuestro ``index.jsx``  importaremos a nuestra app de aap.jsx

`` import { App } from './App' ``
Quitamos el div anterior dejandolo de la siguiente manera

```
ReactDom.render(
    <App/>,
    document.getElementById("root")
);

```

Ahora ya sabemos como son los componentes lo ideal seria crear una carpeta ``components`` donde se encuentren los componentes


## TodoList y TodoItem

Creamos  estos 2 archhivos dentro de components  para ver como es que  se van cambiando propiedades uno con el otros al igual que eventos. 

DATO EXTRA  instalando extencion ES7 + react Esto nos sirve para  los snippets en react  
con el texto ``rfs`` nos dara la estructura de  react.

Ahora dentro de Todo list tenemos este codigo.

```
import React from 'react'

export  function TodoList({ todos }) {
  return (
    <ul>
        {todos.map((todo)=>(
            <li> tarea</li>
        ))}
    </ul>
  );
}
```

Con rfc  tendremos el template  con export default pero lo ideal seria quitar default para acostumbranos a exportar  con el mismo nombre 

Creamos un  .map con todos esto nos regresara una nueva lista  en este caso para hacer una lista de tareas

denotro de App.js  importamos el componente 
``import { TodoList } from './components/TodoList';``

Ahora modificamos nuestra funcion  para mostrar  la lista

```
export function App(){
    return<TodoList todos={[
       {id:1,Tarea:'tarea'}
    ]}/>
};

```
Esta funcion creare un return de todos donde la entra se  id  y tarea


 


