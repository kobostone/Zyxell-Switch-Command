# Zyxell-Switch-Command

![image](https://github.com/user-attachments/assets/b50ef10b-7a9f-4df9-82fe-fdc53e4cf5b3)


![image](https://github.com/user-attachments/assets/75c74d46-6004-48b9-8f4f-3a8eb8936875)


### enable clv mode   

GS2210#config    
GS2210(config)# clv  

![image](https://github.com/user-attachments/assets/75583426-6069-4d71-a2af-9926b0c28123)


### Configuration des VLAN 

![image](https://github.com/user-attachments/assets/8ab875ac-1797-42b7-9948-d039578a92b0)


![image](https://github.com/user-attachments/assets/ba4e2bc9-fb18-46f6-a89d-f52913ca09b1)


![image](https://github.com/user-attachments/assets/47f9f75b-ad25-4590-811e-a8c55d51f29a)



(config)# interface port-channel 1,2,3           
(config-interface)# switchport mode access     
(config-interface)# switchport access vlan 55    
quit

![image](https://github.com/user-attachments/assets/67086aeb-e03f-4f16-8943-b163cfad14bc)


(config)# interface port-channel 1,2,3     
(config-interface)# switchport mode trunk

![image](https://github.com/user-attachments/assets/a3791128-6989-4603-87ce-ed6a57cbd0bc)



![image](https://github.com/user-attachments/assets/32d72acf-0920-4ebb-9927-af2c1c80e4a2)



Dans l’exemple suivant, l’adresse IP du VLAN 1 est remplacée par 172.31.255.71 avec un masque de sous-réseau 255.255.255.0.

sysname # configure    
sysname (config) # vlan1     
sysname # config # ip address default-management 172.31.255.71 255.255.255.0    
sysname (config) # exit     
sysname # write    
sysname # exit     


### Agrégation de liens / équilibrage de charge


L’agrégation de liens (LAG): combiner deux ports en un seul pour obtenir une capacité plus élevée (vitesse ou fiabilité) sur la connexion.   

 regrouper plusieurs ports physiques pour former un seul canal logique (liaison virtuelle) 

 Utilisez la bande passante disponible entre le commutateur et d’autres périphériques
réseau- Améliorez la fiabilité du réseau entre les périphériques réseau



Cela se fait soit par Statique, soit par LACP (Link Aggregation Control Protocol). 

Le LAG statique est utilisé si vous configurez tout manuellement (si les ports sont configurés en tant que membres statiques d’un groupe de jonction), tandis que LACP est utilisé lorsque les ports sont configurés pour rejoindre un groupe de liaisons déjà existant via LACP en utilisant le protocole pour communiquer.

