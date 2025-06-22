FROM node:16.8

# Accept build-time variable
ARG REACT_APP_BACKEND_URL
ENV REACT_APP_BACKEND_URL=$REACT_APP_BACKEND_URL

WORKDIR /frontend-react-js

COPY package*.json ./
RUN npm install

COPY . .

# Inject env into the build (possible fix for data issue)
RUN npm run build

EXPOSE 3000
CMD ["npm", "start"]
