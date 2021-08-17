#Initial name cesarmirandarod/maven-chrome:3.8.1-92
FROM docker.registry.vptech.eu/maven:3.8.1-jdk-8

RUN apt-get update && \
    apt-get -y install libglib2.0-dev libnss3-tools libxcb-randr0-dev libxcb-xtest0-dev libxcb-xinerama0-dev libxcb-shape0-dev libxcb-xkb-dev

#Check versions from here: https://www.ubuntuupdates.org/package/google_chrome/stable/main/base/google-chrome-stable
ARG CHROME_VERSION="92.0.4515.159-1"
#replace the value with the desired version
RUN wget https://dl.google.com/linux/chrome/deb/pool/main/g/google-chrome-stable/google-chrome-stable_${CHROME_VERSION}_amd64.deb
RUN apt install -y ./google-chrome*.deb \
    &&  apt -y --fix-broken install

CMD ["mvn"]

