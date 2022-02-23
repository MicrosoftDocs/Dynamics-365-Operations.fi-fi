---
title: Myymälän varastonhallinta
description: Tässä ohjeaiheessa käsitellään asiakirjatyyppejä, joiden avulla hallitaan varastoa.
author: rubencdelgado
manager: AnnBe
ms.date: 05/15/2020
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
ms.openlocfilehash: a3e6450c358d12dc62c2ffa20e7ff529be86bbe5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411985"
---
# <a name="store-inventory-management"></a>Myymälän varastonhallinta

[!include [banner](includes/banner.md)]

Kun varastoa käsitellään Microsoft Dynamics 365 Commercessa myyntipistesovelluksella, on tärkeää muistaa, että tiettyjä varastodimensioita ja varastonimiketyyppejä tuetaan myyntipisteessä vain rajoitetusti. Myyntipistesovellus ei tue kaikkia niitä nimikkeen määritysominaisuuksia, jotka ovat saatavana Dynamics 365 Supply Chain Managementin nimikkeen määritysasetuksissa.

Myyntipisteratkaisu ei tue tällä hetkellä seuraavia tuotedimensioita ja nimikemäärityksiä:

- Tuotedimensio- ja tuoterakennenimikkeiden määrittäminen (poikkeuksen niitä vähittäismyyntirakenteista, joissa käytetään joitakin tuoterakennekehyksen osia)
- Todellisen painon nimikkeet
- Version tuotedimension avulla ohjatut nimikkeet

Myyntipistesovellus ei tue tällä hetkellä myyntipisteessä seuraavia seurantadimensioita:

- Erän seurantadimensio
- Omistajadimensio

Myyntipisteratkaisu tukee rajoitetusti seuraavia dimensioita. On siis mahdollista, että myyntipiste vie joitakin näitä dimensioita varastotapahtumiin varaston tai kaupan asetusten määritysten perusteella. Myyntipiste ei kuitenkaan tue dimensioita täysimääräisesti siinä määrin kuin jos myyntitapahtuma vietäisiin manuaalisesti Commercen pääkonttoriin. 

- **Varaston sijainti** – Jos käyttäjät käyttävät myyntipisteen uutta [saapuvaa toimintoa](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ja [lähtevää toimintoa](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), he voivat valita varaston varastosijainnin, johon nimikkeitä vastaanotetaan tai josta lähtevät siirtotilaukset lähetetään. Jos käytössä on vanhentunut **Keräys ja vastaanotto** -toiminto, vastaanoton ja lähtevien siirtojen lähettämisen yhteydessä on käytettävissä rajoitettu sijainnin hallinnan tuki. Tämä tuki on käytettävissä vain, jos **Käytä varastonhallintaprosesseja** -vaihtoehto on otettu käyttöön sekä nimikkeen osalta että myymälän varastossa. Varastosijaintia ei voi tällä hetkellä käyttää **Varaston inventointi**- ja **Varastohaku**-toimintojen kanssa.
- **Rekisterikilpi** – Rekisterikilvet ovat käytössä vain, kun **Käytä varastonhallintaprosesseja** -vaihtoehto on otettu käyttöön nimikkeessä ja myymälän varastossa. Jos varasto vastaanotetaan myyntipistesovelluksessa **Saapuva toiminto**- tai **Keräys ja vastaanotto** -toimintoa käyttämällä myymälävarastoon, jossa varaston hallintaprosessi on otettu käyttöön, ja jos nimikkeen vastaanottamiselle valittu sijainti on sidottu sijaintiprofiiliin, joka edellyttää rekisterikilpiohjausta, myyntipistesovellus käyttää vastaanottavan rivin rekisterikilpeä järjestelmällisesti. Myyntipistekäyttäjät eivät voi muuttaa eivätkä hallita näitä rekisterikilven tietoja. Jos rekisterikilpien hallinta on pakollista, kyseisiä nimikkeitä kannattaa hallita myymälässä [varastointisovelluksella](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) tai tausta-asiakasohjelmalla.
- **Sarjanumero** – Myyntipistesovellus tukee rajoitetusti sellaisen yksittäisen sarjanumeron rekisteröintiä, joka luodaan myyntipistesovelluksessa tapahtumamyyntiriville ja joka sisältää sarjoitettuja nimikkeitä. Tätä sarjanumeroa ei ole tarkistettu varastoon jo rekisteröityjen sarjanumeroiden perusteella. Jos myyntitilaus luodaan puhelinkeskuskanavassa tai täytetään ERP-järjestelmän avulla ja yhteen myyntitilausriviin rekisteröidään useita sarjanumeroita tämän täyttämisprosessin aikana, kyseisiä sarjanumeroita ei voida käyttää tai tarkistaa, jos tilauksen palautukset käsitellään myyntipisteessä. Jos varaston vastaanottoon käytetään **saapuvien toimintoa**, käyttäjät voivat [rekisteröidä tai vahvistaa vastaanotetut sarjanumerot](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).
- **Varaston tila** – Jos nimikkeet käyttävät varastonhallintaprosessia ja edellyttävät varaston tilaa, tätä tilakenttää ei voi määrittää eikä muokata myyntipistesovelluksessa. Nimikkeiden varastoon vastaanottamisessa käytetään myymälän varastomäärityksessä määritettyä varaston oletustilaa.

> [!NOTE]
> Kaikkien organisaatioiden on testattava nimikemääritykset myyntipisteen kehitys- tai testiympäristöissä, ennen kuin kyseiset nimikemääritykset otetaan käyttöön tuotantoympäristöissä. Nimikkeet testataan suorittamalla niillä tavallisia itsepalvelutukun myyntitapahtumia ja luomalla (tarvittaessa) asiakastilauksia myyntipisteessä. Myös myyntipisteen täyttämis- ja varastoprosessit (kuten varaston vastaanotto- ja tilauksen täyttämistoiminnot) on testattava ennen uusien nimikemääritysten käyttöönottoa, sillä näin voidaan varmistaa, että myyntipistesovellus tukee niitä. Testauksen on sisällettävä täydelliset laskelmien kirjaamisprosessit testiympäristössä ja sen varmistaminen, että mitään ongelmia ei esiinny, kun kyseisille nimikkeille luodaan ja kirjataan tilauksia Commercen pääkonttorisovelluksessa.
>
> Jos nimikkeet määritetään tavalla, jota myyntipistesovellus ei tue eikä testausta tehdä, tilauksen luontiprosessissa saattaa esiintyviä tietovirheitä, joita ei ole helppo korjata tai joita vakiotuotetuki ei kata.

## <a name="purchase-orders"></a>Ostotilaukset

Ostotilaukset luodaan Commercen pääkonttorisovelluksessa. Jos myymälän varasto sisältyy ostotilauksen otsikkoon tai ostotilausriveille, rivit voidaan vastaanottaa myymälään käyttämällä myyntipisteen [saapuvaa toimintoa](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation). 

## <a name="transfer-orders"></a>Siirtotilaukset

Siirtotilaukset voidaan luoda Commercen pääkonttorisovelluksessa tai myyntipisteessä joko [saapuvien toiminnolla](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) tai [lähtevien toiminnolla](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation). Myyntipisteen **saapuvien toiminnolla** luodaan siirtotilauspyyntö, jolla pyydetään lähettämään varastoa myymälään toisesta varasto- tai myymäläsijainnista. Myyntipisteen **lähtevien toiminnolla** luodaan siirtotilauspyyntö, jolla pyydetään lähettämään varastoa myymälästä toisesta varasto- tai myymäläsijaintiin. Kun myymälän siirtotilaus on luotu, myymälä voi hallita siirtotilauksen varaston vastaanottoa myyntipisteen **saapuvien toiminnolla**. Jos myymälä lähettää varastoa toiseen sijaintiin, kyseisen myymälän lähtevien lähetysprosessia hallitaan myyntipisteen **lähtevien toiminnolla**.

## <a name="stock-counts"></a>Varaston inventoinnit

Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa. Ajoitetut varaston inventoinnit luodaan Commercen pääkonttorisovelluksessa luomalla myymälään varastoon linkitetty Inventointikirjauskansio-asiakirja. Tässä kirjauskansiossa määritetään inventoitavat nimikkeet. Myymälä voi sitten käyttää näitä valmiiksi määritettyjä inventointikirjauskansioita ja käyttää niitä myyntipisteen **Varaston inventointi**-toiminnolla. Myymäläkäyttäjät voivat tarvittaessa käynnistää ajoittamattoman varaston inventoinnin käyttämällä myyntipisteen **Varaston inventointi** -toimintoa. Toisin kuin ajoitetuissa varaston inventoinneissa ajoittamattomilla varaston inventoinneilla ei ole ennalta määritettyä nimikeluetteloa. Inventointityypistä riippumatta inventointi vahvistetaan ja lähetetään pääkonttoriin valmistumisen jälkeen. Inventointi on sitten tarkistettava pääkonttorissa ja kirjattava Commercen pääkonttorisovellukseen erillisenä vaiheena.

## <a name="inventory-lookup"></a>Varastohaku

Tuotteen nykyistä määrää useissa myymälöissä ja varastoissa voi tarkastella **Varastohaku**-sivulla. Nykyisen käytettävissä olevan määrän lisäksi näkyvissä on myös kunkin myymälän luvattavissa oleva määrä (ATP). Valitse ensin myymälä, jonka ATP-määritä haluat tarkastella, ja **Näytä myymälän käytettävyys**. Lisätietoja käytettävissä olevista määritysvaihtoehdoista on kohdassa [Vähittäismyyntikanavien varaston käytettävyyden laskeminen](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).
