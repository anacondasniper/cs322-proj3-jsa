FROM python:3.12
LABEL maintainer="Milo Reynolds miloreyn@uoregon.edu"
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["python3", "flask_vocab.py"]
