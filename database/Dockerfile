# Start from the common base image
FROM boost-base as database-service

# Install PostgreSQL development headers
RUN apt-get update && apt-get install -y libpq-dev

# Copy the C++ source code
COPY . /usr/src/service-app

# Set the working directory
WORKDIR /usr/src/service-app

# Build the application
RUN cmake . && make

# Command to run the application
CMD ["./service"]

