---
title: Asiakastilausten yleiskatsaus
description: "Tässä ohjeaiheessa on tietoja asiakkaiden tilauksista Retail Modern POS (MPOS) -laitteissa. Asiakastilauksia kutsutaan myös erikoistilauksiksi. Aihe sisältää keskustelun liittyvistä parametreista ja tapahtumatyönkuluista."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f68f9dce544256a2b1a9927f019a676a6845f46d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="customer-orders-overview"></a>Asiakastilausten yleiskatsaus

[!include[banner](includes/banner.md)]


Tässä ohjeaiheessa on tietoja asiakkaiden tilauksista Retail Modern POS (MPOS) -laitteissa. Asiakastilauksia kutsutaan myös erikoistilauksiksi. Aihe sisältää keskustelun liittyvistä parametreista ja tapahtumatyönkuluista.

Monikanavaisessa vähittäismyyntimaailmassa monet vähittäiskauppiaat tarjoavat asiakastilausten eli erikoistilausten mahdollisuuden täyttääkseen erilaisia eri tuote- ja palveluvaatimuksia. Seuraavassa on joitakin tyypillisiä skenaarioita:

-   Asiakas haluaa, että tuotteet toimitetaan tiettynä päivänä tiettyyn osoitteeseen.
-   Asiakas haluaa noutaa tuotteet myymälästä tai sijainnista, joka on eri kuin myymälä tai sijainti, josta asiakas osti nämä tuotteet.
-   Asiakas haluaa jonkun toisen noutavan ostamansa tuotteet.

Vähittäiskauppiaat käyttävät asiakastilauksia myös pienentääkseen menetettyä myyntiä, jota varaston tyhjeneminen voi muuten aiheuttaa, koska kauppatavara voidaan toimittaa tai kerätä eri aikaan tai eri paikasta.

## <a name="set-up-customer-orders"></a>Määritä asiakastilaukset
Seuraavassa on joitakin parametreja, jotka voidaan asettaa **Vähittäismyynnin parametrit** -sivulla määrittääksesi, miten asiakkaiden tilaukset suoritetaan:

-   **Oletuskäsirahaprosentti** – määritä summa, joka asiakkaan on maksettava talletuksena ennen tilauksen vahvistamista. Oletuskäsirahaprosentti lasketaan prosenttiosuutena tilauksen arvosta. Oikeuksista riippuen myymälän johtaja saattaa pysytä ohittamaan summan käyttämällä asetusta **Talletuksen ohitus**.
-   **Peruutusmaksuprosentti** – Jos asiakkaan tilauksen peruuttamisesta perittään maksu, määritä kyseisen maksun määrä.
-   **Peruutusmaksun koodi** – Jos asiakkaan tilauksen peruuttamisesta perittään maksu, kyseinen maksu näkyy myyntitilauksessa maksukoodina. Tämän parametrin avulla voit määrittää peruutusmaksun koodin.
-   **Toimitusmaksun koodi** – Vähittäiskauppiaat voivat veloittaa ylimääräisen lisämaksun tavaran lähettämisestä asiakkaalle. Tämän toimitusmaksu näkyy maksukoodina myyntitilauksessa. Tämän parametrin avulla voit yhdistää toimitusmaksun koodia toimitusmaksuihin asiakastilauksessa.
-   **Palauta toimitusmaksut** – Määritä, ovatko asiakastilaukseen liittyvät toimitusmaksut palautettavia.
-   **Enimmäissumma ilman hyväksyntää** – Jos kuljetusmaksut ovat palautettavia, määritä palautustilausten toimitusmaksujen palautusten enimmäismäärä. Jos tämä määrä ylittyy, toiminnon jatkaminen edellyttää esimiehen hyväksyntää. Sopeutuakseen seuraaviin skenaarioihin, toimitusmaksujen palautus voi ylittää alunperin maksetun summan:
    -   Kulut otetaan käyttöön myyntitilauksen otsikon tasolla ja kun tuotelinjan jokin määrä palautetaan, suurinta tuotteille ja määrälle sallittua toimitusmaksun palautusta ei voi määrittää tavalla, joka toimii kaikille vähittäismyynnin asiakkaille.
    -   Kuljetusmaksut syntyvät toimituksen kaikissa esiintymissä. Jos asiakas palauttaa tuotteet useita kertoja ja jälleenmyyjän käytäntö määrittää, että vähittäismyyjä vasta toimituskustannuksista, palautettavat kuljetusmaksut ovat enemmän kuin todelliset kuljetusmaksut.

## <a name="transaction-flow-for-customer-orders"></a>Asiakastilausten tapahtumien työnkulku
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Luo asiakastilaus Retail Modern POS -sovelluksessa

1.  Lisää asiakas tapahtumaan.
2.  Lisää tuotteet ostoskoriin.
3.  Valitse **Luo asiakastilaus** ja valitse sitten tilauksen tyyppi. Tilauksen tyyppi voi olla joko **Asiakastilaus** tai **Tarjous**.
4.  Valitse **Lähetä valitut** tai **Lähetä kaikki** toimittaaksesi tuotteet asiakastilin osoitteeseen. Määritä pyydetty lähetyspäivä ja kuljetusmaksut.
5.  Valitse **Kerää valitut** tai **Kerää kaikki** valitaksesi tuotteet, jotka kerätään nykyisestä myymälästä tai eri myymälästä tiettynä päivänä.
6.  Veloita talletussumma, jos seitä vaaditaan.

### <a name="edit-an-existing-customer-order"></a>Olemassa olevan asiakkaan tilauksen muokkaaminen

1.  Valitse kotisivulla **Etsi tilaus**.
2.  Etsi ja valitse muokattava tilaus. Valitse sivun alareunassa **Muokkaa**.

### <a name="pick-up-an-order"></a>Kerää tilaus

1.  Valitse kotisivulla **Etsi tilaus**.
2.  Valitse kerättävä tilaus. Valitse sivun alareunassa **Keräys ja pakkaus**.
3.  Valitse **Kerää**.

### <a name="cancel-an-order"></a>Tilauksen peruuttaminen

1.  Valitse kotisivulla **Etsi tilaus**.
2.  Valitse peruutettava tilaus. Valitse sivun alareunassa **Peruuta**.

#### <a name="create-a-return-order"></a>Palautustilauksen luominen

1.  Valitse kotisivulla **Etsi tilaus**.
2.  Valitse palautettava tilaus, valitse tilauksen lasku ja sitten tuotelinja, johon kauppatavara palautetaan.
3.  Valitse sivun alareunassa **Palautustilaus**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asiakastilausten tapahtumien asynkroninen työnkulku
Asiakastilauksia voi luoda myyntipisteen (POS) asiakasohjelmassa joko synkronoidussa tai asynkronisessa tilassa.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Ota käyttöön asiakastilausten luonti asynkronisessa tilassa

1.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **POS-profiilit** &gt; **Toimintoprofiilit**.
2.  **Yleiset**-pikavälilehdessä määritä **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvoksi **Kyllä**.

Kun **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvo on **Kyllä**, asiakastilaukset luodaan aina asynkronisessa tilassa, vaikka Retail Transaction Service (RTS) -palvelu on käytettävissä. Jos määrität tämän asetuksen arvoksi **Ei**, asiakkaan tilaukset luodaan aina synkronoidussa tilassa RTS:n avulla. Kun asiakastilaukset on luotu asynkronisessa tilassa, ne ovat vedetään ja lisätään Retailiin Pull (P) -töitä käyttämällä. Retailissa luodaan vastaavat myyntitilaukset, kun **Synkronoi tilaukset** suoritetaan joko manuaalisesti tai eräprosessina.

<a name="see-also"></a>Lisätietoja
--------

[Hybridit asiakastilaukset](hybrid-customer-orders.md)




