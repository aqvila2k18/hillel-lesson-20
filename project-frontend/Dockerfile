FROM node:16
RUN apt update \
    && apt install -y unzip curl
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./aws/install
RUN rm awscliv2.zip
COPY ts-redux-react-realworld-example-app /app
WORKDIR /app
RUN npm clean-install
RUN npm run build
RUN apt purge -y curl unzip
RUN apt autoclean && apt autoremove
ENTRYPOINT [ "/bin/bash" ]