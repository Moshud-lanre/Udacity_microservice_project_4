FROM python:3.7.3-stretch
# Create a working directory
WORKDIR /home
# Copy source code to working directory
COPY . app.py /home/
# Install packages from requirements.txt
RUN pip install --no-cache-dir  --upgrade pip &&\
    pip install --no-cache-dir --trusted-host pypi.python.org -r requirements.txt
    
# hadolint ignore=DL3013
# Expose port 80
EXPOSE 80
# Run app.py at container launch
CMD ["python", "app.py"]

