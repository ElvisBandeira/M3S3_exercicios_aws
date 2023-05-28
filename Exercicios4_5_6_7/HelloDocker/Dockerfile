#base da imagem
FROM openjdk:11

#diretório de trabalho
WORKDIR /app

#copia tudo para a area onde esta o trabalho
COPY . /app/

#executa outros programas na build do programa java
RUN javac HelloDocker.java

#entrada do conteiner
ENTRYPOINT ["java", "HelloDocker"]
