Error: Linea 11: private address owner;
Se ha utilizado el contrato "Ownable" de OpenZeppelin, que tiene un constructor que ya establece el propietario. Por lo tanto es innecesario y redundante definir una variable "propietaria" en el contrato

Error: Linea 49: require(owner().send(address(this).balance));
Aquie  "send" y "transfer" solo están disponibles para objetos de tipo "address payable", no "Address" .El error en la función “withdrawTips” donde se está intentando enviar todo el saldo del contrato al propietario usando owner().send(address(this).balance)Aqui owner() devuelve una dirección y no una dirección de pago, por lo que no puede llamar a la función send()
El código puede cambiarse por :
function withdrawTips() public {
require(payable(owner()).send(address(this).balance)

