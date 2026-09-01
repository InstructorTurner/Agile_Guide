# ⚙️ AdonisJS Guide

## 🚀 Ace Command Cheat Sheet
The `node ace` CLI is the heart of AdonisJS.

| Action | Command | Description |
| :--- | :--- | :--- |
| **Start Server** | `node ace serve --watch` | Run dev server with hot reload |
| **Create Controller** | `node ace make:controller User` | Create a new controller |
| **Create Migration** | `node ace make:migration users` | Create a DB migration file |
| **Run Migration** | `node ace migration:run` | Execute pending migrations |
| **Rollback** | `node ace migration:rollback` | Revert last migration |
| **Create Model** | `node ace make:model User` | Create a Lucid model |

## 💾 Lucid ORM Basics
### Basic Queries
```typescript
// Find by ID
const user = await User.find(1)

// Where clause
const users = await User.query().where('status', 'active').exec()

// Create record
await User.create({ username: 'john_doe', email: 'john@example.com' })

// Update record
const user = await User.find(1)
user.username = 'updated_name'
await user.save()
```

### Relationships
```typescript
// In User model
@hasMany(() => Post)
public posts: HasMany<typeof Post>

// Querying relationship
const user = await User.query().preload('posts').first()
```

## 🛠️ Configuration
*   **Env Variables:** Managed in `.env` file.
*   **Config Files:** Located in `/config` directory.
*   **Routes:** Defined in `start/routes.ts`.
