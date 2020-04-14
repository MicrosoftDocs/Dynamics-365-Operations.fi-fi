---
title: Määritä säännöt ja parametrit cross dockingille ja ostotarjonnalle
description: Tässä menettelyssä esitellään täydennyssääntöjen luontivaiheet.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141128"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a>Määritä säännöt ja parametrit cross dockingille ja ostotarjonnalle

[!include [banner](../includes/banner.md)]

Tässä menettelyssä esitellään täydennyssääntöjen luontivaiheet. Täydennyssääntöjen avulla voidaan hallita tuotteiden jakelua myymälöihin, kun käytössä ovat cross docking ja ostotarjonta. Täydennyssäännöt voidaan määrittää myymälöille tai myymäläryhmille. Säännön kullekin riville määritetty paino määrittää, miten tuotteen määrät jaellaan myymälöihin, kun jakelumenetelmä on cross docking- tai ostotarjonta ja käytössä ovat täydennyssäännöt. Näissä toimintaohjeissa käytetään esittely-yritystä USRT.

1. Siirry Täydennyssäännöt-kohtaan.
2. Valitse Uusi.
3. Kirjoita arvo Täydennyssääntö-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Tallenna.
6. ValitseLisää.
7. Merkitse valittu rivi luettelossa.
    * Tyypiksi voi valita Täydennyshierarkia- tai Kanava-arvon. Arvo määrittää, onko Nimi-kentän valinta kanavahierarkia tai tietty kanava.  Tässä esimerkissä käytetään täydennyshierarkiaa.  
8. Valitse arvo Nimi-kentässä.
    * Painon oletusarvo on varastossa määritetty paino.  Täydennyssäännössä voidaan käyttää painoa. Voit myös syöttää uuden painon Paino-kenttään.  
9. Syötä numero Paino-kenttään.
10. ValitseLisää.
11. Merkitse valittu rivi luettelossa.
12. Valitse Tyyppi-kentässä Kanava.
13. Syötä tai valitse arvo Nimi-kenttään.
14. Syötä numero Paino-kenttään.
15. Valitse Tallenna.

