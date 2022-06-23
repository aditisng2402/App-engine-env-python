#APP ENGINE ENVIRONMENT TO DEPLOY PYTHON APP

-> gcloud projects list (cloud shell)

#gives all projects details
#clicked authorize


-> gcloud config set project xenon-axe-354108 (cloud shell)

#switch project


-> git clone https://github.com/aditisng2402/App-engine-env-python (cloud shell)


-> cd App-engine-env-python/appengine_standard_python3 (cloud shell)


-> ls (cloud shell)

   #to see the files


-> cat main.py/app.yaml (cloud shell)

   #to see what's in main.py/app.yaml


-> virtualenv --python python3 \ ~/envs/appengine_standard_python3


-> source \ ~/envs/appengine_standard_python3/bin/activate


-> pip install -r requirements.txt

-> python main.py

-> ctrl+c 

   #to quit


-> nano main.py
   #edit that file
-> ctrl+x
   #exit and save
-> y
   #agree to save


-> gcloud app create
   #to create application

-> gcloud app deploy app.yaml \
--project xenon-axe-354108

   #to deploy

-> gcloud app browse --project=xenon-axe-354108

   #to see our deployed app
