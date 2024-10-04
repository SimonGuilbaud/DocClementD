# Installation d'un module GeoNature


## Installation automatisée

### **Résumé des étapes**
1. Cloner le repository du module concerné au même niveau que le répertoire GeoNature
2. Passer en environnement virtuel Python
3. Lancer la commande d'installation automatique `install-gn-module`
4. Donner les permisions adéquates
5. Relancer GeoNature et le worker


### **Déroulé des étapes**  
*Exemple avec le module Import* 

[Dépôt Github du SI des PNF pour trouver le modulé GeoNature souhaité](https://github.com/PnX-SI)

+ Cloner le repository de module d'import  
  `git clone https://github.com/PnX-SI/gn_module_import.git`

+ Passer en environnement virtuel Python  
  `source <dossier GeoNature>/backend/venv/bin/activate`  
  ```bash
  source ~/geonature/backend/venv/bin/activate
  ```

+ Lancer la commande d'installation automatique  
  `geonature istall-gn-module <dossier GeoNature> <code du module>`  
  ```bash
  geonature install-gn-module ~/gn_module_import/ IMPORT
  ```

+ Donner les permissions adéquates (ici administrateurs)  
  *changer "Grp_Admin" par le nom de votre groupe d'administrateur si vous l'avez changé* 
  ```bash
  geonature permissions supergrant --group --nom "Grp_admin"
  ```

+ Relancer Geonature et son worker  
  ```bash
  sudo systemctl restart geonature
  sudo systemctl restart geonature-worker
  ```


## Installation manuelle
