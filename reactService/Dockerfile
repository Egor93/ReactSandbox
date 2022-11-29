FROM ubuntu:22.04
RUN apt update
# install NODEJS - JavaScript runtime env + npm (node.js packet manager)
RUN apt install -y curl gnupg
RUN curl -sL https://deb.nodesource.com/setup_19.x | bash -
RUN apt -f install -y nodejs 
RUN npm install -g npm@9.1.2
#ENTRYPOINT ["/bin/sh","-c","&"] prevent container from exiting!
WORKDIR /home/react/my-app
EXPOSE 3000
CMD nohup npm start &> /dev/null  && tail -f /dev/null
#CMD npm start && tail -f /dev/null
#ENTRYPOINT ["tail", "-f", "/dev/null"]  
