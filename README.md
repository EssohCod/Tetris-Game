Welcome to My Tetris
Task
The task is to create a functional Tetris game using only JavaScript, HTML, and CSS without any external libraries, except for Math. The challenge lies in managing the game logic, rendering the game state, and handling user input while adhering to specific guidelines and ensuring smooth gameplay.

Description
The problem is solved by structuring the project into separate files for different concerns: game logic, rendering, and user input. The game logic handles the state of the playfield and the movement of Tetriminos. The renderer draws the game state onto a canvas element, and the controller listens for user inputs to interact with the game. This modular approach ensures maintainability and clarity in the codebase. The game also follows the Tetris guidelines for piece spawning, rotation, scoring, and other gameplay mechanics.

Installation
Clone the repository:

git clone https://github.com/yourusername/tetris-js.git
cd tetris-js
Ensure you have Node.js installed. Then, create a script to serve the HTML file:

cat <<EOL > html_server.js
function start_html_server() {
    const http = require('http');
    const fs = require('fs');

    const hostname = '0.0.0.0';
    const port = 8080;

    const server = http.createServer(function(request, response) {
        response.writeHeader(200, {"Content-Type": "text/html"});
        const html = fs.readFileSync('./index.html', 'utf8');
        response.write(html);
        response.end();
    }).listen(port, hostname, () => {
        console.log("Server running at http://web-XXXXXXXXX.docode.YYYY.qwasar.io");
        console.log("Replace XXXXXXXXX by your current workspace ID");
    });
}

start_html_server();
EOL
Create an initial HTML file to test the server:

echo "Hello world" > index.html
Run the server script:

node html_server.js
Usage
Open your web browser and navigate to the server URL provided by the running server script.

The Tetris game will load in the browser.

Use the following controls to play the game:

Arrow keys: Move Tetrimino left, right, and down.
Up Arrow / X: Rotate Tetrimino 90° clockwise.
Z / Ctrl: Rotate Tetrimino 90° counterclockwise.
Space: Hard drop.
Shift / C: Hold piece.
Esc / F1: Pause the game.
