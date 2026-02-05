# Multiplayer Collaborative Role-Playing Game

![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)

This project is a multiplayer collaborative role-playing game designed as part of an **Operating Systems** course at UNS. In this project, each student had to develop their own client to control their player, while the server process representing the "monster" was handled by the professor. The goal was to learn about process synchronization using shared memory and semaphores.

## Game Description

The game is a text-based, turn-based collaborative combat between players and a monster. Players can choose between different types of attacks (sword, mace, arrow) and must manage their health and energy to defeat the monster. Synchronization between clients (players) and the server (monster) is achieved through shared memory and semaphores.

### Key Features

- **Attacks**: The player can attack the monster with a sword, a mace, or an arrow.
- **Resource Management**: Player health and energy are managed during gameplay.
- **Synchronization**: Use of semaphores and shared memory to coordinate resource access between the player and the monster.

## Requirements

- **Operating System**: Compatible with UNIX-based systems (Linux/macOS).
- **Compiler**: GCC (GNU Compiler Collection).
- **CMake**: To configure the project.

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/lagosmanuel/os-rpg.git]
   cd os-rpg
   ```

2. **Configure the Project with CMake**

   Create a build directory and configure the project:

   ```bash
   mkdir build
   cd build
   cmake ..
   ```

3. **Compile the Code**

   Once configured with CMake, compile the code using `make`:

   ```bash
   make
   ```

   This will generate the executable `juego-rol.bin` in the project's main directory:
   
   ```bash
   cd ..
   ```

## Execution

1. **Start the Server**

   The server represents the "monster" controlled by the professor. It must be executed first:

   ```bash
   ./server-local.bin
   ```

2. **Start the Client**

   Each student must run their own client to control their player. Ensure the server is running before starting the client:

   ```bash
   ./juego-rol.bin
   ```

   Clients will connect to the server, and the game will begin.

## Usage

- **Client Menu**: Upon running the client, a menu will appear with options to attack the monster or exit the game.
- **Options**:
  - `1`: Attack with sword.
  - `2`: Attack with mace.
  - `3`: Attack with arrow.
  - `4`: Exit game.

- **Messages**: Messages regarding the game status and attack results will be displayed in the console.

## Process Synchronization

The game uses semaphores and shared memory to synchronize access between the client and the server. The following are used:

- **Shared Memory**: To store the game state, such as the health and energy of both the player and the monster.
- **Semaphores**: To coordinate access to shared memory and avoid conflicts between the client and the server.

## Screenshots

Here are some screenshots of the game:

1. **Client Main Menu**
   ![Client Main Menu](screenshots/screenshot1.png)

2. **Server Main Menu**
   ![Game State During Combat](screenshots/screenshot2.png)

3. **Client Victory Screen**
   ![Victory Screen](screenshots/screenshot3.png)

3. **Client Defeat Screen**
   ![Defeat Screen](screenshots/screenshot4.png)

## Contributions

This project is part of an academic exercise; however, additional contributions are welcome.

## License

This project is licensed under the [GNU General Public License (GPL)](https://www.gnu.org/licenses/gpl-3.0.html). See the [LICENSE](LICENSE) file for more details.
