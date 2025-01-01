```
flog-activity-service/
├── cmd/
│   └── main.go                        # Entry point for the service (initializes and runs the app)
├── config/
│   └── config.go                      # Configuration management (e.g., DB, API keys, etc.)
├── db/
│   └── migrations/                    # SQL migration files for setting up DB schema
│       ├── 000001_init_activities.up.sql
│       ├── 000001_init_activities.down.sql
├── internal/
│   ├── activity/                      # Activity service domain logic (model, handlers, etc.)
│   │   ├── domain/                    # Domain layer (business entities)
│   │   │   └── activity.go            # Activity entity definition (model)
│   │   ├── handler/                   # HTTP request handlers (controllers)
│   │   │   └── activity_handler.go    # Handlers for activity-related endpoints (create, get, etc.)
│   │   ├── repository/                # Data access layer (DB interaction)
│   │   │   └── activity_repository.go # Activity repository for CRUD operations
│   │   ├── service/                   # Business logic layer (core functionality)
│   │   │   └── activity_service.go    # Activity service for managing activity-related actions
│   │   └── routes.go                  # Routes for activity service API (e.g., POST, GET /activities)
├── pkg/
│   └── response/                      # Standardized API response format
│       └── response.go                # Helper functions for consistent responses
├── Dockerfile                         # Dockerfile for building the container image
├── go.mod                             # Go module dependencies
├── go.sum                             # Go module checksum file
├── README.md                          # Project documentation
└── .env                                # Environment variables (e.g., DB credentials, secret keys)
```
