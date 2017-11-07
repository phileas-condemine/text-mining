First install Docker Toolbox<br>
Create a new folder for data, we assume path is ~/data<br>
Create a folder tm, we assume path is ~/tm<br>
You just need these folder to use them as volumes for your docker container<br>
then run a rstudio docker image from the Docker Quickstart Terminal<br>
docker run -d -v ~/tm/:/home/rstudio/Documents -v ~/data/:/home/rstudio/data -p 8787:8787 --name text_mining rocker/rstudio<br>
then install libxml2 on your container typing in the Docker Quickstart Terminal <br>
docker exec -it text_mining apt-get update<br>
docker exec -it text_mining apt-get install libxml2-dev<br>
docker exec -it text_mining apt-get install zlib1g-dev<br>
