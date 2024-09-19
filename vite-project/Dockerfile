# Use the latest Node.js Alpine version
ARG NODE_VERSION=22.5.1
FROM node:${NODE_VERSION}-alpine

# Set the environment to development
ENV NODE_ENV development

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies, including devDependencies (which includes Vite)
RUN npm install

# Copy the rest of the source files into the image
COPY . .

# Expose the Vite default port
EXPOSE 5173

# Run the application
CMD ["npm", "run", "dev"]
