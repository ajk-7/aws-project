FROM python:3.10-slim-buster

WORKDIR /backend-flask

# Copy requirements.txt (source -> destination)
COPY requirements.txt requirements.txt

# Install the libraries
RUN pip3 install -r requirements.txt

# Copy the rest of the app files
COPY . .

ENV FLASK_ENV=development
EXPOSE ${PORT}

CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=4567"]
