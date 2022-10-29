Presente en la Herencia, Composicion y Parametrizacion. La reusabilidad esta permitida y puede ser aprovechada mediante estos tres mecanismos

### Herencia vs Composicion
En la Composicion la reusabilidad es programatica, debido a que debo enviar mensajes a mis colaboradores y relegar las operaciones para que ellos la satisfascan. En este caso, la clase que mantiene las partes (el todo) tiene la capacidad de decidir que operaciones estan disponibles y cuale sno.
- Enlace Dinamico
- No existe acoplamiento alguno con la clase parte, solo le delego responsabilidades

En la Herencia la reusabilidad es automatica, debido a que teniendo operaciones en la clase padre no necesito redefinir los metodos. El lenguaje lo hace por ti. Caso contrario a la Composicion, la herencia no tiene forma de ocultar metodos heredados por el padre, los tiene que ofrecer si o si.
- Enlace estatico
- Acoplamiento a los atributos de la clase base por modificador 'protected'.

La herencia con polimorfismo es el mecanismo mas fuerte para utilizar en las partes del proyecto que son mas propensas a ser extendidas