ARG NODE_IMAGE=node:16.0.0-alpine

FROM $NODE_IMAGE AS base
RUN mkdir -p /home/node/app && chown node:node /home/node/app
RUN npm install -g nodemon
WORKDIR /home/node/app
USER node
RUN mkdir tmp

COPY --chown=node:node . ./
COPY --chown=node:node . ./
RUN yarn --pure-lockfile install --ignore-engines
COPY --chown=node:node . .
