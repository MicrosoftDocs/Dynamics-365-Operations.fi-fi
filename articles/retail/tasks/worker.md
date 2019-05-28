---
title: Työntekijän konfiguroiminen
description: Tässä menettelyssä kerrotaan, miten määrität vähittäismyynnin työntekijästä myyntiedustajan, joka on oikeutettu myyntipisteen myyntiprovisioihin.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 797640b487884fc487582addea274007e4ba7a7d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563617"
---
# <a name="configure-a-worker"></a>Työntekijän konfiguroiminen

[!include[task guide banner](../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten määrität vähittäismyynnin työntekijästä myyntiedustajan, joka on oikeutettu myyntipisteen myyntiprovisioihin. Menettely käyttää esittelytietojen USRT-yritystä.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Luo työntekijälle myyntiprovisioryhmä
1. Valitse Myynti ja markkinointi > Provisiot > Myyntiryhmät.
    * Työntekijöitä voi liittää yhteen tai useampaan myyntiryhmään. Myyntipisteessä voit valita minkä tahansa myyntiryhmän, joka sisältää työntekijöitä liikkeen osoitekirjasta.  
2. Valitse Uusi.
3. Kirjoita Ryhmä-kenttään arvo.
4. Kirjoita arvo Nimi-kenttään.
5. Valitse Tallenna.
6. Valitse toimintoruudussa Yleiset.
7. Valitse Myyjä.
    * Myyntiryhmä voi sisältää useamman kuin yhden työntekijän. Provisiot voi jakaa työntekijöille sen mukaan, miten provisio-osuus on määritetty.  
8. Syötä tai valitse arvo Nimi-kenttään.
9. Kirjoita Provisio-osuus -kenttään numero.
10. Valitse Tallenna.
11. Sulje sivu.
12. Sulje sivu.

## <a name="assign-the-workers-default-sales-group"></a>Määritä työntekijät oletusmyyntiryhmään
1. Siirry kohtaan Vähittäismyynti ja kauppa > Työntekijät > Työntekijät.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Vähittäismyynti-välilehti.
    * Työntekijä voidaan määrittää myynnin oletusryhmään. Myynnin oletusryhmä automaattisesti lisätään automaattisesti myyntipisteen myyntiriveille, jos asetus on käytössä myymälän toimintoprofiilissa.  
5. Valitse Muokkaa.
6. Syötä tai valitse arvo Oletusryhmä-kentässä.
7. Valitse Tallenna.

