FROM python:3.12

WORKDIR /app

RUN pip3 install jupyter
COPY requirements.txt .
RUN pip3 install --no-cache-dir -r requirements.txt

COPY . .
RUN useradd -d /app jzhang
RUN chown jzhang:staff /app
RUN chown -R jzhang:staff /app

USER jzhang:staff

ENTRYPOINT /app/entry-point.sh
