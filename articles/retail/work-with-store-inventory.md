---
title: Myymälän varastonhallinta
description: Tässä ohjeaiheessa käsitellään asiakirjatyyppejä, joiden avulla hallitaan varastoa.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 551a8408aa730bc1916f1c57b7cfd773966ce8bf
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606800"
---
# <a name="store-inventory-management"></a>Myymälän varastonhallinta

[!include [banner](includes/banner.md)]

Kun varastoa käsitellään Dynamics 365 for Retailissa ja käytössä on myyntipistesovellus, on tärkeää muistaa, että myyntipiste tukee vain rajoitetusti varastodimensioita ja tiettyjä varastonimiketyyppejä.

Myyntipisteratkaisu ei tue seuraavia nimikemäärityksiä:

- Tuoterakennenimikkeet (lukuun ottamatta myyntirakenteita, joissa käytetään joitakin tuoterakennekehikon osia)
- Todellisen painon nimikkeet
- Eräohjatut nimikkeet

Myyntipistesovellus ei tue tällä hetkellä myyntipisteessä seuraavia seurantadimensioita:

- Erän seurantadimensio
- Omistajadimensio

Myyntipisteratkaisu tukee rajoitetusti seuraavia dimensioita. Rajoitettu tuki ilmaisee, että myyntipiste voi palauttaa jotkin näistä dimensioista automaattisesti varastotapahtumiksi varaston tai kaupan asetusten määritysten perusteella. Myyntipiste ei tue dimensioita täysin sillä tavoin kuin niitä tuetaan, jos myyntitapahtuma viedään manuaalisesti ERP:hen. 

- **Fyysisen varastoinnin sijainti** – Käyttäjillä ei ole mahdollisuutta hallita vastaanottovaraston sijaintia nimikkeille, jotka on vastaanotettu myymälävarastoon, kun säilöä ei ole konfiguroitu käyttämään varastonhallintaprosessia. Näille nimikkeille käytetään myymälän varastossa määritettyä oletusarvoista vastaanottosijaintia. Jos varastonhallintaprosessi on otettu käyttöön myymälälle, järjestelmä käynnistää rajoitetun tuen, joka pyytää käyttäjää valitsemaan vastaanottopaikan koko kuittiin. Myymälästä myydyt nimikkeet myydään aina oletusarvoiseen vähittäismyyntisijaintiin, joka on määritetty myymälän varaston määrityksissä. Palautettavan varaston hallinnan sijaintia voidaan hallita myymälävaraston oletusarvon mukaisen palautuksen sijaintimäärityksen avulla tai palautusten syykoodien perusteella, jotka on määritetty palautuksen sijaintikäytännössä.
- **Rekisterikilpi** – Rekisterikilvet ovat käytössä vain, kun **Käytä varastonhallintaprosesseja** on otettu käyttöön nimikkeessä ja kaupan varastossa. Myyntipistesovelluksessa, jos varasto vastaanotetaan myymälävarastoon, jossa varaston hallintaprosessi on otettu käyttöön, ja jos nimikkeen vastaanottamiselle valittu sijainti on sidottu sijaintiprofiiliin, joka edellyttää rekisterikilpiohjausta, myyntipistesovellus käyttää vastaanottavan rivin rekisterikilpeä järjestelmällisesti. Myyntipistekäyttäjillä ei ole mahdollisuutta muuttaa tai hallita tämän rekisterikilven tietoja. Jos rekisterikilpien hallinta on pakollista, myymälästä käytetään WMS-mobiilisovellusta tai Back Office ERP -asiakasohjelmaa näiden nimikkeiden vastaanottamisen hallintaan.
- **Sarjanumero** – Myyntipistesovelluksella on rajallinen tuki yksittäiselle sarjanumerolle, joka rekisteröidään tapahtumamyyntiriville myyntipistesovelluksessa luoduille tilauksille. Tätä sarjanumeroa ei ole vahvistettu varastossa jo rekisteröidyille sarjanumeroille. Jos myyntitilaus luodaan Call Center -kanavalla tai se toteutuu ERP-järjestelmän ja useiden sarjanumeroiden kautta, se kirjataan yhdelle myyntiriville ERP-järjestelmän toteutusprosessin aikana, näitä sarjanumeroita ei voida käyttää tai vahvistaa, jos palautukset käsitellään näiden tilausten myyntipisteessä.
- **Varaston tila** – Nimikkeille, jotka käyttävät varastonhallintaprosessia ja vaativat varastontilan, tätä tilakenttää ei voi määrittää tai muokata myyntipistesovelluksen kautta. Myymälän varaston konfiguraatiossa määritettyä varaston oletustilaa käytetään vastaanotettaessa nimikkeitä varastoon.

> [!NOTE]
> Kaikkien organisaatioiden on testattava nimikemääritykset myyntipisteen kehitys- tai testiympäristössä, ennen kuin ne otetaan käyttöön tuotannossa. Testaa nimikkeet suorittamalla tavallinen itsepalvelutukun myyntitapahtuma ja luomalla (tarvittaessa) nimikkeille asiakastilauksia myyntipisteessä. Testauksen on sisällettävä täydelliset laskelmien kirjaamisprosessit testiympäristössä ja sen varmistaminen, että mitään ongelmia ei esiinny.
>
> Jos nimikkeet määritetään tavalla, jota myyntipistesovellus ei tue ja ilman asianmukaista testausta, voi aiheuttaa laskelmien kirjaamisprosessin epäonnistumisen tuotantoympäristössä ilman, että ongelmat voitaisiin korjata kätevästi. Kumppanin tai asiakkaan sovellukseen tekemiä mukautuksia on mahdollista harkita, jotta nämä kirjausprosessit onnistuisivat. Jos mukautuksia ei tarvita, organisaation on varmistettava, että tuotteiden tuotemääritykset on tehty siten, että tavanomaista myyntipistesovellusta, tilausten luontia ja laskelmien kirjausprosessia tuetaan.

## <a name="purchase-orders"></a>Ostotilaukset

Ostotilaukset luodaan pääkonttorilla. Jos vähittäismyynnin varasto sisältyy ostotilauksen otsikkoon, tilaus voidaan vastaanottaa myymälään käyttämällä Modern POS- tai Cloud POS-toimintoja Microsoft Dynamics 365 for Retailissa **Poiminta / vastaanottaminen** -toiminnolla. Kun myymälälle vastaanotetut määrät on syötetty ostotilausasiakirjan myyntipisteen **vastaanota nyt** -kenttään, ne voidaan tallentaa paikallisesti tai sitoa. Näiden tietojen tallentaminen paikallisesti ei vaikuta varastossa olevaan varastoon. Tallentaminen on tehtävä vain, jos käyttäjä ei ole valmis kirjaamaan vastaanottoa HQ-järjestelmään ja tarvitsee vain tavan tallentaa tilapäisesti aiemmin kirjoitetut **Vastaanota tiedot nyt** -tiedot. Tällöin vastaanottotiedot tallennetaan paikallisesti käyttäjän kanavatietokantaan. Kun asiakirja on käsitelty **Toimitus**-valinnalla, **Vastaanota nyt** -tiedot lähetetään HQ-kohteeseen ja ostotilauksen vastaanotto kirjataan. 

## <a name="transfer-orders"></a>Siirtotilaukset

Siirtotilaus voi määrittää, että tietty myymälä on sijainti, josta nimikkeet voidaan toimittaa, tai varastopaikka, johon nimike saapuu. Jos POS-käyttäjä on siirtotilauksen toimitusvarasto, hän voi syöttää **Toimitus nyt** -määriä suoraan POS:ista. Lähetysmyymälän syöttämiä tietoja voidaan tallentaa paikallisesti tai sitoa. Kun tallennetaan paikallisesti, HQ-siirtotilausasiakirjaan ei tehdä päivityksiä. Tallentaminen on tehtävä vain, jos käyttäjä ei ole valmis kirjaamaan lähetystä HQ-järjestelmään ja tarvitsee vain tavan tallentaa tilapäisesti aiemmin kirjoitetut **Lähetä nyt** -tiedot. Kun myymälä on valmis vahvistamaan lähetyksen, tulee valita **Toimitus**-vaihtoehto. Tämä kirjaa siirtotilauksen lähetyksen HQ-tilaan, jotta vastaanottava varasto voi vastaanottaa sitä vastaan. 

Jos POS-käyttäjä on siirtotilauksen vastaanottava varasto, hän voi syöttää **Vastaanota nyt** -määriä suoraan POS:ista. Vastaanottavan myymälän syöttämiä tietoja voidaan tallentaa paikallisesti tai sitoa. Tallentaminen on tehtävä vain, jos käyttäjä ei ole valmis kirjaamaan vastaanottoa HQ-järjestelmään ja tarvitsee tavan tallentaa tilapäisesti aiemmin kirjoitetut **Vastaanota tiedot nyt** -tiedot. Tällöin vastaanottotiedot tallennetaan paikallisesti käyttäjän kanavatietokantaan. Kun asiakirja on käsitelty **Toimitus**-valinnalla, **Vastaanota nyt** -tiedot lähetetään HQ-kohteeseen ja siirtotilauksen vastaanotto kirjataan. On tärkeää huomata, että vastaanottava myymälä voi sitoutua vastaanottamaan vain määriä, jotka ovat yhtä suuria tai pienempiä kuin toimitetut määrät. Yritys vastaanottaa siirtotilauksen määriä, joita ei ole aiemmin lähetetty aiheuttaa virheitä, eikä vastaanottoa vahvisteta HQ-ohjelmassa.

## <a name="stock-counts"></a>Varaston inventoinnit

Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa. Ajastetut varaston inventoinnit määritetään pääkonttorilla. Ne määrittävät nimikkeet, joista on tehtävä inventointi. Pääkonttori luo inventointiasiakirjan, joka voidaan vastaanottaa myymälässä, jossa todelliset käytettävissä olevat määrät syötetään Modern POS- tai Cloud POS -sovelluksessa. Ajoittamattomat varaston inventoinnit aloitetaan myymälässä ja todelliset käytettävissä olevat varastomäärät päivitetään Modern POS- tai Cloud POS -sovelluksessa. Ajoittamattomilla varaston inventoinneilla ei ole ennalta määritettyä nimikeluetteloa kuten ajoitetun varaston inventoinneilla. Kun jompikumpi varaston inventointi on suoritettu, se vahvistetaan ja lähetetään pääkonttorille. Pääkonttorissa inventointi tarkistetaan ja kirjataan erillisenä vaiheena.

## <a name="inventory-lookup"></a>Varastohaku

Nykyistä tuotteen määrää useissa myymälöissä ja varastoissa voi tarkastella **Varaston haku** -sivulla. Nykyisen käytettävissä olevan määrän lisäksi luvattavissa oleva määrä (ATP) nähdään yksittäisistä myymälöistä. Voit tehdä tämän valitsemalla ensin myymälän, jonka ATP:tä haluat tarkastella, ja sitten **Näytä myymälän käytettävissä oleva määrä**.
