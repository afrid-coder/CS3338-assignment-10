# Step 1: Use a Node.js base image. Choose the version that's appropriate for React.
# As with the backend, use a minimal version like alpine to reduce the image size.
FROM node:18-alpine

# Step 2: Set the working directory inside the container.
# Use a folder name that matches the frontend code’s structure.
WORKDIR /app

# Step 3: Copy package.json and package-lock.json (if present) first to install dependencies.
COPY package*.json ./

# Step 4: Install the npm dependencies.
RUN npm install

# Step 5: Copy the rest of your frontend code into the container.
COPY . .

# Step 6: Expose the port for the React app to run on.
EXPOSE 3000

# Step 7: Set the command to start your React app.
CMD ["npm", "start"]
