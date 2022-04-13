---
title: Välitavoitemallit
description: Tässä aiheessa kerrotaan, miten tilauslaskutuksen tavoitteisiin perustuva laskutus -toiminto määritetään.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: 863ec55c8ba2fcc9d0e624fcca06f4491ce839ac
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462892"
---
# <a name="milestone-billing"></a>Tavoitteisiin perustuva laskutus

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, kuinka voit määrittää malleja tilauslaskutuksen tavoitteisiin perustuva laskutus -toiminnolle. Voit määrittää tavoitemallin kullekin riville kohdistusprosentin tai summan. Voit liittää tavoitemallin laskutusaikatauluun nimikkeitä, jotka käyttävät tavoitelaskutustoimintoja.

## <a name="add-a-template"></a>Lisää malli

Voit lisätä tavoitemallin seuraavasti.

1. Siirry **Tilauslaskutus \> Toistuvan sopimuksen laskutuksen \> Asetukset \> Tavoitemallit**.
2. Valitse **Uusi**.
3. Anna tavoitemallin yksilöivä tunnus **Tavoitemalli**-kenttään.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Valitse kohdistusmenetelmä **Kohdistusmenetelmä**‑kentästä.
6. Valinnainen: Määritä **Kokonaissumma**-kenttään mallin kokonaissumma.
7. Valitse **Lisää** lisätäksesi rivin. Valitse sitten uuden rivin nimiketunnus **Nimiketunnus**-kentästä.
8. Noudata yhtä näistä vaiheita sen arvon mukaan, jonka valitsit **Kohdistustapa**-kentässä:

    - Jos olet valinnut kohdistusmenetelmäksi **prosenttiosuuden**, määritä kunkin rivin kohdistusprosentti **Prosentti**-kenttään. Jos määrität prosenttilukuja, **Kokonaisprosentti**-kentässä näkyvien prosenttien summan on oltava **100**.
    - Jos olet valinnut kohdistusmenetelmäksi **Muuttujan summan**, määritä kunkin rivin summa **Summa**-kenttään.
    - Jos olet valinnut kohdistusmenetelmäksi **Sama summa**, summaa ei tarvitse määrittää. Ohjelma päivittää kullekin riville oikean prosenttiosuuden ja summan malliin lisätyn nimikemäärän perusteella.

9. Valitse **Tallenna**.

## <a name="delete-a-template"></a>Poista malli

Voit poistaa tavoitemallin seuraavasti.

1. Valitse yksi tai useampi poistettava rivi ja valitse sitten **Poista**.
2. Kun järjestelmä pyytää vahvistamaan valinnan, valitse **Kyllä**.

## <a name="milestone-template-fields"></a>Tavoitemallin kentät

**Tavoitemalli**-sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|-------|-------------| 
| Välitavoitemalli | Tavoitemallin yksilöivä tunnus. |
| Kuvaus | Tavoitemallin kuvaus. |
| Kohdistusmenetelmä | <p>Valitse kohdistustapa:</p><ul><li>**Valmistumisprosentti** – Kullekin riville käytetään kumulatiivista valmistumisarvoa.</li><li>**Prosentti** – Kohdistukselle voidaan määrittää prosenttisumma. Kaikkien prosenttien summan on oltava 100.</li><li>**Muuttujan summa** – Kohdistukselle voidaan määrittää summa. Kohdistussumma määritetään tapahtumatasolla.</li><li>**Yhtä suuri summa** – Kohdistusprosentit lasketaan automaattisesti ja tasan mallin nimikkeiden kesken.</li></ul> |
| Kokonaismäärä | Määritä mallin tavoitesumma. |
| **Rivit** | |
| Nimiketunnus | Valitse tavoitemallin nimiketunnus. |
| Tuotteen nimi | Nimikkeen nimi. |
| Prosentti | <p>Määritä rivin kohdistusprosentti:</p><ul><li>Jos **Kohdistusmenetelmä**-kentän arvoksi määritetään **Prosentti**, määritä rivin prosenttiosuus.</li><li>Jos **Kohdistusmenetelmä**-kentän arvo on **Sama summa**, prosenttiosuus jaetaan automaattisesti samaksi prosenttiluvuksi mallin nimikemäärän perusteella.</li></ul><p>Kaikkien prosenttien summan on oltava 100.</p><p>Jos otsikossa on määritetty **kokonaissumman** arvoja muutat rivin **prosentti**-arvoa, **summa**-arvo päivitetään. Vastaavasti jos muutat **Summa**-arvoa, **prosentti**-arvo päivitetään.</p> |
| Määrä | <p>Rivin kohdistussumma:</p><ul><li>Jos **Kohdistusmenetelmä**-kentän arvoksi määritetään **Muuttujan summa**, määritä rivin summa.</li><li>Jos **Kohdistusmenetelmä**-kentän arvo on **Sama summa**, summa jaetaan automaattisesti samaksi summaksi mallin nimikkeiden määrän ja otsikossa määritetyn **kokonaissumman** arvon mukaan.</li></ul><p>Kaikkien summien summan on oltava sama kuin otsikossa määritetty **kokonaissumman** arvo.</p><p>Jos otsikossa on määritetty **kokonaissumman** arvoja muutat rivin **Summa**-arvoa, **Prosenttiosuus**-arvo päivitetään. Vastaavasti jos muutat **Prosenttiosuus**-arvoa, **Summa**-arvo päivitetään.</p> |
| **Summat** | |
| Prosenttia yhteensä | Prosenttien summa. Kaikkien prosenttien summan on oltava 100. |
| Kokonaismäärä | **Summa**-arvojen summa kaikilla riveillä. Tämän summan on oltava sama kuin otsikossa määritetty **kokonaissumman** arvo. |
| Jäljellä oleva summa | Jäljellä oleva summa. Arvo lasketaan seuraavasti: otsikon **kokonaissumma**-arvo vähennettynä kaikkien rivien **summa**-arvoilla.|

## <a name="milestone-allocation"></a>Välitavoitteen kohdistus

Nämä tehtävät on suoritettava ennen tavoitetoimintojen käyttöä.

1. Lisää vähintään yksi tavoitemalli.
2. Laskutusaikatauluryhmän luominen. Määritä nimikkeen tyypiksi **Tavoite** ja valitse malli.
3. Valitse **Nimikkeen asetus** -sivulla (**Tilaussopimus \> Toistuva sopimuslaskutus \> Asetukset \> Nimikkeet**) nimikesuhde ja tavoitemalli nimikkeen asetuksia varten.

Kun olet luonut tavoitemallit, laskutusaikatauluryhmät ja nimikkeet, voit luoda laskutusaikataulun, joka käyttää tavoitetoimintoja.

Voit määrittää välitavoitteita käyttävän laskutusaikataulun noudattamalla seuraavia vaiheita.

1. Valitse **Laskutusaikataulut**-sivun **Kaikki/aktiiviset laskutusaikataulut** -luettelosta **Uusi**.
2. Luo **Kaikki laskutusaikataulut** -sivulla uusi laskutusaikataulu ja määritä asiakastili ja aloituspäivämäärä.
3. Valitse **Laskutusaikataulurivit**-osassa **Lisää rivi**. Lisää sitten nimiketunnus ja määritä **Nimiketyyppi**-kentän arvoksi **Tavoite**.

    Jos nimikkeelle on määritetty oletustavoitemalli, tavoitetapahtumat lisätään automaattisesti laskutusaikataulun riveille. Tavoiterivien lopetuspäivämäärät ovat tyhjiä.

    Jos nimikkeelle ei ole määritetty tavoitemallia, valitse **Tavoitekohdistus**. Valitse sitten **Tavoitekohdistus**-sivulla tavoitemalli ja tee tarvittavat päivitykset. Palaa sitten laskutusaikatauluun valitsemalla **Sulje** ja tee laskutusaikataulun luonti loppuun.

4. Laskujen luominen laskutusaikataulua varten on päivitettävä kunkin tavoitetapahtuman päättymispäivämäärä. Jos haluat käyttää yksittäistä laskutusaikataulua, voit päivittää tavoitetapahtuman päättymispäivän laskutusaikataulun riveille. Voit päivittää useita laskutusaikatauluja valitsemalla **Päivitä valmistumispäivämääräprosessi**.
5. Päättymispäivän päivityksen jälkeen voit luoda laskun. Jos haluat käyttää yksittäistä laskutusaikataulua, valitse **Muodosta lasku** **Kaikki laskutusaikataulut** -sivulla. Voit luoda laskuja useille laskutusaikatauluille valitsemalla **Luo lasku** tai **Luo eräkäsittely** **kausittaisissa tehtävissä**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Laskutusaikataulun rivin tavoitekohdistusten muokkaaminen

Seuraa näitä ohjeita muokataksesi tavoitekohdistusten laskutusaikataulun rivejä.

1. Valitse **Laskutusaikataulut**-sivu > **Kaikki tai aktiiviset laskutusaikataulut** **Aikataulunumero** -kentässä laskutusaikataulun aikataulunumero.
2. Kirjoita **laskutusaikataulun rivit** -osaan nimike, määritä nimikkeeksi **Tavoite** ja valitse **Tavoitekohdistus**.
3. Valitse **Tavoitemalli**-kentässä tavoitemalli.
4. Valitse **Prosessi**. Tavoitemallin rivit lisätään automaattisesti laskutusaikataulun riveille.

## <a name="milestone-allocation-fields"></a>Välitavoitteen kohdistuskentät

**Tavoitteen kohdistus** -sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|-------|-------------|
| Päänimike | Ylätason nimikenumero. |
| Laajennettu hinta | <p>Nimikkeen laajennettu hinta. Arvo vastaa laskutusaikataulurivin **nettosumman** arvoa.</p></p>Tavoitetason päänimikkeen oletusarvo on tavoitemallille määritetty **kokonaissumma**-arvo. Jos kokonaissumma on 0 (nolla), oletusarvo on laskutussuunnitelman rivin **nettosumma**.</p> |
| Välitavoitemalli | Rivinimikkeen tavoitemallin tunnus. |
| Mallin kuvaus | Tavoitemallin kuvaus. |
| Kohdistusmenetelmä | Tavoitemallissa käytettävä kohdistusmenetelmä. |
| **Rivit** | Kaikkien rivien oletusarvot perustuvat valittuun tavoitemalliin. Voit muuttaa niitä vaatimusten mukaan. |
| Nimiketunnus | Tavoitteen kohdistusmallin nimikenumero. |
| Tuotteen nimi | Tuotteen nimi. |
| Prosentti | <p>Rivin kohdistusprosentti. Kaikkien prosenttien summan on oltava 100.</p><p>Jos muutat rivin **Prosenttiosuus**-arvoa, **Nettosumma**-arvo päivitetään. Vastaavasti jos muutat **Nettosumma**-arvoa, **Prosenttiosuus**-arvo päivitetään.</p> |
| Nettosumma | <p>Rivin kohdistussumma. Kaikkien rivien nettosumman on oltava sama kuin otsikossa määritetty **Laajennettu hinta** -arvo.</p><p>Jos muutat rivin **Nettosumma**-arvoa, **Prosenttiosuus**-arvo päivitetään. Vastaavasti jos muutat **Prosenttiosuus**-arvoa, **Nettosumma**-arvo päivitetään.</p> |
| **Summat** | |
| Kokonaisprosentti | **Prosenttiosuus**-arvojen summa kaikilla riveillä. Tämän summan on oltava 100. |
| Kokonaismäärä | **Nettosumma**-arvojen summa kaikilla riveillä. Tämän summan on oltava sama kuin otsikossa määritetty **Laajennetun hinnan** arvo. |
| Jäljellä oleva summa | Jäljellä oleva summa. Arvo lasketaan seuraavasti: otsikon **Laajennetun hinnan**-arvo vähennettynä kaikkien rivien **Nettosumma**-arvoilla. Lopullisen summan on oltava 0 (nolla). |
