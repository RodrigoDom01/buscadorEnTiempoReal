### Buscador en tiempo real utilizando Javascript y Bootstrap 5.3.0

- Práctica utilizando  Javascript, creando un rápido buscador en tiempo real para tus datos. 


# Editor.md

![](https://pandao.github.io/editor.md/images/logos/editormd-logo-180x180.png)

### Links



`<link>` : < https://developer.mozilla.org/es/docs...>




#### Codigo Javascript　

```javascript
const productos = [
    {nombre: "Banana", valor: 500},
    {nombre: "Pera", valor: 500},
    {nombre: "Sandia", valor: 500},
    {nombre: "Melon", valor: 500},
    {nombre: "Frutillas", valor: 500},
    {nombre: "Anana", valor: 500},
    {nombre: "Mandarina", valor: 500},
    {nombre: "Manzanas", valor: 500},
    {nombre: "Guindas", valor: 500},
    {nombre: "Naranja", valor: 500},
]


const formulario = document.querySelector("#formulario");
const boton = document.querySelector("#boton");
const resultado = document.querySelector("#resultado");

const filtrar = ()=>{
    //console.log(formulario.value);
    resultado.innerHTML = "";

    const texto = formulario.value.toLowerCase();
    for (let producto of productos) {
        const nombre = producto.nombre.toLowerCase();
        if(nombre.indexOf(texto) !== -1){
            resultado.innerHTML += `
             <li>${producto.nombre} - Valor: ${producto.valor}</li>
            `
            
            
        }
        
    }

    if(resultado.innerHTML === ""){
        resultado.innerHTML += `
             <li>Producto no encontrado...</li>
            `
    }

}

boton.addEventListener("click", filtrar);
formulario.addEventListener("keyup", filtrar);

filtrar();
```

### End

