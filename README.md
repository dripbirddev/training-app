---

# Application README

This README documents the steps required to get the application up and running.

## Ruby version
- **Ruby**: 3.3.4 (2024-07-09 revision be1089c8ec) +YJIT [arm64-darwin23]
- **Rails**: 7.2.1
- **Rack**: 3.1.7

## System dependencies

Before running the application, ensure you have the following dependencies installed:

- **PostgreSQL**: 16.x
- **Bun**: 1.1.x or later (for managing JavaScript dependencies)
- **Redis**: 7.2 or later (for caching and background jobs)
- **Devbox**: Devbox is used to create isolated development environments.

### Devbox

Devbox is a command-line tool that lets you easily create isolated shells for development. It uses a configuration file to define the list of packages required for your project, and it creates an isolated, reproducible environment with those packages installed.

Make sure you have Devbox installed, and then use the following command to start the isolated environment:

```bash
devbox shell
```

## Configuration


## Database creation

Run the following command to create the database:

```bash
bin/rails db:create
```

## How to run the test suite

1. **RSpec**: To run the unit and integration tests using RSpec:
   ```bash
   bundle exec rspec
   ```

2. **Playwright**: For end-to-end (E2E) testing, use Playwright:
   ```bash
   bun run playwright test
   ```

3. **Code quality**: Check your application for code quality using RuboCop:
   ```bash
   bundle exec rubocop
   ```

## Services (job queues, cache servers, search engines, etc.)

- **Redis**: Redis is used for caching and job processing with ActiveJob. Ensure Redis is running before starting the application:
  ```bash
  redis-server
  ```

- **Background Jobs**: The application uses Sidekiq for background jobs. Start Sidekiq using the following command:
  ```bash
  bundle exec sidekiq
  ```

## Development (Local)

To start the Rails server in the local environment using Devbox, run:

```bash
./bin/dev
```

## Deployment instructions

---
