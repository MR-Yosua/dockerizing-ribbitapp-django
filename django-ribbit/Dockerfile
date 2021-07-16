FROM python:2
ENV PYTHONBUFFERED=1
COPY requirements.txt /code/
WORKDIR /code/
RUN pip install -r requirements.txt
COPY . /code/
RUN python manage.py syncdb --noinput
RUN python manage.py migrate ribbit_app