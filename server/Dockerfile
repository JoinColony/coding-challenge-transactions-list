FROM node:16-alpine

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json before other files
# Utilize Docker cache to save re-installing dependencies if unchanged
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all files
COPY . .

# The default port the app will run at
EXPOSE 4000

# Command to run the app
CMD [ "npx", "nodemon" ]
