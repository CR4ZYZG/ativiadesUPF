# Ocultamento de informação


Os detalhes internos de funcionamento de métodos de uma determinada classe podem, e em certos casos DEVEM permanecer ocultos para outros objetos e isso pode ser feito por meio do "encapsulamento". 

No entando o que diz respeito a Ocultação de Dados e Informações, é um processo e uma tecnica utilizada para proteger dados como senhas e dados importantes de usuarios cadastrados em uma loja online, de um possivel ataque externo e ilegal (Hack) , por exemplo.

Pode-se dizer  que o encapsulamento envelopa dados para ocultar a complexidade de uma sistema, podendo ser privados ou publicos.
A ocultação de dados manipula os dados que foram encapsulados de forma que possa restringir ou permitir o uso dessses dados, esses dados sempre serão privados e inacessiveis por classes e usuários externos

Por exemplo uma classe "Conta" tem um campo "Saldo de (cliente)". O saldo é uma informação sensivel e volatil, um aplicativo externo pode verificar se o saldo é possitivo ou negativo (ex), mas em hipotese alguma pode modificar o saldo.



# Lei de Demeter (LoD)

Também conhecido como principio do menor conhecimento, essa lei estipula que um objeto deve ter conhecimento apenas de informações e recursos estritamente necessários para seu funcionamento;

Um objeto X pode "chamar" uma instancia do objeto Y, mas não pode solicitar um serviço de Z utilizando o objeto Y como uma ponte. Para a lei ser respeitada, o objeto Y deve ser modificada para que atenda o onjeto X diretamente, ou, X pode ter uma referencia direta à Z e fazer a requisição diretamente para ele.

Um exemplo de código em que a lei de Demeter é violada é apresentado a seguir:

**const data = cliente.ultimoPedido.dadosPedido.dataEmissao**

O problema nisso é que em uma modificação da classe ultimoPedido, as propriedades podem não existir mais e assim ocorrerá uma quebra no sistema, um chamado a uma propriedade nula.

Nesse caso o ideal é que seja feito na classe ultimoPedido um getDataEmissao para ser usado em outras classes.

*const data = ultimoPedido.getDataEmissao()*


fonte do exemplo (https://dev.to/ino_gu/lei-de-demeter-4ldf)
