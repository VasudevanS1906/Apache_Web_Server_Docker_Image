# Apache_Web_Server_Docker_Image

# Build Instructions

**1. Create a New Instance**

Once the playground instance is ready, click on the "Add New Instance" button on the left sidebar.
This will create a new Docker host for you to work with.

**2. Create a Dockerfile**

In the terminal window of the new instance, create a new file called Dockerfile by running the following command:

                        vi Dockerfile
This will open the nano text editor, where you can start writing your Dockerfile instructions.

**3. Write your Dockerfile**

In the editor, specify the instructions for building your Docker image. Here's a simple example Dockerfile that creates an Ubuntu-based image with the Apache web server installed:

                          FROM ubuntu:latest
                          RUN apt-get update && apt-get install -y apache2
                          EXPOSE 80
                          CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
                          Press :wq to write and quit the dockerfile

**4. Build the Docker Image**

In the terminal, run the following command to build the Docker image from the Dockerfile:

                    docker build -t my-apache-image .
Replace my-apache-image with your desired image name.
The . at the end of the command specifies the current directory as the build context.
Docker will start building the image based on the instructions in your Dockerfile.

**5. Verify the Built Image**

After the build process completes, you can verify that the image was created by running:

                      docker images
You should see your newly built image listed in the output.

**6. Run a Container from the Image**

To run a container based on the image you just built, use the following command:

docker run -d -p 80:80 my-apache-image
This will start a new container in detached mode (-d) and map port 80 of the host to port 80 of the container (-p 80:80).

**7. Test the Container**

Find the IP address of the Docker host by running:

                      ip addr show
Open a web browser and navigate to http://<host_ip>, replacing <host_ip> with the IP address you obtained.
You should see the Apache default page, indicating that your Docker container is running and serving the Apache web server.


# Screenshots

 The following screenshots visually demonstrates the successful execution of my project

 
