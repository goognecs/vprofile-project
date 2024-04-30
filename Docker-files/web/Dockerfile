FROM nginx
LABEL "Project" = "Vprofile"
LABEL "Author" = "Necs"
RUN rm -rf /etc/nginx/conf.d/default.conf
ADD nginvproapp.conf /etc/nginx/conf.d/nginvproapp.conf
#CREATE your nginvproapp.conf FILE by putting your port, and domain url where users can access. 
EXPOSE 80
