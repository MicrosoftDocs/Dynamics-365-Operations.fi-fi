--- 
title: "Luo, laske ja kirjaa laskelma vähittäismyymälälle"
description: "Tässä menettelyssä kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 33ebb28196baa9ae944dbd124274b05cb587fea4
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a>Luo, laske ja kirjaa laskelma vähittäismyymälälle

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet. Samalle tehtävälle voidaan määrittää myös erätöitä. Erätöiden määrittämisen ja suorittamisen vaiheet löytyvät myös muista aiheista. Tämän menettelyn suorittaminen edellyttää myyntipisteellä tehtyjä ja Dynamics AX:ään siirrettyjä tapahtumia. Tämä tallenne käyttää esittelytietojen USRT-yritystä. Tämä ohje voi viitata Microsoft Dynamics AX -nimeen. Huomaa, että Dynamics AX on nyt nimeltään Microsoft Dynamics 365 for Operations.

1. Valitse Kaikki työtilat > .. > Vähittäismyymälän myyntitiedot.
2. Valitse Uusi laskelma.
3. Avaa haku valitsemalla Myymälä numero -kentässä avattavan valikon painike.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Valitse OK.
    * Asetusryhmässä on asetuksia, jotka ohjaavat laskelmaan sisällytettävien tapahtumien valintaa sekä tapahtumien laskentariveiksi ryhmittelyä. Voit avata asetusryhmän ja muuttaa asetuksia tai käyttää oletusarvoja.  
    * Laskelmatapa-kentässä määritetään, miten laskelmarivit ryhmitellään.  
    * Valitse henkilökunnan jäsen tai kassakone, jos haluat tehdä laskelman vain tietylle henkilökunnan jäsenelle tai kassakoneelle.  
6. Valitse vaihtoehto Sulkemistapa-kentässä.
7. Valitse Laske laskelma.
8. Valitse Kyllä.
    * Kun laskelma on tehty, jokaiselle käytetylle maksu- ja laskelmatavalle on luotu rivejä, jotka sisältävät kokonaissummat.  
    * Voit syöttää kullekin riville lasketun summan, jos summia on syötettävä tai päivitettävä. Laskettuun kenttää siirretään myyntipisteellä kassan maksuvälineittäin tehtyjen laskemistapahtumien summat.  
9. Valitse Kirjaa laskelma.
10. Valitse Sulje.
11. Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälän myyntitiedot.
12. Valitse Kirjatut laskelmat -välilehti.


