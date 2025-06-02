# Use official Node.js LTS Alpine image (no space after "node")
#Stage 1
FROM node:18-alpine AS backend-builder

# Set working directory inside the container
WORKDIR /app

# Copy all local files to /app in the container
COPY . .

# Install dependencies listed in package.json
RUN npm install
#Stage 2
FROM node:18-alpine
#set up working dir
WORKDIR /app
COPY --from=backend-builder /app .
# Expose port 3000 to the host machine
EXPOSE 3000

# Start the app when the container runs
CMD ["node", "index.js"]

