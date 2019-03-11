---
title: Luo sovellustietoja sisältäviä asiakirjoja
description: Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 4 – muodon muokkaaminen) -menettely on suoritettu.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90c6ebc456d3e137e43022fad7d59ce3ca2cdcab
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "363887"
---
# <a name="generate-documents-that-have-application-data"></a>Luo sovellustietoja sisältäviä asiakirjoja

[!include [task guide banner](../../includes/task-guide-banner.md)]

Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 4: muodon muokkaaminen) -menettely on suoritettu.



Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista ja sovellustietojen päivitystä varten. Tässä menettelyssä suoritetaan ER-muotokonfiguraatio Intrastat-raportin luontia ja sovellustietojen päivitystä varten, jotta raportointiprosessin tiedot voidaan arkistoida.



Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla. Ennen kuin aloitat, varmista, että DEMF-yrityksen maakonteksti on BEL (Belgia).


## <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit
1. Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit.
2. Valitse Numerojärjestykset-välilehti.
    * Intrastat-raportointiprosessin tietojen arkistointia varten on tunnistettava kunkin luodun arkiston tietueet. Sitä varten on määritettävä myös erityinen numerosarja.  
3. Valitse Intrastat-arkiston tunnus -viite.
4. Kirjoita arvo Numerosarjan koodi -kenttään.
    * Anna tai valitse Numerosarjan koodi -kenttään Fore_2-arvo.  
5. Ratkaise muutokset numerosarjan koodissa.
6. Valitse Tallenna.
7. Sulje sivu.

## <a name="run-modified-er-format"></a>Muokatun ER-muodon suorittaminen
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa Intrastat (model).
3. Valitse puussa Intrastat (model)\Intrastat (format).
4. Valitse Suorita.
5. Kirjoita Syötä tiedostonimi -kenttään intrastat2.xml.
    * intrastat2.xml  
6. Valitse OK.

## <a name="review-er-format-executions-results"></a>ER-muodon suorittamisen tulosten tarkasteleminen
    * Tarkista luotu XML-tiedosto.  
1. Sulje sivu.
2. Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.
    * Avaa tämä sähköiseen asiakirjaan sisällytetyt Intrastat-tapahtumat sisältävä lomake.  
3. Valitse Intrastat-arkisto.
    * Koska suoritettu ER-muoto sisältää nyt sovellustietojen päivityksen asetukset, valmiin Intrastat-raportoinnin tiedot on arkistoitu. Tämä lomake sisältää luodun arkiston otsikkotietueen.  
4. Valitse Erittely.
    * Tämä lomake sisältää luodun arkiston tiedot.  
5. Sulje sivu.
6. Sulje sivu.
7. Sulje sivu.

