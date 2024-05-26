# Containerizing Apache Web Server using Docker Image

Building Docker images for Apache web servers provides consistent and portable environments, efficient resource utilization, simplified deployment and maintenance, and seamless integration with DevOps practices like CI/CD pipelines.

# Screenshots

 The following screenshots visually demonstrates the successful execution of my project

 ![Screenshot](apache_working_3.png)

 
 ![Screenshot](apache_working_4.png)

# Build Instructions

**1. Create a New Instance**

After the Docker playground instance is ready, click on the "Add New Instance" button on the left sidebar.
This will create a new Docker host for you to work with.

**2. Create a Dockerfile**

In the terminal window of the new instance, create a new file called Dockerfile by running the following command:

                        vi Dockerfile
This will open the nano text editor, where you can start writing your Dockerfile instructions.

**3. Write your Dockerfile**

In the editor, specify the instructions for building your Docker image. 

**4. Build the Docker Image**

In the terminal, run the following command to build the Docker image from the Dockerfile:

                    docker build -t my-apache-image .


Docker will start building the image based on the instructions in your Dockerfile.

**5. Verify the Built Image**

After the build process completes, you can verify that the image was created by running:

                      docker images
You should see your newly built image listed in the output.

**6. Run a Container from the Image**

To run a container based on the image you just built, use the following command:

                    docker run -d -p 80:80 my-apache-image


**7. Test the Container**

Find the IP address of the Docker host by running:

                      ip addr show

You should see the Apache default page, indicating that your Docker container is running and serving the Apache web server.


# Support and Contact

If you have any questions, please feel free to contact me at [vasudevanswornampillai@gmail.com].

# License

This project is licensed under the **Apache 2.0 License**.

# Share with the community

If you find this project interesting or helpful, don't hesitate to share with your community! Let's learn and grow together!

# Conclusion

In this project, we’ve developed a docker image for containerizing apache web servers. The model, a beacon of performance, awaits those go into the beautiful world of Devops.
 
