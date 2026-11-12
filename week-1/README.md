-- Week 1 – Supabase SQL Practice --

**Key SQL concepts practised**

CREATE TABLE – creating database tables.

SELECT – retrieving data.

FROM – choosing a table.

ORDER BY – sorting results.

ASC and DESC – ascending and descending order.

LIMIT – controlling how many rows are returned.

AS – renaming a column in query results.

_____________________________________________________________________________________________________________________________

-- Group Project --

**Sales (D)**

- **Unikaalseid müügikanaleid (2):** online, pood
- **Unikaalseid asukohti (3):** Tallinn, Pärnu, Tartu
- **Lisaks asukoht:** NULL (NULL: füüsilise kaupluse asukoha info puudub.)
- **Makseviise (3):** järelmaks, kaart, sula
- **Tehinguid ilma kaupluse asukohata:** 5204
- **Peamine leid:** 5204 füüsilise kaupluse asukohata tehingut on märgitud unikaalsete asukohtade loendis väärtusega NULL. Kõik need ostud on tehtud veebis (online). Edasises müügianalüüsis oleks mõistlik käsitleda veebimüüki ja füüsiliste kaupluste müüki eraldi, et saada mõlema müügikanali tulemustest selgem ülevaade. Probleeme on ka andmekvaliteediga: Tulemuste hulgas esineb korduvaid tehinguid ja puuduvaid kliendiandmeid.
