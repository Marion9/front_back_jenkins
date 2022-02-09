FROM node:16
WORKDIR /front
COPY frontend/package.json /front
RUN npm install
COPY frontend/ /front
EXPOSE 3000
CMD ["npm", "start"]