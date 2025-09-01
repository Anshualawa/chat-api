# chat-api
A lightweight and scalable API for real-time chat, providing endpoints for managing users, messages, and conversations.

### Project structure
```
chat-api/
│── cmd/                     # Entry points for the application
│   └── server/              # Main server app
│       └── main.go
│
│── configs/                 # Configuration files (YAML, JSON, ENV)
│   └── config.yaml
│
│── internal/                # Private application code
│   ├── api/                 # HTTP handlers and routes
│   │   ├── handlers/        # Request handlers
│   │   │   ├── user.go
│   │   │   ├── message.go
│   │   │   └── auth.go
│   │   └── routes.go
│   │
│   ├── services/            # Business logic
│   │   ├── user_service.go
│   │   ├── message_service.go
│   │   └── auth_service.go
│   │
│   ├── models/              # Data models (structs)
│   │   ├── user.go
│   │   ├── message.go
│   │   └── conversation.go
│   │
│   ├── repository/          # Database interactions
│   │   ├── user_repo.go
│   │   ├── message_repo.go
│   │   └── conversation_repo.go
│   │
│   ├── db/                  # Database setup & migrations
│   │   ├── migrations/
│   │   └── db.go
│   │
│   └── websocket/           # Real-time communication layer
│       ├── hub.go
│       ├── client.go
│       └── manager.go
│
│── pkg/                     # Shared utilities (helpers, middleware, logger)
│   ├── logger/
│   ├── middleware/
│   └── utils/
│
│── test/                    # Integration & unit tests
│   ├── user_test.go
│   ├── message_test.go
│   └── auth_test.go
│
│── .env                     # Environment variables
│── go.mod
│── go.sum
│── README.md
```
### Key Points :
- cmd/ → main entry point (you can later add CLI tools here too).

- internal/ → your core app logic (kept private to avoid misuse).

- pkg/ → reusable utility packages (can be shared).

- repository/ → keeps DB logic separate from business logic.

- websocket/ → for managing real-time chat connections.

- configs/ → all configuration files in one place.