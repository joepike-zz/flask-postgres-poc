
FROM python:2-slim

COPY . /data-api
WORKDIR /data-api

RUN pip install -r requirements.txt

# Create user and change folder permissions
RUN groupadd -r dataapi && useradd -r -g dataapi -u 1000 dataapi && \
    chown -R dataapi:dataapi /data-api

EXPOSE 5000

USER 1000

CMD ["python", "app.py"]
