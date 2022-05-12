---
title: Tilauslaskutuksen tuoton jakomallit
description: Tässä aiheessa kuvataan, miten tuottojen jakomallit määritetään nimikkeille, jotka myydään nippuina.
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 5c2eb6c8e18770eb149c445f662ab7a90aad81a7
ms.sourcegitcommit: 367e323bfcfe41976e5d8aa5f5e24a279909d8ac
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2022
ms.locfileid: "8660452"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Tilauslaskutuksen tuoton jakomallit

**Tuottojen jakomalli** -sivulla voit määrittää mallit tuottojen jakoa varten. Tuottojen jako koostuu päänimikkeestä, jolla on alinimikkeitä. Tämäntyyppinen nimike myydään usein asiakkaille yhtenä nimikkeenä tai nippuna.

Tietokonenimikkeen voi luoda esimerkiksi seuraavasti:

- **Päänimike:** Tilaus – Silver
- **Rivinimikkeet/alinimikkeet:**

    - Tuki
    - Ylläpito
    - Käyttöoikeus

Kun luot päänimikkeen, seuraavat rajoitukset on hyvä pitää mielessä:

- Nimike voidaan määrittää päänimikkeeksi vain kerran.
- Päänimike voidaan valita samaan malliin alinimikkeeksi.
- Kelvollinen malli vaatii vähintään yhden alinimikkeen.
- Nimike voidaan määrittää alinimikkeeksi useammalle kuin yhdelle nippunimikkeelle.
- Kunkin pää- ja alitason suhteen on oltava yksilöllinen.

## <a name="create-a-parent-item-that-has-child-items"></a>Luo päänimike, jolla on alinimikkeitä

Jos haluat luoda päänimikkeen, jolla on alinimikkeitä, toimi seuraavasti.

1. Valitse **Tuottojen jakomalli** -sivulla **Uusi**.
1. Valitse päänimike **Päänimike**-kentässä. **Variantin numero**-kenttä päivittyy automaattisesti. Voit muuttaa arvoa tarpeen mukaan.
1. Valitse kohdistusmenetelmä **Kohdistusmenetelmä**‑kentästä.
1. Lisää alinimikkeitä valitsemalla **Komponenttinimikkeet**-luettelosta **Lisää**.
1. Jos olet valinnut **Kohdistusmenetelmä**-kentässä **Prosenttiosuus**, määritä prosentti **Prosentti**-kentässä.

    - Jos olet valinnut **Kohdistusmenetelmä**-kentästä **Saman summa**, **Prosentti**-kenttä päivittyy automaattisesti niin, että jokaisen nimikkeen prosenttiarvo on sama.
    - Jos **Kohdistusmenetelmä**-kentässä on valittu **Muuttuva summa**, **Ylätason nollasumma** tai **Nollasumma**, **Prosentti**-kentän arvo jää nollaksi **0** eikä sitä voi muuttaa.

1. Valitse **Tallenna**.

## <a name="fields"></a>Kentät

**Tuoton jaon malli**-sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|-------|-------------|
| Päänimike | Valitse nimikenumero. Tästä nimikkeestä tulee luotavan nippunimikkeen päänimike. |
| Tuotteen nimi | Tuotteen nimi. |
| Kohdistusmenetelmä | <p>Valitse kohdistustapa:</p><ul><li>**Yhtä suuri summa** – Kohdistusprosentit lasketaan automaattisesti ja tasan mallin kaikkien nimikkeiden kesken.</li><li>**Prosentti** – Kohdistukselle voidaan määrittää prosenttisumma. Kaikkien prosenttien summan on oltava 100.</li><li>**Muuttuva summa** – Lisättyjen alinimikkeiden nettosumma on 0 (nolla). Alinimikkeiden hinta on määritettävä tapahtumatasolla.</li><li>**Nollasumma** – Päänimike säilyttää yksikköhinnan ja nettosumman. Kaikkien alinimikkeiden nettosumma on 0 (nolla).</li><li>**Ylätason nollasumma** - Päänimikkeellä on kiinteä nettosumma 0 (nolla). Kaikkia alinimikkeitä käsitellään vakionimikkeinä. Oikeellisuustarkistusta ei tehdä sen varmistamiseksi, että alinimikkeiden summat vastaavat päänimikkeen summaa.</li></ul> |
| **Komponenttinimikkeet** | |
| Komponenttinimike | Valitse nimikenumero. Tämä nimike on alinimike. |
| Muuttujan numero | Valitse nimikkeen varianttinumero. |
| Tuotteen nimi | Tuotteen nimi. |
| Prosentti | <p>Välitavoitteen kohdistusprosentti:</p><ul><li>Jos **Kohdistusmenetelmä**-kentän arvoksi määritetään **Prosentti**, määritä prosenttiosuus.</li><li>Jos **Kohdistusmenetelmä**-kentän arvo on **Sama summa**, prosenttiosuus lasketaan automaattisesti siten, että mallin jokaisella nimikkeellä on sama prosenttiosuus.</li><li>Jos **Kohdistusmenetelmä**-kentän arvo on **Muuttuva summa**, **Ylätason nollasumma** tai **Nollasumma** , prosenttiarvo on 0 (nolla), eikä sitä voi muokata.</li></ul><p>Tämän kentän arvo voi olla mikä tahansa positiivinen luku väliltä 0 (nolla) – 100. Kaikkien prosenttien summan on oltava 100.</p> |
| Prosenttia yhteensä | <p>**Prosentti**-sarakkeen arvojen summa.</p><ul><li>Jos **Kohdistusmenetelmä**-kentän arvoksi määritetään **Sama summa** tai **Prosentti**, kaikkien prosenttiosuuksien kokonaissumman tulee olla 100.</li><li>Jos **Kohdistusmenetelmä**-kentän arvo on **Muuttuva summa**, **Ylätason nollasumma** tai **Nollasumma** , kokonaisprosenttiarvo on 0 (nolla).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Myyntitilauksen tuottojen jako

Toimi seuraavasti, kun haluat luoda myyntitilauksen, jolla on tuottojen jakoa varten määritetty nimike.

1. Luo **Myyntitilaus**-sivulla myyntitilaus.
2. Valitse tuottojen jakoa varten määritettyjen nimikkeiden rivillä **Tuottojen jako** -valintaruutu. Tästä nimikkeestä tulee päänimike. Jos malli on jo määritetty, alinimikkeet tulevat automaattisesti näkyviin luetteloon.
3. Voit lisätä lisää alinimikkeitä valitsemalla **Lisää tuoton jaon alituotto** ja valitsemalla lisättävän alinimikkeen.
4. Tallenna tilaus.

## <a name="revenue-split-with-billing-schedules"></a>Tuottojen jako ja laskutusaikataulut

Toimi seuraavasti, kun haluat luoda laskutusaikataulun, jolla on tuottojen jakoa varten määritetty nimike.

1. Luo **Kaikki/Aktiiviset laskutusaikataulut** -sivulla laskutusaikataulu.
2. Valitse tuottojen jakoa varten määritettyjen nimikkeiden rivillä **Tuottojen jako** -valintaruutu. Tästä nimikkeestä tulee päänimike. Jos malli on jo määritetty, alinimikkeet tulevat automaattisesti näkyviin luetteloon.
3. Voit lisätä lisää alinimikkeitä valitsemalla **Lisää tuoton jaon alituotto** ja valitsemalla lisättävän alinimikkeen.
4. Jatka laskutusaikataulun käsittelyn vaiheita.

> [!NOTE]
> Jos **Luo tuoton jako automaattisesti** -asetus on **Kyllä** **Toistuvat sopimuksen laskutusparametrit** -sivulla, seuraavat toiminnot tapahtuvat:
>
> - **Tuoton jako** -valintaruutu valitaan automaattisesti laskutusaikataulun rivillä, jos nimike on määritetty tuoton jakomallissa päänimikkeeksi.
> - Alinimikkeet lisätään automaattisesti myyntitilauksen tai laskutusaikataulun riville.
>
> Jos **Luo tuoton jako automaattisesti** -asetuksena on **Ei**, toimintatapa on kuvattu aiemmin.
