# SuperMegaBank
Deployment files


Deployment Instructions:
1) A simple ssh script has been provided to 'mkdir', clone github, change permissions to make files executable and call the docker-compose command for this project.
2) The project involves 2 services, app and testing.  My solution creates 2 containers, one container for each service - like two microservices standing independently but will still need to talk to each other. I have used docker-compose as my deployment solution for ease of deployment where one configuration file contains all details for both services.  The hosting server will require docker, docker-compose and apache or a similar web service to host the flask 'api's etc.

  Solution Details (system-engineer folder):
        1) Created a new Dockerfile under the app directory.  The configuration file loads Python PIP dependencies contained in the requirements.txt file and runs the app.py module.
        2) Similarly a new Dockerfile has been created under the testing directory, loading Python dependencies and executable, testing.py
        3) In the parent directory, a docker-compose.yml has been created defining the 2 services and linking the testing module with app. A 'depends_on' variable ensures the Flask api app module is started prior to the testing service.  The docker-compose format used is version 3.
        4) The app module has been tested successfully with api enpoints ie. http://localhost:5000/customers/111 returning required json results.
          {
  "data": {
    "name": "Deadpool"
  }, 
  "id": "111"
}
        5) The testing.py script has tested successfully but is slightly problematic when called from docker-compose.  I have copied and pasted the path details and 'from app import app' into the testing.py file but possibly needs a further modification in the system path variable or the removal of __init__.py for Python versions 3.3 and above.

thanks

Sue.
