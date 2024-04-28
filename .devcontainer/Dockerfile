# Use an official Python runtime as a parent image
FROM python:3.8-slim

# Set the working directory
WORKDIR /workspace

# Install any needed packages specified in requirements.txt
COPY requirements.txt /workspace/
RUN pip install --no-cache-dir -r requirements.txt

# Install JupyterLab
RUN pip install jupyterlab

# Make port 8888 available to the world outside this container
EXPOSE 8888

# Run JupyterLab
CMD ["jupyter", "lab", "--allow-root", "--no-browser", "--ip=0.0.0.0"]
