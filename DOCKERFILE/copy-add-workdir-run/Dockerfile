    FROM ubuntu:18.04

    WORKDIR /copy

    COPY host-file .

    WORKDIR /add
    
    ADD add-files.tar.gz .
    ADD https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRgH5eijja18yQOK7ESysxCbZJLEeAF1b41pDoec9x3U7ov_5nwjL84wHz_tbu4sEFgbmg&usqp=CAU .

    RUN apt-get update && apt-get install -y \
    net-tools \
    curl \
    nginx \
    && rm -rf /var/lib/apt/lists/*