# 1.  
Para instalar una imagen alpine utilizamos el siguiente comando:  
docker pull alpine  
Podemos comprobar que se ha instalado con el comando docker images.  

# 2. 
Para crear una red para nuestras pruebas de DNS podemos hacerlo de la siguiente forma:  
 docker network create \  
 --driver=bridge \  
 --subnet=172.28.0.0/16 \  
 --ip-range=172.28.5.0/24 \  
 --gateway=172.28.5.254 \    
 bind9_subnet    

# 3. 
Para hacer las pruebas con dig, necesitamos entrar dentro del contenedor. Para ellos hacemos click derecho y attach shell.  
Una vez dentro del contenedor:  
apt update  
apt install -y dnsutils  
Ahora ya podemos hacer uso de dig para hacer las pruebas.  