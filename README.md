apt update 
apt upgrade
termux-setup-storage
pkg install root-repo
pkg install nodejs
pkg install openssl
pkg install openssl-tool

nano server.js 

const https = require('https');
const fs = require('fs');
const path = require('path');

// Caminho para os arquivos de certificado e chave
const options = {
    key: fs.readFileSync(path.join(__dirname, 'server.key')),
    cert: fs.readFileSync(path.join(__dirname, 'server.crt'))
};

// Criar o servidor HTTPS
const server = https.createServer(options, (req, res) => {
    res.writeHead(200);
    res.end('Olá, você está conectado ao servidor HTTPS!');
});

// Escutar na porta 4443
server.listen(4443, () => {
    console.log('Servidor rodando em https://0.0.0.0:4443');
});

node server.js


ifconfig

https://(coloca o ip ). (a porta que esta rondando)
exemplo: https://19.168.23.2500:443
