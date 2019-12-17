FROM centos 
RUN dnf -y install python3 python3-pip emacs
RUN python3 --version
RUN alternatives --set python /usr/bin/python3
RUN echo "(setq py-shell-name "python3")" > /root/.emacs
CMD /bin/emacs
