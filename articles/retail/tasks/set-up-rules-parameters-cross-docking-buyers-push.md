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
ms.openlocfilehash: a22756279ba316a7efd4d09c48c55e8cc98ba29d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "366325"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a>Määritä säännöt ja parametrit cross dockingille ja ostotarjonnalle

[!include[task guide banner](../includes/task-guide-banner.md)]

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

