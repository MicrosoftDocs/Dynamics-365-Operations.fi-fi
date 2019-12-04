---
title: Suunnittele konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja
description: Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 1 – konfiguraatioiden tuominen) -menettely on suoritettu.
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
ms.openlocfilehash: 9aec1da7fe168b05af10470221ac745ec1c01f6b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182321"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Suunnittele konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
