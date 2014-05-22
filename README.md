SD
==

Projeto de Sistemas Distribuídos 2014


Projeto esta dividido em módulos:
* Infraestrutura (sd-infra)
* HDFS/Hadoop (sd-hadoop)
* HBase/Objetos de Acesso (sd-dao)
* Webservices (sd-service)
* Business (sd-business)
* Web interface (sd-web)
* Request Broker (sd-request)
  
Os módulos Android, iOS e PhoneGap não utilizarão deste repositório, mas devem compreendê-lo para realizarem as chamadas necessárias

Foram criadas branchs para cada módulo, diminuindo assim o risco de que um commit acabe por causar danos a outros módulos
Ao serem aprovados os commits, eles serão vinculados a master

Cada branch possui o nome do módulo relativo a ela, removendo apenas o "sd-".
Exemplo:
* branch de sd-infra -> infra
* branch de sd-web ->web

Foi padronizado Java 7 para o projeto, por questões de infraestrutura

Comandos maven:
* <code>mvn clean install</code> ->realiza o build do projeto com a execução de testes
* <code>mvn clean install -Dmaven.test.skip=true</code> ->realiza o build sem execução de testes ou compilação de suas classes
* <code>mvn clean install -X</code> ->realiza o build do projeto em modo Debug
* <code>mvn eclipse:eclipse</code> ->atualiza o projeto no eclipse
* <code>mvn eclipse:eclipse -DdownloadSources</code> ->atualiza o projeto no eclipse e realiza o download de jars necessários
* <code>mvn eclipse:eclipse -DdownloadJavadocs</code> ->atualiza o projeto no eclipse e realiza o download dos javadocs necessários
* <code>mvn eclipse:eclipse -DdownloadSources -DdownloadJavadocs</code> ->atualiza o projeto no eclipse e realiza o download dos jars e javadocs necessários
  
Comandos Git:
* <code>git status</code> -> exibe o status atual (qual a branch, arquivos modificados para serem commitados)
* <code>git cola</code> -> interface GUI para selecionar arquivos a serem commitados
* <code>git commit -m "String"</code> -> realiza o commit dos arquivos staged pelo git cola com a mensagem String
* <code>git commit --amend</code> ->realiza um commit com um novo patch set para o commit ja em vigor
* <code>git branch</code> ->lista todas as branchs existentes
* <code> git checkout nome-da-branch</code> ->realiza a mudança para a branch especificada
* <code>git push origin master</code> ->realiza o commit do seu local para a branch master no caso
* <code>git push origin nome-da-branch</code> ->realiza o commit do seu local para a branch especificada
* <code>git pull</code> ->realiza o pull da branch, ou seja, recupera todos os arquivos de commits a sua frente
* <code>git reset --hard</code> ->apaga todas as modificações feitas
* <code>git reset --hard HEAD^</code> ->apaga todas as modificações feitas e volta 1 commit
* <code>gitk</code> ->verifica os commits realizados na branch e as modificações em cada comit
* <code>git log</code> ->exibe o log de commits
* <code>git log --oneline</code> exibe o log de commits de forma simplificada
