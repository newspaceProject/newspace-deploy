FROM    jenkins/jenkins:lts
USER    root
RUN     apt-get update \
        && apt-get install -y nodejs npm \
        && apt-get install -y sshfs sshpass \
        && apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common \
        && mkdir -p /etc/apt/keyrings \
        && curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /etc/apt/keyrings/docker.gpg \
        && echo \
            "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
            $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null \
        && apt-get update \
        && apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
        