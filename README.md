SD
==

Projeto de Sistemas Distribuídos 2014


Projeto esta dividido em módulos:
  -Infraestrutura (sd-infra)
  -HDFS/Hadoop (sd-hadoop)
  -HBase/Objetos de Acesso (sd-dao)
  -Webservices (sd-service)
  -Business (sd-business)
  -Web interface (sd-web)
  -Request Broker (sd-request)
  
Os módulos Android, iOS e PhoneGap não utilizarão deste repositório, mas devem compreendê-lo para realizarem as chamadas necessárias

Foi padronizado Java 7 para o projeto, por questões de infraestrutura

Comandos maven:
  -mvn clean install ->realiza o build do projeto com a execução de testes
  -mvn clean install -Dmaven.test.skip=true ->realiza o build sem execução de testes ou compilação de suas classes
  -mvn eclipse:eclipse ->atualiza o projeto no eclipse
  -mvn eclipse:eclipse -DdownloadSources ->atualiza o projeto no eclipse e realiza o Download de jars necessários
  -mvn eclipse:eclipse -DdownloadJavadocs ->atualiza o projeto no eclipse e realiza o download dos javadocs necessários
  
Comandos Git:
  git status -> exibe o status atual (qual a branch, arquivos modificados para serem commitados)
  git cola -> interface GUI para selecionar arquivos a serem commitados
  git commit -m "String" -> realiza o commit dos arquivos staged pelo git cola com a mensagem String
  git push origin master ->realiza o commit do seu local para a branch master no caso
  git pull ->realiza o pull da branch, ou seja, recupera todos os arquivos de commits a sua frente
  git reset --hard ->apaga todas as modificações feitas
  git reset --hard HEAD^ ->apaga todas as modificações feitas e volta 1 commit
  gitk ->verifica os commits realizados na branch e as modificações em cada comit
