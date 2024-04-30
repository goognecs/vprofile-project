FROM nginx
LABEL "Project" = "Vprofile"
LABEL "Author" = "Necs"
RUN rm -rf /etc/nginx/config.d/default.conf
ADD nginvproapp.conf /etc/nginx/config.d/nginvproapp.conf
#CREATE your nginvproapp.conf FILE by putting your port, and domain url where users can access. 
EXPOSE 80
