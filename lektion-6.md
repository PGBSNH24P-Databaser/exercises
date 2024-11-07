## Del 1: Grundläggande normalisering

### 1. Ordrar och produkter

Utgå från denna icke-normaliserad tabell:

```
Orders (
    order_id, 
    customer_name, customer_email, customer_phone,
    product_name, quantity, price_per_unit, total_price
)
```

Övningar:

- Identifiera problemen med denna struktur
- Normalisera till 1NF, 2NF och 3NF
- Skapa normaliserade tabeller

### 2. Skolschema

Utgå från denna ofullständiga tabell:

```
Schedule (
    class_name, teacher_name, teacher_email, teacher_phone,
    room_number, room_building, day_of_week, start_time, end_time
)
```

Övningar:

- Skapa separata tabeller för lärare, rum och lektioner
- Skapa fler, och lämpliga, nycklar/kolumner

### 3. Bokningssystem

Utgå från denna icke-normaliserad tabell:

```
Bookings (
    booking_id,
    guest_name, guest_email, guest_phone,
    room_type, room_price, room_description,
    check_in_date, check_out_date, total_nights, total_price
)
```

Övningar:

- Identifiera beroenden
- Normalisera till 3NF (skapa tabeller, kolumner m.m)

## Del 2: Avancerad normalisering

### 4. Receptdatabas

Normalisera följande tabell:

```
Recipes (
    recipe_name,
    category, cooking_time,
    ingredient1_name, ingredient1_amount, ingredient1_unit,
    ingredient2_name, ingredient2_amount, ingredient2_unit,
    ingredient3_name, ingredient3_amount, ingredient3_unit,
    instructions
)
```

### 5. Sporter

Normalisera följande tabell:

```
Teams (
    team_name, league_name, league_division,
    coach_name, coach_phone, coach_email,
    player1_name, player1_position, player1_number,
    player2_name, player2_position, player2_number,
    home_arena, arena_capacity, arena_city
)
```
