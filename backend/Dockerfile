FROM node:16
WORKDIR /back
COPY backend/package.json /back
RUN npm install
COPY backend/ /back
EXPOSE 8083
CMD ["npm", "start"]