Réseau : 192.168.4.0/24

IP : 192.168.4.1 PC Serveur Local
192.168.4.10 – .29	Objets IoT
192.168.4.30 – .49	Postes de l'équipe


```mermaid
graph TD
    %% Définition des équipements
    Internet((Internet)) -->|Fibre| Box[Box Internet / Routeur]
    Box --> Switch[Switch Principal]
    
    subgraph Réseau Local (LAN)
        Switch --> NAS[NAS Synology\n192.168.1.10]
        Switch --> PC[PC Fixe\n192.168.1.50]
        Switch --> Borne[Borne Wi-Fi]
    end

    subgraph Appareils Wi-Fi
        Borne -.-> Phone[Smartphone]
        Borne -.-> TV[Smart TV]
    end
