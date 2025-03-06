// server.js - Main Node.js server file

const express = require('express');
const app = express();
const PORT = process.env.PORT || 3000;

// Middleware to serve static files
app.use(express.static('public'));

// Default route
app.get('/', (req, res) => {
    res.send('🚀 Hello from Node.js running on Arch Linux!');
});

// Start the server
app.listen(PORT, () => {
    console.log(`Server is running on http://localhost:${PORT}`);
});

// package.json - Project metadata and dependencies
const packageJson = `{
  "name": "node-app",
  "version": "1.0.0",
  "description": "A simple Node.js application",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "express": "^4.18.2"
  }
}`;

// .gitignore - Ignoring unnecessary files
const gitignore = `node_modules/
.env
`; 

// README.md - Basic project documentation
const readme = `# Node.js Application

## Overview
This is a simple Node.js application using Express.js. It serves static files and runs a basic web server.

## Installation
1. Clone the repository:
   \`\`\`
git clone https://github.com/akhileshchary/node-app.git
   \`\`\`
2. Navigate to the project directory:
   \`\`\`
cd node-app
   \`\`\`
3. Install dependencies:
   \`\`\`
npm install
   \`\`\`

## Usage
To start the server, run:
\`\`\`
npm start
\`\`\`

Then open [http://localhost:3000](http://localhost:3000) in your browser.

## Features
- Simple Express.js server
- Serves static files
- Runs on Arch Linux

## License
MIT
`;

module.exports = { packageJson, gitignore, readme };
