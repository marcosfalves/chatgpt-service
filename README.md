# fullcyclelx
Projeto de integração com chatGPT desenvolvido durante o evento FullCycle Learning Experience

# Executar local
- Instalar golang-migrate: https://github.com/golang-migrate/migrate
    ```sh
    curl -L https://packagecloud.io/golang-migrate/migrate/gpgkey | apt-key add -
    echo "deb https://packagecloud.io/golang-migrate/migrate/ubuntu/ focal main" > /etc/apt/sources.list.d/migrate.list
    apt-get update
    apt-get install -y migrate
    ```
- Duplicar `.env.example` para `.env`
- Editar `.env` e informar token da openAI em OPENAI_API_KEY
- Subir microserviço em go:
  - ```sh
    docker compose up -d
    ```
  - ```sh
    make migrate 
    ```
    Obs: Somente na primeira execução

  - ```sh
    docker exec -it chatservice_app bash
    ```
  - ```sh
    go run cmd/chatservice/main.go
    ```