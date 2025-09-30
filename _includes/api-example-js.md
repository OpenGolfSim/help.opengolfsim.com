```javascript
const net = require('net');

const PORT = 3111;
const ADDRESS = '127.0.0.1';

const client = new net.Socket();

function sendData(data) {
  client.write(JSON.stringify(data));
}

client.connect(PORT, ADDRESS, () => {
  console.log('Connected to OpenGolfSim!');

  // send device ready
  console.log('Sending device ready event...');
  sendData({
    type: 'device',
    status: 'ready'
  });

  console.log('Sending test shot...');
  // send a shot
  sendData({
    type: 'shot',
    shot: {
      ballSpeed: 135.0, // mph
      verticalLaunchAngle: 11.1, // degrees
      horizontalLaunchAngle: 1.2, // degrees
      spinAxis: -2.5, // degrees, positive = hook/left, negative = slice/right
      spinSpeed: 4800 // ball RPM 
    }
  });

});

client.on('data', (data) => {
  console.log('Received data from OpenGolfSim: ' + data);
});

client.on('close', () => {
  console.log('Connection was closed');
});
```