# Use the official Node.js image.
FROM node:14

# Create and change to the app directory.
WORKDIR /app

# Copy application dependency manifests to the container image.
COPY app2/package*.json ./
#COPY app2/.npmrc ./

# Install dependencies.
RUN npm install --force

# Copy local code to the container image.
COPY app2/ .

# Set environment variables
ENV MY_GITHUB_TOKEN=${MY_GITHUB_TOKEN}

# Build the React app.
RUN npm run build

# Expose the port the app runs on.
EXPOSE 3001

# Run the web service on container startup.
CMD [ "node", "server2.js" ]
