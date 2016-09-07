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

1. A pesar que la variable var feature está declarada la cuenta como undefined y pasa a la condición else.