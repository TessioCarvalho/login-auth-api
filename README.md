Readme Login Auth API

Java 17
Spring Boot 3.2.5

Maven dependencies
	Spring Web
	Spring Boot DevTools
	Spring Data JPA
	Spring Security
	Lombok
	H2 Database
	JWT

Como utilizar:

Para pré-configurar o projeto utilizei o Spring initializr através do link: https://start.spring.io/

Na seção Project escolha Maven.
Na seção Language escolha Java.
Na seção Spring Boot escolha a versão 3.2.5.
Em Project Metadata no campo Artifact escreva login-auth-api.
Em Description escreva uma descrição para o seu projeto.
Em packaging marque a opção Jar.
Em Java escolha marque a opção 17.

Clique em add dependencies e adicione as dependências:
	Spring Web
	Spring Boot DevTools
	Spring Data JPA
	Spring Security
	Lombok

Agora clique em generate e baixe o arquivo .zip no seu local de preferência.

Importe a pasta extraída para o editor de sua preferência.

Agora adicione as dependências do H2 e JWT no arquivo pom.xml

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

Agora em src/main/resources/application.properties abaixo da linha spring.application.name=NOME-ESCOLHIDO-POR-VOCE adicione as seguinte Configurações:

		spring.datasource.url=jdbc:h2:mem:testdb
		spring.datasource.driver-class-name=org.h2.Driver
		spring.datasource.username=sa
		spring.datasource.password=

Aplicação pré-configurada.
