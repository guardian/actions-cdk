FROM node:23-alpine

WORKDIR /cdk

# Install Dependencies
COPY package.json ./
COPY package-lock.json ./
RUN npm install --frozen-lockfile

# Copy CDK files
COPY cdk.ts ./
COPY cdk.json ./
COPY tsconfig.json ./
COPY jest.setup.js ./

ENTRYPOINT [ "npm", "run" ]