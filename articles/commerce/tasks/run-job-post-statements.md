---
title: Määritä ja suorita työ laskelmien kirjaamiseksi
description: Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.
author: josaw1
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52baa707c36f3468263782dc8ec735e44af88e38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804230"
---
# <a name="configure-and-run-job-to-post-statements"></a>Määritä ja suorita työ laskelmien kirjaamiseksi

[!include [banner](../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia. Menettely käyttää esittelytietojen USRT-yritystä.

1. Valitse Kaikki työtilat > .. > Myymälän myyntitiedot.
2. Napsauta Laskelmien kirjaaminen eräajona.
    * Valitse organisaatiohierarkia ja sitten organisaatiosolmujen puu. Valitse yksittäinen myymälä tai solmu. Valitse solmu, jos haluat luoda myymäläryhmän erätyön.  
    * Lisää valinta nuolen avulla.  
3. Valitse Suorita taustalla -välilehti. ![Suorita taustalla](../dev-itpro/media/runbackground.png "Suorita taustalla") 
4. Valitse Eräkäsittely-valintaruutu tai poista sen valinta.
![Eräkäsittely](../dev-itpro/media/batchprocessing.png "Eräkäsittely & toistuvuus") 
5. Valitse Toistuminen.
6. Syötä päivämäärä Aloituspäivä-kenttään.
7. Syötä Aloitusaika-kenttään aika.
    * Määritä, päätetäänkö toisto tietyn suoritusmäärän jälkeen, tiettynä päivänä vai ei koskaan. Määritä sitten työn toistovälit eri vaihtoehtojen avulla.  
8. Valitse OK.
9. Valitse OK.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]