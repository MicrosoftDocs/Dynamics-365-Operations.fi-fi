---
title: Organisaatiot ja organisaatiohierarkiat (Commerce-perustiedot)
description: "Commerce-perustiedoissa on kolmenlaisia sisäisiä organisaatioita, joita voit määrittää auttaaksesi organisaatiota liiketoimintaprosessin suorittamisessa tai tavoitteen saavuttamisessa."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 93711977ad8d861ca75ba80ee542ee112c8ddd2f
ms.lasthandoff: 03/31/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Organisaatiot ja organisaatiohierarkiat (Commerce-perustiedot)

[!include[banner](includes/banner.md)]


Commerce-perustiedoissa on kolmenlaisia sisäisiä organisaatioita, joita voit määrittää auttaaksesi organisaatiota liiketoimintaprosessin suorittamisessa tai tavoitteen saavuttamisessa. 

Organisaatio muodostuu joukosta ihmisiä, jotka työskentelevät yhdessä liiketoimintaprosessin suorittamiseksi tai tavoitteen saavuttamiseksi. Organisaatiohierarkiaa edustaa organisaatiosi muodostavien liiketoimintayksiköiden välisiä suhteita.

## <a name="organizations"></a>Organisaatiot
Commerce-perustiedoissa voit määrittää kolmentyyppisiä sisäisiä organisaatioita: yrityksiä, toimintayksiköitä ja ryhmiä. Kaikki Microsoft Dynamics AX:n sisäiset organisaatiot ovat Osapuoli-tyyppisiä yksiköitä. Tämän vuoksi nämä organisaatiot käyttävät osoitekirjaa osoitteen ja muiden yhteystietojen tallentamiseen. Osapuoli voi olla joko henkilö tai organisaatio, ja se voi kuulua yhteen tai useampaan osoitekirjaan.
### <a name="legal-entities"></a>Oikeushenkilöt

Yritys on organisaatio, jolla on rekisteröity tai lain vaatima rakenne. Yritys voi solmia oikeudellisia sopimuksia ja yritykseltä edellytetään suorituskykyä kuvaavien lausuntojen valmistelemista. Yritys on tietyntyyppinen oikeushenkilö Microsoft Dynamics AX:ssä, ja jokainen oikeushenkilö on liitetty yritystunnukseen. Tämä liitos on olemassa, koska yritystunnusta, tai DataAreaId:tä käytetään joissain tietomalleissa, joissa yrityksiä käytetään tietoturvan rajoittamiseen. Käyttäjillä on pääsy vain sen yrityksen tietoihin, jonka järjestelmään he ovat sillä hetkellä kirjautuneena.

### <a name="operating-units"></a>Käyttöyksiköt

Toimintayksikkö on organisaatio, jota käytetään jakamaan liiketoiminnan taloudellisten resurssien hallinta ja operationaaliset prosessit. Toimintayksikön henkilöiden vastuulla on rajattujen resurssien maksimointi, prosessien tehostaminen ja suorituskyvyn raportointi. Commerce-perustiedoissa toimintayksiköihin kuuluvat kustannuspaikat, liiketoimintayksiköt, arvovirrat, osastot ja vähittäismyyntikanavat. Seuraavassa taulukossa on lisätietoja jokaisesta toimintayksikön tyypistä:
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Toimintayksikön tyyppi** | **Kuvaus**                                                                         | **Tarkoitus**                                                                                                                                 |
| Liiketoimintayksikkö           | Osittain itsenäinen toimintayksikkö, joka luodaan vastaamaan yrityksen strategisiin tavoitteisiin. | Käytä liiketoimintayksiköitä taloushallinnan raportointiin, joka perustuu toimialoihin tai tuotelinjoihin, joita organisaatio tarjoaa yrityksille. |
| Vähittäismyyntikanava          | Toimintayksikkö, joka edustaa kivijalkaliikettä.                             | Käytä yhden tai useamman myymälän hallintaan yrityksen sisällä tai niiden välisesti.                                                               |

## <a name="organizational-hierarchies"></a>Organisaatiohierarkiat
Jokaiseen hierarkiaan liitetään tarkoitus Commerce-perustiedoissa. Hierarkian tarkoitus määrittää hierarkiaan sisällytettävät organisaatiotyypit. Tarkoitus määrittää myös käyttötilanteet, joissa hierarkiaa voidaan käyttää. Esimerkiksi vähittäismyyntihierarkiaa voi käyttää tuotteiden myyntiin ja ostamiseen myymälässä. Hierarkian organisaatiot voivat jakaa parametrejä, käytäntöjä ja tapahtumia. Organisaatio voi periä tai ohittaa ylätason organisaation parametrit. Jaetut perustiedot, kuten tuotteet ja osoitekirjat koskevat koko organisaatiota, eikä niitä voi ohittaa yksittäisissä organisaatioissa.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Parhaat käytännöt organisaatiohierarkian määrittämiseen

Ota huomioon seuraavat suositeltavat menetelmät organisaatiohierarkian käyttöönoton yhteydessä:
-   Luo osasto määrittämään yrityksen ja liiketoimintayksikön välistä liitosta. Sitten voit koota tietoja osastosta yritykseen lakisääteistä raportointia varten ja osastosta liiketoimintayksikköön sisäistä raportointia varten.
-   Yksittäisessä yrityksessä ei mallinneta useita hierarkioita samaan hierarkiatarkoitukseen.
-   Älä luo hierarkiaa joka tarkoitukseen. Voit yleensä käyttää yhtä hierarkiaa moneen tarkoitukseen. Esimerkiksi yksi toimintayksiköiden hierarkia voidaan määrittää kaikkiin käytäntöön liittyviin tarkoituksiin.
-   Luo tasapainotetut hierarkiat. Hierarkiassa kaikki solmut, jotka ovat yhtä kaukana juurisolmusta, määritellään tasona. Tasapainotetussa hierarkiassa vain yhdentyyppinen liiketoiminnan yksikkö voi esiintyä kussakin tasossa, ja etäisyys juurisolmusta tasoihin on yhdenmukainen. Jos on keskitasoja osaston ja yrityksen tai liiketoimintayksikön välillä, paikkamerkin organisaatiot voivat olla pakollisia tasapainotetun hierarkian luomiseksi.
-   Älä määritä toimintayksiköille erillistä hierarkiaa, jos yritysten rakenne on myös toimintarakenteesi. Yhdistelmähierarkia, johon kuuluu yrityksiä ja toimintayksiköitä voi olla hyödyllinen molemmille.
-   Ennen kuin määrität tärkeimpiä uudelleenjärjestelyn tilanteita, käytä hierarkian voimassaolopäivämääriä vaikutusanalyysiin ja oikeellisuustarkistukseen.
-   Tallenna hierarkia luonnoksena, jos luulet tekeväsi siihen muutoksia ennen sen julkaisemista.
-   Rajoita niiden käyttäjien määrää, joilla on oikeudet lisätä organisaatioita hierarkiaan tai poistaa niitä tuotantoympäristössä. Pienempi numero laskee kalliiden virheiden mahdollisuutta ja tarvetta korjata virheitä.

## <a name="retail-store-management"></a>Vähittäismyymälän hallinta
Seuraavassa taulukossa kuvataan Commerce-perustietojen skenaariot, joissa käytetään organisaatiohierarkioita.
| Tehtävä                                                                           | Kuvaus                                                                                                                                                                                                                                                                                                | Hierarkian tarkoitus    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Hallitse vähittäismyyntivalikoimia                                                      | Tunnista tuotteet, jotka ovat myynnissä jokaisessa myymälässä.                                                                                                                                                                                                                                             | Vähittäismyyntivalikoima    |
| Hallitse vähittäismyynnin täydennystä                                                    | Ryhmittele myymälät täydentääksesi varastot täydennyssääntöjen mukaisesti.                                                                                                                                                                                                                                          | Vähittäismyynnin täydennys |
| Myymälöiden raporttitiedot                                                         | Ryhmittele myymälät raportointiin.                                                                                                                                                                                                                                                                                | Vähittäismyynnin raportointi     |
| Kirjaa varasto, laske laskelmat tai kirjaa laskelmat myymäläryhmälle | Luo myymäläryhmä, joka voidaan liittää erätyöhön. Kun määrität erätyön varaston kirjausta varten, lasket laskelmia tai kirjaat laskelmia, voit määrittää mitä hierarkiaa työ koskee. Kun myymälöitä lisätään hierarkiaan tai poistetaan siitä, sinun ei tarvitse muokata komentojonotyötä. | Vähittäismyynnin myyntipistekirjaus   |






