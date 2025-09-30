```python
import socket
import json

def sendData(sock, payload):
  payload_bytes = (json.dumps(payload) + '\n').encode('utf-8')
  sock.sendall(payload_bytes)
  print(f"Sent: {payload_bytes}")


def main():
    host = '127.0.0.1'  # or replace with your server's IP
    port = 3111

    with socket.create_connection((host, port)) as sock:
        # Send device ready event
        sendData(sock, {
          "type": "device",
          "status": "ready"          
        })
        
        # Send shot data event
        sendData(sock, {
          "type": "shot",
          "shot": {
            "ballSpeed": 135.0,
            "verticalLaunchAngle": 11.1,
            "horizontalLaunchAngle": 1.2,
            "spinAxis": -2.5,
            "spinSpeed": 4800
          }
        })

        buffer = ''
        while True:
            data = sock.recv(4096)
            if not data:
                break
            buffer += data.decode('utf-8')

            # Handle multiple messages (delimited by '\n')
            while '\n' in buffer:
                msg, buffer = buffer.split('\n', 1)
                if msg.strip():
                    try:
                        json_msg = json.loads(msg)
                        print(f"Received JSON: {msg}")
                    except json.JSONDecodeError:
                        print(f"Received non-JSON: {msg}")

if __name__ == "__main__":
    main()
```