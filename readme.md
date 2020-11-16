# FlaskVue App

Create python virtual environment:

    - python3 -m venv env 

"Virtual environments allow you to manage separate package installations for different projects. They essentially allow you to create a “virtual” isolated Python installation and install packages into that virtual installation. When you switch projects, you can simply create a new virtual environment and not have to worry about breaking the packages installed in the other environments. It is always recommended to use a virtual environment while developing Python applications."
[Detail about virtual environments](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment).

Install packages:

    - pip3 install -r requirements.txt

**Note: -r means requirement**

To run flask python app:

    - python3 app.py

To run Vue Client App:

    - cd client
    - npm install
    - npm run serve

## TO DO

    - Connect to database
    - Create routes and endpoints
    - Create test
    - Secure api
    - Implement CI/CD
