# Stage 1: awscli-donwload
# Download and install the AWS CLI
FROM hashicorp/tfc-agent:latest AS awscli-download

RUN apt-get update && apt-get install -y --no-install-recommends unzip curl

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip awscliv2.zip

RUN ./aws/install

# Stage 2: Copy the installed AWS CLI to the TFC Agent container
FROM hashicorp/tfc-agent:latest

COPY --from=awscli-download /usr/local/aws-cli /usr/local/aws-cli

RUN ln -s /usr/local/aws-cli/v2/current/bin/aws /usr/local/bin/aws 
