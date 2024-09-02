El problema parece estar relacionado con la declaración de la variable "ownable" en la línea 11.
En Solidity, no puede declarar una variable de estado de tipo "dirección" como privada.
En Solidity, no puede declarar una variable de estado de tipo "Address" como privada. En su lugar, debe declararse en el constructor y luego usarse internamente dentro de las funciones haciendo referencia a la dirección del contrato usando la palabra clave `this` como esta: “address payable owner”
