# Use an official Node.js runtime as a parent image
FROM node:14-alpine

# Set the working directory to /app
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the rest of the application files to the container
COPY . .

# Set environment variables for the app
ENV PORT=5000
ENV MONGODB_URI="mongodb://mongo:27017/mydatabase"

# Expose the port the app will listen on
EXPOSE 5000

# Start the app
CMD ["npm", "start"]
