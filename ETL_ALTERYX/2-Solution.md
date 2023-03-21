# Solution : Les enseignements de spécialité au baccalauréat en forte demande:

- Drag and Drop le noeud Text Input :

![image](https://user-images.githubusercontent.com/123749462/226664717-297b3898-7fb3-466f-9ae2-794b4188a0e4.png)

![image](https://user-images.githubusercontent.com/123749462/226667385-66f3d533-df55-407d-a5db-3b343d664742.png)

- Cliquer sur cette icon import :

![image](https://user-images.githubusercontent.com/123749462/226669297-0c95fc3d-9b64-4961-a0ca-59e7c372e133.png)

- Puis cliquer sur insert > Row :

![image](https://user-images.githubusercontent.com/123749462/226673963-f7ce7727-4775-4060-93a1-1c715ab11566.png)

- Copier le contenu du fichier students.txt (ctrl+A > ctrl+C) et coller (ctrl+V ) le contenu ici :

![image](https://user-images.githubusercontent.com/123749462/226674903-0fe9925b-b253-40d4-bbe8-05d44fd1b30d.png)

![image](https://user-images.githubusercontent.com/123749462/226675277-3f828f32-96bf-4be0-a5e4-5a2ca23e2ac5.png)

- Drag and Drop Text to Columns :

![image](https://user-images.githubusercontent.com/123749462/226678411-986ae2e3-8a56-4770-8149-cbc7dbb53a62.png)

![image](https://user-images.githubusercontent.com/123749462/226678476-721676ba-9d46-4eb1-a8eb-90c6d01763b8.png)

- Spécifier le nombre de colonnes en 10 :

![image](https://user-images.githubusercontent.com/123749462/226678990-779afd65-d616-4819-9654-f4c7320bd7c3.png)

- Exécuter le noeud Text to Columns :

![image](https://user-images.githubusercontent.com/123749462/226679492-0bd753f2-b925-4a0d-bdaa-6643458154cf.png)

- En utilisant la barre de recherche , trouver le noeud Dynamic Rename :

![image](https://user-images.githubusercontent.com/123749462/226681457-5099ef91-be85-42c3-be79-c026c56b43ab.png)

- Drag and Drop le noeud Dynamic Rename :

![image](https://user-images.githubusercontent.com/123749462/226681662-519edcc7-d104-4f65-94b1-f8684a94f27a.png)

- Choisir ``Take Field Names from First Row of Data`` du Rename Mode :

![image](https://user-images.githubusercontent.com/123749462/226682693-b2f59af0-1938-4d4f-ba92-7993f2e92bc8.png)

- Cliquer sur Run :

![image](https://user-images.githubusercontent.com/123749462/226683147-fe907228-df3d-446c-8d1a-3d6de468320a.png)

- Drag and Drop le noeud Select :

![image](https://user-images.githubusercontent.com/123749462/226683685-094afffc-149a-4a9b-a78f-a957df57dc31.png)

![image](https://user-images.githubusercontent.com/123749462/226683857-fc6ca692-9611-48c9-af2d-bad44f3c5d12.png)

- Décocher cette ligne , et changer le type de ces champs en int64 :

![image](https://user-images.githubusercontent.com/123749462/226685805-47c66f04-f8a4-4de3-8edd-c1ab39c16cfc.png)

- Cliquer sur Run :

![image](https://user-images.githubusercontent.com/123749462/226686545-db2640f0-f78a-4af8-81fa-d801072c4ccb.png)

- Drag and Drop le noeud Formula : 

![image](https://user-images.githubusercontent.com/123749462/226686935-ea282d35-eb55-41fa-b8ae-1e78d7f2f529.png)

![image](https://user-images.githubusercontent.com/123749462/226687120-02fe03f1-9381-4805-a6c6-bf47bdc4c640.png)

- On va configurer notre formule :

![image](https://user-images.githubusercontent.com/123749462/226688078-746052d6-a7db-4ed1-b6bf-18ff5906aead.png)

  - On ajoute une nouvelle colonne ( Add Column ) avec le nom ``Percentage_Employed``
  - On ajoute la formule :
  ```
  Ceil([Employed]/[Total]*100)
  ```
  - Choisir le type de donnée Double 









