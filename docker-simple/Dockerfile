FROM nginx:latest
# highly recommend you always pin versions for anything beyond dev/learn

# LABEL maintainer <maintainer name and emal>

WORKDIR /usr/share/nginx/html
# change working directory to root of nginx webhost
# using WORKDIR is prefered to using 'RUN cd /some/path'

COPY index.html index.html

# I don't have to specify EXPOSE or CMD because they're in FROM
