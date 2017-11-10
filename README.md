First install Docker Toolbox<br>
Then create local folders
<ul>
<li> Create a new folder for data, we assume path is ~/Documents/data, if you followed the instructions in phileas-condemine/hackathon_nov2017 you might already have this folder
<li> open cmd
<li> cd Documents
<li> mkdir data
<li> Create a folder tm, we assume path is ~/Documents/tm
<li> mkdir tm
<li> cd tm
<li> git clone https://github.com/phileas-condemine/text-mining.git
</ul>
You just need these folder to use them as volumes for your docker container<br>
then run a rstudio docker image from the <b>Docker Quickstart Terminal</b><br>
<ul>
<li> you may need to stop your current container
<li> docker stop practice_hackathon
<li> docker stop keras_demo
<li> docker run -d -v ~/Documents/tm/:/home/rstudio/Documents -v ~/Documents/data/:/home/rstudio/data -p 8787:8787 --name text_mining rocker/rstudio
<li>then install libxml2 on your container typing in the Docker Quickstart Terminal
<li> docker exec -it text_mining apt-get update
<li> docker exec -it text_mining apt-get install -y libxml2-dev
<li> docker exec -it text_mining apt-get install zlib1g-dev
<li> docker exec -it text_mining apt-get install gsl-bin libgsl0-dev

</ul>
then move to your container following the links http://192.168.99.100:8787 or http://192.168.99.101:8787 check your ip with `docker-machine ip`
<ul>
<li> user : rstudio
<li> password : rstudio
<li> open text_mining.Rpres
<li> run the chunk related to packages
<li> check the preview
</ul>
