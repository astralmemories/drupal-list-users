# drupal-list-users
Repositorio de mi módulo personalizado **user_list** para Drupal 10/11.
- [https://github.com/astralmemories/user_list](https://github.com/astralmemories/user_list/) 

## **Iniciar el Proyecto Drupal con DDEV**  

### **Requisitos Previos**  
Asegúrate de tener instalados los siguientes programas en tu sistema:  
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)  
- [DDEV](https://ddev.readthedocs.io/en/stable/)  

### **Instrucciones de Configuración**  

1. **Clonar el repositorio del proyecto**  
   ```sh
   git clone https://github.com/astralmemories/drupal-list-users.git
   cd drupal-list-users
   ```

2. **Iniciar el entorno de DDEV**  
   ```sh
   ddev start
   ```

3. **Instalar las dependencias de Drupal**  
   ```sh
   ddev composer install
   ```

4. **Clonar el módulo personalizado `user_list`**  
   ```sh
   git clone https://github.com/astralmemories/user_list.git web/modules/custom/user_list
   ```

5. **Importar la base de datos de Drupal**  
   ```sh
   ddev drush sql-cli < ./BBDD/database.sql
   ```

6. **Limpiar la caché de Drupal**  
   ```sh
   ddev drush cr
   ```

7. **Acceder a la página del módulo personalizado**  
   Abre la siguiente URL en tu navegador:  
   [https://drupal-list-users.ddev.site/user-list](https://drupal-list-users.ddev.site/user-list)  
