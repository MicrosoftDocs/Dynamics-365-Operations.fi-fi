--- 
title: Luo myyntipiste (kassakone)
description: "Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: b477b201df62c9fbbbb18978a4a15fa3b4a964ae
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="create-point-of-sale-registers"></a>Luo myyntipiste (kassakone)

[!include [task guide banner](../includes/task-guide-banner.md)]

Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan. Menettely käyttää USRT-demotietoyritystä.

1. Siirry kohtaan Vähittäismyynti ja kauppa > Kanavan asetukset > Myyntipisteen asetukset > Kassakoneet.
2. Valitse Uusi.
3. Kirjoita Kassakoneen numero -kenttään uuden kassakoneen tunnus.
    * Kassakoneen tunnus sisältää yleensä koodeja, joiden avulla kassakone yhdistetään myymälään, johon se kuuluu sekä sijaintiin myymälässä.  
4. Kirjoita Nimi-kenttään kassakonetta kuvaava nimi.
5. Syötä tai valitse arvo Myymälän numero -kentässä.
6. Syötä tai valitse arvo Laiteprofiili-kentässä.
    * Laiteprofiileilla määritetään vähittäismyynnin oheislaitteet, jotka liitetään kassakoneeseen, kuten käteislokero ja kuittitulostin.  
7. Anna tai valitse Visuaalinen profiili -kentässä arvo.
    * Visuaalisten profiilien avulla määritetään kuvat, joita käytetään myyntipisteen taustalla ja kirjautumissivulla. Niillä määritetään myös myyntipisteen teema.  
8. Kirjoita arvo EFT:n POS-kassakoneen numero -kenttään.
    * EFT:n POS-kassakoneen numeroa käytetään ilmoittamaan maksun käsittelijälle, miltä maksupäätteeltä varmennuspyyntö on lähetetty. Tätä arvoa kutsutaan usein nimellä "päätteen tunnus" tai "TID". TID löytyy yleensä maksupäätteen tarrasta.  
9. Valitse Tallenna.


