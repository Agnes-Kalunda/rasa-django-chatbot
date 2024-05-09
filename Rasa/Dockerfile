# Use the existing Rasa image as the base image
FROM rasa/rasa:3.6.20-full

# Set the working directory inside the container
WORKDIR /app

# Copy the contents of the Rasa project directory into the container at /app
COPY . .

# Install any additional dependencies required for your chatbot
# For example, if you have custom actions, you might need to install Python packages
# using pip
RUN pip install -r requirements.txt

# Expose the Rasa server port (default is 5005)
EXPOSE 5005

# Command to run the Rasa server when the container starts
CMD ["rasa", "run", "-m", "models", "--enable-api", "--cors", "*", "--debug"]
