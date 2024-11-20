# Use Node.js as the base image
FROM node:20-alpine

# Set the working directory
WORKDIR /app

# Copy only package files to leverage Docker caching
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the production files
RUN npm run build

# Expose the port for the Vite preview server
EXPOSE 3000

# Use the locally installed Vite binary to start the production server
CMD ["npm", "run", "preview", "--", "--host", "0.0.0.0", "--port", "3000"]
