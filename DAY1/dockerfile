# Use an existing Docker image as a base
FROM node:14-alpine
# FROM node:14-alpine: This line specifies the base image to use for the container. In this case, it's a lightweight Alpine Linux-based image with Node.js version 14 installed.

# Set the working directory inside the container
WORKDIR /app
#WORKDIR /app: Sets the working directory inside the container where subsequent commands will be executed.

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./
#COPY package*.json ./: Copies package.json and package-lock.json from the host machine to the working directory inside the container.

# Install dependencies
RUN npm install
#RUN npm install: Runs the npm install command inside the container to install dependencies specified in package.json.

# Copy the rest of the application files to the working directory
COPY . .
#COPY . .: Copies the rest of the application files from the host machine to the working directory inside the container.

# Expose port 3000 to the outside world
EXPOSE 3000
#EXPOSE 3000: Exposes port 3000 on the container to allow communication with the outside world.

# Command to run the application when the container starts
CMD ["node", "index.js"]
#CMD ["node", "index.js"]: Specifies the command to run when the container starts. In this case, it runs the Node.js application file index.js using the Node.js runtime.
