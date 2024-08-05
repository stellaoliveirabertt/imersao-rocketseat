# Rocketseat

## Descrição do Projeto

O projeto **Rocketseat** é uma aplicação web construída utilizando Go no backend e React no frontend. A aplicação permite a criação de várias salas onde usuários podem entrar, fazer perguntas e curtir as perguntas dos outros usuários. Toda a comunicação é gerenciada em tempo real utilizando Websockets.

## Funcionalidades

- **Criação de Salas**: Usuários podem criar salas com um nome único, e cada sala recebe um ID exclusivo.
- **Gerenciamento de Perguntas**: Dentro de uma sala, usuários podem enviar perguntas.
- **Curtidas nas Perguntas**: Usuários podem curtir as perguntas enviadas por outros usuários.
- **Comunicação em Tempo Real**: Uso de Websockets para comunicação em tempo real entre o frontend e o backend.

## Tecnologias Utilizadas

- **Backend**:
  - Go
  - Gorilla Websocket
- **Frontend**:
  - React
  - Axios
- **Outras**:
  - Docker (para containerização)
  - Git (para controle de versão)

## Instalação e Configuração

### Pré-requisitos

- Go 1.16 ou superior
- Node.js 14 ou superior
- Docker (opcional, para desenvolvimento com containerização)

### Passos para Configuração

1. **Clone o Repositório**

```bash
git clone https://github.com/seuusuario/star.git
cd star
```

2. **Inicialize o Módulo Go**

```bash
cd backend
go mod init github.com/seuusuario/star
go mod tidy
```

3. **Instale Dependências do Backend**

```bash
go get -u github.com/gorilla/websocket
```

4. **Instale Dependências do Frontend**

```bash
cd ../frontend
npm install
```

5. **Executar o Projeto**

Para iniciar o backend, execute:

```bash
cd backend
go run main.go
```

Para iniciar o frontend, execute:

```bash
cd ../frontend
npm start
```

### Docker

Se você preferir usar Docker, execute os seguintes comandos na raiz do projeto:

```bash
docker-compose up --build
```

## Estrutura do Projeto

```plaintext
.
├── backend
│   ├── main.go
│   ├── models
│   ├── handlers
│   └── websockets
├── frontend
│   ├── public
│   ├── src
│   │   ├── components
│   │   ├── services
│   │   └── App.js
│   └── package.json
├── docker-compose.yml
└── README.md
```

## Contribuindo

1. Faça um fork do projeto
2. Crie uma nova branch (`git checkout -b feature/nova-feature`)
3. Commit suas alterações (`git commit -m 'Adiciona nova feature'`)
4. Faça o push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## Licença

Este projeto está licenciado sob a MIT License - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
