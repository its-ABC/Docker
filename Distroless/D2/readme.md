# run the following commands

docker build -t cheking .
# "docker build" command used to create a new Docker image from the instructions in a Dockerfile
# "-t" used to setting the tag
# "checking" this the name i have given
# "." tells Docker where to look for the Dockerfile

docker images ls
# used to see the created images

docker rmi ID
# used to remove image if not needed
# "ID" specify the id of image that has to be deleted
