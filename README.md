# Workshop W6 — Maven vs Gradle (TMS 2026/1)

Este repositório faz parte do Workshop W6 da disciplina TMS. A turma está dividida em dois times: um usando **Maven** e outro usando **Gradle**. O objetivo é realizar as 3 etapas abaixo e comparar o fluxo de cada ferramenta.

## Pré-requisitos

Verifique se você tem tudo instalado antes de começar:

```bash
java -version   # precisa ser Java 17
mvn -version
gradle -version
git --version
```

## Etapa 1 — Clonar e rodar o build inicial

```bash
git clone https://github.com/ViniciussSartori/workshop-maven-gradle.git

# Time Maven:
cd workshop-maven-gradle/projeto-maven && mvn package

# Time Gradle:
cd workshop-maven-gradle/projeto-gradle && gradle build
```

## Etapa 2 — Adicionar a dependência `org.json` e descomentar o código

**Maven** — adicione dentro de `<dependencies>` no `pom.xml`:

```xml
<dependency>
  <groupId>org.json</groupId>
  <artifactId>json</artifactId>
  <version>20240303</version>
</dependency>
```

**Gradle** — adicione dentro de `dependencies { }` no `build.gradle`:

```groovy
implementation 'org.json:json:20240303'
```

Depois, abra o `App.java` e descomente o import e o bloco marcados com `ETAPA 2`. Rode o build novamente.

## Etapa 3 — Executar o `.jar`

```bash
# Time Maven:
java -jar target/workshop-demo-1.0.jar

# Time Gradle:
java -jar build/libs/workshop-demo-1.0.jar
```

Saída esperada: o banner + o JSON impresso na tela.

## Entrega

Envie um print do build com sucesso + o link do **seu** repositório com a dependência adicionada.
