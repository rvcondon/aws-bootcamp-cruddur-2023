FROM python:3.10-slim-buster

#Inside Container
#make a new folder inside container
WORKDIR /backend-flask

#Outside Container --> Inside Container
#libraries to run the app
COPY requirements.txt requirements.txt

#Inside Container
#Install python libraries
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
# python3 -m flask run --host=0.0.0.0 --port=4567