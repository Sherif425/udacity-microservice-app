FROM node:12
# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json ./
ENV POSTGRES_USERNAME=postgres
ENV POSTGRES_PASSWORD=postgres
ENV POSTGRES_HOST=postgres.cmxddatlnnw5.us-east-2.rds.amazonaws.com
ENV POSTGRES_DB=postgres
ENV AWS_BUCKET=my-230082686011-bucket
ENV AWS_REGION=us-east-2
ENV AWS_PROFILE=default
ENV JWT_SECRET=testing
ENV URL=http://localhost:8100
RUN npm ci 
# Bundle app source
COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]