---
title: Erätyön luominen
description: Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4360cd7068658a170f5b44c2ce7c71c39c44fa8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679885"
---
# <a name="create-a-batch-job"></a>Erätyön luominen

[!include [banner](../../includes/banner.md)]

Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten. Erätyöt suoritetaan sen käyttäjän käyttöoikeustiedoilla, joka on luonut työn. Luo erätyö seuraavien ohjeiden mukaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-the-batch-job"></a>Luo erätyö
1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Kyselyt > Erätyöt**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Työnkuvaus** -kenttään.
4. Määritä päivämäärä ja kellonaika **Ajoitettu alkamispäivämäärä/-kellonaika** -kentässä.
5. Valitse **Tallenna**.

## <a name="create-a-recurrence"></a>Luo toistuvuus
1. Valitse toimintoruudussa **Erätyö**.
2. Valitse **Toistuminen**. Aseta toistumisalue ja -kuvio näiden asetusten avulla.  
3. Valitse **OK**.

## <a name="add-alerts"></a>Lisää hälytyksiä
1. Valitse toimintoruudussa **Erätyö**.
2. Valitse **Hälytykset**. Ilmaise, haluatko lähettää hälytysviestin, kun erätyö on päättynyt tai peruutettu, tai jos siinä on kohdattu virhe. Määritä sitten, haluatko ilmoitukset ponnahdussanomina.   
3. Valitse **OK**.

## <a name="adjust-batch-job-status"></a>Erätyön tilan säätäminen
1. Valitse **Järjestelmän hallinta > Kyselyt > Erätyöt**.
2. Valitse soveltuva erätyö.
3. Valitse toimintoruudussa **Erätyö > Toiminnot > Muuta tila**.
4. Valitse sopiva tila:
    - **Pidätä**: Määritä erätyö **pidätettynä**, jolloin sitä ei anneta erätyön ajastukseen. Vastaa *pysäyttämistä*.
    - **Odottaa**: Määritä erätyö **odottavaksi**, jolloin se odottaa erätyön ajastuksen tekemään poimimista. Vastaa *siirtymistä*.
5. Valitse **OK**.
