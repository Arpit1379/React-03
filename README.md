Socket.io 
Polling :- checking the server again and again if there are any message or update as it is overkilling 
WebSocket :- bi dIRECTION Communication protocal (full Duplex Communcation)
how its work :- Simply send http request and in header upgrade it to web socket 

io server created on backend
socket.emit :- send the message to all
socket.broadcast;_ send message to except the user and send to all other user
socket.io() to connect 

import http from 'https';
import express from 'express';
import {Server} from 'socket.io";
const app=express();
const server=http.createServer(app);

const io=Server(server);
io.on("connnection",(socket){
socket.on("user-message",(message)=>{
io.emit("message",(message);)}
)})
server.listen(3000,()=>{});

const socket=io();
socket.on("message",message=>{console.log(message);})
socket.emit(message);
