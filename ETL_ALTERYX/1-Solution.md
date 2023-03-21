# Solution : Réservation Hotel :

- Créer un nouveau Workflow : File > New Workflow :

![image](https://user-images.githubusercontent.com/123749462/225887830-b6b1f4e9-dab7-4de7-a07d-0cb17012dae7.png)

- Drag and Drop Input Data : 

![image](https://user-images.githubusercontent.com/123749462/225889061-946b85d5-7ee5-4c25-9111-35d751b4d766.png)

![image](https://user-images.githubusercontent.com/123749462/225889641-03cd003d-15ee-4f85-bed3-f2af19fffd71.png)

- Maintenant on va configurer notre Input Data ici : 

![image](https://user-images.githubusercontent.com/123749462/225890068-5ed47111-b975-4d47-bab5-adb7cbabb148.png)

- On va ajouter le fichier hotel.csv
- Cliquer sur Set Up a Connection : 

![image](https://user-images.githubusercontent.com/123749462/225891232-ce2f7df2-214a-4209-b62d-0045378a940f.png)

- Cliquer sur Files > Select file :

![image](https://user-images.githubusercontent.com/123749462/225898050-c26d8aff-4c59-4b44-acc0-58a297a3621b.png)


- Sélectionner hotel_reservation > cliquer sur ouvrir :

![image](https://user-images.githubusercontent.com/123749462/226624135-2470f572-7f0d-4a32-908f-9e5867bc30f9.png)

- Cliquer sur Run pour éxecuter Input Data , Voilà ce que vous allez avoir comme output : 

![image](https://user-images.githubusercontent.com/123749462/226625216-68efd0e4-8e6e-4c06-a178-4cdd5e49b8b2.png)


![image](https://user-images.githubusercontent.com/123749462/226625381-6ee02f95-1e8a-4edb-912d-3bfd49ff9acf.png)

- Drag and Drop Filter : 

![image](https://user-images.githubusercontent.com/123749462/225903341-2e00af8d-bd8e-405e-a9a5-7dc0d0ce2cc3.png)

![image](https://user-images.githubusercontent.com/123749462/226625591-150f6b06-385a-4f1b-b5c7-d4101562216e.png)

- On va configurer notre filtre avec un filtre basique sur les réservation qui n'ont  pas été annuler :

![image](https://user-images.githubusercontent.com/123749462/226632913-c1b6acbf-1452-4b6d-b9e4-6687fae1bc5d.png)

- Exécuter ce filtre : 

![image](https://user-images.githubusercontent.com/123749462/226633409-134c955d-7082-40df-9369-b8e386c77f02.png)

- Drag and Drop Formula : 

![image](https://user-images.githubusercontent.com/123749462/225916331-e469509e-85cc-46bc-b86a-a0d3f2bada81.png)

![image](https://user-images.githubusercontent.com/123749462/226633489-9090dbdf-5ece-4eeb-8df3-9e1cf8e015c1.png)

- Configuration de notre formule : 
  - On va ajouter une nouvelle colonne ``Date d'arrivée (Check in date)`` et on va predre cette formule : 
  ```
  [Jour_mois_date_arrivée]+" "+ [Mois_date_arrivée]+" "+[Année_date_arrivée]
  ```
  ![image](https://user-images.githubusercontent.com/123749462/226634121-e924c1dc-2326-4c0b-b467-440444f88ed5.png)

- Exécuter le noeud de formula :

![image](https://user-images.githubusercontent.com/123749462/226634471-9fe75c2a-e8f8-4dbb-a3a1-9a59819f3d6a.png)

- Drag and drop le noeud DateTime : Parse > DateTime : 

![image](https://user-images.githubusercontent.com/123749462/226353469-50f01aa8-1f53-4ace-a97f-b0ae1dbc56f0.png)

![image](https://user-images.githubusercontent.com/123749462/226634610-b3903cf3-96b1-402f-bf6c-9273ee2cd2c2.png)
- Configurer le Noeud DateTime : 

![image](https://user-images.githubusercontent.com/123749462/226358616-b9af9328-6be5-46c8-bc70-f0c28984f746.png)

- Exécuter le noeud DateTime :

![image](https://user-images.githubusercontent.com/123749462/226636461-020137ad-5cb6-4bd4-83e6-c320196feb2f.png)

- Drag and Drop un autre noeud : Formula 

![image](https://user-images.githubusercontent.com/123749462/226638064-3d37a167-d80b-46bb-954f-8f7ff62148b9.png)

- Configuration de notre formule : 
  - On va ajouter une nouvelle colonne ``Longueur du séjour`` et on va predre cette formule : 
  ```
  DateTimeDiff([Date d'arrivée revue],[Date_réservation_status],"days")*-1

  ```
  - Data type : Int16

![image](https://user-images.githubusercontent.com/123749462/226473445-44484a03-6745-4000-9072-15b15d3280a3.png)

- Exécuter le noeud de formula :

![image](https://user-images.githubusercontent.com/123749462/226639855-f84b9bc1-5164-4e3c-be12-dcd385e9d514.png)

- Drag and Drop le noeud Filter :

![image](https://user-images.githubusercontent.com/123749462/226640307-d51c4614-23e6-4c76-80b7-efbb0d61e2ff.png)

- On va configurer notre filtre avec un filtre basique sur la longueur du séjour :

![image](https://user-images.githubusercontent.com/123749462/226494446-1406bd6b-9832-42a8-b7f8-f031d6b83484.png)

- Exécuter ce filtre : 

![image](https://user-images.githubusercontent.com/123749462/226641057-27c80df4-6040-4a94-9125-a0f12a6fdddb.png)

- Drag and Drop le noeud Summarize : Transform > Summarize 

![image](https://user-images.githubusercontent.com/123749462/226377095-ba283b84-d015-46c0-91ed-10a56ecace7e.png)

![image](https://user-images.githubusercontent.com/123749462/226641312-bd4b3bf2-5c6e-4bcd-b3bb-bd5c7b376179.png)

- On va configurer notre noeud Summarize 
  - 1ère étape : 

  ![image](https://user-images.githubusercontent.com/123749462/226643865-751188c4-64e4-46b2-9c58-ca1affbce5e4.png)
  
  - 2ème étape : 

  ![image](https://user-images.githubusercontent.com/123749462/226648010-9a1a95b5-e9ee-403d-a70a-fd0eb31898a5.png)
  
  - 3ème étape :

  ![image](https://user-images.githubusercontent.com/123749462/226650025-679e0e58-341e-48e2-808c-630165b7313e.png)
 
