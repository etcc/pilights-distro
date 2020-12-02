FROM debian:9

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y \
  wget \
  parted \
  sudo \
  udev

RUN wget https://raw.githubusercontent.com/Drewsif/PiShrink/master/pishrink.sh && \
  chmod +x pishrink.sh && \
  mv pishrink.sh /usr/local/bin/pishrink

ADD fix_orphaned_inode_list.sh .
RUN chmod +x fix_orphaned_inode_list.sh && \
  mv fix_orphaned_inode_list.sh /usr/local/bin/fix_orphaned_inode_list

WORKDIR /root/
