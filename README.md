1.Download  nyc_collision_data.csv from 
https://data.cityofnewyork.us/Public-Safety/NYPD-Motor-Vehicle-Collisions/h9gi-nx95
click export -> csv

2. Donwload nyc_collision_template.json to current folder
3. Download nyc_collision_logstash.conf to current folder
4. Open the kibana DEV tool we talked in the slides
5. Input the following in the DEV tool 

PUT _template/template_1
{REQUEST_BODY}

please replace the {REQUEST_BOD} with the content in file nyc_collision_template.json. Please remove any empty lines so that the Green arrow shows up  in DEV tool , then click and run it

6.Download load.sh 
7. $chmod a+x load.sh
8. ./load.sh
 
You should see a lot of dots showing up on screen. Wait a couple of minutes so that you see the dots stopped showing up.
9. In DeV tool run following
GET nyc_visionzero/_count

this should return a count of roughly 1 million records
