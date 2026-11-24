
# Stage 1: Build React application
FROM node:18 AS build

WORKDIR /app

# Copy dependency files
COPY package.json package-lock.json ./

# Install dependencies
RUN npm ci --legacy-peer-deps

# Copy application source code
COPY . .

# Fix OpenSSL compatibility for React Scripts 4
ENV NODE_OPTIONS=--openssl-legacy-provider

# Create production build
RUN npm run build


# Stage 2: Serve application using Nginx
FROM nginx:alpine

# Copy React production build
COPY --from=build /app/build /usr/share/nginx/html

# Expose Nginx port
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
