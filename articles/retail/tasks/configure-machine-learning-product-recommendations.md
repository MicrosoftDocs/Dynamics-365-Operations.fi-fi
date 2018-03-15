--- 
title: "Määritä automaattiset tuotesuositukset"
description: "Tämä menettely päivittää yksikkösäilän tiedot, joita käyttää tuotesuosituksista vastaava automaattianalyysijärjestelmää, ja ottaa sitten käyttöön tuotesuositukset myyntipisteiden asiakasohjelmissa."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a>Määritä automaattiset tuotesuositukset

[!include[task guide banner](../includes/task-guide-banner.md)]

Tämä menettely päivittää yksikkösäilän tiedot, joita käyttää tuotesuosituksista vastaava automaattianalyysijärjestelmää, ja ottaa sitten käyttöön tuotesuositukset myyntipisteiden asiakasohjelmissa. Menettely käyttää esittelytietojen USRT-yritystä.

1. Valitse Järjestelmän hallinta > Asetukset > Yksikkösäilö.
2. Etsi tietue "RetailSales" luettelosta ja valitse se.
3. Valitse Päivitä.
4. Valitse OK.
5. Sulje sivu.
6. Siirry kohtaan Vähittäismyynti ja kauppa > Pääkonttorin asetukset > Parametrit > Vähittäismyyntiparametrit.
7. Valitse Automaattianalyysi-välilehti.
8. Valitse Ota tuotesuositukset käyttöön -kentän arvoksi Kyllä.
    * Jos näyttöön tulee sanoma "Suositusmalleja ei voitu noutaa", se johtuu siitä, että olet päivittänyt yksikkösäilön hiljattain eikä järjestelmä ole vielä käsitellyt uusia tietoja. Odota 2-3 tuntia ja yritä uudelleen.  
9. Valitse Tallenna.
10. Sulje sivu.


