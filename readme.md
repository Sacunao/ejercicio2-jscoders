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
Nota: Solo modificar una línea para que se obtenga el resultado deseado.
Al subir a GitHub, indicar el motivo por el que está mostrando el primer mensaje en el README.md.