---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/linux-dentro-do-windows/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Linux

## criado em: 
-  28-05-2023 - 14:36

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Coisas que dá para fazer com sub sistema de linux em windows\|Coisas que dá para fazer com sub sistema de linux em windows]]
- tags: #ANELO 
- Fontes & Links: 

---

# COMO USAR LINUX DENTRO DO WINDOWS 11

Para executar o Linux dentro do Windows 11, você tem algumas opções diferentes. Aqui estão dois métodos comumente usados:

1. Subsistema Windows para Linux (WSL):
   - O Subsistema Windows para Linux é uma camada de compatibilidade que permite executar distribuições Linux nativamente no Windows sem a necessidade de uma máquina virtual.
   - Abra a Microsoft Store em seu sistema Windows 11 e pesquise "Linux" ou o nome da distribuição específica do Linux que deseja usar (por exemplo, Ubuntu, Debian, Fedora).
   - Escolha a distribuição desejada, instale-a e siga as instruções fornecidas.
   - Depois de instalada, você pode iniciar a distribuição do Linux no menu Iniciar ou digitando seu nome na barra de pesquisa do Windows.
   - Esse método fornece uma interface de linha de comando para o Linux, mas não oferece suporte à execução de aplicativos gráficos.

2. Software de virtualização:
   - Você também pode usar um software de virtualização, como o Oracle VM VirtualBox ou o VMware Workstation, para executar um sistema operacional Linux completo dentro de uma máquina virtual no sistema Windows 11.
   - Faça download e instale o software de virtualização de sua escolha (por exemplo, VirtualBox) em seus sites oficiais.
   - Obtenha uma imagem ISO da distribuição do Linux que você deseja usar (por exemplo, Ubuntu, CentOS).
   - Crie uma nova máquina virtual no software de virtualização e defina as configurações, como memória, armazenamento e opções de rede.
   - Monte a imagem ISO do Linux na máquina virtual e inicie o processo de instalação.
   - Siga o assistente de instalação para configurar a distribuição do Linux.
   - Depois de instalada, você pode iniciar a máquina virtual para executar o Linux dentro do Windows 11. Esse método permite a execução de aplicativos Linux gráficos e de linha de comando.

Observação: a disponibilidade e as etapas específicas podem variar de acordo com a configuração do sistema e a distribuição do Linux escolhida. Consulte sempre a documentação fornecida pelo software ou pela distribuição para obter instruções detalhadas.

---

## Prós & Contras


Aqui estão os prós e os contras dos dois métodos mencionados:

**Subsistema Windows para Linux (WSL)**:

Prós:
1. Integração: A WSL oferece integração perfeita entre o Windows e o Linux, permitindo que você acesse e gerencie arquivos do Linux a partir do Windows File Explorer.
2. Desempenho: A WSL tem baixa sobrecarga, pois executa os binários do Linux nativamente no Windows, sem a necessidade de uma camada de virtualização completa.
3. Conveniência da linha de comando: Se você trabalha principalmente com a linha de comando, a WSL oferece uma experiência familiar de shell do Linux diretamente no Windows.
4. Fácil instalação: A instalação da WSL e das distribuições Linux da Microsoft Store é simples e fácil de usar.

Contras:
1. Aplicativos gráficos limitados: A WSL não oferece suporte à execução de aplicativos gráficos do Linux prontos para uso. Embora existam soluções alternativas disponíveis, a configuração pode ser mais complexa.
2. Limitações do kernel: A WSL usa uma camada de compatibilidade leve e não fornece um kernel completo do Linux. Algumas funcionalidades específicas do Linux ou módulos do kernel podem não funcionar como esperado.
3. Opções de distribuição limitadas: Embora existam várias distribuições do Linux disponíveis para a WSL, as opções podem ser mais limitadas em comparação com o uso do software de virtualização.

**Software de virtualização:**

Prós:
1. Experiência completa com o Linux: A execução do Linux em uma máquina virtual oferece um ambiente Linux completo com acesso total a aplicativos gráficos e de linha de comando.
2. Amplo suporte a distribuições: O software de virtualização permite instalar e executar uma ampla variedade de distribuições do Linux, o que lhe dá mais flexibilidade para escolher a que melhor se adapta às suas necessidades.
3. Melhor compatibilidade: Alguns aplicativos do Linux podem exigir um kernel completo do Linux, que está disponível quando se usa o software de virtualização.

Contras:
1. Excesso de recursos: A execução de uma máquina virtual requer recursos adicionais do sistema, incluindo memória, espaço em disco e potência da CPU.
2. Isolamento: A máquina virtual é executada separadamente do seu ambiente Windows, o que significa que você precisará alternar entre a máquina virtual Linux e o Windows se quiser acessar arquivos ou aplicativos de ambos.
3. Complexidade de instalação e configuração: A configuração e a instalação de uma máquina virtual com a distribuição Linux desejada podem ser mais complicadas em comparação com a instalação da WSL.

Considere esses prós e contras com base em seus requisitos e preferências específicos para determinar qual método é mais adequado ao seu caso de uso.