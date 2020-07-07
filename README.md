# Como rodar

## Você vai pecisar instalar

1. [dotnet](https://dotnet.microsoft.com/download)
2. [docker](https://www.docker.com/get-started)
3. [vs code](https://code.visualstudio.com/)

* Primeiro execute o brocker com o comando

`docker-compose -f ./rabbir-composer.yml up`

* Então inicie o _worker_ em `./work-queues/worker` com o comando

`dotnet run`

```bash
[*] Waiting for messages.
Press [enter] to exit.
```

* Depois rode o _new-task_ em `work-queues\new-task` com o comando

`dotnet run`

```bash
 [x] Sent Hello World!
 Press [enter] to exit.
```

Em seguida irá ser processada a mensagem no _worker_

```bash
[*] Waiting for messages.
Press [enter] to exit.
[x] Received Hello World!
[x] Done
```
