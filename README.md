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
* limit risk for client side manipulation
  * offload critical tasks to server side
  * verify client data?
      * timestamp & checksum?


### Server
* Receive WS from clients
* Assign player Id to new client
* Keepalive / ping clients 5s?
  * calc client latency/ping
  * remove disconnected clients
* Hardwired server "tick" 30/60/? fps for each player
  * 
* Update client changes & broadcast to other players
  * position, ...
      * player collision
      * map walls & dimensions
  * damage, health, ...
    * gatekeep dead & alive
* Player comms / chat
* Matchmaking
* ...
* Player accounts DB
    * login
    * stats
    * ...
