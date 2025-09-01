#FROM node:latest
#WORKDIR /app

#COPY ./social_networking_app_backend/package*.json ./
#RUN npm install --force

#COPY ./social_networking_app_backend/ ./
#WORKDIR /app/social_networking_app_backend

#EXPOSE 4000

#CMD ["node", "index.js"]
#FROM mongodb/mongodb-community-server:7.0.24-rc0-ubi9
#FROM node:18-slim
#WORKDIR /app
#COPY ./social_networking_app_backend/package*.json ./
#RUN npm install --force
#COPY ./social_networking_app_backend/ ./
#CMD ["node", "index.js"]
#EXPOSE 4000

FROM node:18-slim

WORKDIR /app

# Copy only package.json and package-lock.json first
COPY ./social_networking_app_backend/package*.json ./

# Install dependencies inside the container
RUN npm install --force

# Now copy the rest of the app
COPY ./social_networking_app_backend/ ./

EXPOSE 4000
CMD ["node", "index.js"]