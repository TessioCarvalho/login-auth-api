<h1 align="center">Login Auth API</h1>

<h4 align="center">Java 17 / Spring Boot 3.2.5 / Maven</h4>

Utilize o [Spring initializr](https://start.spring.io/) para pré-configurar o projeto.
* Na seção *'Project'* escolha *'Maven'*.
* Na seção *'Language' escolha 'Java'*.
* Na seção *'Spring Boot'* escolha *'3.2.5'*.
* Em *'Project Metadata'* no campo *'Artifact'* digite nome do projeto.
* Em *'Description'* escreva uma descrição para o seu projeto.
* Em *'Packaging'* marque a opção *'Jar'*.
* Em *'Java'* marque a opção *'17'*.
<p>Clique em 'add dependencies' e adicione as seguintes dependências:</p>

* Spring Web
* Spring Boot DevTools
* Spring Data JPA
* Spring Security
* Lombok

Agora clique em *'Generate'* e baixe o arquivo *.zip* no seu local de preferência.

Importe a pasta extraída para o editor de sua preferência.

Adicione as dependências do H2 e JWT no arquivo *pom.xml*

		<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
			<scope>runtime</scope>
		</dependency>

		<dependency>
			<groupId>com.auth0</groupId>
			<artifactId>java-jwt</artifactId>
			<version>4.4.0</version>
		</dependency>

Agora em *'src/main/resources/application.properties'* abaixo da linha '*spring.application.name*', adicione as seguinte configurações:

		spring.datasource.url=jdbc:h2:mem:testdb
		spring.datasource.driver-class-name=org.h2.Driver
		spring.datasource.username=sa
		spring.datasource.password=
