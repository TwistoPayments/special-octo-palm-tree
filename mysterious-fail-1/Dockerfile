FROM python:3.8-slim

ARG USERID

ENV USERID=${USERID}

RUN adduser --uid=${USERID} --system mysterious

COPY requirements.txt /app/
WORKDIR /app
USER mysterious

RUN pip install --user -r requirements.txt

ENV PATH="${PATH}:/home/mysterious/.local/bin"

COPY . /app

CMD ["python3", "reverse_figlet.py"]
