
medusa -h 192.168.6.102 -U users.txt -P pass.txt -M http -m PAGE:/dvwa/login.php -m FORM:"username=^USER^&password=^PASS^&Login=Login" -m FAIL:"Login failed" -t 6


Host de destino (-h 192.168.56.102)
O parâmetro -h é utilizado para especificar o endereço IP do sistema-alvo presente no ambiente de laboratório.

Lista de usuários (-U users.txt)

O parâmetro -U referencia um arquivo de texto contendo uma relação de usuários previamente definidos para fins de teste.

Lista de senhas (-P pass.txt)
O parâmetro -P indica o arquivo que contém as senhas utilizadas durante os testes. 

Módulo de comunicação (-M http)

O parâmetro -M define o módulo responsável pela interação com o serviço avaliado.

Página de autenticação (-m PAGE:/dvwa/login.php)
Esse parâmetro especifica o recurso web que contém o formulário de autenticação da aplicação.


Estrutura do formulário (-m FORM:"username=^USER^&password=^PASS^&Login=Login")

O parâmetro FORM descreve a estrutura lógica dos dados enviados ao formulário de autenticação. Os marcadores ^USER^ e ^PASS^ representam variáveis utilizadas pela ferramenta para inserir, dinamicamente, os nomes de usuário e senhas provenientes das listas de teste. 


Critério de identificação de falha (-m FAIL:"Login failed")

O parâmetro FAIL estabelece o padrão textual que deve ser interpretado como uma tentativa de autenticação malsucedida.

Quantidade de processos simultâneos (-t 2)
O parâmetro -t define o número de processos de execução simultânea utilizados durante os testes.

