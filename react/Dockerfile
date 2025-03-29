# Use an official Node.js image as a base
FROM node:14-slim

# Set the working directory to /app
WORKDIR /app

# Copy the package*.json files
COPY package*.json ./

# Install the dependencies
RUN npm install eslint@latest --save-dev

# Copy the application code
COPY . .

# Expose the port
EXPOSE 3000

# Run the command to start the development server
CMD ["npm", "start"]
