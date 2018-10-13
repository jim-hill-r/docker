# Use an official Python runtime as a parent image
FROM jimhillr/julia:1.0.1

WORKDIR /caesar

ADD . /caesar

# Install packaged needed for most navi applications
RUN apt-get update
RUN apt-get --yes install gcc g++ automake zip make python-dev 
RUN apt-get --yes install hdf5-tools libfontconfig1 gettext libcairo2  libmagickwand-6.q16-2 libpango1.0-0 libglib2.0-dev
RUN apt-get --yes install libqt4-dev libgtk-3-dev
#RUN apt-get --yes install libvtk5-qt4-dev python-vtk libpcre2-8-0

# Install caesar
RUN julia ./caesarInstall.jl

# Run Julia
CMD [ "julia"]
