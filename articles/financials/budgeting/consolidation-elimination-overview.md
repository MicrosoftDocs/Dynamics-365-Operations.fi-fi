---
title: Konsolidoinnin ja eliminoinnin yhteenveto
description: "Tässä artikkelissa on yleisiä tietoja konsolidointi- ja eliminointiprosessista. Artikkeli sisältää myös vastauksia usein kysyttyihin kysymyksiin."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c9568d1cac05db83d00108e8b16c03aa4c807cac
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="consolidation-and-elimination-overview"></a>Konsolidoinnin ja eliminoinnin yhteenveto

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on yleisiä tietoja konsolidointi- ja eliminointiprosessista. Artikkeli sisältää myös vastauksia usein kysyttyihin kysymyksiin.

Kun tietoja konsolidoidaan, useiden tytäryhtiöiden taloudelliset tulokset yhdistetään yhteen konsolidointiyritykseen. Tytäryhtiöt voivat käyttää eri versioita tai järjestelmiä. Niitä ei ehkä omisteta kokonaan, ja käytössä voi olla eri valuutat. Tietoja voidaan konsolidoida useilla eri tavoilla.

-   **Konsolidoi verkossa** – Tämä vaihtoehto konsolidoi päivittäiset saldot valittujen tilien ja dimensioiden mukaan. Ne tallennetaan konsolidointiyritykseen.
-   **Talousraportointi** – Tämä vaihtoehto ottaa käyttöön tapahtumien ja saldojen konsolidoinnin. Se voidaan luoda milloin tahansa. Hierarkioita voidaan luoda useita eri tasoja, ja eri raportointivaluuttojen tarkastelu on mahdollista.
-   **Konsolidoi tuonnin kanssa** – Tämä vaihtoehto tuo saldot konsolidointiyritykseen.
-   **Vie yrityksen saldot** – Tämä vaihtoehto mahdollistaa yrityksen saldotiedoston viennin. Tiedosto voidaan tämän jälkeen tuoda muihin instansseihin tai järjestelmiin. Talousraportointia voidaan käyttää myös vietäessä saldoja Microsoft Excel -tiedostoon.

Eliminoinnit voidaan raportoida useilla eri tavoilla.

-   Eliminointisäännöt voidaan määrittää järjestelmässä. Tämän jälkeen ne käsitellään konsolidointiprosessin aikana tai eliminointiehdotuksen kautta. Säännöt voidaan kirjata mihin tahansa yritykseen, jonka yritysten asetuksissa on valittu **Käytetään taloushallinnon eliminointiprosessissa**.
-   Eliminointitapahtumien manuaalista määrittämistä ja kirjaamista varten voidaan luoda erillinen yritys. Tätä yritystä voidaan käyttää konsolidointiprosessissa tai talousraportoinnissa.
-   Konsernin sisäisen toiminnan määrittämisessä käytettävät tilit ja taloushallinnon dimensiot voidaan suodattaa talousraportoinnin rivi- tai sarakemäärityksessä. Käytössä ovat kaikki porautumisominaisuudet. Tämän jälkeen lasketun sarakkeen tai rivin avulla voidaan poistaa tilejä tai taloushallinnon dimensioita konsolidoinnin yhteissummasta.

Konsolidointiskenaarioita on useita. Kukin menetelmä voi käsitellä skenaarioita eri tavoin.

## <a name="frequently-asked-questions"></a>Usein kysyttyjä kysymyksiä
1.  Haluan kirjata eliminoinnit tietokantaan. Mitä vaihtoehtoja minulla on?

Vaihtoehtoja on useita. Voit sisällyttää eliminoinnit prosessin aikana tai ehdotuksena **Konsolidoi verkossa** -vaihtoehto. Tapahtumat kirjataan konsolidointiyritykseen. Vaihtoehtoisesti eliminoinnit voidaan luoda manuaalisesti erilliseen yritykseen. Tämän jälkeen yritystä voidaan käyttää talousraportoinnissa tai konsolidointiprosessissa.

2.  Tarvitsemme konsolidointituloksia useissa raportointivaluutoissa.

**Talousraportointi**-vaihtoehto sisältää rajoittamattoman määrän raportointivaluuttoja. Tiedot muunnetaan raportin luonnin aikana päätilillä määritetyn vaihtokurssin tyypin ja valuutan muunnosmenetelmän perusteella. Koska **Konsolidoi verkossa** -vaihtoehto sisältää vain yhden raportointivaluutan, vaihtoehdon valinta edellyttää konsolidointiyrityksen jokaiselle raportointivaluutalle. Suositeltu menetelmä on **Talousraportointi**.

3.  Haluan tarkastella kunkin yrityksen tapahtumatasoa.

Ratkaisu on **Talousraportointi**-vaihtoehto, koska sen avulla tarkastella kaikkien raportointipuun määritykseen sisältyvien yritysten tapahtumatason tietoja.

4.  Käytössämme on budjettisuunnittelu tai budjetin hallinta, joka on konsolidoitava.
**Talousraportointi**-vaihtoehto on oikea ratkaisu minkä tahansa budjettisuunnittelun tai budjetin hallinnan tietojen konsolidointia varten.

5.  Tytäryhtiömme sijaitsevat eri maissa, ja meillä on useita tilikarttoja. Mikä on paras tietojen konsolidointimenetelmä meille?

Useiden tilikarttojen käsittelyä varten on monia vaihtoehtoja. Eräs niistä on **Konsolidoi verkossa** -vaihtoehto. Tässä vaihtoehdossa määritetään, käytetäänkö päätilillä määritettyä konsolidointitiliä vai konsolidointitiliryhmää. Toinen mahdollinen vaihtoehto on **Talousraportointi**. Tässä vaihtoehdossa taloushallinnon dimensioihin sisällytetään useita linkkejä rivimäärityksessä. Tämän jälkeen tilit yhdistetään.

6.  Tarvitsemme useita konsolidointitasoja. Konsolidoimme ensin kaikki Euroopassa sijaitsevat tytäryhtiömme Ison-Britannian punnaksi (GBP). Tämän jälkeen konsolidoitu summa muunnetaan Yhdysvaltojen dollareiksi. Miten tämä tehdään?

Kun konsolidointi tehdään useilla tasoilla, joilla käytetään eri valuuttoja, on valittava **Konsolidoi verkossa** -vaihtoehto. Tällöin on luotava useita konsolidointiyrityksiä, joilla on erilaiset kirjanpito- ja raportointivaluutat. Konsolidointi on suoritettava useita kertoja. **Talousraportointi**-vaihtoehto muuntaa aina kunkin lähdeyrityksen kirjanpitovaluutan valituksi valuutaksi.

7.  Tytäryhtiöitämme löytyy eri järjestelmistä. Miten voimme konsolidoida ne?

**Konsolidoi tuonnin kanssa** -vaihtoehdon avulla saldot voidaan tuoda konsolidointiyritykseen.

8.  Emme omista kaikkia tytäryhtiöitämme kokonaan. Mikä on paras konsolidointimenetelmä niitä varten?

Osittain omistettuja tytäryhtiöitä varten on useita vaihtoehtoja. Kun käytössä on **Talousraportointi**-vaihtoehto, määritetään raportointipuun määritys ja omistajuus. Myös laskettua riviä tai saraketta voidaan käyttää osittain omistetun summan esittämisessä. Myös vähemmistöosuus voidaan näyttää raportissa omalla rivillä. **Konsolidoi verkossa** -vaihtoehtoa voi myös käyttää. **Yritykset**-välilehti sisältää **Omistajuus**-sarakkeen, jossa pääyrityksen omistama prosenttiosuus määritetään.

9.  Konsolidoinnit on esitettävä organisaatiossa liiketoimintayksikön mukaan tai organisaatiossa halutaan käyttää organisaatiohierarkioita.

Ratkaisu on **Talousraportointi**-vaihtoehto. Organisaatiohierarkiat, jotka sisältävät yrityksiä tai taloushallinnon dimensioita, voidaan raportoida talousraportoinnin avulla. Voit myös luoda omia monitasoisia hierarkioita yritysten ja dimension arvojen yhdistelmiä sisältävän raportintipuun määrityksen avulla.

10. Käytössä on useita järjestelmän esiintymiä.

**Vie yrityksen saldot** -vaihtoehdon avulla voidaan suorittaa vienti yhdestä esiintymästä. Tämän jälkeen tiedot voidaan konsolidoida käyttämällä toisen esiintymän **Konsolidoi tuonnin kanssa** -vaihtoehtoa.


Lisätietoja on ohjeaiheessa [Valuutan uudelleenarvostus konsolidointiyrityksessä](..\general-ledger\currency-revaluation-consolidation-company.md).



