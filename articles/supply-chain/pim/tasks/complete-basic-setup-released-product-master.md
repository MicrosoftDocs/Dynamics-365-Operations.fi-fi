--- 
title: "Julkaistun päätuotteen perusmääritysten päättäminen"
description: "Tässä menettelyssä selvitetään, mitkä asetukset on ainakin määritettävä, ennen kuin päätuotetta voi käyttää tuoterakenneversioissa."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 35617f5bec877fbe8a89d015eda16a66ee14d335
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Julkaistun päätuotteen perusmääritysten päättäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä selvitetään, mitkä asetukset on ainakin määritettävä, ennen kuin päätuotetta voi käyttää tuoterakenneversioissa.

Tämä on kolmas kahdeksasta menettelystä, joissa selitetään, miten dimensioihin perustuvia konfiguraatioyhdistelmiä luodaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.

1. Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse toisessa menettelyssä vapautettu päätuote. Tämä päätuote on luotu dimensioihin perustuvalla konfiguraatiomenetelmällä.  
3. Valitse toimintoruudussa Tuote.
4. Avaa valintaikkunalomake valitsemalla Dimensioryhmät.
5. Avaa haku valitsemalla Varastodimensioryhmä-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
    * Varastodimensioryhmä määrittää, mitä varastodimensioita käytetään tuotetapahtumassa. Valitse Toimipaikka tässä menettelyssä.  
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku valitsemalla Seurantadimensioryhmä-kentässä avattavan valikon painike.
9. Etsi haluamasi tietue luettelosta ja valitse se.
    * Seurantadimensioryhmä määrittää, mitä seurantadimensioita käytetään tuotetapahtumassa. Valitse tässä menettelyssä Ei mitään.  
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Valitse OK.
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Valitse Muokkaa.
    * Jatka asennustehtävää avaamalla vapautetun tuotteen tietolomake.  
14. Avaa haku valitsemalla Nimikemalliryhmä-kentässä avattavan valikon painike.
15. Etsi haluamasi tietue luettelosta ja valitse se.
    * Nimikemalliryhmien sisältämät asetukset määrittävät, kuinka nimikkeitä hallitaan ja käsitellään nimikkeiden vastaanotoissa ja varasto-otoissa. Ne määrittävät myös, millä tavalla nimikkeiden kulutus lasketaan. Valitse tähän menettelyyn FIFO.  
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
17. Laajenna tai tiivistä Kustannusten hallinta -osa.
18. Avaa haku valitsemalla Nimikeryhmä-kentässä avattavan valikon painike.
19. Etsi haluamasi tietue luettelosta ja valitse se.
    * Nimikeryhmiä käytetään varaston hallintaan jakamalla varastonimikkeet ryhmiin. Valitse CarAudio tähän menettelyyn.  
20. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
21. Valitse toimintoruudussa Suunnitelma.
22. Valitse Tilauksen oletusasetukset.
23. Valitse Oletusarvoinen tilaustyyppi -kentässä vaihtoehto.
    * Valitsemalla Tuotanto voit määrittää, että tämän päätuotteen oletustoimitusvalinta on sen tuottaminen.  
24. Sulje sivu.
25. Sulje Vapautetun tuotteen tiedot -lomake.


