# Estudo de modularização no Java

**Antes de rodar a módulo precisamos o compilar**

## Compilando um módulo

```sh
javac --module-path mods -d feeding java/zoo/animal/feeding/*.java java/module-info.java
```

## Rodando um módulo

```sh
java --module-path feeding --module zoo.animal.feeding/zoo.animal.feeding.Task
```
ou
```sh
java -p feeding -m zoo.animal.feeding/zoo.animal.feeding.Task
```

## Empacotando o módulo

**Criar a pasta mods e depois executar o comando**

```sh
jar -cvf mods/zoo.animal.feeding.jar -C feeding/ .
```

## Executando o jar criado

```sh
java -p mods -m zoo.animal.feeding/zoo.animal.feeding.Task
```