# Mini Message Board

A simple message board built with Node.js, Express, and EJS. Users can read posted messages, add a new one through a form, and open any message to see its full details.

This project was built as part of **The Odin Project** Node.js certification (Node.js path).

## Features

- View all messages on the home page (author, text, and date added)
- Post a new message through a form
- Open a dedicated page for each message
- Server-side rendering with EJS templates
- Basic input validation and a 404 page

## Tech Stack

- Node.js
- Express
- EJS

## Project Structure

```
mini-message-board/
├── app.js
├── routes/
│   └── indexRouter.js
├── views/
│   ├── index.ejs
│   ├── form.ejs
│   └── message.ejs
├── .gitignore
└── package.json
```

## Routes

| Method | Route          | Description                    |
| ------ | -------------- | ------------------------------ |
| GET    | `/`            | List all messages              |
| GET    | `/new`         | Show the new message form      |
| POST   | `/new`         | Add a message and redirect `/` |
| GET    | `/message/:id` | Show details of one message    |

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or newer recommended)
- npm

### Installation

```bash
git clone https://github.com/YOUR-USERNAME/mini-message-board.git
cd mini-message-board
npm install
```

### Run the app

```bash
node app.js
```

Or, with automatic restarts on file changes:

```bash
node --watch app.js
```

Then open `http://localhost:3000` in your browser.

## Notes

- Messages are stored in an in-memory array, so they reset whenever the server restarts. A database is not used in this project.
- Output in the templates is escaped with `<%= %>` to prevent HTML injection.

## Acknowledgements

Project assignment from [The Odin Project](https://www.theodinproject.com/lessons/node-path-nodejs-mini-message-board).

## Author

Junaid Kanwar
