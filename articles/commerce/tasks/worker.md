---
title: Työntekijän konfiguroiminen
description: Tässä menettelyssä kerrotaan, miten määrität työntekijästä myyntiedustajan, joka on oikeutettu myyntipisteen myyntiprovisioihin.
author: jblucher
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 43e65de1fda223c2d0503848e7e57936898c1b73
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804062"
---
# <a name="configure-a-worker"></a>Työntekijän konfiguroiminen

[!include [banner](../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten määrität työntekijästä myyntiedustajan, joka on oikeutettu myyntipisteen myyntiprovisioihin. Menettely käyttää esittelytietojen USRT-yritystä.


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
1. Siirry kohtaan Retail ja Commerce > Työntekijät > Työntekijät.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Comemrce-välilehti.
    * Työntekijä voidaan määrittää myynnin oletusryhmään. Myynnin oletusryhmä automaattisesti lisätään automaattisesti myyntipisteen myyntiriveille, jos asetus on käytössä myymälän toimintoprofiilissa.  
5. Valitse Muokkaa.
6. Syötä tai valitse arvo Oletusryhmä-kentässä.
7. Valitse Tallenna.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]