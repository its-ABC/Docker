FROM ubuntu
#pecifies the base image for the Docker image you are building

WORKDIR /app
# sets the working directory inside the Docker container.

COPY requirements.txt /app
# Copies the "requirements.txt" file from your local machine to the /app directory in the Docker image

COPY test-10 /app
#Copies the entire test-10 directory from your local machine to the /app directory in the Docker image

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install -r requirements.txt && \
    cd devops

ENTRYPOINT ["python3"]
# sets python3 as the main executable that runs when the container starts. This means every time the container runs, it will execute python3 by default

CMD ["manage.py", "runserver", "0.0.0.0:8000"]
# provides default arguments for the command defined in ENTRYPOINT or specifies a default command if ENTRYPOINT is not set, and can be overridden at runtime



