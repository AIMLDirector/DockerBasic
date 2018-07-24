FROM python:3.6
WORKDIR /app
COPY requirements.txt /app/
RUN pip install -r requirements.txt && \
     django-admin startproject FirstApp

WORKDIR /app/FirstApp
COPY views.py .
COPY urls.py .

#RUN python manage.py runserver

COPY start.sh /app/FirstApp/start.sh

# EXPOSE port 8000 to allow communication to/from server
EXPOSE 8000

RUN chmod +x /app/FirstApp/start.sh

# CMD specifcies the command to execute to start the server running.
CMD ["/app/FirstApp/start.sh"]
