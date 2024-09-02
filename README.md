El problema esta relacionado con la declaración de la variable "ownable" en la línea 11.
En Solidity, no se puede declarar una variable de estado de tipo "Address" como privada. En su lugar, debe declararse en el constructor y luego usarse internamente dentro de las funciones haciendo referencia a la dirección del contrato usando la palabra clave `this` como esta: “address payable owner”



Error 2. (error de declaración)
Se intenta declarar una variable o función con el mismo nombre que otra en su código. En este caso, tanto el contrato Ownable de OpenZeppelin como su propia variable "owner" están intentando definir un identificador llamado "owner".
