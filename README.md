#Comandos úteis do Maven

## Criação de Projeto

### desktop java (jar)

```
mvn archetype:generate \
  -DarchetypeGroupId=org.apache.maven.archetypes \
  -DarchetypeArtifactId=maven-archetype-quickstart \
  -Dversion=1.0-SNAPSHOT \
  -DgroupId=com.erkobridee.exemplo.mvn \
  -DartifactId=ExemploMavenDesktop
```

preparar o projeto para o eclipse

```
mvn eclipse:eclipse 
```


### web java

```
mvn archetype:generate \
    -DarchetypeGroupId=org.apache.maven.archetypes \
    -DarchetypeArtifactId=maven-archetype-webapp \
    -Dversion=1.0-SNAPSHOT \
    -DgroupId=com.erkobridee.exemplo.mvn \
    -DartifactId=ExemploMavenWeb
```

preparar o projeto para o eclipse

```
mvn eclipse:eclipse -Dwtpversion=2.0
```

## Comandos para utilizar em projeto

mostra a arvore de dependencies(.jar)

	mvn depedency:tree 

copia os jar(dependencies) para pasta target/dependency [ evita eventuais problemas de ambiente ]

	mvn dependency:copy-dependencies

compile o projeto

	mvn compile

executa os testes

	mvn test 

gerar os .jars , muito usado em projetos ear

	mvn package 

limpa todas as dependencies(.jars)

	mvn clean 

procura todos os comandos que vc deu para o maven

	history | grep mvn 

boa prática adotada para gerar o pacote de deploy do projeto

	mvn clean install


## Links úteis

* [Introduction to the Build Lifecycle](http://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)

* [maven em 5 minutos](http://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)

* [iniciando com maven](http://maven.apache.org/guides/getting-started/index.html)

* [Introduction to Archetypes](http://maven.apache.org/guides/introduction/introduction-to-archetypes.html)

* [Archetypes List](http://docs.codehaus.org/display/MAVENUSER/Archetypes+List)

* [repositório do Maven](http://mvnrepository.com/)
