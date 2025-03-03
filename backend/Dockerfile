# Use AWS Lambda Node.js 18 runtime base image
FROM public.ecr.aws/lambda/nodejs:18 

# Set the working directory inside the container
WORKDIR /var/task

# Copy package.json and install dependencies (if needed)
COPY package.json package.json
RUN npm install

# Copy the Lambda function code
COPY index.js index.js

# Set the Lambda function handler (index.js exports `handler`)
CMD ["index.handler"]
