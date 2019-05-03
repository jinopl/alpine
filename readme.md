hi this is gernaral template for docker based testing 

Step 1 : Clone this project
Setp 2 : Edit docker-entrypoint.sh 
            uncomment #composer_location and add location
step 3 : Bulid the project using " docker build -t docktemp . "
step 4 : Run the container 
                docker run --rm -v "$(pwd)\"/html:/var/www/localhost/htdocs/ -e MYSQL_ROOT_PASSWORD=riosis -p 8012:80 -p 3366:3306 --name "project_name" docktemp

step 5 : project can be accesed via localhost:8012
