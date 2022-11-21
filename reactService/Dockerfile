FROM ubuntu:22.04
RUN apt update
# install NODEJS - JavaScript runtime env + npm (node.js packet manager)
RUN apt install -y curl gnupg
RUN curl -sL https://deb.nodesource.com/setup_19.x | bash -
RUN apt -f install -y nodejs 
RUN npm install -g npm@9.1.2
#ENTRYPOINT ["/bin/sh","-c","&"] prevent container from exiting!
EXPOSE 3000
ENTRYPOINT ["tail", "-f", "/dev/null"]  
