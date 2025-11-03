# Step 1: Use an official Node.js base image with a specific version.
# Here, we use an Alpine version to keep the image lightweight.
FROM node:18-alpine

# Step 2: Set the working directory inside the container.
WORKDIR /app

# Step 3: Set metadata for the image (optional but good practice).
LABEL maintainer="Your Name <your.email@example.com>" \
      version="1.0" \
      description="Backend service for Assignment 10"

# Step 4: Copy package.json and package-lock.json (if present) first to install dependencies.
COPY package*.json ./

# Step 5: Install npm dependencies.
RUN npm install

# Step 6: Copy the rest of the backend code into the container.
COPY . .

# Step 7: Expose the port the backend application will listen on.
EXPOSE 5000

# Step 8: Create a volume to persist data that is shared with the host machine (optional).
VOLUME [ "/app/data" ]

# Step 9: Specify the default command to run your application when the container starts.
CMD ["npm", "start"]
