# Use the official Python image as the base image
FROM python:3.9

# Set environment variables for Python and Django
ENV PYTHONUNBUFFERED=1 \
    DJANGO_SETTINGS_MODULE=chatbotproject.settings \
    PORT=8000

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt /app/

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code into the container
COPY . /app/

# Set entrypoint
ENTRYPOINT ["./entrypoint.sh"]

# Command to run the Django development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:$PORT"]
