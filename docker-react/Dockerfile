# pull official base image
FROM node:16.10.0-alpine

# set working directory
WORKDIR /app

# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# install app dependencies
COPY package.json .
RUN yarn install
RUN yarn global add react-scripts
COPY . .

EXPOSE 3000

# start app
CMD ["yarn", "start"]
# ADD ./bootup.sh /app
# RUN cd /app
# RUN chmod +x /app/bootup.sh