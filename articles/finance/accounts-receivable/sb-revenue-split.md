---
title: Tilauslaskutuksen tuoton jakomallit
description: Tässä artikkelissa kuvataan, miten tuottojen jakomallit määritetään nimikkeille, jotka myydään nippuina.
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
ms.openlocfilehash: 145ca6e6f0673a5a09fe9a23cf5e163421617fd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904756"
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

## <a name="additional-revenue-split-information"></a>Tuoton jaon lisätiedot

Kun lisäät nimikkeen, joka on osa tuoton jakoa, ota huomioon seuraavat tiedot: 

- Päätason summa ei voi olla lykätty.
- Alanimikkeiden aloituspäivä-, päättymispäivä-, määrä-, yksikkö-, toimipaikka- ja varastoarvot perustuvat päänimikkeeseen. Näitä alanimikkeiden arvoja ei voi muuttaa. Kaikki muutokset on tehtävä päänimikkeeseen. 
- Hinnoittelumenetelmä on **Kiinteä**, ja sitä ei voi muuttaa.
- Alanimikkeitä voi lisätä tai poistaa.
- Pää- ja alanimikkeissä on käytettävä samaa nimikeryhmää. 
- Alanimikkeillä voi olla jokin seuraavista asetuksista:

    - Kentät **Laskutustiheys** ja **Laskutusvälit** on määritetty samaan arvoon kuin päänimike. 
    - Kenttä **Laskutustiheys** on märitetty arvoon **Kerran**. Tässä tapauksessa **Laskutusvälit**-kenttä on määritetty automaattisesti arvoon **1**. 

- Alanimikkeiden nettosummien summa on yhtä suuri kuin päätason summa. Kohdistusmenetelmä on **Nollasumma**, sekä alanimikemäärien summa että päätason summa on 0 (nolla). 

    > [!NOTE]
    > Jos kohdistusmenetelmä on **Ylätason nollasumma**, alanimikkeiden summa (joka ei ole nolla) ei ole sama kuin päätason summa, joka on 0 (nolla). Tätä kohdistusmenetelmää käytetään sisäisissä tarkoituksissa, jotta työntekijät näkevät alanimikkeet. Asiakkaat näkevät kuitenkin vain päänimikkeen.

- Jos myyntitilauksen usean elementin järjestelyn tyyppi on **Yksittäinen**, vastaava usean elementin tuoton kohdistuksen tapahtumarivi luodaan, kun pää- ja alanimikkeet lisätään. 
- Jos tuoton jaon kohdistusmenetelmä on **Samat summat** ja päätason määrä on muutettu, kaikkien alarivien määrät lasketaan uudelleen. 
- Jos tuoton jaon kohdistusmenetelmä on **Muuttuva summa**, tapahtuu seuraavaa:

    - Päänimikkeen nettosumma tulee näkyviin **Päätason summa** -sarakkeeseen. Arvoa voi muokata. Yksikköhinta, nettosumma ja alennus ovat kuitenkin 0 (nolla), eikä niitä voi muokata.
    - Alanimikkeiden yksikköhinta on 0 (nolla). Voit muokata yksikköhintaa tai nettosummaa. Kun muokkaat yhtä arvoa, toinen arvo päivittyy automaattisesti.

- Jos tuoton jaon kohdistusmenetelmä on **Prosentti**, tapahtuu seuraavaa:

    - Päänimikkeen nettosumma tulee näkyviin **Päätason summa** -sarakkeeseen. Arvoa voi muokata. Yksikköhinta, nettosumma ja alennus ovat kuitenkin 0 (nolla), eikä niitä voi muokata. 
    - Alanimikkeiden nettosumma lasketaan: *Prosentti* &times; *Päätason summa*.

- Jos tuoton jaon kohdistusmenetelmä on **Sama summa**, tapahtuu seuraavaa:

    - Päänimikkeen nettosumma tulee näkyviin **Päätason summa** -sarakkeeseen. Arvoa voi muokata. Yksikköhinta, nettosumma ja alennus ovat kuitenkin 0 (nolla), eikä niitä voi muokata. 
    - Alanimikkeiden nettosumma lasketaan jakamalla pääsumma tasaisesti kaikkien alanimikkeiden kesken. 
    - Jos alanimikkeitä poistetaan tai lisätään, nettosumma ja yksikköhinnat lasketaan uudelleen niin, että kaikkien alarivien summat ovat samat. 
    - Jos pääsummaa ei voi jakaa tasan, viimeisen alanimikkeen nettosumma ja yksikköhinta saattavat olla hieman pienemmät kuin muiden alanimikkeiden nettosumma ja yksikköhinta. 

- Jos tuoton jaon kohdistusmenetelmä on **Nollasumma**, tapahtuu seuraavaa:

    - Yksikköhintaa, nettosummaa ja alennusta voi muokata. Päätason summa on 0 (nolla), eikä sitä voi muokata. 
    - Alanimikkeiden määrä-, yksikkö-, toimipaikka- ja varastoarvot perustuvat päänimikkeeseen. Näitä alanimikkeiden arvoja ei voi muuttaa. Kaikki muutokset on tehtävä päänimikkeeseen. 
    - Alanimikkeiden yksikköhinta ja nettohinta ovat 0 (nolla), eikä niitä voi muokata. 

- Jos tuoton jaon kohdistusmenetelmä on **Ylätason nollasumma**, tapahtuu seuraavaa:

    - Päänimikkeen yksikköhinta, päätason määrä ja nettosumma ovat 0 (nolla).
    - Laskutusaikataulussa alarivit näkyvät manuaalisesti lisättyinä, ja kaikki arvot päivitetään valitun laskutusaikatauluryhmän perusteella. Näitä arvoja voi muokata. Alanimikkeiden osalta voit käyttää vaihtoehtoja **Eskalointi ja alennus** ja **Hinnoittelun lisäasetukset** käyttämällä kenttiä **Määritetty määrä**, **Yksikköhinta**, **Alennus** ja **Nettosumma** kohdassa **Näytä laskutustiedot**. 
    - Myyntitilauksessa alarivien alennus ja alennusprosentti ovat 0 (nolla). 
    - Pää- ja alanimikkeiden laskutustiheys voidaan muuttaa, ja jokaisella rivillä voi olla eri tiheys. Päänimike päivitetään kuitenkin automaattisesti niin, että se käyttää alariviensä lyhyintä tiheyttä. Tuoton jaolla on esimerkiksi kaksi alanimikettä, joista yksi käyttää **Kuukausittain**-laskutustiheyttä ja toinen **Vuosittain**-laskutustiheyttä. Tässä tapauksessa päänimikkeen laskutustiheydeksi päivitetään **Kuukausittain**.
