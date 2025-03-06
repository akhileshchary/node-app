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
