Projeto: Simulação de Ataque de Brute Force com Medusa (Kali Linux) em Metasploitable

Bootcamp: Santander – Cibersegurança 2025
Autor: Fabio Ferreira Reis
Data: 29/10/2025

Escopo

Este projeto tem como objetivo simular um ataque de força bruta (brute force) contra serviços de rede expostos em uma 
VM Metasploitable, utilizando a ferramenta Medusa a partir de uma VM Kali Linux.

O foco é demonstrar:

técnicas de auditoria de senhas,
coleta de evidências,
identificação de vulnerabilidades,
e recomendações de segurança.

⚠️ Aviso Ético e Legal

Este projeto deve ser executado exclusivamente em laboratório, em máquinas que você possui ou tem autorização expressa para testar.
Realizar testes de intrusão sem permissão é crime.se este material somente para fins educacionais e de pesquisa controlada.

Tecnologias e Ferramentas Utilizadas

Kali Linux – Sistema utilizado para realizar os ataques.
Metasploitable – Máquina vulnerável usada como alvo.
Medusa – Ferramenta de brute force para ataques em serviços como SSH, FTP, Telnet, SMB etc.
Virt-Manager – Ambiente de virtualização para rodar as máquinas no Ubuntu.

Ambiente de Testes

Máquina de Ataque: Kali Linux (Virt-Manager).
Máquina Alvo: Metasploitable (Virt-Manager).
Rede: Ambiente isolado, configurado no Virt-Manager, garantindo comunicação entre as máquinas sem exposição à Internet.

Mitigações e Contramedidas
Políticas de bloqueio após N tentativas (rate-limiting).
MFA (Autenticação Multifator).
Senhas fortes e únicas.

Monitoramento e alertas de tentativas suspeitas.
Desativação de serviços não utilizados.
Restrições de firewall / ACL.
Boas Práticas para o Relatório

Inclua preferencialmente:
Descrição do ambiente (IPs, versões, topologia).
Comandos executados e suas saídas.
Tempo total e taxa de tentativas por minuto.
Impacto e recomendações priorizadas.
Capturas de tela dos testes.
Logs relevantes (Medusa, nmap, enum4linux etc).

Estrutura deste Repositório
screenshots/ — Imagens e evidências dos testes.
wordlists/ — Amostras de listas de senhas usadas nos ataques.
reports/ — Saídas brutas das ferramentas utilizadas durante a auditoria.

Conclusão

A simulação demonstrou o processo completo de um teste de força bruta:
Preparação do ambiente
Enumeração de serviços
Execução do ataque
Registro e análise das evidências
Sugestões de mitigação
O experimento reforça a importância de políticas de segurança robustas, monitoramento ativo e uso de mecanismos de defesa como MFA e bloqueio por tentativas.

Principais Aprendizados

A enumeração inicial (nmap, enum4linux, smbclient) é fundamental para direcionar ataques com precisão.
Ferramentas como Medusa agilizam ataques contra múltiplos protocolos, mas também provocam maior ruído na rede.
Documentar cada passo e resultado facilita auditorias, correções e reprodutibilidade do teste.
