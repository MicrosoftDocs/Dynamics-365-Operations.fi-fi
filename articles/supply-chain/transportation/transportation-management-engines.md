---
title: Kuljetuksenhallinnan moduulit
description: Kuljetuksenhallinnan moduulit määrittävät logiikan, jota käytetään kuljetushintojen luomiseen ja käsittelemiseen Kuljetuksenhallinnassa.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine, TMSFreightBillTypeAssignment, TMSZoneMaster, TMSEngineParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4a49ed7a91ec9a1b89564d40bef38cc4ea45532
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669597"
---
# <a name="transportation-management-engines"></a>Kuljetuksenhallinnan moduulit

[!include [banner](../includes/banner.md)]

Kuljetuksenhallinnan moduulit määrittävät logiikan, jota käytetään kuljetushintojen luomiseen ja käsittelemiseen Kuljetuksenhallinnassa. 

Kuljetuksen hallintamoduuli laskee tehtäviä, kuten rahdinkuljettajan kuljetushinnan. Moduulijärjestelmän ansiosta voit muuttaa laskentastrategioita suorituksen aikana Supply Chain Managementin tietojen perusteella. Kuljetuksen hallintamoduuli muistuttaa laajennusta, joka liittyy tietyn rahdinkuljettajan sopimukseen.

## <a name="what-engines-are-available"></a>Mitä laskentoja on käytettävissä?
Seuraavassa taulukossa on kuvattu käytettävissä olevat kuljetuksenhallintamoduulit.

| Kuljetuksenhallinnan moduuli | Kuvaus                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hinnan laskenta**                  | Laskee hinnat.                                                                                                                                                                                                                                                                                                           |
| **Yleinen laskenta**               | Yksinkertaiset muiden moduulien käyttämät apumoduulit, jotka eivät edellytä tietoja Supply Chain Managementista, esimerkiksi jako-osuuden laskenta. Jako-osuuden laskentojen avulla vähennetään tiettyjen tilausten ja rivien lopullisia kuljetuskustannuksia dimensioiden, kuten volyymin ja painon, perusteella. |
| **Kilometrien laskenta**               | Laskee kuljetusetäisyyden.                                                                                                                                                                                                                                                                                     |
| **Siirtoajan laskenta**          | Laskee ajan, joka tarvitaan alusta loppuun kulkemiseen.                                                                                                                                                                                                                                       |
| **Vyöhykkeen laskenta**                  | Laskee valitun osoitteen perusteella alueen ja laskee alueiden määrän, jotka on ylitettävä siirryttäessä osoitteesta A osoitteeseen B.                                                                                                                                                                    |
| **Rahtilaskun tyyppi**            | Standardoi rahtilaskun ja rahtikirjan rivit ja sitä käytetään automaattiseen rahtikirjan täsmäyttämiseen.                                                                                                                                                                                                                |


## <a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Mitä laskentoja on määritettävä, jotta lähetykselle voidaan laskea hinta?

Jos haluat arvioida lähetyksen käyttäen tiettyä rahdinkuljettajaa, sinun on määritettävä useita kuljetushallintamoduuleita. **Hinnan laskenta** on pakollinen, mutta muiden kuljetuksen hallinnan moduulien on ehkä tuettava **Hinnan laskenta** -moduulia. **Hinnan laskenta** -moduulia voidaan käyttää esimerkiksi tietojen noutamiseen **Kilometrien laskenta** -moduulista ja hinnan laskemiseksi lähteen ja kohteen välillä kilometrien perusteella.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Mitä tarvitaan kuljetuksenhallintamoduulin alustamiseen?
Kuljetuksen hallintamoduuli edellyttää, että määrität alustustiedot tietynlaista toiminnallisuutta varten. Asetus voi sisältää seuraavan tyyppisiä tietoja:
-   Viitteet muihin kuljetushallinnan moduuleihin. Katso lisätietoja tämän osion määritysesimerkistä.
-   Viitteitä .NET-tyyppeihin, joita käytetään kuljetuksen hallintamoduulissa.
-   Yksinkertaiset konfigurointitiedot.

Useimmissa tapauksissa voit konfiguroida alustustiedot valitsemalla **Parametrit**-painikkeen kuljetuksen hallintamoduulin asetuslomakkeissa. **Esimerkki kilometrien laskentaan viittaavan hinnan laskennan määrityksestä** Seuraavassa esimerkissä kuvataan asetus, joka vaaditaan hinnan laskennalle, joka perustuu .NET-moduulin tyyppiin Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine ja viittaa kilometrien laskentaan.

|          Parametri           |                                                                                  Kuvaus                                                                                  |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <em>RateBaseAssigner</em>   | .NET-tyyppi, joka tulkitsee hintaan perustuvat määritystiedot tietylle skeemalle. Parametriarvon syntaksi koostuu kahdesta pystyviivalla erotetusta segmentistä ( |
|  <em>MileageEngineCode</em>  |                       Kilometrien laskennan koodi, joka tunnistaa kilometrien laskentatietueen tietokannassa.                        |
| <em>Jako-osuuden laskenta</em> |                        Yleinen jako-osuuden laskennan yksilöivä koodi tietokannassa.                        |

## <a name="how-is-metadata-used-in-transportation-management-engines"></a>Metatietojen käyttö kuljetuksen hallintalaskuihin

Kuljetuksenhallinnan moduulit, jotka perustuvat Supply Chain Managementissa määriteltyihin tietoihin, saattavat käyttää erilaisia tietomalleja. Kuljetuksen hallintajärjestelmä mahdollistaa, että erilaiset kuljetuksen hallintamoduulit voivat käyttää samoja yleisiä fyysisiä tietokantatauluja. Varmistaaksesi, että ajoaikainen moottorin tietojen tulkinta on täsmällistä, voit määrittää metatiedot tietokannan taulukoihin. Tämä vähentää uusien kuljetuksenhallintamoduulien rakentamiskustannuksia, koska Operations ei vaadi lisärakenteita tauluille ja lomakkeille.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Mitä voidaan käyttää hakutietona hintalaskelmissa?
Hintojen laskentaan käyttämiäsi tietoja hallitaan metatietomäärityksellä. Esimerkiksi jos haluat etsiä postinumeroihin perustuvia hintoja, sinun on määritettävä metatiedot, jotka perustuvat postinumeron hakutyyppiin.

## <a name="do-all-engine-configurations-require-metadata"></a>Kaikki moduulin konfiguraatiot vaativat metatiedot?
Ei, kuljetuksen hallintamoduulit, joita käytetään hinnan laskemiseen ulkoisista järjestelmistä vaadittavien tietojen noutamiseen, eivät tarvitse metatietoja. Näiden moduulien hintatiedot voidaan noutaa ulkoisista rahdinkuljettajien järjestelmistä tavallisesti verkkopalvelun kautta. Voit käyttää esimerkiksi kilometrien laskentaa, joka noutaa tiedot suoraan Bing-kartoista, joten et tarvitse metatietoja tälle moduulille.

| **Huomautus**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Supply Chain Managementin mukana toimitettavat kuljetuksen hallintamoduulit käyttävät sovelluksesta noudettavia tietoja. Ulkoisiin järjestelmiin liittyvät moduulit eivät sisälly Operationsiin. Moduuleihin perustuvan laajennettavuusmallin avulla voit kuitenkin rakentaa laajennuksia käyttämällä Visual Studio-työkaluja. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>MIten määritän kuljetuksen hallinnan moduulin metatiedot?
Kuljetuksenhallintamoduulin metatiedot määritetään eri tavalla eri tyyppisille moduuleille.

| Kuljetuksenhallinnan moduuli               | Metatietojen konfigurointi                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hinnan laskenta**                                | Edellyttää **hintaperusteen tyyppiä**. Hintaperusteen tyyppi sisältää metatietoja hintaperusteen tiedoille ja hintaperusteen määritystiedoille. Hintaperusteen metatietojen rakenne määritetään hinnan laskennan tyypin perusteella. Hintaperusteen määrityksen metatietojen rakenne määritetään hinnan laskentaan liitetyn hintaperusteen määrittäjän tyypillä. Voit määrittää hinnan laskennassa käytettävän hintaperusteen tyypin **Hinnan laskenta**- ja **Hinnan päätiedot** -sivuilla. |
| **Vyöhykkeen laskenta**                                | Edellyttää, että metatiedot voidaan määrittää suoraan vyöhykkeessä.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Siirtoajan laskenta** ja **Kilometrien laskenta** | Hakee metatietoja suoraan kilometrikorvausmoduulin konfigurointiasetuslomakkeesta.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Esimerkki hinnan laskennan metatiedoista** Kuljetuksen hallintamoduuli vaatii alkuperäisen osoitteen, kohdeosavaltion ja maan/alueen sekä lähetyksen alku- ja päätepisteen tunnistamisen. Käyttämällä näitä vaatimuksia metatiedot näyttävät tiedot seuraavan taulukon mukaisesti. Taulukko sisältää myös tietoja vaadittavien syöttötietojen tyypistä.
-   Voit määrittää nämä tiedot valitsemalla **Hintaperusteen tyyppi** -sivulta **Kuljetuksen hallinta** &gt; **Asetukset**.

| Järjestys | Nimi                          | Kentän tyyppi | Tietotyyppi | Hakutyyppi    | Pakollinen |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Alkuperä - postinumero            | Määritys | merkkijono    | Postinumero    | Valittu  |
| 2        | Kohteen osavaltio             | Määritys | merkkijono    | Tila          |           |
| 3        | Kohteen alkupostinumero | Määritys | merkkijono    | Postinumero    | Valittu  |
| 4        | Kohteen loppupostinumero   | Määritys | merkkijono    | Postinumero    | Valittu  |
| 5        | Kohdemaa           | Liitos | Merkkijono    | Maa tai alue |           |

### <a name="whitepaper"></a>Tekninen raportti

Lisätietoja saa lataamalla seuraava tekninen raportti (joka on kirjoitettu tukemaan AX2012-versiota, mutta koskee myös Dynamics 365 Supply Chain Managementia)

- [Kuljetustenhallintamoduulit](https://download.microsoft.com/download/e/0/9/e0957665-c12f-43c7-94c0-611cc49d7d61/TransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]