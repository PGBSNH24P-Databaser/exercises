## Del 1: Databastyper

1. Förklara skillnaden mellan följande databastyper:
   - Relationsdatabaser
   - NoSQL-databaser
   - In-memory databaser

2. Lista en fördel och en nackdel med relationsdatabaser jämfört med NoSQL-databaser.

3. Vilken databastyp och mest lämplig och anpassad för följande scenarios (motivera):
   - En e-handelsbutik med produkter, ordrar och kunder (e.g. Amazon, Elgiganten)
   - En realtids-chattapplikation (e.g. Discord, Teams)
   - Ett system för lagring av sensormätningar från IoT-enheter (e.g. temperatur)

4. Para ihop följande databaser med deras databastyper (var gärna specifik):
   - MongoDB
   - PostgreSQL
   - Redis

5. Ge flera exempel på specifika databaser av följande typer:
   - Relationsdatabaser (SQL)
   - Document-databaser
   - NoSQL-databaser
   - In-memory databaser

6. Ge minst två anledningar till varför PostgreSQL är bättre än MySQL.

## Del 2: Begrepp och koncept

7. Vad kan SQL rader jämföras med i C#?
8. Vad kan SQL kolumner jämföras med i C#?
9. Vad kan SQL constraints jämföras med i C#?
10. Vad kan SQL tabeller jämföras med i C#?
11. Förklara vad en modell är.
12. Vad är det för skillnad på en query och en rad (row)?
13. Vilket nyckelord används i SQL för att hämta data med en query?
14. Förklara vad följande termer betyder och ge ett exempel på varje:

- DML (Data Manipulation Language)
- DDL (Data Definition Language)
- DCL (Data Control Language)

15. Para ihop följande termer med rätt beskrivning:

Termer:

- ACID
- Schema
- Primary Key
- Foreign Key
- Index
- Query
- Transaction

Beskrivningar:

- En strukturerad fråga för att hämta eller modifiera data
- En serie databas-operationer som behandlas som en enhet
- En referens till en primary key i en annan tabell
- En datastruktur som förbättrar sökhastigheten
- Egenskaper som garanterar databas-integritet
- Den logiska strukturen för hur data organiseras
- Ett unikt identifierande värde för varje rad i en tabell

16. För följande data, identifiera lämpliga PostgreSQL datatyper och förklara ditt val:

- Personnummer
- E-postadress
- Telefonnummer
- Födelsedatum
- Prisinformation
- Status (aktiv/inaktiv)

17. Vad är en SQL relation?

## Del 3: Docker och PostgreSQL

18. Vad används Docker till?

19. Hur laddar man ned PostgreSQL med Docker?
20. Hur skapar man en PostgreSQL databas med Docker?
21. Vad är images?
22. Vad är containers?

23. Vad är Docker kommandot för att starta upp en container som tidigare har stoppats?

24. Lista stegen att ta för att komma åt en PostgreSQL databas som ligger i en container (exempelvis för att skapa en tabell. hints: exec, psql.)

25. Lista stegen för att:

- Kontrollera om en Docker-container körs
- Stoppa en körande container
- Ta bort en container
