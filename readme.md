# Installation of Odoo 16 with docker-compose
### Requirements
* Docker and docker-compose installed

### Steps
1. Duplicate and rename:
    * Duplicate copy.odoo-postgres.docker-compose.yaml and rename the copy to docker-compose.yaml.
    * Duplicate copy.env and rename the copy to .env.
    * Duplicate odoo.conf.copy and rename the copy to odoo.conf.

    It is important not to edit or rename files containing the word "copy" in their name, as these are part of your template.
2. Set the parameters of your instance in the .env file.
3. Set the parameters of your instance in the config/odoo.conf file.
    * The parameters DB_HOST, DB_PASSWD, and DB_USER are set in .env. These are also configured in the odoo.conf file.
    * If you are in production, the parameter ADMIN_PASSWD in odoo.conf should be a secure one, as it is used to manage databases.
4. Execution with docker-compose
In the same root of the project where docker-compose.yaml is located, you should execute:
    * The first time it will download the Odoo and PostgreSQL images, which may take several minutes.
    * Subsequent executions should only take a few seconds to start.

    ~~~~
    docker-compose up -d
    ~~~~
    
    
5. Access Odoo
    * You defined the WEB_PORT parameter in the .env file.
    * Access localhost:<WEB_PORT>
    * The first time you access the system, it will show you a form to create a database.

### Contact Us
If you have encountered any difficulties in any of these steps or have any questions, you can contact us at hola@bigodoo.com and we will gladly provide you with assistance.
