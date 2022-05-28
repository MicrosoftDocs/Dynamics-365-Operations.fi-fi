---
title: Kirjauskansiorivien ja asiakirjojen julkaiseminen Excelistä
description: Tässä ohjeaiheessa kerrotaan, kuinka voit syöttää ja julkaista yleisten kirjauskansioiden rivejä Microsoft Excelistä. Se sisältää tietoja eri malleista, joita voit käyttää riippuen syöttämistäsi tapahtumista.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af478f9dba8dc17791e15017be2720c2aa21a2f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727030"
---
# <a name="publish-journal-lines-and-documents-from-excel"></a>Kirjauskansiorivien ja asiakirjojen julkaiseminen Excelistä

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit syöttää ja julkaista yleisten kirjauskansioiden rivejä Microsoft Excelistä. Se sisältää tietoja eri malleista, joita voit käyttää riippuen syöttämistäsi tapahtumista.

Käyttäjät voivat syöttää ja julkaista taloushallinnon kirjauskansioiden rivejä Microsoft Excelistä. Sen jälkeen, kun käyttäjä on luonut kirjauskansion, **Avaa rivit Excelissä** -painike näyttää käytettävissä olevat mallit. Mallit on suunniteltu tukemaan tiettyjä skenaarioita, mutta kirjauskansio ei tue kaikkia tilityyppien yhdistelmiä. Seuraavassa taulukossa esitetään käytettävissä olevat mallit ja niiden tukemat tilityypit.

| Sapluuna             | Tuetut tilityypit | Mallin käyttäminen                                                          |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Kirjanpidon kirjauskansiorivit     | Tuetaan seuraavia – tili: Kirjanpito, Asiakas, toimittaja, pankki – vastatili: Kirjanpito, asiakas, toimittaja, konsernin pankkitili.       | Kirjauskansio                                                                         |
| Laskurekisteri         | Ei tueta – tili: toimittaja – vastatili: konsernin kirjanpito.                                                    | Ostoreskontran laskurekisteri                                                                     |
| Laskukirjauskansio          | Tuetaan – tili: toimittaja – vastatili: konsernin kirjanpito.                                                      | Ostoreskontran laskukirjauskansio                                                                      |
| Toimittajan lasku           |                                                                                                                         | Toimittajan lasku                                                                          |
| Myyntilaskukirjauskansio | Tuetaan – tili: asiakas – vastatili: konsernin kirjanpito.                                                     | Kirjauskansio                                                                         |
| Vapaatekstilasku        |                                                                                                                         | Valitse **Vapaatekstilasku**-sivulla **Avaa Excelissä** (Microsoft Office -kuvake). |
| Käyttöomaisuuden kirjauskansio     | Varat kirjanpitoon, pankkiin, asiakkaalle tai toimittajalle. Konsernitapahtumia ei tueta.                                               | Käyttöomaisuuserän kirjauskansio                                                                     |
| Toimittajan maksukirjauskansio   | Tuetaan – tili: toimittaja – vastatili: kirjanpito, konsernin pankkitili.                                                 | Toimittajan maksukirjauskansio                                                                  |
| Asiakkaan maksukirjauskansio | Tuetaan – tili: asiakas – vastatili: kirjanpito, konsernin pankkitili.                                               | Asiakkaan maksukirjauskansio                                                                |
| Projektin kulukirjauskansio  | Tuetaan seuraavia – tili: projekti, Kirjanpito, Asiakas, toimittaja, pankki – vastatili: projekti, Kirjanpito, asiakas, toimittajakonserni. | Yleisen päiväkirjan kulu (kohdassa Projektinhallinta ja kirjanpito)                       |

Kun rivit julkaistaan, ne vahvistetaan, jotta varmistetaan, että ne noudattavat sääntöjä, jotka on määritetty taloushallinnon kirjauskansioihin. Kun rivit on julkaistu, käyttäjät voivat muokata tai kirjata tositteita Dynamics 365 Financesta. 

Jos haluat lisätä malliin taloushallinnon dimensiot, lisää muutoksia tarvitaan. Lisätietoja on ohjeaiheessa [Dimensioitten lisääminen Microsoft Excel -malliin](../../fin-ops-core/dev-itpro/financial/add-dimensions-excel-templates.md). Kun dimensiot on lisätty yksikköön, ne ovat käytettävissä Excelin suunnittelussa ja voidaan lisätä malliin.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
