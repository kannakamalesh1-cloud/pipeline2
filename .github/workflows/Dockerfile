# Use official Node image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package files first (better caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy remaining project files
COPY . .

# Build app (ignore if not needed)
RUN npm run build || true

# Expose application port
EXPOSE 3000

# Start application
CMD ["npm", "start"]
