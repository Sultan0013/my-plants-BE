# My Plants — Backend API

A RESTful API for a plant care mobile app. Users can identify plants, build a personal collection, track watering schedules, and earn rewards for keeping their plants alive.

Built with **Node.js**, **Express**, and **MongoDB**.

---

## 🔗 Links

- **Demo:** [northcoders.com/project-phase/my-plants-app](https://northcoders.com/project-phase/my-plants-app)
- **Frontend Repo:** [github.com/AOYousufi/my-plants-FE](https://github.com/AOYousufi/my-plants-FE)

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Runtime | Node.js |
| Framework | Express.js |
| Database | MongoDB |
| ODM | Mongoose |
| Testing | Jest + Supertest |

---

## 📡 API Endpoints

### Auth & Users

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/register` | Register a new user |
| POST | `/api/login` | Login with username & password |
| GET | `/api/users/:username` | Get user profile |
| PATCH | `/api/users/:username/rewards` | Update reward count |

### Plants

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/users/:username/plants` | Get all plants for a user |
| POST | `/api/users/:username/plants` | Add a plant to collection |
| GET | `/api/users/:username/plants/:plant_id` | Get a specific plant |
| PATCH | `/api/users/:username/plants/:plant_id` | Update plant nickname |
| PATCH | `/api/users/:username/plants/:plant_id/water` | Log a watering event |
| PATCH | `/api/users/:username/plants/:plant_id/dead` | Move plant to graveyard |
| DELETE | `/api/users/:username/plants/:plant_id` | Delete a plant |

### Graveyard

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/users/:username/plants_graveyard` | Get all deceased plants |

---

## ⚙️ Local Setup

### 1. Clone the repo

```bash
# HTTPS
git clone https://github.com/odonnellrory/my-plants-BE.git

# SSH
git clone git@github.com:odonnellrory/my-plants-BE.git

cd my-plants-BE
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create environment file

Create a `.env` file at the project root:

```
MONGODB_URI=your_mongodb_connection_string
PORT=9090
```

> This file is gitignored — never commit it.

### 4. Run the server

```bash
npm start
```

---

## 🧪 Testing

Integration tests cover all endpoints and error cases using **Jest** and **Supertest**.

```bash
# Run all tests
npm test

# Run a specific file
npm test test.js
```

### Error handling coverage

| Code | Meaning |
|---|---|
| 400 | Invalid request / bad input |
| 401 | Missing or invalid authentication |
| 404 | Resource not found |
| 409 | Conflict — resource already exists |
| 500 | Internal server error |

---

## Requirements

- Node.js `v18+`
- MongoDB `v6+` (local or Atlas)

---

*Built as a group project during the Northcoders Digital Skills Bootcamp in Software Engineering.*
