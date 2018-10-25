FROM alpine
MAINTAINER aalokhin <aalokhin@student.unit.ua>
RUN apk update && \
	apk upgrade && \
	apk add --no-cache vim
ENTRYPOINT ["sh", "-c", "vim ."]

# docker build --tag=vim .
# docker run -it --rm vim
# docker rmi $(docker images -q)