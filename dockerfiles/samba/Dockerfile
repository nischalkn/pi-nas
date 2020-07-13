FROM alpine:latest

RUN apk --no-cache --upgrade add samba samba-common-tools samba-server

RUN mkdir -p /mnt/disk1

COPY smb.conf /etc/samba/

EXPOSE 445/tcp 139/tcp 445/udp 139/udp

ENTRYPOINT ["smbd", "--foreground", "--no-process-group"]
CMD []
