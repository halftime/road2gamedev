# road2gamedev

## Broad multiplayer game reqs

### Client
* WS connection with server
* Receive personal playerId from server
* Load game sprites
* HUD
    * HP
    * FPS, ...
    * Lobby scoreboard
* Don't crash
* MM to Quick match public lobby
* Limit risk for client side manipulation
  * offload critical tasks to server side
  * verify client data?
      * timestamp & checksum?
* Clients game menus
     * text, size, navigation, ...
* Hotkeys
   * ESC : quit game? verify
   * TAB : display score/...
     



### Server
* Receive WS from clients
* Assign player Id to new client
* Keepalive / ping clients 5s?
  * calc client latency/ping
  * remove disconnected clients
* Fixed server "tick" 30/60/? fps for each player
* Update client changes & broadcast to other players
  * position, ...
      * player collision
      * map walls & dimensions
  * damage, health, ...
       * dismiss input from dead player(s)
       * play dead-scene sprite on all clients (in view of dead player)
* Respawn dead players
   * prevent spawn camping
   * randomized spawns (pref. empty location;  spawnpoints > maxplayers)
* Player comms / chat
* Matchmaking
* ...
* ....
* Player accounts DB
    * login
    * stats
    * ...


![afbeelding](https://github.com/user-attachments/assets/c52cee2c-7cb9-4cdb-a0de-c3b4da97bd90)
