---
title: Prospektista käteiseksi -tietojen siirtäminen tietojen integrointiohjelmasta kaksoiskirjoitukseen
description: Tässä artikkelissa käsitellään Prospektista käteiseksi -tietojen siirtämistä tietojen integrointiohjelmasta kaksoiskirjoitukseen.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: bbf5a7c2f409003816e2becf1a58ee7d7d5aafb2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289077"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Prospektista käteiseksi -tietojen siirtäminen tietojen integrointiohjelmasta kaksoiskirjoitukseen

[!include [banner](../../includes/banner.md)]

Tietojen integraattorille käytettävissä oleva Prospektista käteiseksi -ratkaisu ei ole yhteensopiva kaksoiskirjoituksen kanssa. Tämän syy on msdynce_AccountNumber-indeksi tilitaulussa, joka tuli osana Prospektista käteiseksi -ratkaisua. Jos tämä indeksi on olemassa, samaa asiakastilinumeroa ei voi luoda kahdessa eri yrityksessä. Voit joko aloittaa alusta kaksoiskirjoituksen kanssa siirtämällä Prospektista käteiseksi -tiedot tietojen integraattorista kaksoiskirjoitukseen tai voit asentaa viimeisimmän Prospektista käteiseksi -ratkaisun dorman-version. Tässä artikkelissa kuvataan nämä molemmat vaihtoehdot.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Asenna tietojen integroijan Prospektista käteiseksi -ratkaisun viimeisin dorman-versio

**P2C-versiota 15.0.0.2** pidetään viimeisimpänä tietojen integroijan Prospektista käteiseksi -ratkaisun dorman-versiona. Voit ladata sen kohteesta [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Se on asennettava manuaalisesti. Asennuksen jälkeen kaikki pysyy samana, paitsi että msdynce_AccountNumber-indeksi poistetaan.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Vaiheet Prospektista käteiseksi -tietojen siirtämiseksi tietojen integrointiohjelmasta kaksoiskirjoitukseen

Prospektista käteiseksi -tiedot siirretään tietojen integrointiohjelmasta kaksoiskirjoitukseen seuraavien ohjeiden mukaisesti.

1. Tee viimeinen täydellinen synkronointi suorittamalla tietojen integrointiohjelman Prospektista käteiseksi -työt. Tällä tavoin varmistetaan, että molemmissa järjestelmissä (talous- ja toimintosovelluksissa sekä asiakkaiden aktivointisovelluksissa) on kaikki tiedot.
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
5. Luo kaksoiskirjoitusyhteys talous- ja toimintosovelluksen sekä asiakkaan aktivointisovelluksen välille vähintään yhdessä yrityksessä.
6. Ota kaksoiskirjoituksen taulujen yhdistämismääritykset käyttöön ja suorita tarvittavien viitetietojen ensimmäinen synkronointi. (Lisätietoja on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).) Pakollisia tietoja ovat esimerkiksi asiakasryhmät, maksuehdot ja maksuaikataulut. Älä ota kaksoiskirjoituksen yhdistämismäärityksiä käyttöön tauluissa, jotka on alustettava. Tällaisia tauluja ovat esimerkiksi tili, tarjous, tarjousrivi, tilaus ja tilausrivi.
7. Valitse asiakkaan aktivointisovelluksessa **Lisäsetukset \> Järjestelmäasetukset \> Tietojen hallinta \> Kaksoiskappaleiden tunnistussäännöt** ja poista kaikki säännöt käytöstä.
8. Alusta vaiheessa 2 mainitut taulut. Lisätietoja on jäljempänä tässä artikkelissa.
9. Avaa talous- ja toimintosovellus ja ota käyttöön taulujen yhdistämismääritykset, kuten tilin, tarjouksen, tarjousrivin, tilauksen ja tilausrivin taulujen yhdistämismääritykset. Suorita sitten ensimmäinen synkronointi. (Lisätietoja on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).) Tämä prosessi synkronoi talous- ja toimintosovelluksen lisätiedot, kuten käsittelyn tilan, toimitus- ja laskutusosoitteet, toimipaikat ja varastot.

## <a name="account-table"></a>Tilitaulu

1. Anna yrityksen nimi, kuten **USMF**, **Yritys**-sarakkeessa.
2. Anna **Asiakas** staattisen arvona **Suhteen tyyppi** -sarakkeessa. Jokaista tilityyppiä ei ehkä kannata luokitella asiakkaaksi liiketoimintalogiikassa.
3. Anna **Asiakasryhmän tunnus** -sarakkeessa asiakasryhmän numero talous- ja toimintosovelluksesta. Prospektista käteiseksi -ratkaisun oletusarvo on **10**.
4. Jos käytössä on Prospektista käteiseksi -ratkaisua, jossa **asiakasnumeroa** ei ole mukautettu, anna **Asiakasnumero**-arvon **Osapuolinumero**-sarakkeessa. Jos mukautuksia on tehty etkä tiedä osapuolinumeroa, nouda tämä tietotalous- ja toimintosovelluksesta.

## <a name="contact-table"></a>Yhteyshenkilötaulu

1. Anna yrityksen nimi, kuten **USMF**, **Yritys**-sarakkeessa.
2. Määritä seuraavat sarakkeet CSV-tiedoston **IsActiveCustomer**-arvon perusteella:

    - Jos **IsActiveCustomer**-arvoksi on CSV-tiedostossa määritetty **Kyllä**, määritä **Myytävissä**-sarakkeen arvoksi **Kyllä**. Anna **Asiakasryhmän tunnus** -sarakkeessa asiakasryhmän numero talous- ja toimintosovelluksesta. Prospektista käteiseksi -ratkaisun oletusarvo on **10**.
    - Jos **IsActiveCustomer**-arvoksi on CSV-tiedostossa määritetty **Ei**, määritä **Myytävissä**-sarakkeen arvoksi **Ei** ja **Yhteyshenkilö kohteelle** -sarakkeen arvoksi **Asiakas**.

3. Jos käytössä Prospektista käteiseksi -ratkaisu, jossa **yhteyshenkilön numeroa** ei ole mukautettu, määritä seuraavat sarakkeet:

    - Siirrä yhteyshenkilön numero CSV-tiedostosta (**msdynce\_contactnumber**) **Yhteyshenkilö**-taulun yhteyshenkilön numeroon (**msdyn \_contactnumber**).
    - Käytä **Yhteyshenkilön numero** -taulun arvoja **Osapuoli**-sarakkeessa.
    - Käytä **Yhteyshenkilön numero** -taulun arvoja **Tilinumero tai yhteyshenkilön tunnus** -sarakkeessa.

## <a name="invoice-table"></a>Laskutaulu

Koska **Lasku**-taulun tiedot on suunniteltu siirtymään vain yhteen suuntaan, talous- ja toimintosovelluksesta asiakkaan aktivointisovellukseen, alustusta ei tarvita. Ensimmäisen synkronoinnin suorittaminen siirtää kaikki tarvittavat tiedot talous- ja toimintosovelluksesta asiakkaan aktivointisovellukseen. Lisätietoja on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).

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

Koska **Tuotteet**-taulun tiedot on suunniteltu siirtymään vain yhteen suuntaan, talous- ja toimintosovelluksesta asiakkaan aktivointisovellukseen, alustusta ei tarvita. Ensimmäisen synkronoinnin suorittaminen siirtää kaikki tarvittavat tiedot talous- ja toimintosovelluksesta asiakkaan aktivointisovellukseen. Lisätietoja on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Tarjous- ja tarjoustuotetaulut

Käytä **Tarjous**-taulun osalta tämän artikkelin aiemmassa osassa [Tilaustaulu](#order-table) annettuja ohjeita. Käytä **Tarjoustuote**-taulun osalta [Tilaustuotteet-taulu](#order-products-table)-kohdassa annettuja ohjeita.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

