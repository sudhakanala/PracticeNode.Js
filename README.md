# REST API with Node.js and Express ✅

This is a minimal Node.js REST API using Express. It exposes CRUD endpoints for a simple `todos` resource.

## Features
- GET /api/todos - list todos
- GET /api/todos/:id - get a todo by id
- POST /api/todos - create a todo
- PUT /api/todos/:id - update a todo
- DELETE /api/todos/:id - delete a todo

Data is stored in-memory (no DB). The project includes tests using Jest and SuperTest.

## Setup
1. Install dependencies

```powershell
npm install
```

2. Start in development mode (auto-reloads with nodemon)

```powershell
npm run dev
```

3. Run tests

```powershell
npm test
```

## Files
- `src/index.js` - Express server and route setup
- `src/routes/todos.js` - Todos router
- `src/data/todosData.js` - Simple in-memory store
- `tests/todos.test.js` - Integration tests

## Notes
- The API is designed to be a minimal starting project. To persist data, replace `todosData.js` with a database-backed store.

## Example requests

Create a todo:
```powershell
curl -X POST http://localhost:3000/api/todos -H "Content-Type: application/json" -d '{"title":"Buy milk"}'
```

Get all todos:
```powershell
curl http://localhost:3000/api/todos
```

Update a todo:
```powershell
curl -X PUT http://localhost:3000/api/todos/1 -H "Content-Type: application/json" -d '{"completed":true}'
```

Delete a todo:
```powershell
curl -X DELETE http://localhost:3000/api/todos/1
```
