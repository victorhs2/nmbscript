# NMBScript - Script de instalação e configuração do NMBOT
#### Versão atual: 1.3

Este script foi desenvolvido para automatizar a instalação e a configuração do NMBOT em servidores rodando o Ubuntu Linux 18.04 LTS. O script foi amplamente testado no shell 'bash' versões 4.4.20 e 5.1.8, sendo provável que funcione em outras versões. Entretanto, para uso com outros tipos de shell ou com outras versões do 'bash', podem ser necessários ajustes no código. É recomendado que o sistema em que for utilizado não tenha outro uso além da execução do NMBOT, de forma que sugere-se a sua instalação em uma máquina virtual, possivelmente em ambiente de nuvem.

O presente script foi criado com o intuito único e exclusivo de auxiliar os usuários da plataforma NM a configurarem o robô para seu uso pessoal. É oferecido com base na solidariedade e de boa fé para que os usuários tenham uma melhor experiência com o uso do robô. Todas as suas funções e comandos atuam de modo a automatizar e facilitar a configuração do robô e do sistema operacional, de tal forma que tudo o que o script faz pode também ser feito manualmente.

Todas as alterações introduzidas no sistema por este script podem ser removidas com o comando 'nms-remover'. Por motivos de transparência, todos os comandos do script trazem comentários explicativos no código fonte, tornando o seu conteúdo mais facilmente acessível para aqueles que desejarem estudá-lo antes da execução. O autor incentiva os interessados a examinar e estudar o código do script de modo a entender as modificações que ele realiza no sistema. Use-o por sua conta e risco.

A distribuição do script é livre para uso, estudo, cópia, modificação e redistribuição. Ele não é fornecido sob nenhuma licença específica, tampouco são exigidos créditos ou direitos de autoria. Da mesma forma, não é oferecido nenhum tipo de suporte por parte do seu autor. Salienta-se que não há nenhuma pretensão de uso comercial e que o autor não pode ser responsabilizado por eventual e hipotético uso comercial realizado por terceiros.

O autor deste script não possui nenhum vínculo com os criadores do NMBOT, os quais não prestarão nenhum tipo de suporte para o seu uso. Tenha em mente que a equipe da plataforma NM não presta suporte para o uso do NMBOT no sistema operacional Linux. O autor também esclarece que não se deseja, com esta aplicação, alterar de qualquer maneira o funcionamento intrínseco do NMBOT, em especial com relação às condicionantes de acesso ao robô instituídas pela equipe responsável por ele. É sabido que a execução do NMBOT está sujeita à adesão a uma assinatura paga, e o autor deste script recomenda que todos os interessados façam sua adesão pelo site oficial (investidordesucesso.com.br).

Durante o processo de instalação e também no uso de determinadas funções, a depender da forma como você acessou o servidor, pode ser solicitada a sua senha de usuário pelo terminal. Neste caso, é a senha do usuário do sistema Linux que você configurou. Isso é necessário para ajustar algumas configurações do NMBOT que demandam privilégios de administrador do sistema. Se você acessou o servidor com um arquivo de chave privada, o que é recomendado, essa senha não será solicitada com a mesma frequência.

Autor do script original: Victor H.S.

### Download
    wget bit.ly/nmbscript -O .nmbscript

### Instalação
    . .nmbscript

### Desinstalação

Mantendo instalador do script:

    nms-remover

Remoção completa, incluindo o instalador do script:

    nms-remover -f

Desinstalação manual:

    rm -f ~/.nmbscript
    sudo rm -f /etc/profile.d/nmbscript-variables.sh
    sudo sed -i /^NM_COUNT/d /etc/environment
    sudo sed -i /^NMBOT/d /etc/environment
    mv -f ~/.bashrc.bak ~/.bashrc

### Lista de comandos disponíveis:

Comandos do robô:

    nm-instalar
    nm-desinstalar
    nm-listar
    nm-configurar
    nm-agendar
    nm-backup
    nm-registros
    nm-atualizar

Comandos do script:

    nms-atualizar
    nms-ajuda
    nms-info
    nms-remover
