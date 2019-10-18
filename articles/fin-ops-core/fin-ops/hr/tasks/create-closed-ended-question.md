---
title: Luo suljettu kysymys
description: Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e4f9697fc00798d917db6f7f50d7e3b8739233
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177647"
---
# <a name="create-a-closed-ended-question"></a>Luo suljettu kysymys

[!include [task guide banner](../../includes/task-guide-banner.md)]

Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita. Ensin luodaan vastaukset sisältävä vastausryhmä. Tämän jälkeen luodaan kysymys, joka käyttää vastausryhmää. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-an-answer-group"></a>Vastausryhmän luominen
1. Valitse Kyselylomake > Suunnittelu > Vastausryhmät.
2. Valitse Uusi.
3. Syötä Vastausryhmä-kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
    * Sijoita vastaukset satunnaiseen järjestykseen Muodosta satunnaisesti -toiminnon avulla aina, kun vastausryhmää käytetään kysymyksessä.  
5. Valitse Vastaus.
6. Valitse Uusi.
    * Järjestysnumero määrittää vastausten näyttöjärjestyksen, ellei vastausryhmän Muodosta satunnaisesti -kohtaa ole valittu.  
    * Vastauksille voidaan myöntää pisteitä, kun kyselylomake pistetytetään.  
7. Syötä Pisteet-kenttään numero.
    * Oikea vastaus voidaan merkitä. Näin kyselylomakkeen pisteytyksessä usein tehdään.  
8. Syötä Vastaus-kenttään arvo.
    * Jatka vastausryhmän vastausten valinnan asetusten luomista.  
9. Valitse Uusi.
10. Syötä Pisteet-kenttään numero.
11. Syötä Vastaus-kenttään arvo.
12. Valitse Uusi.
13. Syötä Pisteet-kenttään numero.
14. Syötä Vastaus-kenttään arvo.
15. Valitse Uusi.
16. Syötä Pisteet-kenttään numero.
17. Syötä Vastaus-kenttään arvo.
18. Valitse Uusi.
19. Syötä Pisteet-kenttään numero.
20. Syötä Vastaus-kenttään arvo.
21. Sulje sivu.
22. Sulje sivu.

## <a name="create-the-question"></a>Kysymyksen luominen
1. Siirry kohtaan Kyselylomake > Suunnittelu > Kysymykset.
2. Valitse Uusi.
3. Ryhmittele liittyvät kysymykset yhteen Tyyppi-kentän avulla.
    * Voit käyttää monivalintakysymyksissä valintaruudun, vaihtoehtopainikkeen tai yhdistelmäruudun syöttötyyppejä.  
4. Valitse vaihtoehto Syötetyyppi-kentässä.
5. Anna tai valitse arvo Vastausryhmä-kenttään.
6. Kirjoita arvo Teksti-kenttään.

