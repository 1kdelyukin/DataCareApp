# Use Node.js official image
FROM node:18

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy rest of the app code
COPY . .

# Expose port (match your Express server)
EXPOSE 8080

# Start your app
CMD ["node", "server.js"]
