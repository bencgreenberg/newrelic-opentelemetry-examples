FROM python:3.7

RUN mkdir /app
ADD app /app
WORKDIR /app
RUN pip install -r requirements.txt

EXPOSE 5000
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0"]