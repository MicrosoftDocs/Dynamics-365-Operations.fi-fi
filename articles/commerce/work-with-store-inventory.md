---
title: Myymälän varastonhallinta
description: Tässä ohjeaiheessa käsitellään asiakirjatyyppejä, joiden avulla hallitaan varastoa.
author: rubencdelgado
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 64106cb1aeea01f1f227247d32b8b1dfdea98362
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020192"
---
# <a name="commerce-inventory-management"></a>Commercen varastonhallinta

[!include [banner](includes/banner.md)]

Kun käsittelet varastoa Microsoft Dynamics 365 Commercessa ja käytät mitä tahansa Commerce-sovellusta, joka on liitetty Commerce Scale Unit (CSU) -yksikköön, on tärkeää tietää, että CSU:n tilaustenkäsittelylogiikka tukee rajoitetusti joitakin varastodimensioita ja joitakin varastonimiketyyppejä. Commerce-sovellukset eivät tue kaikkia niitä nimikkeen määritysominaisuuksia, jotka ovat saatavana Dynamics 365 Supply Chain Managementin nimikkeen määritysasetuksissa.

CSU-pohjaiset Commerce-sovellukset eivät tue seuraavia tuotedimensioita ja nimikemäärityksiä:

- Tuotedimensio- ja tuoterakennenimikkeiden määrittäminen (poikkeuksen niitä vähittäismyyntirakenteista, joissa käytetään joitakin tuoterakennekehyksen osia)
- Todellisen painon nimikkeet
- Version tuotedimension avulla ohjatut nimikkeet

CSU-pohjaiset Commerce-sovellukset eivät tue seuraavia seurantadimensioita:
- Omistajadimensio

- Myyntipistesovellus voi tarjota rajoitettua tukea seuraaville dimensioille. Myyntipiste saattaa merkitä joitakin näitä dimensioita varastotapahtumiin varaston tai myymälän asetusten määritysten perusteella. Myyntipiste ei kuitenkaan tue dimensioita täysimääräisesti siinä määrin kuin jos myyntitapahtuma vietäisiin manuaalisesti Commerce headquarters -sovellukseen. 

- **Varaston sijainti** – Jos käyttäjät käyttävät myyntipisteen uutta [saapuvaa toimintoa](./pos-inbound-inventory-operation.md) ja [lähtevää toimintoa](./pos-outbound-inventory-operation.md), he voivat valita varaston varastosijainnin, johon nimikkeitä vastaanotetaan tai josta lähtevät siirtotilaukset lähetetään. Jos käytössä on vanhentunut **Keräys ja vastaanotto** -toiminto, vastaanoton ja lähtevien siirtojen lähettämisen yhteydessä on käytettävissä rajoitettu sijainnin hallinnan tuki. Tämä tuki on käytettävissä vain, jos **Käytä varastonhallintaprosesseja** -vaihtoehto on otettu käyttöön sekä nimikkeen osalta että myymälän varastossa. Varastosijaintia ei voi tällä hetkellä käyttää **Varaston inventointi**- ja **Varastohaku**-toimintojen kanssa.

- **Rekisterikilpi** – Rekisterikilvet ovat käytössä vain, kun **Käytä varastonhallintaprosesseja** -vaihtoehto on otettu käyttöön nimikkeessä ja myymälän varastossa. Jos varasto vastaanotetaan myyntipistesovelluksessa **Saapuva toiminto**- tai **Keräys ja vastaanotto** -toimintoa käyttämällä myymälävarastoon, jossa varaston hallintaprosessi on otettu käyttöön, ja jos nimikkeen vastaanottamiselle valittu sijainti on sidottu sijaintiprofiiliin, joka edellyttää rekisterikilpiohjausta, myyntipistesovellus käyttää vastaanottavan rivin rekisterikilpeä järjestelmällisesti. Myyntipistekäyttäjät eivät voi muuttaa eivätkä hallita näitä rekisterikilven tietoja. Jos rekisterikilpien hallinta on pakollista, kyseisiä nimikkeitä kannattaa hallita myymälässä [varastointisovelluksella](../supply-chain/warehousing/install-configure-warehousing-app.md) tai tausta-asiakasohjelmalla.

- **Sarjanumero** – Myyntipistesovellus tukee rajoitetusti sellaisen yksittäisen sarjanumeron rekisteröintiä, joka luodaan myyntipistesovelluksessa tapahtumamyyntiriville ja joka sisältää sarjoitettuja nimikkeitä. Tätä sarjanumeroa ei ole tarkistettu varastoon jo rekisteröityjen sarjanumeroiden perusteella. Jos myyntitilaus luodaan puhelinkeskuskanavassa tai täytetään ERP-järjestelmän avulla ja yhteen myyntitilausriviin rekisteröidään useita sarjanumeroita tämän täyttämisprosessin aikana, kyseisiä sarjanumeroita ei voida käyttää tai tarkistaa, jos tilauksen palautukset käsitellään myyntipisteessä. Jos varaston vastaanottoon käytetään **saapuvien toimintoa**, käyttäjät voivat [rekisteröidä tai vahvistaa vastaanotetut sarjanumerot](./pos-serialized-items.md).

- **Erätunnus**: Myyntipistesovellus tarjoaa rajoitetusti tukea laskelman kirjaamisen aikana, jos eräohjattua nimikettä myydään, mutta myyntipisteen käyttäjät eivät voi määrittää myyntipistesovelluksen käytön kautta myydyn tai kerätyn erän tunnusta.

- **Varaston tila** – Jos nimikkeet käyttävät varastonhallintaprosessia ja edellyttävät varaston tilaa, tätä tilakenttää ei voi määrittää eikä muokata myyntipistesovelluksessa. Nimikkeiden varastoon vastaanottamisessa käytetään myymälän varastomäärityksessä määritettyä varaston oletustilaa.

> [!NOTE]
> Kaikkien organisaatioiden on testattava nimikemääritykset Commerce-sovellusten kehitys- tai testiympäristöissä, ennen kuin kyseiset nimikemääritykset otetaan käyttöön tuotantoympäristöissä. Testaa nimikkeet käyttämällä niitä suorittamaan tavallisia käteisostomyyntitapahtumia myyntipisteessä ja luo asiakastilauksia (jos käytettävissä) myyntipisteen, soittokeskuksen tai sähköisen kaupan kautta, jotta voidaan varmistaa, että niitä tuetaan kokonaisvaltaisesti. Myös myyntipisteen täyttämis- ja varastoprosessit (kuten varaston vastaanotto- ja tilauksen täyttämistoiminnot) on testattava ennen uusien nimikemääritysten käyttöönottoa, sillä näin voidaan varmistaa, että myyntipistesovellus tukee niitä. Testauksen on sisällettävä täydelliset laskelmien/tilauksien kirjaamisprosessit testiympäristössä ja sen varmistaminen, että mitään kirjausongelmia ei esiinny, kun kyseisille nimikkeille luodaan ja kirjataan tilauksia Commerce headquarters -sovelluksessa.
>
> Jos nimikkeet on konfiguroitu niin, että Commerce-sovellukset eivät tue niitä ja soveltuvaa testausta ei tehdä, saattaa ilmetä virheitä, joita ei helposti korjata tai joita ei välttämättä pystytä ollenkaan korjaamaan.

## <a name="purchase-orders"></a>Ostotilaukset

Ostotilaukset luodaan Commercen pääkonttorisovelluksessa. Jos myymälän varasto sisältyy ostotilauksen otsikkoon tai ostotilausriveille, rivit voidaan vastaanottaa myymälään käyttämällä myyntipisteen [saapuvaa toimintoa](./pos-inbound-inventory-operation.md). 

## <a name="transfer-orders"></a>Siirtotilaukset

Siirtotilaukset voidaan luoda Commercen pääkonttorisovelluksessa tai myyntipisteessä joko [saapuvien toiminnolla](./pos-inbound-inventory-operation.md) tai [lähtevien toiminnolla](./pos-outbound-inventory-operation.md). Myyntipisteen **saapuvien toiminnolla** luodaan siirtotilauspyyntö, jolla pyydetään lähettämään varastoa myymälään toisesta varasto- tai myymäläsijainnista. Myyntipisteen **lähtevien toiminnolla** luodaan siirtotilauspyyntö, jolla pyydetään lähettämään varastoa myymälästä toisesta varasto- tai myymäläsijaintiin. Kun myymälän siirtotilaus on luotu, myymälä voi hallita siirtotilauksen varaston vastaanottoa myyntipisteen **saapuvien toiminnolla**. Jos myymälä lähettää varastoa toiseen sijaintiin, kyseisen myymälän lähtevien lähetysprosessia hallitaan myyntipisteen **lähtevien toiminnolla**.

## <a name="stock-counts"></a>Varaston inventoinnit

Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa. Ajoitetut varaston inventoinnit luodaan Commercen pääkonttorisovelluksessa luomalla myymälään varastoon linkitetty Inventointikirjauskansio-asiakirja. Tässä kirjauskansiossa määritetään inventoitavat nimikkeet. Myymälä voi sitten käyttää näitä valmiiksi määritettyjä inventointikirjauskansioita ja käyttää niitä myyntipisteen **Varaston inventointi**-toiminnolla. Myymäläkäyttäjät voivat tarvittaessa käynnistää ajoittamattoman varaston inventoinnin käyttämällä myyntipisteen **Varaston inventointi** -toimintoa. Toisin kuin ajoitetuissa varaston inventoinneissa ajoittamattomilla varaston inventoinneilla ei ole ennalta määritettyä nimikeluetteloa. Inventointityypistä riippumatta inventointi vahvistetaan ja lähetetään pääkonttoriin valmistumisen jälkeen. Inventointi on sitten tarkistettava pääkonttorissa ja kirjattava Commercen pääkonttorisovellukseen erillisenä vaiheena.

## <a name="inventory-lookup"></a>Varastohaku

Tuotteen nykyistä määrää useissa myymälöissä ja varastoissa voi tarkastella **Varastohaku**-sivulla. Nykyisen käytettävissä olevan määrän lisäksi näkyvissä on myös kunkin myymälän luvattavissa oleva määrä (ATP). Valitse ensin myymälä, jonka ATP-määritä haluat tarkastella, ja **Näytä myymälän käytettävyys**. Lisätietoja käytettävissä olevista määritysvaihtoehdoista on kohdassa [Vähittäismyyntikanavien varaston käytettävyyden laskeminen](./calculated-inventory-retail-channels.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]