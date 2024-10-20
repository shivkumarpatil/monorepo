# Use the official Node.js image.
FROM node:14

# Create and change to the app directory.
WORKDIR /app

# Copy application dependency manifests to the container image.
COPY package.json ./
COPY package*.json ./
#COPY .npmrc ./

# Install dependencies.
RUN npm install

# Copy local code to the container image.
COPY . .

# Build the React app.
RUN npm run build

# Expose the port the app runs on.
EXPOSE 3001

# Run the web service on container startup.
CMD [ "node", "server2.js" ]


