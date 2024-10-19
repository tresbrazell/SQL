# SQL
Running a docker postgres container with pgadmin4

# docker-container.yml
1. open new terminal in VSCode
2. ls to directory containing you docker-container.yml file
3. type docker-container up
4. open browser and goto localhost:5050
5. login to pgadmin4 using user and pass as defined by yml docker-container.yml file
6. now we need to attach our newly spun server
7. go back to your VSCode and open a new terminal
8. type docker container ls (do no type docker-container)
9. you are looking for the CONTAINER ID of your postgres IMAGE
10. back to your terminal type docker inspect YOUR_CONTAINER_ID where your will paste in your alphanumeric string in place of YOUR_CONTAINER_ID
11. look for "IPAddress:" and copy the ip address for you postgres server
12. head back over to pgadmin4, right click on Servers and select register, then server
13. in this window you will enter the postgres db name that was defined in the docker-container.yml file
14. click the connection tab and paste in the IP Address
15. for user and pass refer to docker-container.yml 
