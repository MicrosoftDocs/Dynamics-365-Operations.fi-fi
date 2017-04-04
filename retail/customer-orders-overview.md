---
title: "Asiakkaan tilaukset yleistä"
description: "Tässä ohjeaiheessa on tietoja asiakkaiden tilaukset-Retail Moderni POS (MPOS). Asiakastilausten kutsutaan myös erikoistilauksia. Aihe sisältää keskustelun vastaavat parametrit ja tapahtuman virrat."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Asiakkaan tilaukset yleistä

Tässä ohjeaiheessa on tietoja asiakkaiden tilaukset-Retail Moderni POS (MPOS). Asiakastilausten kutsutaan myös erikoistilauksia. Aihe sisältää keskustelun vastaavat parametrit ja tapahtuman virrat.

Omni-kanavainen retail-maailmassa monet vähittäiskauppiaat antaa asiakkaalle mahdollisuuden tilauksia tai erikoistilauksia eri tuotteiden ja fulfillment vaatimusten täyttämiseksi. Seuraavassa on joitakin tyypillisiä skenaarioita:

-   Asiakas haluaa tuotteet toimitetaan tiettynä päivänä tiettyyn osoitteeseen.
-   Asiakas haluaa noutaa tuotteet myymälän tai sijaintiin, joka poikkeaa myymälä tai sijainti, jossa asiakas ostaa näitä tuotteita.
-   Asiakas haluaa jonkun päiväkodista, jossa asiakas ostaa tuotteita.

Vähittäiskauppiaiden käyttää myös asiakkaan tilausten pienentää menetetty myynti, osakkeiden katkokset voi muuten aiheuttaa, koska kauppatavaran voidaan toimittaa tai kerätä eri aika tai paikka.

## <a name="set-up-customer-orders"></a>Määritä asiakkaan tilausten
Seuraavassa on joitakin parametreja, jotka voidaan asettaa **vähittäismyynnin parametreja** sivulla voit määrittää, miten asiakkaiden tilaukset täyttyvät:

-   **Oletus talletusten osuus** – määrittää talletuksen summa, joka asiakkaan on maksettava ennen tilauksen vahvistamista. Oletus Talletussumma lasketaan prosentteina arvo. Oikeudet, mukaan myymälän osakkuusyrityksen ehkä summa ohittaa käyttämällä **Talletuksen ohitus**.
-   **Peruutusmaksuprosentti** – Jos varausta käytetään, kun asiakkaan tilaus on peruutettu, määritä kyseisen maksun määrä.
-   **Peruutusmaksun koodi** – Jos varausta otetaan käyttöön, kun asiakkaan tilaus on peruutettu, että kulut näkyvät kulun koodi-kohtaan Microsoft Dynamics AX: n myyntitilauksen. Tämän parametrin avulla voit määrittää, peruutusmaksun koodi.
-   **Toimitusmaksun koodin** – vähittäiskauppiaiden voidaan veloittaa ylimääräinen lisämaksu tavaraa lähetyksen asiakkaalle. Toimitusmaksua, kyseinen määrä vaikuttaa kulujen koodi alla Dynamics AX: n myyntitilauksen. Tämän parametrin avulla voit yhdistää asiakkaan tilauksen kuljetusmaksuja toimitusmaksun koodia.
-   **Hyvityksen kuljetusmaksut** – määrittää, ovatko kuljetusmaksuja, jotka asiakastilaus liittyvät ostoihin.
-   **Suurin summa ilman lupaa** – Jos kuljetusmaksut ovat ostoihin, määrittää enimmäismäärän toimitus kulut tuet palautustilaukset välillä. Jos tämä määrä ylittyy, ohitus hallinta edellyttää tuen jatkaa. Rahani kuljetusmaksut voivat ylittää summan, joka oli alun perin maksettu sopimaan seuraavissa tilanteissa:
    -   Kulut otetaan käyttöön tasolla myyntitilauksen otsikon ja kun tuotelinjan määrä palautetaan, suurin korvaamisesta kuljetusmaksuja, joita voidaan käyttää tuotteiden ja määrää ei voida määrittää tapa, joka toimii retail kaikille asiakkaille.
    -   Kuljetusmaksut ovat syntyneet toimitus esiintymiä. Jos asiakas palauttaa tuotteet useita kertoja ja jälleenmyyjän käytäntö määrittää, että vähittäismyyjän kustannuksista palaa kuljetusmaksut, palaa kuljetusmaksut on enemmän kuin todellinen kuljetusmaksut.

## <a name="transaction-flow-for-customer-orders"></a>Tapahtuman asiakastilausten virtaus
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Luo Retail POS-sovelluksen Moderni asiakkaan tilaukseen

1.  Lisää asiakas tapahtumaan.
2.  Lisää ostoskorin tuotteet.
3.  Valitse **luo tilauksen asiakkaan**, ja valitse sitten tilauksen tyyppi. Tilauksen tyyppi voi olla joko **asiakkaan tilauksen** tai **tarjous**.
4.  Valitse **valittu aluksen** tai **toimittaa kaikki** toimittamaan osoitteeseen tuotteet asiakkaan Määritä pyydetty lähetyspäivä ja kuljetusmaksut.
5.  Valitse **poiminta ylöspäin valittu** tai **noudettavissa kaikki** voit valita tuotteita, jotka kerätään nykyisen myymälän tai myymälän eri tiettynä päivänä.
6.  Kerää Pano, jos talletusta ei tarvita.

### <a name="edit-an-existing-customer-order"></a>Olemassa olevan asiakkaan tilauksen muokkaaminen

1.  Valitse kotisivun, **löydä tilauksen**.
2.  Etsi ja valitse Muokkaa järjestystä. Valitse sivun alareunassa **Muokkaa**.

### <a name="pick-up-an-order"></a>Nosta tilaus

1.  Valitse kotisivun, **löydä tilauksen**.
2.  Valitse järjestys, päiväkodista. Valitse sivun alareunassa **keräysluettelon ja pakkausluettelon**.
3.  Valitse **Nosta**.

### <a name="cancel-an-order"></a>Peruuta tilaus

1.  Valitse kotisivun, **löydä tilauksen**.
2.  Valitse Peruuta tilaus. Valitse sivun alareunassa **peruuttaa**.

#### <a name="create-a-return-order"></a>Palautustilauksen luominen

1.  Valitse kotisivun, **löydä tilauksen**.
2.  Valitse tilaus, palauttaa tilauksen lasku ja valitse palauttaa tavaraa tuotelinjan.
3.  Valitse sivun alareunassa **palautustilausten**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Tapahtuman asynkroninen virtauksen asiakkaan tilausten
Asiakas myynti (POS) kohdan asiakastilausten voi luoda synkronoitu tila tai asynkronista tilaa.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Ota käyttöön asynkroninen tilassa luodaan myyntitilaukset

1.  Valitse Dynamics AX- **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiili**&gt;**Toimintoprofiilit**.
2.  - **Yleisen** -pikavälilehdessä määrittää **Luo asiakastilaus async-tilassa** asetuksella **Kyllä**.

Kun **Luo asiakastilaus async-tilassa** asetus **Kyllä**, asiakkaan tilaukset luodaan aina asynkroninen tilassa, vaikka Retail Transaction Service-palvelun (RTS) on käytettävissä. Jos määrität tämän asetuksen arvoksi **ei**, asiakkaan tilaukset luodaan aina synkronoitu tila-RTS avulla. Kun myyntitilaukset on luotu asynkroninen tilassa, ne ovat vedetään ja lisätään Dynamics AX: N Pull (P) töiden. Dynamics AX: ssä luodaan vastaava myyntitilauksia kun **Synkronoi tilaukset** suoritetaan joko manuaalisesti tai eräkohtainen prosessi.

<a name="see-also"></a>Lisätietoja
--------

[Hybrid asiakkaiden tilaukset](hybrid-customer-orders.md)


