# contact-form
PWP Contact form Demo

Commands to run from directory with Dockerfile in it:

Build the image:
`docker build -t contact-form .`

`-t contact-form` allows us to give the image our own name
`.` refers to where you want to create the image from

Check for the image:
`docker images`

Create a new container from the image:
`docker run --rm -p 8080:80 -d contact-form`

`--rm` means to delete the container when it stops running (default is to be manually removed)
`-p 8080:80` means to publish Docker's port 80 to your local machine's port 8080
`-d` means to run in detach mode, or in other words in the background of your terminal

Check for the running container:
`docker container ls`

Go to localhost:8080 to see your app!
