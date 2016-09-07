# EJERCICIO JSCODERS

Modificar el siguiente script para que muestre el resultado correcto.

var feature = 'closures'; 
(function () {     
	if ( typeof feature === 'undefined' ){         
		var feature = 'callbacks';         
		console.log('JS coders love its ' + feature );     
	} else {         
		console.log('JS developers love its ' + feature );     
	} 
})();

El código muestra el mensaje JS coders love its callbacks, mientras que el resultado debería ser JS developers love its closures.

##RESOLUCIÓN:

Tal como está la función y la mandamos a inspeccionar encontramos la siguiente imagen:

![FLUJOGRAMA](http://3.1m.yt/xrwAlKq.jpg "Flujograma")


Donde se puede observar:

1. El var declarado en la linea 5 hace que el interprete "Eleve" mi variable asi : (function () {
var feature; // ----> la variable esta elevada if ( typeof feature === "undefined" ){
feature = "callbacks";
console.log("JS coders love its " + feature );//----> undefined
} else {
console.log("JS developers love its " + feature );
} })();

al eliminar el var de la linea 5 ya el interprete ya no "Eleva" la variable es decir ya no es undefined asi imprimira el ELSE.
