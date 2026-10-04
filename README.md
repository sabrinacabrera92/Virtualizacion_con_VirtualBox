# Virtualizacion con VirtualBox

Configuración de Red e Instantáneas
Curso: Ciberseguridad Coderhouse
Sabrina Cabrera


Configuración de red de la VM:
Para garantizar un entorno de pruebas controlado y seguro, se configuró el adaptador de red de la máquina virtual en modo Red Interna.

<img width="808" height="513" alt="kali_red_modo_red_interna" src="https://github.com/user-attachments/assets/c23c95ec-44a6-4e2f-93b6-20361bdf2360" />


La VM de Kali Linux fue configurada con un adaptador de red en modo NAT para aislar la máquina de la red local física, actuando como un router invisible. Permite tener salida a Internet para instalar las actualizaciones, pero impide que dispositivos externos se conecten directamente a ella, protegiendo así a la computadora anfitriona de posibles fugas o ataques.

Elegí la configuración de Red interna para que la en la prueba inicial la VM no tenga salida a internet ni comunicación con la red física ya que no es necesario en este caso, así la maquina queda aislada y se impide el tráfico hacia la red doméstica o al exterior.
No usé el modo NAT porque entonces se permitiría que la VM tenga salida libre a internet a través del host. 
Tampoco usé el modo puente (bridged) porque conecta la VM directo al router de la red física y expone la misma a la red domestica e internet lo que podría ser un riesgo de seguridad.


Captura primer snapshot:

Creé un punto de restauración inicial antes de realizar cambios o pruebas sobre el SO.

<img width="1232" height="605" alt="kali_instantanea_instalacion_limpia" src="https://github.com/user-attachments/assets/9b5e021e-e8cb-4a31-90ee-dcd23e3182d1" />

