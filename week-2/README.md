-- Week 2 – Finding Duplicates with GROUP BY and HAVING --

- `GROUP BY` – grouping rows that share the same value.
- `COUNT(*)` – counting the rows in each group.
- `HAVING` – filtering groups after they are created.
- `ORDER BY ... DESC` – showing the largest values first.

**Important difference: WHERE vs HAVING**

- `WHERE` filters individual rows **before** grouping.
- `HAVING` filters groups **after** grouping.


-- Group Project --
# Sales – Müügiandmete puhastamine 

> **Staatus:** Andmekvaliteedi kontroll tehtud · Parandused alles tegemata

## Kokkuvõte

Müügiandmetes on **5 116 liigset duplikaatrida** ja **1 487 tehingul puudub kliendi ID**. Lisaks on **50 tehingut** kuupäevaga pärast andmestiku eeldatavat lõppu (28.02.2025). Kõigil tehingutel on müügikuupäev ja müügisumma olemas.

## Kontrolli tulemused

| Kontroll | Tulemus | Osakaal | Staatus |
|---|---:|---:|:---:|
| Kontrollitud müügitehinguid | 15 234 | 100% | ℹ️ |
| Korduvaid arveid (`invoice_id`) | 4 013 | 26,3% | ⚠️ |
| Liigseid duplikaatridu | 5 116 | 33,6% | ❌ |
| Puuduvaid kliendi ID-sid (`customer_id` IS NULL) | 1 487 | 9,8% | ❌ |
| Puuduvaid müügikuupäevi | 0 | 0% | ✅ |
| Puuduvaid müügisummasid | 0 | 0% | ✅ |
| Kuupäevi pärast tänast kuupäeva | 0 | 0% | ✅ |
| Kuupäevi pärast andmete eeldatavat lõppu (28.02.2025) | 50 | 0,3% | ⚠️ |

*Osakaalud on arvutatud kontrollitud tehingute koguarvust (15 234).*

## Peamised leiud

1. **Duplikaadid:** 5 116 liigset rida, mis on ligikaudu kolmandik kogu andmestikust.
2. **Puuduvad kliendiviited:** 1 487 tehingul on `customer_id` NULL.
3. **Ootamatud kuupäevad:** 50 tehingut jääb pärast andmestiku eeldatavat lõppu (28.02.2025).
4. **Täielikud väljad:** müügikuupäev ja müügisumma on kõigil tehingutel olemas.
