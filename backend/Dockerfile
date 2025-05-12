# filepath: /Users/guilherme/code/YaroslavPedrovic/hiring_test/backend/Dockerfile
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application
COPY . .

# Expose the backend port
EXPOSE 5000

# Start the backend server
CMD ["npm", "start"]