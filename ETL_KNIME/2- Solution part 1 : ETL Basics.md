# ETL Basics :

- L'objectif de ce flux de travail est de passer d'une série de contrats avec différents clients dans différents pays à une description synthétique sur une ligne pour chacun des clients.

![image](https://user-images.githubusercontent.com/123749462/225282716-31c4ee3e-cd20-4bfb-82e4-f109eb4cf9b4.png)

# Solution Part 1 :

- Créer un nouveau Workflow ETL_Basics :

![image](https://user-images.githubusercontent.com/123749462/225283697-12aa84cf-a491-4be4-97ee-107e4fb5bfd8.png)

- Drag and Drop le noeud CSV Reader :

![image](https://user-images.githubusercontent.com/123749462/225284076-2c1d0bfc-d96b-4a20-9a0b-495aa33bb8d6.png)

![image](https://user-images.githubusercontent.com/123749462/225284275-faf707b3-273e-43bc-8454-67b9acee6275.png)

- Cliquer sur le noeud CSV Reader > Boutton Droit > Configure :
- Ajouter le fichier csv sales_2008_2011 :

![image](https://user-images.githubusercontent.com/123749462/225286026-5e1442ad-503a-4c82-92c0-93a5a295af07.png)

- Cliquer sur le noeud CSV Reader > Boutton Droit > Execute :

![image](https://user-images.githubusercontent.com/123749462/225286536-b683a97a-b611-4d06-aab9-8135c179cdf9.png)

- Drag and Drop le noeud String to Date&Time :

![image](https://user-images.githubusercontent.com/123749462/225291215-2c19292d-87d7-4c6e-842e-8eaa02c80e02.png)

![image](https://user-images.githubusercontent.com/123749462/225291354-6f9d6047-3db1-4343-970b-cde2a076a561.png)


- Ajouter une connexion entre le noeud CSV Reader et le noeud String to Date&Time :

![image](https://user-images.githubusercontent.com/123749462/225295569-57293c4f-3a9b-449d-9604-43c092a8778a.png)

- Cliquer sur le noeud String to Date&Time > Boutton Droit > Configure :

![image](https://user-images.githubusercontent.com/123749462/225298033-ebb729cc-11ee-4004-8bad-3673ebdb76a3.png)

- Cliquer sur le noeud String to Date&Time > Boutton Droit > Execute :

![image](https://user-images.githubusercontent.com/123749462/225298909-9a1f09d1-f529-476c-8d81-aba97cef7ea0.png)

- Drag and Drop le noeud Sorter :

![image](https://user-images.githubusercontent.com/123749462/225300642-125ed89b-1fa0-4ffd-8b2f-30981efd41c2.png)

- Ajouter une connexion entre le noeud String to Date&Time et le noeud Sorter :

![image](https://user-images.githubusercontent.com/123749462/225300944-a817956e-5043-4917-8f92-d61a7b1c547c.png)

- Cliquer sur le noeud Sorter > Boutton Droit > Configure :

![image](https://user-images.githubusercontent.com/123749462/225301516-adb126c5-5b34-4890-b0a4-21b2fc835fa0.png)

- Cliquer sur le noeud Sorter > Boutton Droit > Execute :

![image](https://user-images.githubusercontent.com/123749462/225303453-bd52e0eb-f612-41c3-90a0-4814e56d985f.png)

- Drag and Drop le noeud Column Filter : 

![image](https://user-images.githubusercontent.com/123749462/225304506-ee5caf6e-24c6-4a08-a77e-c470693c9867.png)

- Ajouter une connexion entre le noeud Sorter et le noeud Column Filter :

![image](https://user-images.githubusercontent.com/123749462/225306583-f512db41-d867-466d-995a-e97f4f40c21e.png)


- Cliquer sur le noeud Column Filter > Boutton Droit > Configure :(Exclure le colonne "card")

![image](https://user-images.githubusercontent.com/123749462/225306853-f2ba632b-536e-45ac-bc2b-df77499a6121.png)

- Cliquer sur le noeud Column Filter > Boutton Droit > Execute :

![image](https://user-images.githubusercontent.com/123749462/225307220-e9b7ce14-e05f-4eb3-81bd-4decefa5a5f3.png)
