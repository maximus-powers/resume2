FROM nginx:1.24.0

RUN apt update && apt -y upgrade

RUN apt install -y git

WORKDIR /usr/share/nginx/

RUN rm -f -r /usr/share/nginx/html

RUN git clone https://github.com/maximus-powers/resume2.git html

# RUN cp -r ./resume2 /usr/share/nginx/html

# Set the working directory to the Nginx config directory
WORKDIR /etc/nginx

# Copy the local Nginx configuration file to the container
# COPY nginx.conf .

# Expose port 80 for HTTP traffic
EXPOSE 80

# Start Nginx when the container launches
CMD ["nginx", "-g", "daemon off;"]
