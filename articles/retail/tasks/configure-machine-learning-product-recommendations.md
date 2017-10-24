--- 
title: "Määritä automaattiset tuotesuositukset"
description: "Tämä menettely päivittää yksikkösäilän tiedot, joita käyttää tuotesuosituksista vastaava automaattianalyysijärjestelmää, ja ottaa sitten käyttöön tuotesuositukset myyntipisteiden asiakasohjelmissa."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

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


