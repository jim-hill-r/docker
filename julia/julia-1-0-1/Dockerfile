# Use an official Python runtime as a parent image
FROM ubuntu:16.04

# Set working directory to julia
WORKDIR /julia

# Install any needed packages specified in requirements.txt
RUN apt-get update
RUN apt-get --yes install wget
RUN apt-get --yes install zip unzip build-essential

# Install Julia
RUN wget https://julialang-s3.julialang.org/bin/linux/x64/1.0/julia-1.0.1-linux-x86_64.tar.gz
RUN tar xvf julia-1.0.1-linux-x86_64.tar.gz

# Include Julia in ENV Path
ENV PATH="/julia/julia-1.0.1/bin:${PATH}"

# Run Julia
CMD [ "julia" ]
