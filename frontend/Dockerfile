# filepath: /Users/guilherme/code/YaroslavPedrovic/hiring_test/frontend/Dockerfile
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install dependencies
RUN npm install

# Rebuild esbuild binary to ensure version compatibility
RUN node node_modules/esbuild/install.js

# Copy the rest of the application
COPY . .

# Expose the frontend port
EXPOSE 5173

# Start the frontend server with host flag to allow external access
CMD ["npm", "run", "start", "--", "--host", "0.0.0.0"]