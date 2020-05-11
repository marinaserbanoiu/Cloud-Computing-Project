 # Proiect Cloud-Computing
                                    
 ### Introducere

Aplicația dezvoltată de mine vine în ajutorul iubitorilor de cărți, oferindu-le acestora posibilitatea de a-și creea o listă de cărți favorite și de a putea cauta informații despre o anumită carte, prin intermediul unei bare de cautare.

 ### Descriere problemă
 O problemă cu care m-am confruntat și eu, ca și cititor a fost aceea că nu puteam să îmi amintesc uneori ce cărți am citit mai demult sau ce evenimente erau prezentate într-o anumită carte.
 Din acest motiv, m-am gândit să creez o aplicație care să gestioneze informațiile despre cărțile citite, dându-ți posibilitatea de a adăuga în listă titlul cărții respective, autorul, subiectul cărții sau o descriere scurtă în care să poți spune câteva cuvinte despre aceea carte. 
 Consider că este foarte util pentru un cititor să poată să își noteze undeva câteva detalii despre o carte citită și să aibă posibilitatea de a revedea oricând informații despre acele cărți. 
 ### Descriere API
 Aplicația are la bază 2 API-uri, unul creat de mine, prin care au fost evidențiate metodele HTTP și un API deja existent care a fost integrat în interiorul aplicației.
 Primul API, cel creat de mine, este folosit pentru a adăuga o carte în listă, a șterge și a salva informațiile adăugate.
 Acest API are în spate o bază de date MySql numită info_books, care are în alcătuirea sa tabela books.
 Cel de-al doilea API folosit în realizarea aplicației este Google Books API. Acest API este util deoarece iți dă posibilitatea să găsești informații despre anumite cărți: recenzii, un scurt rezumat etc. În aplicația mea, prin intermediul acestuia am reușit să creez bara de search, prin care utilizatorul poate căuta o anumită carte dupa titlul său exact sau după un cuvânt semnificativ.
 
 ### Flux de date
 Aplicația are la bază un server creat cu ajutorul Node.js și ExpressJs. Datele sunt stocate într-o bază de date MySql și pot fi accesate prin metodele HTTP (POST, GET, UPDATE, DELETE). Accesul la baza de date se realizează automat prin biblioteca Sequelize.
Utilizatorul va putea adăuga o carte, actualiza, șterge și afișa toate cărțile adăugate până atunci.
Atunci când utilizatorul face o cerere pe server de tip CRUD, serverul web va prelucra această cerere și va returna un conținut pe care browserul îl va interpreta și îl va afișa utilizatorului în format JSON,XML etc.
 ### 1) Exemple de request-response
 ```
 { 
    "hello":"everyone"
 }
 ```
 
  ![ex1](example1.PNG) 
   
 ```
 {
     "title": "Silent Patient";
     "author":"Alex Michaelides"
 }
 ```
 ![ex1](example2.PNG)
 ```
 {
     "Smartphone":"LenovoP70A";
     "Price":"800 Ron";
     "Guarantee":"1 year"
 }
 
 ```
 ![ex1](example3.PNG)  
 ### 2) Metode HTTP
  #### POST 
  Această metodă presupune crearea unor noi date pe server. În imaginea de mai jos, este reprezentat un request de tip POST, prin intermediul programului Postman.
  
 
 
 ### Referinte:
 https://developers.google.com/books/docs/v1/getting_started   
 https://www.w3schools.com/default.asp
