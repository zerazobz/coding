FROM python:3.10.4
COPY ./restpython restpython
WORKDIR /restpython
COPY ./requirements.txt requirements.txt
RUN pip install -r requirements.txt
COPY ./manage.py manage.py
COPY ./restpython restpython
RUN python manage.py migrate
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]