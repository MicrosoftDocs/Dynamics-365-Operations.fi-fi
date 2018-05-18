--- 
title: "Maksutavan määrittäminen ISO20022-tilisiirtoja varten"
description: "Näiden ohjeiden avulla voi määrittää toimittajan ISO20022-tilisiirron tai minkä tahansa muun maksutyypin luomaan tiedostoja sähköisen raportoinnin avulla."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bed51f8749dfa0264ad39f51f9ceb295ac46fe93
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Maksutavan määrittäminen ISO20022-tilisiirtoja varten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Näiden ohjeiden avulla voi määrittää toimittajan ISO20022-tilisiirron tai minkä tahansa muun maksutyypin luomaan tiedostoja sähköisen raportoinnin avulla. 

Viennin muotokonfiguraatiot ja maksutilit on määritettävä ennen tämän tehtävän suorittamista.

Tämän tehtävän luomisessa käytettiin esittelytietojen DEMF-yritystä.

Tämä on kolmas viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.

1. Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Maksutapa-kenttää arvolla SEPA CT.
3. Valitse Muokkaa.
4. Valitse Kausi-kentässä Yhteensä.
5. Valitse Maksutyyppi-kentässä Sähköinen maksu.
6. Laajenna Tiedostomuodot-osa.
7. Valitse Yleinen sähköinen raportointi -kentässä Kyllä.
8. Syötä Vie muotokonfiguraatio -kenttään arvo tai valitse arvo.
    * Valitse luettelosta arvo ISO20022 - tilisiirto (DE). Jos luettelo on tyhjä, tuotua ja aktiivista toimittajan maksun viennin muotokonfiguraatiota ei ole.  
9. Valitse Tilityyppi-kentässä Pankki.
10. Syötä Maksutili-kenttään arvot DEMF OPER.
11. Valitse Tallenna.


