# Start from the official Python base image
FROM python:3.12

# Set the current working directory to /code 
#This is where the dependencies.txt file and the app directory will be.
WORKDIR /code

# Copy the file with the dependencies to the /code directory.
# Copy only the file with the dependencies first, not the rest of the code.
# As this file doesn't change often, Docker will detect it and use the cache
# for this step, enabling the cache for the next step too.
COPY ./dependencies.txt /code/dependencies.txt

# Install the package dependencies in the dependencies file.
# The --no-cache-dir option tells pip to not save the downloaded packages locally, 
# as that is only if pip was going to be run again to install the same packages,
# but that's not the case when working with containers.
# The --upgrade option tells pip to upgrade the packages if they are already installed.
# Because the previous step copying the file could be detected by the Docker
# cache, this step will also use the Docker cache when available.
# Using the cache in this step will save a lot of time when building the
# image again and again during development, instead of downloading and
# installing all the dependencies every time.
RUN pip install --no-cache-dir --upgrade -r /code/dependencies.txt

# Copy the ./app directory inside the /code directory.
# Docker cache won't be used for this or any following steps easily.
# So, it's important to put this near the end of the Dockerfile,
# to optimize the container image build times.
COPY ./app /code/app

# CMD takes a list of strings.
# This command will be run from the current working directory.
EXPOSE 3001
CMD ["uvicorn", "app.main:app", "--host", " 0.0.0.0", "--port", "3001"]