# Use official Node.js LTS Alpine image (no space after "node")
FROM node:lts-alpine

# Set working directory inside the container
WORKDIR /app

# Copy all local files to /app in the container
COPY . .

# Install dependencies listed in package.json
RUN npm install

# Expose port 3000 to the host machine
EXPOSE 3000

# Start the app when the container runs
CMD ["node", "index.js"]

