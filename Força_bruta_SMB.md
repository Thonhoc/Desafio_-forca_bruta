medusa -h 192.168.56.102 -U users.txt -P senhas.txt -M smbnt -t 2 -T 5

-h endereço IP do sistema analisado.
-U  arquivo contendo usuários de teste.
-P arquivo contendo senhas utilizadas na avaliação.
-M módulo responsável pela comunicação com o serviço SMB.
-t quantidade de processos simultâneos por tarefa.
-T limite máximo de tarefas executadas de forma concorrente.