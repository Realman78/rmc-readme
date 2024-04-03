# RMC: Live Streaming Platform

RMC introduces a straightforward live streaming service where users can share content, and viewers can tune in.

## How It Works

At the heart of RMC is the integration of P2P streaming facilitated by WebRTC, enabling efficient and high-quality content delivery. The use of the VP9 codec is a deliberate choice to ensure that streams are not only smooth but also maintain fidelity, even at lower bandwidths.

### Server-Side Infrastructure

- **Go for Application Management**: The backbone of RMC, my server-side logic, is built with Go.
- **WebSockets for Signaling**: Establishing P2P connections between users is critical for the WebRTC protocol. To manage this, I utilize WebSockets, enabling real-time, bidirectional communication necessary for signaling.
- **TURN Server for Traffic Relaying**: Not all environments permit direct P2P connections due to NAT/firewall restrictions. To circumvent this, I've configured a TURN server on the same machine hosting the Go server, ensuring that all users can connect, regardless of their network environment.

## Future
I'm planning on replacing the streaming engine with my own custom protocol in the (hopefully) near future.