## Del 1: Grundläggande joins

### 1. Klasser

Skapa tabellerna:

- `teachers` (teacher_id, name, subject)
- `classes` (class_id, name, teacher_id)

Lägg till 4 lärare och ge varje lärare 1-2 klasser.
Lista alla klasser med lärarens namn (klass + lärare).

### 2. Böcker

Skapa en tabell `authors` med kolumnerna:

- `id` (primary key)
- `name` (text)
- `birth_year` (nummer)

Skapa också en tabell `books` med kolumnerna:

- `id` (primary key)
- `title` (text)
- `author_id` (foreign key som refererar till `authors`)
- `publication_year` (nummer)
- `price` (nummer)

Lägg sedan till minst 5 författare och 10 böcker med korrekt relation mellan dem.
Skriv sedan en query som visar alla böcker med tillhörande författarnamn.

### 3. E-handel

Skapa två tabeller med en enkel relation:

- `customers` (customer_id, name, email)
- `orders` (order_id, customer_id, order_date, total_amount)

Lägg till 5 kunder och 10 ordrar.
Skriv en query som visar alla ordrar med kundernas namn (order + kund).

### 4. Artiklar

Skapa två tabeller:

- `categories` (category_id, name)
- `articles` (article_id, title, category_id, published_date)

Lägg till 3 kategorier och 6 artiklar.
Visa alla artiklar med sina kategorier.

### 5. Butik

Skapa tabellerna:

- `departments` (department_id, name)
- `products` (product_id, name, price, department_id)

Lägg till 3 avdelningar och 9 produkter.
Visa alla produkter grupperade efter avdelning.

### 6. Länder och städer

Skapa tabellerna:

- `countries` (country_id, name, population)
- `cities` (city_id, name, country_id, population)

Lägg till 4 länder och 12 städer.
Lista alla städer med tillhörande land.

## Del 2: Komplexa relationer

### 7. E-handel

Skapa ett system för en e-handelsbutik med följande tabeller:

- `customers` (id, name, email)
- `orders` (id, customer_id, order_date, status)
- `products` (id, name, price, stock)
- `order_items` (order_id, product_id, quantity, price_at_time)

Skriv sedan queries för att visa:

- Alla ordrar med kundnamn och totalsumma
- Produkter som aldrig har beställts
- Kunder som har handlat för mer än 1000 kr totalt

### 8. Anställda

Implementera en self-referencing relation:
Skapa en tabell `employees` med:

- `employee_id` (primärnyckel)
- `name` (text)
- `manager_id` (främmande nyckel som refererar tillbaka till employees)

Skriv en query som visar varje anställd med sin chefs namn.

### 9. Blogg

Skapa ett bloggsystem med:

- `users` (id, username, email)
- `posts` (id, user_id, title, content, created_at)
- `comments` (id, post_id, user_id, content, created_at)
- `post_tags` (post_id, tag_id)
- `tags` (id, name)

Skriv queries för att visa:

- Alla posts med antal kommentarer (post + count)
- Alla användare och antal posts de har skrivit
- Posts med sina tags
- De 3 mest använda taggarna
