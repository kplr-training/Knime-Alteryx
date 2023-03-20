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


- Sélectionner hotel_booking.csv > cliquer sur ouvrir :

![image](https://user-images.githubusercontent.com/123749462/225898300-1d611080-5a1d-4cd3-bf60-6dfd4c2647ff.png)

- Cliquer sur Run pour éxecuter Input Data , Voilà ce que vous allez avoir comme output : 

![image](https://user-images.githubusercontent.com/123749462/225902097-ca0787a6-a501-4f60-bebc-b8c8b4633910.png)


![image](https://user-images.githubusercontent.com/123749462/225900590-dc149ea8-9bcd-48c9-83ec-303f39616648.png)

- Drag and Drop Filter : 

![image](https://user-images.githubusercontent.com/123749462/225903341-2e00af8d-bd8e-405e-a9a5-7dc0d0ce2cc3.png)

![image](https://user-images.githubusercontent.com/123749462/225906619-8c382864-100b-47bd-9c14-da598b36413f.png)


- On va configurer notre filtre avec un filtre basique sur les réservation qui n'ont  pas été annuler :

![image](https://user-images.githubusercontent.com/123749462/225912417-5f242a64-875e-4739-a474-140d8ffbdd1c.png)

- Exécuter ce filtre : 

![image](https://user-images.githubusercontent.com/123749462/225913012-304537e0-a280-4db8-bd3d-d76be8e48d78.png)

- Drag and Drop Formula : 

![image](https://user-images.githubusercontent.com/123749462/225916331-e469509e-85cc-46bc-b86a-a0d3f2bada81.png)

![image](https://user-images.githubusercontent.com/123749462/225916457-a0a958cd-89e9-41a3-a9ae-1fdb33c196df.png)

- Configuration de notre formule : 
  - On va ajouter une nouvelle colonne ``Date d'arrivée (Check in date)`` et on va predre cette formule : 
  ```
  [arrival_date_day_of_month]+" "+[arrival_date_month]+" "+[arrival_date_year]
  ```
- Exécuter le noeud de formula :

![image](https://user-images.githubusercontent.com/78825764/226331801-9f990ff3-292f-46b2-9091-e94275bc9189.png)

- Drag and drop le noeud DateTime : Parse > DateTime : 

![image](https://user-images.githubusercontent.com/123749462/226353469-50f01aa8-1f53-4ace-a97f-b0ae1dbc56f0.png)

![image](https://user-images.githubusercontent.com/123749462/226355559-2a149795-3b45-4448-acf4-de251a32b211.png)

- Configurer le Noeud DateTime : 

![image](https://user-images.githubusercontent.com/123749462/226358616-b9af9328-6be5-46c8-bc70-f0c28984f746.png)

- Exécuter le noeud DateTime :

![image](https://user-images.githubusercontent.com/123749462/226363365-e8d2803f-b2f3-4c55-a09f-0e81bfa0f6f9.png)

- Drag and Drop un autre noeud : Formula 

![image](https://user-images.githubusercontent.com/123749462/226363711-31079a14-9b82-4529-ae39-6458d6df3441.png)

- Configuration de notre formule : 
  - On va ajouter une nouvelle colonne ``Longueur du séjour`` et on va predre cette formule : 
  ```
  DateTimeDiff([Date d'arrivée revue],[reservation_status_date],"days")*-1
  ```

![image](https://user-images.githubusercontent.com/123749462/226366762-5c5e1e2d-7a78-450c-95b0-a1e624294073.png)

- Exécuter le noeud de formula :

![image](https://user-images.githubusercontent.com/123749462/226371791-b13bd0e7-6f53-490c-80c0-5c09b09dba6f.png)

- Drag and Drop le noeud Filter :

![image](https://user-images.githubusercontent.com/123749462/226372014-e79479b3-0b46-4942-8f21-150b5f311314.png)

- On va configurer notre filtre avec un filtre basique sur la longueur du séjour :

![image](https://user-images.githubusercontent.com/123749462/226374690-0e463f56-8962-4faf-b2cd-a5edb874dce9.png)
