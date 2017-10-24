--- 
title: "Asiakirjojen luominen päivitetyillä sovellustiedoilla sähköistä raportointia (ER) varten"
description: "Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 1 – konfiguraatioiden tuominen) -menettely on suoritettu."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c724ce3c39ed7097a5a842b44a095628dcdfa131
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Asiakirjojen luominen päivitetyillä sovellustiedoilla sähköistä raportointia (ER) varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 1: konfiguraatioiden tuominen) -menettely on suoritettu.



Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista varten. Tässä menettelyssä suoritetaan tuotu ER-muotokonfiguraatio, joka on luotu malliyritykselle Litware Inc. sähköisten asiakirjojen luomista varten.



Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla. 



Ennen kuin aloitat, muuta DEMF-yrityksen maakonteksti DEU (Saksa) -arvosta BEL (Belgia) -arvoksi. Valitse Organisaation hallinto > Organisaatiot > Yritykset, kun haluat päivittää yrityksen DEMF ensisijaisen osoitteen maakoodin. Käynnistä sovellus uudelleen.


## <a name="run-imported-er-format"></a>Tuodun ER-muodon suorittaminen
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa Intrastat (model).
3. Valitse puussa Intrastat (model)\Intrastat (format).
4. Valitse Suorita.
    * Suorita ER-muotokonfiguraation luonnosversio, kun haluat luoda Intrastat-raportin.  
5. Kirjoita Syötä tiedostonimi -kenttään intrastat.xml.
    * Anna tiedoston nimi.  
6. Valitse OK.
    * Tarkista luotu XML-tiedosto.  
7. Sulje sivu.
8. Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.
    * Avaa tämä lomake, kun haluat tarkastella luodun sähköisen asiakirjan Intrastat-tapahtumia.  
9. Valitse Intrastat-arkisto.
    * Koska suoritettu ER-muoto ei sisällä sovellustietojen päivityksen asetuksia, valmiin Intrastat-raportin tietoja ei ole arkistoitu.  
10. Sulje sivu.
11. Sulje sivu.


