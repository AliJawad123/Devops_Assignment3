
FROM python:3.8
WORKDIR /backend
COPY requirements.txt /backend/requirements.txt
RUN apt-get update && apt-get install -y libgl1-mesa-glx libcrypt1
RUN pip install --no-cache-dir -r /backend/requirements.txt
COPY . /backend
WORKDIR /backend
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
