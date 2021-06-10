FROM python:3.8-slim

ARG USERID

ENV USERID=${USERID}

RUN useradd -u ${USERID} -d mysterious

COPY requirements.txt /app/
WORKDIR /app
USER mysterious

RUN pip install --user -r requirements.txt

COPY . /app

CMD ["python3", "reverse_figlet.py"]
