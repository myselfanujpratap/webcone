
![Screenshot 2025-01-24 at 11 49 07 PM](https://github.com/user-attachments/assets/ef2256ac-fa8b-4793-8a70-13a6ac429ca5)

## About 
Webcone is a dockerised service for hosting files onto the web with ease and minimal configuration 


## Components 
* NGINX - nginx is being used to serve files over the web with routing and configuration stuff 
* DOCKER - Docker is used to provide containerised env for all the components 
* HTML , CSS , JS  - web based tech are used to build website to use 


## Working 
![Screenshot 2025-01-24 at 12 15 44 AM](https://github.com/user-attachments/assets/77d943cc-93b4-4456-8608-f860a0d3d669)

The setup has been implemented using docker compose init the ports are configured to 80 (default port for the nginx) , all the files inside the repo are mounted accordingy including nginx.conf file at location /etc/nginx/nginx.conf in the nginx container and other website content mounted at /etc/nginx/website/* when compose setup is run traffic from client -> host is redirected to docker container which serves the request (files which are mounted) on the same way passing from container to host to client.    


## Usecase 
This setup is useful when needed to spontaneously host some files for testing purposed or for hosting static web siles for hosting a website just like in the current case the website is hosted withit.


# Setup 
1. Install docker (prequisite)

2. Clone the repo
     ```bash
     git clone https://github.com/myselfanujpratap/webcone.git 
     ```

3. Move inside the repo
   ```
   cd webcone
   ```

5. Put the file you want to host inside the repo 

4. Run the setup
   ```
   docker compose -f webcone.yml
   ```

5. Test and verify by moving to browser by typing the url
   ```
   http://localhost/FILE-PRESENT-INSIDE-THE-REPO
   ```
