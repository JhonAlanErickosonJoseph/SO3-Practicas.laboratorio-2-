# SO3-Practicas.laboratorio-2-
aqui esta los comando del laboratorio numero 2 de sistema operactivo 3. con el profesor adrian alcantara. dueño del archivo es Jhon Alan Erickson Joseph
Comandos usados en la práctica de Rocky Linux
==================================================

# Práctica 1: Actualización y gestión de paquetes

# Actualizar repositorios y paquetes
sudo dnf update -y

# Verificar los repositorios en uso
dnf repolist

# Buscar la herramienta Bashtop en los repositorios
dnf search bashtop

# Instalar Bashtop si está disponible
sudo dnf install bashtop -y

# Ejecutar Bashtop para verificar la instalación
bashtop

# Desinstalar Bashtop y eliminar su configuración
sudo dnf remove bashtop -y

# Eliminar dependencias no utilizadas
sudo dnf autoremove -y

==================================================

# Práctica 2: Automatización con Cron y At

# Crear un trabajo cron para actualizar el sistema a las 11 PM diariamente
echo "0 23 * * * root dnf update -y" | sudo tee -a /etc/crontab

# Programar un reinicio del sistema todos los domingos a las 3 AM
echo "0 3 * * 0 root /sbin/shutdown -r now" | sudo tee -a /etc/crontab

# Usar el comando 'at' para eliminar el contenido de /tmp en 1 minuto
echo "rm -rf /tmp/*" | at now + 1 minute

==================================================

Fin del archivo.
