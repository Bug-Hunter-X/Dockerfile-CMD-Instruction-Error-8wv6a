# Dockerfile CMD Instruction Bug
This repository demonstrates a common error in Dockerfiles: an incorrectly specified CMD instruction that prevents the application from running correctly inside the container.

## Bug Description
The Dockerfile attempts to run a Python application using `CMD ["python3", "/app/main.py"]`. However, the `main.py` file is not included in the image, so the command fails to execute.

## Solution
The corrected Dockerfile copies the necessary files into the image before running the application.