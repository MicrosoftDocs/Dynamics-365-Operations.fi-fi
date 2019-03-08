---
title: Myymälän varastonhallinta
description: Tässä ohjeaiheessa käsitellään asiakirjatyyppejä, joiden avulla hallitaan varastoa.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
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
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "339231"
---
# <a name="store-inventory-management"></a>Myymälän varastonhallinta

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään asiakirjatyyppejä, joiden avulla hallitaan varastoa.

Organisaation varastoa voi hallita seuraavien asiakirjatyyppien avulla.

Kun varastoa käsitellään Dynamics 365 for Retailissa ja käytössä on myyntipistesovellus, on tärkeää muistaa, että myyntipiste tukee vain rajoitetusti varastodimensioita ja tiettyjä varastonimiketyyppejä.  

Myyntipisteratkaisu ei tue seuraavia nimikemäärityksiä:
- Tuoterakennenimikkeet (lukuun ottamatta myyntirakenteita, joissa käytetään joitakin tuoterakennekehikon osia)
- Todellisen painon nimikkeet
- Eräohjatut nimikkeet

Myyntipistesovellus ei tue tällä hetkellä myyntipisteessä seuraavia seurantadimensioita:
- Erän seurantadimensio
- Omistajadimensio

Myyntipisteratkaisu tukee rajoitetusti seuraavia dimensioita. Rajoitettu tuki ilmaisee, että myyntipiste voi palauttaa jotkin näistä dimensioista automaattisesti varastotapahtumiksi varaston tai kaupan asetusten määritysten perusteella. Myyntipiste ei tue dimensioita täysin sillä tavoin kuin niitä tuetaan, jos myyntitapahtuma viedään manuaalisesti ERP:hen. 

- Paikka
- Rekisterikilpi (käytössä vain, kun **Käytä varastonhallintaprosesseja** on otettu käyttöön nimikkeessä ja kaupan varastossa)
- Sarjanumero
- Varaston tila

> [!NOTE]
> Kaikkien organisaatioiden on testattava nimikemääritykset myyntipisteen kehitys- tai testiympäristössä, ennen kuin ne otetaan käyttöön tuotannossa. Testaa nimikkeet suorittamalla tavallinen itsepalvelutukun myyntitapahtuma ja luomalla (tarvittaessa) nimikkeille asiakastilauksia myyntipisteessä. Testauksen on sisällettävä täydelliset laskelmien kirjaamisprosessit testiympäristössä ja sen varmistaminen, että mitään ongelmia ei esiinny.
> Jos nimikkeet määritetään tavalla, jota myyntipistesovellus ei tue ja ilman asianmukaista testausta, voi aiheuttaa laskelmien kirjaamisprosessin epäonnistumisen tuotantoympäristössä ilman, että ongelmat voitaisiin korjata kätevästi. Kumppanin tai asiakkaan sovellukseen tekemiä mukautuksia on mahdollista harkita, jotta nämä kirjausprosessit onnistuisivat. Jos mukautuksia ei tarvita, organisaation on varmistettava, että tuotteiden tuotemääritykset on tehty siten, että tavanomaista myyntipistesovellusta, tilausten luontia ja laskelmien kirjausprosessia tuetaan.

## <a name="purchase-orders"></a>Ostotilaukset

Ostotilaukset luodaan pääkonttorilla. Jos vähittäismyynnin varasto sisältyy ostotilauksen otsikkoon, tilaus voidaan vastaanottaa myymälään Microsoft Dynamics 365 for Retailin Modern POS- tai Cloud POS -sovelluksen avulla. Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten. Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin. Pääkonttorissa myymälään vastaanotetut määrät näytetään Dynamics 365 for Retailissa ostotilauksen **Ota vastaan nyt** -kentässä.

## <a name="transfer-orders"></a>Siirtotilaukset

Siirtotilaus voi määrittää, että nimikkeet lähetetään tietystä myymälästä. Tässä tapauksessa siirtotilaus näkyy myymälässä poimintapyyntönä Modern POS- tai Cloud POS -sovelluksessa. Kun pyydetyt määrät on kerätty, ne vahvistetaan ja lähetetään pääkonttoriin. Pääkonttorissa myymälässä kerätyt määrät näytetään Dynamics 365 for Retailissa siirtotilauksen **Lähetä nyt** -kentässä. Siirtotilaus voi määrittää, että nimikkeet lähetetään tiettyyn myymälään. Tässä tapauksessa siirtotilaus näkyy myymälässä vastaanottopyyntönä Modern POS- tai Cloud POS -sovelluksessa. Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten. Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin. Pääkonttorissa myymälään vastaanotetut määrät näytetään Dynamics 365 for Retailissa siirtotilauksen **Ota vastaan nyt** -kentässä.

## <a name="stock-counts"></a>Varaston inventoinnit

Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa. Ajastetut varaston inventoinnit määritetään pääkonttorilla. Ne määrittävät nimikkeet, joista on tehtävä inventointi. Pääkonttori luo inventointiasiakirjan, joka voidaan vastaanottaa myymälässä, jossa todelliset käytettävissä olevat määrät syötetään Modern POS- tai Cloud POS -sovelluksessa. Ajoittamattomat varaston inventoinnit aloitetaan myymälässä ja todelliset käytettävissä olevat varastomäärät päivitetään Modern POS- tai Cloud POS -sovelluksessa. Ajoittamattomilla varaston inventoinneilla ei ole ennalta määritettyä nimikeluetteloa kuten ajoitetun varaston inventoinneilla. Kun jompikumpi varaston inventointi on suoritettu, se vahvistetaan ja lähetetään pääkonttorille. Pääkonttorissa inventointi tarkistetaan ja kirjataan.

## <a name="inventory-lookup"></a>Varastohaku

Nykyistä tuotteen määrää useissa myymälöissä ja varastoissa voi tarkastella varaston haku-sivulla. Nykyisen käytettävissä olevan määrän lisäksi luvattavissa oleva määrä (ATP) nähdään yksittäisistä myymälöistä. Voit tehdä tämän valitsemalla ensin myymälän, jonka ATP:tä haluat tarkastella, ja sitten **Näytä myymälän käytettävissä oleva määrä**.
