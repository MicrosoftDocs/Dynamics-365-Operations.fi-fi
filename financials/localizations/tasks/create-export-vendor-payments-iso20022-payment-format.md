--- 
title: Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa
description: "Näiden ohjeiden avulla voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 16c2af862a73047a2e6ebdc056275392fa8a0d93
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa

[!include[task guide banner](../../includes/task-guide-banner.md)]

Näiden ohjeiden avulla voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla. 

Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.

Tämä on viides viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="create-payment-lines"></a>Maksurivien luominen
1. Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Syötä tai valitse arvo Nimi-kenttään.
5. Valitse Rivit.
6. Valitse Maksuehdotus.
7. Valitse Luo maksuehdotus.
8. Laajenna Tietueet-kohta ja sisällytä osaan.
9. Valitse Suodatin.
10. Valitse luettelosta Toimittajat-taulukon ja Toimittajan tili -kentän rivi.
11. Syötä tai valitse arvo Ehdot-kenttään.
    * Voit käyttää kaikkia maksettavien toimittajatapahtumien valintaehtoja, tässä esimerkissä toimittajan tilinä käytetään arvoa DE-001.  
12. Valitse OK.
13. Valitse OK.
14. Valitse Luo maksut.

## <a name="generate-an-iso20022-payment-file"></a>ISO20022-maksutiedoston luominen


