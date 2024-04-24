# Teste de Sistemas Operativos - Módulo 3

Faz *fork* do repositório para teres a tua cópia.

Preenche o ficheiro README diretamente no GitHub. A partir da página principal do repositório, clica em "Edit File" (ícone representando um lápis).

Escreve as respostas dentro dos blocos correspondentes. Substitui as reticências pelo que é pedido em cada pergunta. Não desformates o documento.

Quando acabares, carrega no botão "Commit Changes".

## Informação do aluno

    Nome: .Hélio Cesar Miranda Tavares..

## P1 - Para as seguintes questões, assinala a opção correta: (2.5v)

  1. Qual das seguintes afirmações caracteriza melhor um SO servidor?

    a) Projetado para computação de uso geral
    b) Otimizado para alta disponibilidade e confiabilidade
    c) Destinado a usuários individuais
    d) Usado principalmente para jogos
    
    Resposta: b) Otimizado para alta disponibilidade e confiabilidade...

  2. Das seguintes, qual é a função mais apropriada para um SO servidor?

    a) Executar aplicações de desktop
    b) Desenvolver aplicações móveis
    c) Fornecer software de entretenimento
    d) Gerir recursos e serviços de rede
    
    Resposta: d) Gerir recursos e serviços de rede...
   
  3. Qual dos seguintes é um sistema operativo servidor popular?

    a) Windows 11
    b) macOS Big Sur
    c) Ubuntu Server
    d) Android
    
    Resposta:   c) Ubuntu Server...

  4. Qual é o papel de um servidor num modelo cliente-servidor?

    a) Consumir recursos fornecidos pelos clientes
    b) Fornecer recursos e serviços aos clientes
    c) Atuar como uma estação de trabalho independente
    d) Facilitar a comunicação ponto a ponto
    
    Resposta:  b) Fornecer recursos e serviços aos clientes...

  5. Qual dos seguintes protocolos é mais usado para aceder remotamente a servidores?

    a) FTP
    b) HTTP
    c) SSH
    d) SMTP
    
    Resposta: c) SSH...

## P2 - Indica, sequencialmnente, os comandos para realizar as seguintes instruções: (7.5v)

  1. Cria um diretório com o nome "ex1", entra no mesmo, e cria 3 ficheiros vazios com os nomes "f1", "f2", "f3". No fim, lista os conteúdos do diretório atual.

    Resposta:mkdir ex1         //Cria um diretório com o nome "ex1"
            cd ex1             //Entra no diretório"ex1"
            touch f1 f2 f3     //Cria 3 arquivos vazios com os nomes "f1", "f2" e "f3"
            ls                  //Lista os conteúdos do diretório atual

    ...
    
  2. Assumindo que estás no diretório "ex1", renomeia os ficheiros "f1" e "f2" para que acabem com "_antigo", e cria cópias dos mesmos.

    Resposta:mv f1 f1_antigo       //Renomeia o arquivo "f1" para "f1_antigo"
             mv f2 f2_antigo     //Renomeia o arquivo"f2" para "f2_antigo"
             cp f1_antigo f1      //Cria uma cópia do arquivo "f1_antigo" com o nome "f1"
             cp f2_antigo f2     //Cria uma cópia do arquivo"f2_antigo" com o nome "f2"

    ...

  3. Assumindo que estás no diretório "ex1", cria o diretório "ex2", e move os ficheiros copiados no exercício anterior para o novo diretório. Seguidamente, apaga os ficheiros originais.

    Resposta:mkdir ../ex2               //Cria o diretório"ex2" um nível acima do diretório atual
             mv f1 f2 ../ex2            // Move os arquivos "f1" e "f2" para o diretório "ex2"
             rm f1_antigo f2_antigo    //Apaga os arquivos originais"f1_antigo" e "f2_antigo"

    ...

  4. Atualiza os repositórios de *packages* para garantir acesso às *packages* mais recentes, e instala o serviço **htop**.

    Resposta:sudo apt update        //Atualiza a lista de pacotes disponiveis
             sudo apt install htop  // Instala o serviço htop

    ...

  5. Cria um novo utilizador com o teu primeiro nome, e com o diretório "/home/nome_de_utilizador". Mostra a informação (ID) do utilizador criado.

    Resposta:sudo adduser Hélio --home /home/Hélio
             id Hélio

    ...

## P3 - Realiza os seguintes exercícios, com respostas detalhadas: (6v)

  1. Indica alguns aspetos que diferenciam um SO cliente de um SO servidor.

    Resposta:SO Cliente: Atividades de usuário final, como navegação na web, processamento de documentos e entretenimento. Lida com cargas de trabalho leves a moderadas, focadas em tarefas individuais ou de pequenos grupos de usuários.
            SO Servidor: Fornecer serviços de rede a outros dispositivos e usuários. Lida com cargas de trabalho pesadas e intensivas, suportando múltiplos usuários simultâneos e fornecendo serviços críticos de rede, como hospedagem de sites, bancos de dados e armazenamento de arquivos.
    ...
     
  2. Explica a importância de otimizar um sistema operativo servidor, com exemplos de técnicas para otimização.

    Resposta:
A otimização de um sistema operativo servidor é fundamental para garantir alto desempenho e segurança dos serviços que ele fornece. Isso é importante porque um servidor eficiente pode lidar com cargas de trabalho intensivas, minimizar interrupções não planejadas e proteger contra ameaças cibernéticas. Algumas técnicas de otimização incluem afinamento do kernel, ajuste de recursos, otimização de rede, monitoramento em tempo real, segurança reforçada e desfragmentação de discos. Essas práticas garantem que o servidor opere de forma eficaz, atendendo às demandas dos usuários e garantindo a integridade dos dados.
    

  3. Descreve o processo de instalar e configurar um servidor web num SO servidor, incluindo as etapas necessárias.

    Resposta://sudo apt update   uma boa prática garantir que os repositórios do sistema estejam atualizados;
             //sudo apt install apache2  Use o gerenciador de pacotes apt para instalar o servidor web Apache;
             //sudo systemctl status apache2  Após a instalação, verifique se o Apache está em execução;
             //sudo ufw allow 'Apache'  Se estiver usando o firewall UFW (Uncomplicated Firewall), abra as portas HTTP (80) e HTTPS (443).


    ...

## P4 - Indica os comandos **git** para realizar as seguintes operações: (4v)

  1. Considera que estás no ramo 'master' de um repositório git criado localmente. Associa este repositório ao repositório remoto contido no url 'https://github.com/SO/OMeuRepositorioRemoto'. Altera o nome do ramo atual para 'main', e envia os *commits* já feitos localmente para o repositório remoto.

    Resposta:git remote add origin https://github.com/SO/OMeuRepositorioRemoto
             git branch -m master main
             git push -u origin main

    ...

  2. Considera que estás na pasta raiz do teu repositório local, onde atualizaste um ficheiro de nome 'index.html'. Envia **apenas** esta atualização para o teu repositório remoto, com uma mensagem de commit apropriada.

    Resposta:git add index.html
             git commit - "Atualização do arquivo index.html"
             git push origin main

    ...
