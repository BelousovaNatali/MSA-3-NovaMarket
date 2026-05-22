FROM node:18-alpine
WORKDIR /app
RUN echo 'const http = require("http"); const os = require("os"); let requestCount = 0; const server = http.createServer((req, res) => { if (req.url === "/") { requestCount++; res.writeHead(200, {"Content-Type": "text/plain"}); res.end(`Pod: ${os.hostname()}\n`); } else if (req.url === "/metrics") { res.writeHead(200, {"Content-Type": "text/plain"}); res.end(`http_requests_total ${requestCount}\n`); } else { res.writeHead(404); res.end(); } }); server.listen(8080);' > server.js
CMD ["node", "server.js"]