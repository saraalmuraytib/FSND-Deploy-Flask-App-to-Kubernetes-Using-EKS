# 1- Use the python:stretch image as a source image
FROM python:stretch

# 2- Set up an app directory for the code
COPY . /app
WORKDIR /app

# 3- Install pip and needed Python packages from requirements.txt
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

#4- Define an entrypoint which will run the main app using the Gunicorn WSGI server. The Gunicorn should run with the arguments as follows: 
ENTRYPOINT ["gunicorn", "-b", ":8080", "main:APP"]