# Week 3 – Roll B: Kadunud klientide tuvastamine

## Ülesanne
Leida kliendid, kes pole kunagi ostnud, kasutades `LEFT JOIN` päringut tabelite `customers` ja `sales` ühendamiseks.

## Tulemused

- Kliente kokku: **3 150**
- Kadunud kliente: **599 (19%)**
- Aktiivseid kliente: **2 551**
- Linnasid: **12**
- Kõige uuem registreerimiskuupäev kadunud klientide seas: **27.02.2025**

**Kõige rohkem kadunud kliente:**

| Linn | Kliente |
|---|---:|
| Tallinn | 231 |
| Tartu | 133 |
| Pärnu | 70 |

## Peamine leid ja soovitus

599 klienti pole kunagi ostnud. Soovitan käivitada Tallinnas, Tartus ja Pärnus personaalsed turunduskampaaniad ning pakkuda esimese ostu sooduskoodi, et julgustada kliente ostu sooritama.

**Äriline järeldus Annale:**
Kadunud klientide arv kasvas märgatavalt alates 2023. aasta teisest poolest ning saavutas kõrgeima taseme 2024. aasta detsembris ja 2025. aasta jaanuaris. See võib viidata sellele, et registreerimiskampaaniad tõid palju uusi kliente, kuid ei muutnud neid ostjateks. Soovitan analüüsida nende perioodide kampaaniaid ning pakkuda uutele klientidele tervituskirju ja esimese ostu soodustusi.

Oluline: need on kadunud klientide arvud, mitte ostukonversiooni määrad. Et teada, kas kampaaniad tegelikult halvemini toimisid, tuleks võrrelda ka kõigi samal kuul registreerunud klientide arvu

## Failid
- `week3_roll_b_kadunud_kliendid.sql`
- Supabase'i tulemuste tabelid:
-- 1. Leia kõik kliendid, kellel pole ühtegi ostu - 599
-- 2. Loe kokku kadunud klientide arv - 599
-- 3. Kadunud kliendid linnade kaupa -
| city       | kadunud_kliente |
| ---------- | --------------- |
| Tallinn    | 231             |
| Tartu      | 133             |
| Pärnu      | 70              |
| Narva      | 32              |
| Valga      | 25              |
| Kuressaare | 18              |
| Viljandi   | 18              |
| Haapsalu   | 17              |
| Rakvere    | 17              |
| Võru       | 15              |
| Jõhvi      | 12              |
| Paide      | 11              |
-- 4. Millal kadunud kliendid registreerusid? - 27.05.2025
-- 5. Võrdle kadunud ja aktiivsete klientide arvu
| staatus               | kliente |
| --------------------- | ------- |
| Aktiivne (on ostnud)  | 2551    |
| Kadunud (pole ostnud) | 599     |


## Tiimi ühine töö
[UrbanStyle-ladu – GitHub](https://github.com/vvaiko1/UrbanStyle-ladu)
