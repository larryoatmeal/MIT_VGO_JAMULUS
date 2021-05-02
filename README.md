# MIT_VGO_JAMULUS




# Starting/Stopping Servers
- ssh into DO droplet
- `cd` into `MIT_VGO_JAMULUS` folder
- To start servers: `sudo docker-compose up -d`
- To stop servers: `sudo docker-compose down`


# Starting/Stopping Recording
- `ps aux | fgrep Jamulus | fgrep -v grep` to list running Jamulus instances
- Copy the pid of the room you want to control (2nd column) 
- `sudo kill -s SIGUSR2 {THE PID}` (without the curly braces) toggles recording on and off
- You can verify recording has started by checking the corresonding `room1`, `room2`, or `room3` directory
