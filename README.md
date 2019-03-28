Docker Image for Python based on Ubuntu.


## Supported tags and respective `Dockerfile` links


- `2.7-bionic` ([2.7/bionic/Dockerfile](https://github.com/pyfreyr/docker-python/blob/master/2.7/bionic/Dockerfile))
- `3.5-bionic` ([3.5/bionic/Dockerfile](https://github.com/pyfreyr/docker-python/blob/master/3.5/bionic/Dockerfile))
- `3.6-bionic` ([3.6/bionic/Dockerfile](https://github.com/pyfreyr/docker-python/blob/master/3.6/bionic/Dockerfile))
- `3.7-bionic` ([3.7/bionic/Dockerfile](https://github.com/pyfreyr/docker-python/blob/master/3.7/bionic/Dockerfile))


## How to use this image

Create a Dockerfile in your Python app project:

```yaml
FROM pyfreyr/python:3.6-bionic

WORKDIR /web

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python", "./app.py" ]
```

You can then build and run the Docker image:

    $ docker build -t my-python-app .
    $ docker run -it --rm --name my-running-app my-python-app