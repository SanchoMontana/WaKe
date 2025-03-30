# Use an official Node.js image as a base
FROM node:latest

# Set the working directory to /app
WORKDIR /app

# Copy the package*.json files
COPY package*.json ./

# Install the dependencies
RUN npm install -g npm@latest

# Copy the application code
COPY . .

# Build the React app
RUN npm run build

# Expose the port
EXPOSE 3000

# Run the command to start the development server
CMD ["npm", "start"]