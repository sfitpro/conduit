# My configuration files for Conduit App

This repo includes my configuration files for [Conduit app](https://github.com/gothinkster/realworld).

## Instruction

1. Install [docker](https://docs.docker.com/engine/install/) and [docker-compose](https://docs.docker.com/compose/install/)
2. Create a "conduit" directory
3. Clone the following repos
   - [Frontend repo](https://github.com/gothinkster/react-redux-realworld-example-app.git) to conduit/frontend
   - [Backend repo](https://github.com/gothinkster/node-express-realworld-example-app.git) to conduit/backend
   - [This repo](https://github.com/sfitpro/conduit.git) to conduit/myconfig
4. `cd conduit`
5. `mv myconfig/nginx .`
6. `cp myconfig/frontend/Dockerfile ./frontend/`
7. `cp myconfig/backend/Dockerfile ./backend`
8. `vi frondend/src/agent.js` update API_ROOT with your Docker host IP or DNS name
9. `vi backend/app.js` add `isProduction = true` after line `var isProduction = process.env.NODE_ENV === 'production';`
10. `docker-compose build`
11. `docker-compose up -d`
12. Access via `http://<your-dockerhost-ip>`
