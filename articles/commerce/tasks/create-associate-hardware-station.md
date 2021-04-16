---
title: Luo ja liitä laiteasema
description: Tässä menettelyssä kerrotaan, miten uusi laiteasema luodaan.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4402e8d1179499512034e7deb8b3eb78f12096f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798582"
---
# <a name="create-and-associate-a-hardware-station"></a>Luo ja liitä laiteasema

[!include [banner](../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten uusi laiteasema luodaan. Luodaan uusi laiteprofiili ja käytetään sitä uusien laiteasemien lisäämisessä ennalta määritettyyn myymälään (kanava). Menettely käyttää esittelytietojen USRT-yritystä.

1. Valitse Commerce-perustiedot > Kanavat > .. > .. > .. > Laiteaseman profiilit.
2. Valitse Uusi.
3. Syötä Laiteaseman tunnus -kenttään TestHWProfile.
4. Kirjoita arvo Nimi-kenttään.
5. Lisää Portin numero -kenttään numero.
6. Avaa haku valitsemalla Laiteprofiili-kentässä avattavan valikon painike.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Avaa haku valitsemalla Paketin nimi -kentässä avattavan valikon painike.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Tämä on vakiopaketti, joka sisältyy uuteen ympäristöön. Versionumero voi vaihdella.  
11. Valitse Tallenna.
12. Sulje sivu.
13. Valitse Retail ja Commerce > Kanavat > Kaikki myymälät.
14. Valitse luettelosta rivi 17.
    * Jos käytössä on esittelytietojen USRT-yritys, tämä on Houstonin myymälä.  
15. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
16. Ota käyttöön Laiteasemat-osan laajennus.
17. ValitseLisää.
18. Merkitse valittu rivi luettelossa.
19. Avaa haku valitsemalla Profiilin tunnus -kentässä avattavan valikon painike.
20. Etsi haluamasi tietue luettelosta ja valitse se.
    * Tämän on oltava edellisissä vaiheissa luotu uusi laiteaseman profiili.  
21. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
22. Kirjoita arvo Isännän nimi -kenttään.
23. Syötä EFT-päätteen tunnus -kenttään arvo.
24. Valitse Tallenna.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]