
FROM python:3.6

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY requirements.txt /usr/src/app/
RUN pip install -i https://pypi.douban.com/simple --no-cache-dir -r requirements.txt


COPY .  /usr/src/app

#RUN apt-get update && apt-get install -y \
#		gcc \
#		gettext \
#		mysql-client libmysqlclient-dev \
#		postgresql-client libpq-dev \
#		sqlite3 \
#	--no-install-recommends && rm -rf /var/lib/apt/lists/*

#RUN apt-get update && apt-get install -y \
#		gcc \
#		sqlite3 \
#	--no-install-recommends && rm -rf /var/lib/apt/lists/*

EXPOSE 8080
CMD ["python", "manage.py", "runserver", "0:8080"]
