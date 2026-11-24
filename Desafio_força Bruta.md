
Projeto Prático: Avaliação de Resistência a Ataques de Autenticação com Kali Linux e Medusa

1. Objetivo
	Este projeto teve como objetivo estudar técnicas de autenticação e validar mecanismos de proteção contra tentativas de acesso indevido em ambientes controlados de laboratório. Foram utilizados o Kali Linux como estação de testes e ambientes vulneráveis para fins educacionais, permitindo observar o comportamento dos serviços diante de múltiplas tentativas de autenticação e analisar medidas de mitigação.

2. Ambiente Utilizado
	Máquina 1 – Kali Linux

- Sistema operacional: Kali Linux
- Função: estação de testes e análise

	Máquina 2 – Ambiente Vulnerável

- Sistema operacional: Metasploitable 2
- Aplicações utilizadas: 
- Servidor FTP
- Serviço SMB
- DVWA (Damn Vulnerable Web Application)
I
nfraestrutura

- Hypervisor: Oracle VirtualBox
- Tipo de rede: Host-Only
- Comunicação restrita ao laboratório

3. Metodologia
Os testes foram realizados exclusivamente em ambiente isolado e controlado.

As atividades consistiram em:

- Identificação dos serviços disponíveis.
- Avaliação do comportamento dos mecanismos de autenticação.
- Simulação de múltiplas tentativas de login utilizando listas de credenciais de laboratório.
- Registro dos eventos observados.
- Aplicação de controles defensivos para comparação dos resultados.

4. Cenário 1 – Serviço FTP

	Objetivo

Avaliar a resistência do serviço FTP frente a repetidas tentativas de autenticação.
Observações
	Durante os testes foi possível verificar:

- Existência de contas com senhas fracas.
- Ausência de bloqueio após múltiplas tentativas.


Impacto
Contas com credenciais previsíveis podem ser comprometidas rapidamente quando não existem políticas adequadas de segurança.

5. Cenário 2 – Aplicação Web (DVWA)

Objetivo

	Analisar a segurança do processo de autenticação de uma aplicação web vulnerável.
Observações
Foram avaliados:

- Tratamento de autenticações inválidas.
- Existência de limitação de tentativas.
- Mensagens de erro exibidas ao usuário.
- Site em texto simples sem SSL

	Impacto
Aplicações sem controles de autenticação robustos podem facilitar tentativas automatizadas de acesso indevido.

	6. Cenário 3 – Serviço SMB

	Objetivo

	Avaliar mecanismos de autenticação e proteção de contas em compartilhamentos de rede.
Observações
Foi observado:

- Comportamento do serviço diante de diversas tentativas de autenticação.
- Eficiência das políticas de senha.
- Presença ou ausência de bloqueio de contas.
- Registros produzidos pelo sistema.

	Impacto
Senhas reutilizadas ou excessivamente simples aumentam significativamente o risco de comprometimento.

	7. Medidas de Mitigação
As seguintes recomendações foram identificadas como boas práticas:

	Políticas de Senha

- Mínimo de 12 caracteres.
- Combinação de letras, números e símbolos.
- Proibição de senhas comuns.

	Bloqueio de Conta

- Limitação de tentativas consecutivas.
- Bloqueio temporário após falhas sucessivas.

	Autenticação Multifator

- Implementação de MFA sempre que possível.
Monitoramento

- Centralização de logs.
- Alertas para múltiplas falhas de autenticação.
- Correlação de eventos de segurança.
Hardening dos Serviços

- Desativação de serviços desnecessários.
- Restrição de acesso por firewall.
- Segmentação de rede.

	8. Conclusão
O laboratório permitiu compreender como credenciais fracas representam um dos principais vetores de comprometimento de sistemas. A atividade demonstrou a importância de políticas de senha adequadas, mecanismos de bloqueio de contas, monitoramento contínuo e autenticação multifator para reduzir a superfície de ataque. A utilização de ambientes vulneráveis foi fundamental para observar os riscos sem impactar sistemas reais.
