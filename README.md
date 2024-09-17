Por lo poco que estoy aprendiendo, en solidity la palabra privado no es un moficador de visibilidad de una variable. En este código se lo utiliza de esta forma. Lo que hice en este caso es eliminar la palabra. Pero también creo que  la propiedad es manejada por el propietario del contrato por lo que desde mi punto de vista seria redundante declararla en el código y se podría eliminar la palabra Owner tambien

Despues en la función WithdrawTips. En solidity Cuando tenemos que enviar o recibir  ether debemos hacerlo con direcciones payables( por lo que lei y vi en youtube, las direcciones estándar no pueden recibir ether sin antes estar marcadas como payable)..por ende creo que se debería convertir la  dirección del propietario en una dirección pagable y usar la función transferir para tratar de enviar el saldo del contrato al propietario

En SendMeATip.sol modifique el codigo intentando corregirlo. Estoy en proceso de aprendizaje desde ya muuchas gracias por leer
