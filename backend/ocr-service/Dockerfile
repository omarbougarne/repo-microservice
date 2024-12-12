# Base image
FROM node:18

# Set working directory
WORKDIR /usr/src/app

# Copy package.json and pnpm-lock.yaml
COPY package.json pnpm-lock.yaml ./

# Install pnpm
RUN npm install -g pnpm

# Install dependencies using pnpm
RUN pnpm install --frozen-lockfile

# Copy application code
COPY . .

# Expose application port
EXPOSE 3001

# Start the application
CMD ["pnpm", "start"]
