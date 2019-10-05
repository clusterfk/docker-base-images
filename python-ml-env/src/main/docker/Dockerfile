FROM ${base}

ADD requirements.txt /tmp/requirements.txt

RUN pip install -r /tmp/requirements.txt && rm /tmp/requirements.txt

CMD ["python3"]