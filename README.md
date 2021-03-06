# NLP-demo-template
NLP demo: backend and web application template

## Goal
We aim to provide guidance on how to disign and create a NLP demos for your research work.

## Overall guidelines
* Make sure your code is organized and documented
* Do not include absolute paths within your code; instead, use env variables or config setup files as much as possible

## README file
Your final README must include:
* A brief description of your system
* Requirements in order to make it run (e.g. Python packages and specific versions)
* Detailed installation instructions and setup
* Running instructions and how to interpret results (make sure that your code is reproducing the same results reported in your paper)
* Datasets - if your code requires specific datasets that are not being provided as part of your repository, please make it clear how to download them and where exactly they should reside.


## Step-by-step
in  the following sections we provide guidance on how to disign and create a NLP demo.

### Describe your demo
Write a short description what your demos is about. If possible provide an schematic diagram to show how end-to-end compnents are integrated.

**_This template example demonstrates how to compose back- and front-end components in order to build an NLP Demo. Our example uses spiCy to performs Named Entity Recognition (NER) over a piece of text (English only)._**

### Backend entry point functions

[python/backend.py](backend.py) implements the basic resp api functionalities:
* It uses cherrypy to enable the http resp api protocol
```
import cherrypy
```

Uses 

### UI

## Final deployment checklist
Check whether you have accomplished the expected GitHub requirements before making your code publicly available.

* Does your README contain a brief description of your system?
* Are you providing a list of dependencies required to run your code?
* Do you have clear instructions on how to install and set up your system?
* Have you successfully installed your system from scratch lately?
* Is it clear in your instructions what datasets should be available?
* Are you providing clear instructions on how to run your code?
* Were you able to fully reproduce your experiments lately?
* Does the result from your code comply with the results reported in your paper?
* Do you have explicit instructions for processing single entry input?
* Is the resulting output from single entry processing clearly documented?


## Docker
If you want to make your demo available using Docker, folow the instructions below:

1. Write a Dockerfile for each sevice that you want to make available: eventually can have distinct rest services running in different ports, and make all backend services independent regarding the UI.
2. Make sure you have all the required Python packages added to your Docker image
3. Use a docker-compose file to connect all services and interfaces, reassign ports, and make large files available.


