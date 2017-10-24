--- 
title: "Siirrä materiaaleja kanban-töiden avulla (vain helmikuu 2016)"
description: "Tässä menettelyssä keskitytään otto-kanbaneihin materiaalien siirtämiseksi."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c79480d844627a7eed8129515924f1f70ad04f95
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a>Siirrä materiaaleja kanban-töiden avulla (vain helmikuu 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä keskitytään otto-kanbaneihin materiaalien siirtämiseksi. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu varastotyöntekijälle.


## <a name="display-transfer-jobs"></a>Siirtotöiden näyttäminen
1. Siirry kohtaan Tuotannonhallinta > Kanban > Siirtotöiden Kanban-taulu.
2. Laajenna tai tiivistä Suodattimet-osa.
    * Suodattimet-osassa voit määrittää, mitkä työt näkyvät suodatettaessa tuotantovirran, tehtävän nimen, lähetysvaraston ja -sijainnin ja vastaanottovaraston ja -sijainnin mukaan.  
3. Syötä Varastosta-kenttään 11.
4. Syötä Varastoon-kenttään arvo 12.

## <a name="start-a-transfer-job"></a>Aloita siirtotyö
1. Poista luettelosta mahdollisen valitun rivin valinta.
2. Valitse luettelosta rivi 4.
    * Valitse ensimmäisen työ, jonka tila on Ei Suunniteltu. Varmista, että tämä on ainoa valittu työ.  
3. Valitse Käynnistys.
    * Huomaa, että kuvake osoittaa työn alkaneen.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Toisen siirtotyön valitseminen ja määrän muuttaminen
1. Etsi haluamasi tietue luettelosta ja valitse se.
    * Voit valita useita töitä, mutta valitse tässä vaiheessa rivi 5.  
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Varmista, että edellisen vaiheen työ on ainoa valittuna oleva. Poista muiden töiden valinta.  
3. Merkitse Työn määrä- kentän arvo muistiin myöhempää käyttöä varten
4. Määritä Työn määrä -kenttään arvo 30.
    * Huomaa varoitus! 30 on liikaa siirrettäväksi. Kanban-säännön asetusten perusteella voit siirtää vain alkuperäisen määrän.  
5. Käytä aiempaa Työn määrä -kentän arvoa
    * Määritä työn määräksi edellinen arvo.  

## <a name="start-the-second-transfer-job"></a>Toisen siirtotyön aloittaminen
1. Valitse Käynnistys.
    * Nyt rivillä 5 olevan työn siirto alkaa.  

## <a name="complete-both-transfer-jobs"></a>Molempien siirtotöiden suorittaminen
1. Valitse luettelosta rivi 4.
    * Nyt on valittuna kaksi siirtotyötä rivillä 4 ja 5.  
2. Valitse Valmis.
    * Molempien töiden siirto suoritetaan.  


