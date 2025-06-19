Clone the Repo
git clone 
cd Scaleable-WebSocket
✅ 2. Install Yarn (if you don’t already have it)

npm install -g yarn
✅ 3. Install Dependencies
From the root of the project:
yarn install
This installs all dependencies for all apps/ and packages/ using Yarn workspaces.

✅ 4. Configure .env Files
create env file and paste it in apps/server folde


now type  yarn add next react react-dom for next js in root

next navigate terminal to apps/server

yarn add ioredis for apps/server
yarn add kafkajs for apps/server
yarn add prisma 
yarn add typsript or tsc (if it gives any typescript error log)

example package.json file for apps/server

{
  "name": "server",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "start": "node dist/index",
    "build": "tsc -p .",
    "dev": "tsc-watch --onSuccess \"node dist/index.js\""
  },
  "devDependencies": {
    "@types/node": "^20.10.4",
    "prisma": "^5.7.0",
    "ts-node": "^10.9.2",
    "tsc-watch": "^6.0.4",
    "typescript": "^5.3.3"
  },
  "dependencies": {
    "@prisma/client": "5.7.0",
    "ioredis": "^5.6.1",
    "kafkajs": "^2.2.4",
    "socket.io": "^4.8.1"
  }
}

paste socket.ts file in apps/server/src/services
add host username urls to kafka and redis files
for some reason kakfa one was push as it replace its credentials with yours 
got to kafka on aiven
bottom left -> service settings -> advanced configuration -> sasl connection select, to get username and password go back to its service 
yarn dev to run
