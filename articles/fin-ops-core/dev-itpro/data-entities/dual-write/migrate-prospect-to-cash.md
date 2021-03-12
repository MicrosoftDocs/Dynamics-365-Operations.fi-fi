---
title: Prospektista käteiseksi -tietojen siirtäminen tietojen integrointiohjelmasta kaksoiskirjoitukseen
description: Tässä aiheessa käsitellään Prospektista käteiseksi -tietojen siirtämistä tietojen integrointiohjelmasta kaksoiskirjoitukseen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: f1478f0246e7f1ff8bd72232cbaf4c2034cf4edb
ms.sourcegitcommit: 6af7b37b1c8950ad706e684cc13a79e662985b34
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2021
ms.locfileid: "4959843"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Prospektista käteiseksi -tietojen siirtäminen tietojen integrointiohjelmasta kaksoiskirjoitukseen

[!include [banner](../../includes/banner.md)]

Prospektista käteiseksi -tiedot siirretään tietojen integrointiohjelmasta kaksoiskirjoitukseen seuraavien ohjeiden mukaisesti.

1. Tee viimeinen täydellinen synkronointi suorittamalla tietojen integrointiohjelman Prospektista käteiseksi -työt. Tällä tavoin varmistetaan, että molemmissa järjestelmissä (Finance and Operations -sovelluksissa ja asiakkaiden aktivointisovelluksissa) on kaikki tiedot.
2. Mahdolliset tietohävikit estetään viemällä Prospektista käteiseksi -tiedot Microsoft Dynamics 365 Salesista Excel-tiedostoon tai CSV-tiedostoon. Vie seuraavien entiteettien tiedot:

    - [Tili](#account-table)
    - [Kontakti](#contact-table)
    - [Lasku](#invoice-table)
    - Laskutustuotteet
    - [Tilaus](#order-table)
    - [Tilauksen tuotteet](#order-products-table)
    - [Tuotteet](#products-table)
    - [Tarjous](#quote-and-quote-product-tables)
    - [Tarjoustuotteet](#quote-and-quote-product-tables)

3. Poista Prospektista käteiseksi -ratkaisun asennus Sales-ympäristöstä. Tämä vaihe poistaa sarakkeet ja vastaavat tiedot, jotka Prospektista käteiseksi -ratkaisu otti käyttöön.
4. Asenna kaksoiskirjoitusratkaisu.
5. Luo kaksoiskirjoitusyhteys Finance and Operations -sovelluksen ja asiakkaan aktivointisovelluksen välille vähintään yhdessä yrityksessä.
6. Ota kaksoiskirjoituksen taulujen yhdistämismääritykset käyttöön ja suorita tarvittavien viitetietojen ensimmäinen synkronointi. (Lisätietoja on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).) Pakollisia tietoja ovat esimerkiksi asiakasryhmät, maksuehdot ja maksuaikataulut. Älä ota kaksoiskirjoituksen yhdistämismäärityksiä käyttöön tauluissa, jotka on alustettava. Tällaisia tauluja ovat esimerkiksi tili, tarjous, tarjousrivi, tilaus ja tilausrivi.
7. Valitse asiakkaan aktivointisovelluksessa **Lisäsetukset \> Järjestelmäasetukset \> Tietojen hallinta \> Kaksoiskappaleiden tunnistussäännöt** ja poista kaikki säännöt käytöstä.
8. Alusta vaiheessa 2 mainitut taulut. Lisätietoja on jäljempänä tässä aiheessa.
9. Avaa Finance and Operations -sovellus ja ota käyttöön taulujen yhdistämismääritykset, kuten tilin, tarjouksen, tarjousrivin, tilauksen ja tilausrivin taulujen yhdistämismääritykset. Suorita sitten ensimmäinen synkronointi. (Lisätietoja on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).) Tämä prosessi synkronoi Finance and Operations -sovelluksen lisätiedot, kuten käsittelyn tilan, toimitus- ja laskutusosoitteet, toimipaikat ja varastot.

## <a name="account-table"></a>Tilitaulu

1. Anna yrityksen nimi, kuten **USMF**, **Yritys**-sarakkeessa.
2. Anna **Asiakas** staattisen arvona **Suhteen tyyppi** -sarakkeessa. Jokaista tilityyppiä ei ehkä kannata luokitella asiakkaaksi liiketoimintalogiikassa.
3. Anna **Asiakasryhmän tunnus** -sarakkeessa asiakasryhmän numero Finance and Operations -sovelluksesta. Prospektista käteiseksi -ratkaisun oletusarvo on **10**.
4. Jos käytössä on Prospektista käteiseksi -ratkaisua, jossa **asiakasnumeroa** ei ole mukautettu, anna **Asiakasnumero**-arvon **Osapuolinumero**-sarakkeessa. Jos mukautuksia on tehty etkä tiedä osapuolinumeroa, nouda tämä tieto Finance and Operations -sovelluksesta.

## <a name="contact-table"></a>Yhteyshenkilötaulu

1. Anna yrityksen nimi, kuten **USMF**, **Yritys**-sarakkeessa.
2. Määritä seuraavat sarakkeet CSV-tiedoston **IsActiveCustomer**-arvon perusteella:

    - Jos **IsActiveCustomer**-arvoksi on CSV-tiedostossa määritetty **Kyllä**, määritä **Myytävissä**-sarakkeen arvoksi **Kyllä**. Anna **Asiakasryhmän tunnus** -sarakkeessa asiakasryhmän numero Finance and Operations -sovelluksesta. Prospektista käteiseksi -ratkaisun oletusarvo on **10**.
    - Jos **IsActiveCustomer**-arvoksi on CSV-tiedostossa määritetty **Ei**, määritä **Myytävissä**-sarakkeen arvoksi **Ei** ja **Yhteyshenkilö kohteelle** -sarakkeen arvoksi **Asiakas**.

3. Jos käytössä Prospektista käteiseksi -ratkaisu, jossa **yhteyshenkilön numeroa** ei ole mukautettu, määritä seuraavat sarakkeet:

    - Siirrä yhteyshenkilön numero CSV-tiedostosta (**msdynce\_contactnumber**) **Yhteyshenkilö**-taulun yhteyshenkilön numeroon (**msdyn \_contactnumber**).
    - Käytä **Yhteyshenkilön numero** -taulun arvoja **Osapuoli**-sarakkeessa.
    - Käytä **Yhteyshenkilön numero** -taulun arvoja **Tilinumero tai yhteyshenkilön tunnus** -sarakkeessa.

## <a name="invoice-table"></a>Laskutaulu

Koska **Lasku**-taulun tiedot on suunniteltu siirtymään vain yhteen suuntaan, Finance and Operations -sovelluksesta asiakkaan aktivointisovellukseen, alustusta ei tarvita. Ensimmäisen synkronoinnin suorittaminen siirtää kaikki tarvittavat tiedot Finance and Operations -sovelluksesta asiakkaan aktivointisovellukseen. Lisätietoja on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).

## <a name="order-table"></a>Tilaustaulu

1. Anna yrityksen nimi, kuten **USMF**, **Yritys**-sarakkeessa.
2. Kopioi CSV-tiedoston **Tilaustunnus**-sarakkeen arvo **Myyntitilausnumero**-sarakkeeseen.
3. Kopioi CSV-tiedoston **Asiakas**-sarakkeen arvo **Laskutusasiakkaan numero**-sarakkeeseen.
4. Kopioi CSV-tiedoston **Toimitusasiakkaan maa tai alue** -sarakkeen arvo **Toimitusasiakkaan maa tai alue** -sarakkeeseen. Tällainen arvo on esimerkiksi **USA** ja **Yhdysvallat**.
5. Määritä **Pyydetty vastaanottopäivämäärä** -sarake. Jos vastaanottopäivämäärä ei ole käytössä, käytä CSV-tiedoston **Pyydetty toimituspäivämäärä**-, **Toteutuspäivä**- ja **Lähetyspäivämäärä**-sarakkeita. Tällainen arvo on esimerkiksi **2020-03-27T00:00:00Z**.
6. Määritä **Kieli**-sarake. Tällainen arvo on esimerkiksi **en-us**.
7. Määritä **Tilauksen tyyppi** -sarake käyttämällä **Nimikeperusteinen**-saraketta.

## <a name="order-products-table"></a>Tilaustuotteet-taulu

- Anna yrityksen nimi, kuten **USMF**, **Yritys**-sarakkeessa.

## <a name="products-table"></a>Tuotteet-taulu

Koska **Tuotteet**-taulun tiedot on suunniteltu siirtymään vain yhteen suuntaan, Finance and Operations -sovelluksesta asiakkaan aktivointisovellukseen, alustusta ei tarvita. Ensimmäisen synkronoinnin suorittaminen siirtää kaikki tarvittavat tiedot Finance and Operations -sovelluksesta asiakkaan aktivointisovellukseen. Lisätietoja on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Tarjous- ja tarjoustuotetaulut

Käytä **Tarjous**-taulun osalta tämän aiheen aiemmassa [Tilaustaulu](#order-table)-kohdassa annettuja ohjeita. Käytä **Tarjoustuote**-taulun osalta [Tilaustuotteet-taulu](#order-products-table)-kohdassa annettuja ohjeita.
