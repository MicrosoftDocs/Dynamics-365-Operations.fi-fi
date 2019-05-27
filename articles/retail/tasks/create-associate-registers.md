---
title: Luo ja liitä rekisterit
description: Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07e4b9f32a3a74b273272bd0b759d35c2a963e2e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548298"
---
# <a name="create-and-associate-registers"></a>Luo ja liitä rekisterit

[!include[task guide banner](../includes/task-guide-banner.md)]

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

