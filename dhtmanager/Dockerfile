FROM fedora
RUN yum -y install python3 python3-virtualenv git
RUN yum -y install uwsgi uwsgi-plugin-python3 python3-psycopg2
RUN python3 -m virtualenv /app
COPY start_dhtmanager /bin
RUN . /app/bin/activate; pip install git+https://github.com/larsks/dhtmanager
CMD ["/bin/start_dhtmanager"]
