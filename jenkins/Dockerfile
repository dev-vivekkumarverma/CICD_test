FROM jenkins/jenkins:lts

# Install Docker CLI
USER root
RUN apt-get update && apt-get install -y docker.io

# Switch back to Jenkins user
USER jenkins
