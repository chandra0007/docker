
FROM ubuntu

ARG DEF_PATH="/usr/share/nginx/html"

ENV H_NAME="nginx"


RUN 	apt-get update -y &&\
	apt-get install nginx -y &&\
	apt-get install net-tools -y &&\
	service nginx start &&\
	useradd -ms /bin/bash chandan &&\
	mv $DEF_PATH/index.html $DEF_PATH/text.html
		#RUN apt-get install curl -y

#RUN chown -R chandan:chandan $DEF_PATH &&\
#	mv index.html text.html
#RUN sudo usermod -aG sudo chandan &&\
#RUN mv $DEF_PATH/index.html $DEF_PATH/text.html

WORKDIR $DEF_PATH/ 

#RUN mv index.html text.html
#RUN mv /usr/share/nginx/html/index.html /usr/share/nginx/html/text.html
#RUN echo "<h1>New Nginx</h1>" > /usr/share/nginx/html/index.html

COPY index.html . 

EXPOSE 80

#USER chandan
        #RUN usermod -aG docker chandan && usermod -aG wheel chandan

WORKDIR /home/chandan

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
