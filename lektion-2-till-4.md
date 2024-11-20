## Del 1: Skapa och modifiera tabeller

1. Skapa en tabell `persons` som har två kolumner: `name` (text) och `age` (nummer)
2. Skapa en tabell `products` som har tre kolumner: `name` (text), `description` (text), `price` (nummer)
3. Lägg in tre rader i `persons` tabellen med följande värden:
   - Ironman, 47
   - Superman, 33
   - Batman, 26
4. Lägg in tre rader i `products` tabellen:
   - Bread, "Fresh whole grain bread", 25.50
   - Milk, "Organic whole milk", 12.99
   - Coffee, "Dark roast coffee beans", 89.00
5. Lägg till en ny kolumn `category` (text) i `products` tabellen och uppdatera befintliga produkter med valfria kategorier

## Del 2: Grundläggande queries

6. Skapa en tabell `movies` med kolumnerna: `title` (text), `year` (nummer), `rating` (nummer från 1-5). Lägg in minst 30 filmer med olika årtal och betyg. Tips: använd AI för att generera dessa.
7. Skriv queries för att visa:
   - Alla filmer
   - Alla filmer, men endast med `title`
   - Alla filmer, men endast med `title` och `rating`
   - Alla filmer med rating högre än 3
   - Alla filmer, men endast `title`, för 2020, med rating högre än 3
   - Antal filmer per årtal
   - Alla filmer sorterade efter år (äldst först)
8. Skapa en tabell `books` med kolumnerna: `title` (text), `author` (text), `pages` (nummer), `published` (datum). Lägg in minst 3 böcker.
9. Skriv en query som visar böcker publicerade efter år 2000 och som har fler än 300 sidor.
10. Skapa en tabell `employees` med: `name`, `department`, `salary`. Lägg in 6 anställda i olika avdelningar med olika löner. Skriv sedan en query som visar genomsnittlig lön per avdelning.

## Del 3: Svårare queries

11. Skapa en tabell `orders` med kolumnerna:
    - `id` (serienummer som auto-ökar)
    - `customer_name` (text)
    - `order_date` (datum)
    - `total_amount` (nummer)
      Lägg in 5 olika orders och skriv sedan en query som visar alla orders från den senaste månaden (datumet för query:n skall inte hårdkodas.)

12. Modifiera `employees` tabellen genom att lägga till kolumnen `hire_date`. Uppdatera alla befintliga anställda med olika anställningsdatum. Skriv en query som visar alla som varit anställda längre än 2 år (datumet för query:n skall inte hårdkodas.)

13. Skapa en tabell `tasks` med:
    - `title` (text)
    - `status` (text: 'pending', 'in_progress', eller 'completed')
    - `created_at` (datum)
    - `completed_at` (datum, kan vara null)
      Lägg in 7 olika tasks och skriv en query som visar hur många tasks som finns i varje status.

14. Skapa en tabell `students` med:
    - `name` (text)
    - `grade` (nummer mellan 1-100)
    - `course` (text)
      Lägg in 10 studenter i olika kurser med olika betyg. Skriv en query som visar genomsnittsbetyget per kurs, men bara för kurser med minst 2 studenter.

## Del 4: Avancerade koncept

15. Skapa en tabell `articles` med:
    - `title` (text)
    - `content` (text)
    - `views` (nummer)
    - `published` (datum)
      Lägg in 8 artiklar och skriv en query som visar de 3 mest visade publicerade artiklarna.

16. Uppdatera `products` tabellen (från övning 2) genom att lägga till en kolumn `stock_quantity`. Skriv en query som visar alla produkter med mindre än 5 i lager och ett pris över 100.

17. Skapa en tabell `weather_data` med:
    - `date` (datum)
    - `temperature` (nummer)
    - `rainfall` (nummer)
      Lägg in väderdata för de senaste 10 dagarna. Skriv en query som visar genomsnittstemperaturen för dagar med regn (rainfall > 0).

18. Skapa en tabell `user_logins` med:
    - `user_id` (nummer)
    - `login_time` (datum)
    - `success` (boolean)
      Lägg in 15 loginförsök och skriv en query som visar användare med fler än 2 misslyckade inloggningar.

19. Skapa en tabell `transactions` med:
    - `account_id` (nummer)
    - `type` (text: 'deposit' eller 'withdrawal')
    - `amount` (nummer)
    - `transaction_date` (datum)
      Lägg in minst 10 transaktioner och skriv en query som visar det totala saldot per konto (summan av insättningar minus summan av uttag).

## Bonusövningar för extra utmaning

20. Skapa tabellerna `categories` och `products_v2`:

```sql
CREATE TABLE categories (
    id SERIAL PRIMARY KEY,
    name TEXT,
    description TEXT
);

CREATE TABLE products_v2 (
    id SERIAL PRIMARY KEY,
    name TEXT,
    price NUMERIC(10,2),
    category_id INTEGER REFERENCES categories(id)
);
```

Lägg in data i båda tabellerna och skriv en query som visar alla produkter med sina kategorier, även kategorier som inte har några produkter.

21. Uppdatera `weather_data` (från övning 17) tabellen för att inkludera `location` (text). Skriv en query som visar den varmaste och kallaste temperaturen per plats, men bara för platser med minst 3 mätningar.

22. Modifiera `user_logins` (från övning 18) tabellen för att inkludera `device_type` (text). Skriv en query som visar procentandelen lyckade inloggningar per enhetstyp.
