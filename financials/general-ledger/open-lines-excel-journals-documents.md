---
title: Kirjauskansiorivit- ja Excel-asiakirjojen julkaiseminen
description: "Tässä ohjeaiheessa kerrotaan, kuinka voit kirjoittaa ja julkaista Microsoft Excelin yleisten kirjauskansioiden rivit. Se sisältää tietoja eri malleja, joita voit käyttää tapahtumia, jotka olet kirjoittanut tyypin mukaan."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Kirjauskansiorivit- ja Excel-asiakirjojen julkaiseminen

Tässä ohjeaiheessa kerrotaan, kuinka voit kirjoittaa ja julkaista Microsoft Excelin yleisten kirjauskansioiden rivit. Se sisältää tietoja eri malleja, joita voit käyttää tapahtumia, jotka olet kirjoittanut tyypin mukaan.

Käyttäjät voivat kirjoittaa ja julkaista Microsoft Excel taloushallinnon kirjauskansioiden rivit. Sen jälkeen, kun käyttäjä luo kirjauskansio, **avata Excelissä rivit** -painike näyttää käytettävissä olevat mallit. Mallit on suunniteltu tukemaan tiettyjä skenaarioita, tuetaan kirjauskansion tilityyppi ei kuitenkaan ole kaikki yhdistelmät. Seuraavassa taulukossa esitetään käytettävissä olevat mallit ja tilityyppeihin, joita ne palvelevat.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Tuetut tyypit**                                                                                             | **Mallin käyttäminen**                                                          |
| Kirjanpidon kirjauskansiorivit     | Tili: Kirjanpito, asiakas, toimittaja, pankin vastatili: Kirjanpito, asiakkaan, toimittajan, pankkitilin konsernin tuetaan.       | Kirjauskansio                                                                         |
| Laskurekisteri         | Tili: Toimittajan vastatili: yritysten Kirjanpito ei ole tuettu.                                                    | AP Laskurekisteri                                                                     |
| Laskukirjauskansio          | Tilit: Toimittajan vastatili: tuetaan yritysten kirjanpitoon.                                                      | Ostoreskontran laskukirjauskansio                                                                      |
| Toimittajan lasku           |                                                                                                                         | Toimittajan lasku                                                                          |
| Myyntilaskukirjauskansio | Asiakas: Asiakkaan vastatili: tuetaan yritysten kirjanpitoon.                                                     | Kirjauskansio                                                                         |
| Vapaatekstilasku        |                                                                                                                         | - **Vapaatekstilaskun** -sivulla **avaa Excelin** (Microsoft Office-kuvake). |
| Käyttöomaisuuden kirjauskansio     | Käyttöomaisuuden Kirjanpito, pankki, asiakas tai toimittaja. Yritysten ei ole tuettu.                                               | Käyttöomaisuuserän kirjauskansio                                                                     |
| Toimittajan maksukirjauskansio   | Tili: Toimittajan vastatili: Kirjanpito, pankki-konsernin tuetaan.                                                 | Toimittajan maksukirjauskansio                                                                  |
| Asiakkaan maksukirjauskansio | Asiakas: Asiakkaan vastatili: Kirjanpito, pankki-konsernin tuetaan.                                               | Asiakkaan maksukirjauskansio                                                                |
| Projektin kulukirjauskansio  | Tili: Projektin kirjanpidon, asiakkaan, toimittajan vastatili: projektin, pääkirjanpidon, asiakkaan, toimittajan konsernin sisäinen tuetaan. | Yleisen päiväkirjan Kulu (kohdassa projektinhallinta ja laskentatoimi)                       |

Kun rivit julkaistaan, ne vahvistetaan varmistaaksesi, että ne noudattavat sääntöjä, jotka on määritetty taloushallinnon kirjauskansioihin. Rivit julkaistaan, kun käyttäjät voivat muokata tai tositteet kirjataan Microsoft Dynamics-365 operaatioille. 

Jos haluat lisätä mallin taloushallinnon dimensiot, lisää muutoksia tarvitaan. Lisätietoja on ohjeaiheessa [dimensioitten lisääminen Microsoft Excel-malli](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Mitat lisätään kohteeseen, kun ovat käytettävissä Excelin suunnittelussa ja lisätään malliin.




