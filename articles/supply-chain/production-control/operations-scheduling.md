---
title: Työvaiheiden ajoitus
description: Tämä aihe sisältää yleisiä tietoja työvaiheiden ajoittamisesta. Työvaiheiden ajoitusta voidaan käyttää, kun tuotantoprosessin kestosta halutaan yleisarvio.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 298c07346427a949ffa544e66eb6b01995dadc38
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560253"
---
# <a name="operations-scheduling"></a>Työvaiheiden ajoitus

[!include [banner](../includes/banner.md)]

Tämä aihe sisältää yleisiä tietoja työvaiheiden ajoittamisesta. Työvaiheiden ajoitusta voidaan käyttää, kun tuotantoprosessin kestosta halutaan yleisarvio.

Voit ajoittaa tuotannon työvaiheiden tasolla ja työn tasolla. Päinvastoin kuin töiden ajoituksessa, työvaiheiden ajoituksessa ei hajoteta reitityksen tuotannon työvaiheita töiksi. Jos haluat sisällyttää ajoitukseen yksityiskohtaisia tietoja, esimerkiksi tietoja nykyisestä kapasiteetista, voit suoritta työn ajoituksen työvaiheiden ajoituksen jälkeen. Voit myös suorittaa ainoastaan töiden ajoituksen. Töiden ajoitusta käytetään yleensä yksittäisten töiden ajoituksessa tuotannossa, ja normaalisti se tapahtuu välittömästi tai lyhyellä aikakehyksellä..

## <a name="components-of-operations-scheduling"></a>Työvaiheiden ajoittamisen komponentit
Työvaiheiden ajoituksen pääkomponentit ovat ajoituksen suunta, resurssien kapasiteetti sekä materiaalien optimointi. Käyttämällä työvaiheiden ajoitusta saavutetaan seuraavat tavoitteet:

-   suunnittelumenetelmän hallinta ajoittamalla tietystä päivämäärästä eteen- tai taaksepäin
-   resurssien käytön optimointi aikatauluttamalla tuotantoja resurssien kapasiteetin perusteella. Tämä auttaa myös tunnistamaan tilanteet, joissa tarvitaan vaihtoehtoista resursseja.
-   materiaalien käytön optimointi aikatauluttamalla tuotantoja tarvittavien materiaalien saatavuuden perusteella.
-   viitetuotannon aikatauluttaminen ja synkronointi. Viitetuotannot päivämäärät korjataan, kun tuotantotilauksen aikataulua muutetaan.

Työvaiheiden ajoitus voidaan suorittaa vasta sen jälkeen, kun tuotantotilauksen kustannukset on arvioitu. Jos et ole suorittanut arviointia, se suoritetaan automaattisesti ennen työvaiheiden ajoituksen aloittamista. Työvaiheiden aikataulussa määritetään seuraavat tiedot:

-   tuotannolle suunnitellut tuotteet
-   tuotteen konfiguraatio
-   tuotantoon tarvittavat määrät
-   tuotannon aloitus- ja lopetuspäivä
-   kapasiteetin varaukset resursseille, jotka suorittavat tuotantotehtäviä.

Tuotannon työvaiheille määritetään asetusaika, prosessiaika ja ajoaika. Kun suoritat työvaiheiden ajoituksen, tuotantotilauksen tilana on **ajoitettu**, ja kaikki työvaiheet ajoitetaan siinä järjestyksessä, joka on määritetty tuotantoreitityksessä. Kuitenkin vain työvaiheen kesto otetaan huomioon. Aloitus- ja lopetusaikoja ei aikatauluteta.

## <a name="scheduling-direction-and-date"></a>Ajoitussuunta ja -päivämäärä
Ajoitussuunta on perustava osa ajoitusprosessia. Tuotanto voidaan ajoittaa eteenpäin tai taaksepäin mistä tahansa päivämäärästä alkaen ajoitus- ja suunnitteluvaatimusten mukaisesti.

-   **Eteenpäinajoitus ajoituspäivästä**: voit ajoittaa tuotannon alkamaan mahdollisimman aikaisin. Tuotanto voidaan aloittaa tänään, huomenna tai minä tahansa tulevana päivänä. Tuotanto ajoitetaan eteenpäin päättymään aikaisempina mahdollisena päättymispäivänä.
-   **Taaksepäinajoitus ajoituspäivästä**: voit ajoittaa tuotannon alkamaan mahdollisimman myöhään. Taaksepäinajoitus perustuu päivämäärään, jolloin tuotannon on oltava valmis. Aikataulu lasketaan määräpäivästä taaksepäin myöhäisimpään mahdolliseen päivämäärään, jolloin tuotannon voi aloittaa niin, että se saadaan valmiiksi määräaikaan mennessä.

## <a name="resource-scheduling"></a>Resurssien ajoitus
Kun suoritat työvaiheiden ajoituksen, jokainen tuotantoreitityksen työvaihe ajoitetaan työvaiheelle määritetyn resurssin mukaan. Lisäksi kunkin työvaiheen kesto määritetään tuotantoreititykseen. Jos työvaiheelle määritetään resurssiryhmä, ajoitus varaa ryhmän kapasiteettia. Työvaiheiden ajoittaminen ei kuitenkaan valitse tiettyjä ryhmän resursseja, kuten töiden ajoituksessa tapahtuu. Jos käytettävissä on vain rajallisesti kapasiteettia, ajoitus on riippuvainen tuotantoon tarvittavien resurssien saatavuudesta. Työvaiheiden ajoitus noudattaa tuotantoreitityksessä määritettyä työvaihesarjaa. Ajoitus varaa kapasiteettia resurssiryhmistä tuotannon reititykselle määritettyjen työvaiheaikojen perusteella. Resurssiryhmän kapasiteetti on kaikkien tuotantoon osallistuvien resurssien käytettävissä olevan kapasiteetin summa. Resursseille jo aiemmin tehdyt kapasiteettivaraukset katsotaan kapasiteetiksi, joka ei ole käytettävissä. Jos tuotannolle ei ole riittävästi käytettävissä olevaa kapasiteettia, tuotantotilaukset saattavat viivästyä tai jopa pysähtyä. Voit myös halutessasi määrittää tuotantoon osallistuvalta resurssilta odotettavan tehokkuuden. Tehokkuus määritetään resurssin prosenttiosuutena. Tehokkuusprosentti muokkaa resurssin tuotantokapasiteettia. Tämä muutos vaikuttaa resurssille varattavaan aikaan. Resursseja käyttävien työvaiheiden läpimenoaikoja oikaistaan vastaavasti.

## <a name="operations-scheduling-and-master-planning"></a>Työvaiheiden ajoitus ja pääsuunnittelu
Työvaiheiden aikataulu vaikuttaa myös pääsuunnitteluun ja määrittää materiaalitarvelaskennat. Työvaiheiden aikataulussa huomioidaan seuraavat tiedot:

-   **käsittelemättömät tuotannot**: tuotteet, jotka on suunniteltu, julkaistu tai käynnistetty
-   **materiaalin saatavuus**: varasto, osatuotannot, alihankkijat ja toimittajat
-   **Kapasiteetin saatavuus**: resurssit, jotka tarvitaan tuotantoon

## <a name="cancellations"></a>Peruutukset
Kun suoritat työvaiheen ajoituksen, voit peruuttaa tiettyjä reitityksen osia. Näitä osia ovat esimerkiksi jonotusaika, asetusaika, prosessiaika, päällekkäisaika ja kuljetusajat.

## <a name="finite-materials"></a>Rajallinen materiaali
Jos käsittelet rajallista materiaalia, ajoitukseen vaikuttaa myös tuotantoon tarvittavien materiaalien saatavuus. Jos tuotantoon ei ole riittävästi komponentteja käytettävissä, tuotanto voi viivästyä. Ajoitus voi perustua myös materiaalien käyttöön määrittämällä tuotannolle välttämättömät materiaalit. Kun optimoit sekä resurssikapasiteetin että materiaalien saatavuuden, tuotanto lasketaan näiden rajoitusten perusteella. Tuotantotilausta ei voi ajoittaa alkamaan ennen kuin kapasiteetti ja materiaalit ovat käytettävissä samaan aikaan ja vaaditun määrän mukaisesti.

<a name="additional-resources"></a>Lisäresurssit
--------

[Työvaiheen ajoitusvaihtoehdot](operation-scheduling-options.md)



