--- 
title: "Erätyön luominen"
description: "Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-batch-job"></a>Erätyön luominen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten. Erätyöt suoritetaan sen käyttäjän käyttöoikeustiedoilla, joka on luonut työn. Luo erätyö seuraavien ohjeiden mukaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-the-batch-job"></a>Luo erätyö
1. Valitse Järjestelmänhallinta > Kyselyt > Erätyöt.
2. Valitse Uusi.
3. Kirjoita arvo Työnkuvaus -kenttään.
4. Määritä päivämäärä ja kellonaika kentässä Ajoitettu alkamispäivämäärä/-kellonaika.
5. Valitse Tallenna.

## <a name="create-a-recurrence"></a>Luo toistuvuus
1. Valitse toimintoruudussa Erätyö.
2. Valitse Toistuminen.
    * Aseta toistumisalue ja -kuvio näiden asetusten avulla.  
3. Valitse OK.

## <a name="add-alerts"></a>Lisää hälytyksiä
1. Valitse toimintoruudussa Erätyö.
2. Valitse Hälytykset.
    * Ilmaise, haluatko lähettää hälytysviestin, kun erätyö on päättynyt tai peruutettu, tai jos siinä on kohdattu virhe. Määritä sitten, haluatko ilmoitukset ponnahdussanomina.   
3. Valitse OK.


