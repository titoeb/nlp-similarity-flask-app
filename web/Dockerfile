FROM python:3

WORKDIR /usr/web

COPY ./ ./

COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

RUN python -m spacy download en_core_web_sm

ENV FLASK_APP=app.py

CMD ["flask", "run", "--host=0.0.0.0"]
