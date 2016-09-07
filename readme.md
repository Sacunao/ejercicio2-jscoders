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

var feature = 'closures'; //window.feature = "clousure"

(function () { //lee el valor de window first

    var feature; // Por el hoisting el interprete lee la declaracion de la variable primero, pero al leerla solo declarada y sin valor asignado nos da como resultado undefined, ya que el valor (la función), no está siendo tomada en cuenta.
    
	if ( typeof feature === 'undefined' ){         
		feature = 'callbacks';         
        
		console.log('JS coders love its ' + feature );     
	} else {         
		console.log('JS developers love its ' + feature );     
	} 
})();

###Código de Resolución
var feature = 'closures'; //window.feature = "clousure"

(function () { //lee el valor de window first

	if ( typeof feature === 'undefined' ){ 
                //aqui lo lee como window.feature = "clousure"
                
		feature = 'callbacks';   // busca en el window si esta variable tiene algun valor y por eso la encuentra en el global. Se utiliza la teoria de Scope.
        
		console.log('JS coders love its ' + feature );     
	} else {         
		console.log('JS developers love its ' + feature );     
	} 
})();