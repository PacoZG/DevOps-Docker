# Start from the alpine image
FROM ubuntu:20.04

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.
WORKDIR /usr/src/app

# Copy the hello.sh file from this location to /usr/src/app/ creating /usr/src/app/hello.sh.
COPY script.txt .

# Install curl inside the image
RUN apt-get update
RUN apt-get install -y curl

# make sure file has required permissions
RUN chmod +x script.txt

# When running docker run the command will be ./script.txt
CMD ./script.txt