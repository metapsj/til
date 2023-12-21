# notes

### jupyter server documentation for developers

These pages target people writing Jupyter Web applications and server
extensions, or people who need to dive deeper in Jupyter Server’s REST API
and configuration system.

- architecture diagrams
- depending on jupyter server
- the rest api
- server extensions
- file save hooks
- contents api
- websocket kernel wire protocols
- api docs

https://jupyter-server.readthedocs.io/en/latest/developers/index.html

### architecture diagrams

This page describes the Jupyter Server architecture and the main workflows.
This information is useful for developers who want to understand how Jupyter
Server components are connected and how the principal workflows look like.

https://jupyter-server.readthedocs.io/en/latest/developers/architecture.html

### websocket kernel wire protocols

The Jupyter Server needs to pass messages between kernels and the Jupyter web
application. Kernels use ZeroMQ sockets, and the web application uses a WebSocket.

https://jupyter-server.readthedocs.io/en/latest/developers/websocket-protocols.html
