Projeto: Simulação de Ataque de Brute Force com Medusa (Kali Linux) em Metasploitable.

Bootcamp - Santander - Cibersegurança 2025

Autor: Fabio Ferreira Reis

Data: 2025-10-29

Escopo

Simular um ataque de força bruta (brute force) de senhas contra serviços de rede expostos em uma VM Metasploitable, utilizando a ferramenta Medusa a partir de uma VM Kali Linux. O objetivo é demonstrar técnicas de auditoria de senhas, coleta de evidências e contramedidas.

Aviso Ético e Legal

Este projeto deve ser executado apenas em ambiente isolado e controlado (laboratório) com máquinas que você possui ou tem autorização explícita para testar. Qualquer tentativa de ataque contra sistemas sem autorização é ilegal. Use este material apenas para fins educativos e de teste em ambientes de laboratório.

Tecnologias e Ferramentas Utilizadas :

- Kali Linux: Sistema operacional baseado em Debian, utilizado para realizar os ataques.
- Metasploitable: Máquina virtual vulnerável, configurada para ser o alvo do ataque.
- Medusa: Ferramenta de brute force para realizar tentativas de login em serviços de rede.
- Virt-Manager: Ferramenta para criar e gerenciar máquinas virtuais no Ubuntu.

Ambiente de Testes :

- Máquina de Ataque: Kali Linux (máquina atacante) configurada no Virt-Manager.
- Máquina Alvo: Metasploitable (máquina vulnerável), com IP (em uma rede interna configurada no Virt-Manager).
- Rede: Ambiente isolado configurado com Virt-Manager no Ubuntu, permitindo comunicação entre as duas máquinas virtuais.

Mitigações e contramedidas :

- Políticas de bloqueio após N tentativas (account lockout / rate-limiting).
- Autenticação multifator (MFA).
- Senhas fortes (compridas e únicas).
- Monitoramento e alertas de tentativas de login anormais.
- Desativar serviços desnecessários ou restringir acesso por firewall/ACL.
  
Boas práticas para o relatório :

Contexto do ambiente (IPs, versões, topologia).
- Comandos exatos executados e resultados.
- Tempo total e taxa de tentativas (tentativas/minuto).
- Impacto e recomendações priorizadas.
- Anexar capturas e logs.

Arquivos que serão incluídos neste repositório: 

- screenshots/ — Prints dos resultados dos testes (ex.: telas do Medusa, nmap, enum4linux).
- wordlists/ — Exemplos de listas usadas nos testes. Somente amostras e arquivos
- reports/ — Saídas das ferramentas (medusa, nmap, enum4linux) com resultados relevantes.

Conclusão

Este projeto apresentou uma simulação controlada de ataque de força bruta utilizando a ferramenta Medusa a partir de uma VM Kali Linux contra uma VM Metasploitable em um ambiente de laboratório. 
O objetivo principal foi demonstrar o fluxo de um teste de auditoria de senhas: preparação do ambiente, enumeração de serviços, execução do ataque, e coleta de evidências, seguido de recomendações práticas para mitigação.

Principais aprendizados

A enumeração prévia (nmap, enum4linux, smbclient) é essencial para identificar serviços e direcionar os ataques de maneira eficiente.
Ferramentas como Medusa permitem automatizar ataques contra múltiplos serviços (SSH, FTP, SMB), mas também aumentam o ruído na rede e podem acionar mecanismos de defesa se existirem proteções configuradas.
Mesmo em ambientes de laboratório, documentar cuidadosamente os passos, salvar saídas e gerar relatórios facilitam a reprodução, auditoria e correção das vulnerabilidades encontradas.
