# start from linux machine with node 24 installed in it
FROM node:24-alpine 
# defining the working directory in that machine
WORKDIR /app
			
# Copying package.json file to the working directory
COPY package*.json ./
			
# Copying the code and typescript config files to the working directory
COPY ./app ./app
COPY ./public ./public
COPY ./tsconfig.json ./tsconfig.json
COPY ./postcss.config.mjs ./postcss.config.mjs

# map environment variable and build time variable
ARG NEXT_PUBLIC_BACKEND_URL
ENV NEXT_PUBLIC_BACKEND_URL=$NEXT_PUBLIC_BACKEND_URL

# chaining RUN commands to reduce the build image size (multiple RUN commands create additional layers)
# install the dependencies
RUN npm ci \
# building project to create the dist folder containing all the JS Code
&& npm run build \
# Remove all dependencies
&& rm -rf ./node_modules \
# Reinstall only production dependencies
&& npm ci --omit=dev

EXPOSE 4000
CMD ["npm", "start"]
