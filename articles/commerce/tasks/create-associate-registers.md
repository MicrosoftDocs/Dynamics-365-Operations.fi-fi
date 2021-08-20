---
title: Luo ja liitä rekisterit
description: Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan.
author: rubencdelgado
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff6fb42cd0b080ff576aa3a784cfce985d69fe0347af44dfa9935b4e8e5ffe00
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743356"
---
# <a name="create-and-associate-registers"></a>Luo ja liitä rekisterit

[!include [banner](../includes/banner.md)]

Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan. Menettely käyttää USRT-demotietoyritystä.

1. Siirry kohtaan Retail ja Commerce > Kanavan asetukset > Myyntipisteen asetukset > Kassakoneet.
2. Valitse Uusi.
3. Kirjoita Kassakoneen numero -kenttään uuden kassakoneen tunnus.
    * Kassakoneen tunnus sisältää yleensä koodeja, joiden avulla kassakone yhdistetään myymälään, johon se kuuluu sekä sijaintiin myymälässä.  
4. Kirjoita Nimi-kenttään kassakonetta kuvaava nimi.
5. Syötä tai valitse arvo Myymälän numero -kentässä.
6. Syötä tai valitse arvo Laiteprofiili-kentässä.
    * Laiteprofiileilla määritetään oheislaitteet, jotka liitetään kassakoneeseen, kuten käteislokero ja kuittitulostin.  
7. Anna tai valitse Visuaalinen profiili -kentässä arvo.
    * Visuaalisten profiilien avulla määritetään kuvat, joita käytetään myyntipisteen taustalla ja kirjautumissivulla. Niillä määritetään myös myyntipisteen teema.  
8. Kirjoita arvo EFT:n POS-kassakoneen numero -kenttään.
    * EFT:n POS-kassakoneen numeroa käytetään ilmoittamaan maksun käsittelijälle, miltä maksupäätteeltä varmennuspyyntö on lähetetty. Tätä arvoa kutsutaan usein nimellä "päätteen tunnus" tai "TID". TID löytyy yleensä maksupäätteen tarrasta.  
9. Valitse Tallenna.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]