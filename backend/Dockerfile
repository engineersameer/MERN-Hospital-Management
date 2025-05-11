FROM node:18

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json first for npm install to leverage Docker cache
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the app files into the container
COPY . .

# Expose the port the app will run on
EXPOSE 3000

# Use npm start to run the app
CMD ["npm", "start"]
