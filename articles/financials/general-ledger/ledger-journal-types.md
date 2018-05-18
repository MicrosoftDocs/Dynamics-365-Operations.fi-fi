---
title: Kirjanpidon kirjauskansiotyypit
description: "Tässä artikkelissa kuvataan kirjauskansiotyypit, joita voit määrittää talouskirjauskansioille. Määritä koko Microsoft Dynamics 365 for Finance and Operationsissa käytettävät kirjauskansiot **Kirjauskansioiden nimet** -sivulla."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9f8fc40f199b83a9e0cb36ce905163c3ed547057
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="ledger-journal-types"></a>Kirjanpidon kirjauskansiotyypit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan kirjauskansiotyypit, joita voit määrittää talouskirjauskansioille. Määritä koko Microsoft Dynamics 365 for Finance and Operationsissa käytettävät kirjauskansiot **Kirjauskansioiden nimet** -sivulla.

| Kirjauskansion tyyppi                      | Tarkoitus                       | Syötä tapahtumakoodi tälle sivulle                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Varaus                        | Luo kohdistustapahtumat kohdistuskirjauskansiossa. Ennen kohdistuskirjauskansion luomista sinun on luotava kohdistussääntö **Kirjanpidon kohdistussääntö** -sivulla.      | Käsittele kohdistuspyyntö             |
| Hyväksyminen                          | Kirjaa hyväksytyt toimittajan laskut asianmukaisille kirjanpitotileille.  | Hyväksyttyjen laskujen kirjauskansio                                       |
| Pankkisekin palautus               | Kirjatun sekin peruuttaminen. Jos haluat käyttää tätä kirjauskansiotyyppiä, valitse **Käytä tarkistusprosessia maksujen palautuksissa** -vaihtoehto **Maksuliikennetiedot**-sivulla.   | Sekin peruutukset, maksujen mitätöinnit                   |
| Pankkitalletuskuitin peruutus    | Peruuta talletuskuitti. Jos haluat käyttää tätä kirjauskansiotyyppiä, valitse **Käytä tarkistusprosessia talletuskuittimaksujen peruutuksissa** -vaihtoehto **Maksuliikennetiedot**-sivulla.   | Tallennuskuittien maksujen peruutukset            |
| Budjetti                            | Käsittele budjettimäärärahat. Jos haluat käyttää tätä kirjauskansiotyyppiä, valitse **Ota käyttöön budjettivaraus** -vaihtoehto **Kirjanpitoparametrit** -sivulla. Budjetin kirjauskansiomerkinnät sisältävät tietoja, jotka perustuvat sivulla **Kirjausmääritykset** määriteltyihin kirjanpitotileihin.                                                        |                                                                |
| Asiakkaan hyväksymä vekseli  | Luo asiakkaan hyväksyntätapahtumia vekselille.             | Aseta vekselikirjauskansio, Vekselin uudelleenasettamisen kirjauskansio |
| Asiakkaan pankkisiirtomääräys          | Luo vekselin maksusuoritustiedosto, joka voidaan lähettää organisaatiosi pankkiin. Jos haluat käyttää tätä kirjauskansiotyyppiä, tyhjennä **Automaattinen tilitys** -vaihtoehto **Ostoreskontra** **parametrit**-sivulla.            | Maksusuoritus                                                     |
| Asiakkaan asettama vekseli    | Luo asiakkaan asettamien vekselien tapahtumia. Kun haluat käyttää tätä kirjauskansiotyyppiä, poista valinta **Luo ja kirjaa asetettu kirjauskansio automaattisesti laskujen kirjauksen yhteydessä** sivulla **Maksutapa - Asiakkaat**.   | Aseta vekselikirjauskansio                                  |
| Asiakkaan maksu                  | Luo asiakkaan maksutapahtumia.                             | Maksukirjauskansio             |
| Asiakkaan protestoitu vekseli | Luo asiakkaan protestoitujen vekselien tapahtumia.                    | Protestoi vekselikirjauskansio                               |
| Asiakkaan tarkistettu vekseli  | Luo asiakkaan tarkistettujen vekselien tapahtumia.                     | Tarkista vekselikirjauskansio                                |
| Asiakkaan selvittämä vekseli  | Luo asiakkaan selvittämien vekselien tapahtumia.                       | Selvitä vekselikirjauskansio                                |
| Päivittäin                             | Luo päivittäiset tapahtumat yleisessä kirjauskansiossa.                          | Kirjauskansio                                                |
| Eliminointi                       | Luo eliminointitapahtumat eliminointien kirjauskansiossa. Kun halut käyttää tätä kirjauskansiotyyppiä, valitse **Käytetään taloushallinnon eliminointiprosessissa** ja **Käytä kirjanpidon konsolidointiprosessissa** -valinnat **Oikeushenkilöt**-sivulla. Sinun on luotava kirjanpidon eliminointisääntö **Kirjanpidon eliminointisääntö** -sivulla ennen tämän kirjauskansiotyypin käyttämistä. | Eliminointi                                                    |
| Käyttöomaisuusbudjetti                | Luo käyttöomaisuuden budjettirekisterimerkinnät.                                                                                                                                                                                                                                                                                                                 | Käyttöomaisuusbudjetti                                             |
| Laskurekisteri                  | Rekisteröi toimittajalaskun perustiedot.                                                                                                                                                                                                                                                                                                           | Laskurekisteri                                               |
| Palkanlaskennan suoritus              | Suorita palkanlaskennan maksutositteisiin perustuvia maksuja. Et voi kirjoittaa manuaalisesti tapahtumia tässä kirjauskansiossa. Sinun on luotava maksulaskelmat ja lähetettävä nämä laskelmat maksettavaksi.                                                                                                                                                              |                                                                |
| Kausittainen                          | Luo kausittaisia tapahtumia kausikirjauskansiolle.                                                                                                                                                                                                                                                                                                      | Kausikirjauskansiot                                              |
| Kirjaa käyttöomaisuus                 | Kirjaa Käyttöomaisuuserätapahtumia.                                                                                                                                                                                                                                                                                                                              | Käyttöomaisuudet                                                   |
| Projekti - Kulut                | Luo projektin kulutapahtumat.                                                                                                                                                                                                                                                                                                                        | Kulut                                                        |
| Tilastotapahtumat            | Luo tilastollisia tapahtumia.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Toimittajan pankkisiirtomääräys            | Luo velkakirjan maksusuoritustiedosto, joka voidaan lähettää organisaatiosi pankkiin.                                                                                                                                                                                                                                                                      | Maksusuoritusten kirjauskansio                                             |
| Toimittajan suoritus               | Luo toimittajan suoritustapahtumat.                                                                                                                                                                                                                                                                                                                    | Maksukirjauskansio                                                |
| Toimittajan asettama velkakirja       | Aseta toimittajan velkakirjat maksutavaksi Kun haluat käyttää tätä kirjauskansiotyyppiä, poista valinta **Luo ja kirjaa asetettu kirjauskansio automaattisesti laskujen kirjauksen yhteydessä** sivulla **Maksutapa - Toimittajat**.                                                                                                                                          | Aseta velkakirjakirjauskansio                                   |
| Toimittajalaskupooli ilman kirjaamista | Luo toimittajan laskutapahtumat, joita ei vielä ole kirjattu väliaikaiselle saapumistilille.                                                                                                                                                                                                                                                             | Toimittajan laskupooli, ei sisällä kirjaustietoja                  |
| Toimittajalaskupooli               | Luo toimittajalaskupoolitapahtumat.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Toimittajan laskun kirjaus          | Kirjaa kirjauskansion toimittajalaskut.                                                                                                                                                                                                                                                                                                                 | Laskukirjauskansio                                                |
| Toimittajan tarkistama velkakirja     | Aseta uudelleen velkakirja, jonka organisaatiosi pankki on aiemmin lunastanut.                                                                                                                                                                                                                                                                      | Tarkista velkakirjakirjauskansio                                 |
| Toimittajan selvittämä velkakirja     | Luo toimittajan selvittämien velkakirjojen tapahtumat.                                                                                                                                                                                                                                                                                                          | Selvitä velkakirjakirjauskansio                                 |






