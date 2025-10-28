Título: Simulação de Ataque de Brute Force com Medusa (Kali Linux) em Metasploitable
Autor: Seu Nome
Data: 2025-10-28

Escopo

Simular um ataque de força bruta (brute force) de senhas contra serviços de rede expostos em uma VM Metasploitable, utilizando a ferramenta Medusa a partir de uma VM Kali Linux. O objetivo é demonstrar técnicas de auditoria de senhas, coleta de evidências e contramedidas.

Aviso Ético e Legal

Este projeto deve ser executado apenas em ambiente isolado e controlado (laboratório) com máquinas que você possui ou tem autorização explícita para testar. Qualquer tentativa de ataque contra sistemas sem autorização é ilegal. Use este material apenas para fins educativos e de teste em ambientes de laboratório.

Tecnologias e Ferramentas

Kali Linux (máquina atacante)

Metasploitable (máquina alvo)

Medusa (ferramenta de brute force)

Virt-Manager / QEMU / libvirt (virtualização no Ubuntu)

nmap, enum4linux, smbclient, tcpdump (enumeração e captura)

wordlists

Mitigações e recomendações

Implementar bloqueio de conta ou rate-limiting após N tentativas.

Implementar autenticação multifator (MFA).

Políticas de senha fortes e listas de bloqueio para senhas comuns.

Monitoramento e alertas para tentativas de autenticação anormais.

Restringir acesso por firewall/ACL e desativar serviços desnecessários.

Arquivos que serão incluídos neste repositório

Este repositório vai conter, além dos scripts e relatórios, os seguintes artefatos de evidência sanitizados:

screenshots/ — Prints dos resultados dos testes (ex.: telas do Medusa, nmap, enum4linux). 

wordlists/ — Exemplos de listas usadas nos testes. 

reports/ — Saídas das ferramentas (medusa, nmap, enum4linux) com resultados relevantes.


Conclusão

Este projeto apresentou uma simulação controlada de ataque de força bruta utilizando a ferramenta Medusa a partir de uma VM Kali Linux contra uma VM Metasploitable em um ambiente de laboratório. O objetivo principal foi demonstrar o fluxo de um teste de auditoria de senhas: preparação do ambiente, enumeração de serviços, execução do ataque, e coleta de evidências, seguido de recomendações práticas para mitigação.

Principais aprendizados

A enumeração prévia (nmap, enum4linux, smbclient) é essencial para identificar serviços e direcionar os ataques de maneira eficiente.

Ferramentas como Medusa permitem automatizar ataques contra múltiplos serviços (SSH, FTP, SMB), mas também aumentam o ruído na rede e podem acionar mecanismos de defesa se existirem proteções configuradas.

Mesmo em ambientes de laboratório, documentar cuidadosamente os passos, salvar saídas e gerar relatórios facilitam a reprodução, auditoria e correção das vulnerabilidades encontradas.
