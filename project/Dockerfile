FROM python:3.8
LABEL maintainer="Sudipta Sen"

WORKDIR /usr/src/app
COPY techtrends/requirements.txt ./
RUN pip install -r requirements.txt

COPY techtrends .

EXPOSE 3111

RUN python init_db.py

CMD ["python", "app.py", "--host=0.0.0.0"]

