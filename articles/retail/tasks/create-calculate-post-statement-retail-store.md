--- 
title: "Luo, laske ja kirjaa laskelma vähittäismyymälälle"
description: "Tässä menettelyssä kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42ab631e29a7fae1140acd41ad80c13e55ca1404
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a>Luo, laske ja kirjaa laskelma vähittäismyymälälle

[!include[task guide banner](../includes/task-guide-banner.md)]

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


