# contact-form
PWP Contact form Demo

Commands to run from directory with Dockerfile in it:


Build the image:

`docker image build -t contact-form .`

`-t contact-form` allows us to give the image our own name

`.` refers to where you want to create the image from


Check for the image:

`docker images`


Create a new container from the image:

`docker container run --rm -p 8080:80 -d contact-form`

`--rm` means to delete the container when it stops running (default is to be manually removed)

`-p 8080:80` means to publish Docker's port 80 to your local machine's port 8080

`-d` means to run in detach mode, or in other words in the background of your terminal


Check for the running container:

`docker container ls`


Go to localhost:8080 to see your app!


[For Hyper hosting](https://hyper.sh/howto/deploying-a-docker-based-php-project-with-hyper.sh.html):


Push image to dockerhub using username:

`docker build . -t <YOUR_USERNAME>/tiny-php-app`

`docker push <YOUR_USERNAME>/tiny-php-app`


Run hyper container from dockerhub image:

`hyper run -d -p 80:80 <YOUR_USERNAME>/tiny-php-app`


Allocate & attach floating IP:

`hyper fip allocate 1`

`hyper fip attach <YOUR_IP> <YOUR_CONTAINER_ID>`
