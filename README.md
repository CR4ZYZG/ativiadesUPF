# Ocultamento de informação


Os detalhes internos de funcionamento de métodos de uma determinada classe podem, e em certos casos DEVEM permanecer ocultos para outros objetos e isso pode ser feito por meio do "encapsulamento". 

No entando o que diz respeito a Ocultação de Dados e Informações, é um processo e uma tecnica utilizada para proteger dados como senhas e dados importantes de usuarios cadastrados em uma loja online, de um possivel ataque externo e ilegal (Hack) , por exemplo.

Pode-se dizer  que o encapsulamento envelopa dados para ocultar a complexidade de uma sistema, podendo ser privados ou publicos.
A ocultação de dados manipula os dados que foram encapsulados de forma que possa restringir ou permitir o uso dessses dados, esses dados sempre serão privados e inacessiveis por classes e usuários externos

Por exemplo uma classe "Conta" tem um campo "Saldo de (cliente)". O saldo é uma informação sensivel e volatil, um aplicativo externo pode verificar se o saldo é possitivo ou negativo(ex), mas em hipotese alguma pode modificar o saldo.
