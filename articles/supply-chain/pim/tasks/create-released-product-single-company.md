---
title: Luo vapautettu tuote yhdessä yrityksessä
description: Tässä menettelyssä kerrotaan, miten yksittäinen vapautettu tuote luodaan yksittäisessä yrityksessä.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4a34a03dc5bb3cec37bbccdf913bee5088af6a0
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844606"
---
# <a name="create-a-released-product-for-a-single-company"></a>Luo vapautettu tuote yhdessä yrityksessä

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten yksittäinen vapautettu tuote luodaan yksittäisessä yrityksessä. Kun vapautettu tuote on luotu, se on heti käytettävissä vain tässä yksikössä. Voit suorittaa tämän menettelyn esittely-yrityksessä USMF. Tuotesuunnittelija tekee yleensä tämän tehtävän.


## <a name="create-a-released-product"></a>Vapautetun tuotteen luominen
1. Siirry Vapautetut tuotteet -kohtaan.
2. Valitse Uusi.
3. Kirjoita arvo Tuotenumero-kenttään.
    * Jos tuotenumeroa ei automaattisesti syötetä Tuotenumero-kenttään, kirjoita yksilöivä tuotenumero. Tämä vaihe vaaditaan vain, jos tuotenumeroille ei ole määritetty numerosarjaa.  
4. Kirjoita arvo Tuotteen nimi -kenttään.
    * Tuotenimen oletusarvoksi määritetään hakunimi. Tarvittaessa voit muuttaa hakunimen.  
5. Avaa haku valitsemalla Nimikemalliryhmä-kentässä avattavan valikon painike.
    * Nimikemalliryhmien sisältämät asetukset määrittävät, kuinka nimikkeitä hallitaan ja käsitellään nimikkeiden vastaanotoissa ja varasto-otoissa. Asetukset myös määrittävät, miten nimikkeiden kulutus lasketaan.  
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku valitsemalla Nimikeryhmä-kentässä avattavan valikon painike.
    * Käyttämällä nimikeryhmiä voidaan varastoa hallita jakamalla varastonimikkeet ryhmiin nimikkeiden ominaisuuksien mukaan. Voit esimerkiksi hallinnoida sitä, miten tiedot kirjataan päätileille, luomalla erilaisia tiettyihin päätileihin liittyviä nimikeryhmiä. Tämä mahdollistaa nimikkeiden varastoarvon seuraamisen eri vaiheissa.  
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Avaa haku valitsemalla Varastodimensioryhmä-kentässä avattavan valikon painike.
    * Varastodimensioilla hallitaan nimikkeiden tallentamista varastoon ja ottamista sieltä. Varastodimensio voi olla esimerkiksi toimipiste ja varasto.  
12. Etsi haluamasi tietue luettelosta ja valitse se.
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
14. Avaa haku valitsemalla Seurantadimensioryhmä-kentässä avattavan valikon painike.
    * Seurantadimensioryhmä määrittää, mitkä seurantadimensiot voit tuotteelle määrittää. Esimerkiksi eränumeroa ja sarjanumeroa voidaan käyttää varastonimikkeiden seurantaan.  
15. Etsi haluamasi tietue luettelosta ja valitse se.
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
17. Avaa haku valitsemalla Varastoyksikkö-kentässä avattavan valikon painike.
    * Varastoyksikkö määrittää, kuinka tuote mitataan, kun se varastoidaan varastoon.  
18. Etsi haluamasi tietue luettelosta ja valitse se.
19. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
20. Avaa haku valitsemalla Ostoyksikkö-kentässä avattavan valikon painike.
    * Ostoyksikkö määrittää, kuinka tuote mitataan, kun se on ostettu toimittajalta.  
21. Etsi haluamasi tietue luettelosta ja valitse se.
22. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
23. Avaa haku valitsemalla Myyntiyksikkö-kentässä avattavan valikon painike.
    * Myyntiyksikkö määrittää, kuinka tuote mitataan, kun se myydään asiakkaalle.  
24. Etsi haluamasi tietue luettelosta ja valitse se.
25. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
26. Avaa haku valitsemalla Tuoterakenteen yksikkö -kentässä avattavan valikon painike.
    * Tuoterakenneyksikkö määrittää, kuinka tuote mitataan, kun se sisällytetään tuoterakenteeseen.  
27. Etsi haluamasi tietue luettelosta ja valitse se.
28. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
29. Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.
    * Nimikkeen arvonlisäveroryhmä Myynnin verotus -ryhmässä määrittää, miten arvonlisävero lasketaan kullekin nimikkeelle.  
30. Etsi haluamasi tietue luettelosta ja valitse se.
31. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
32. Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.
    * Nimikkeen arvonlisäveroryhmä Ostojen verotus -ryhmässä määrittää, miten oston vero lasketaan kullekin nimikkeelle.  
33. Etsi haluamasi tietue luettelosta ja valitse se.
34. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
35. Valitse OK.

## <a name="add-product-characteristics"></a>Tuotteen fyysisten ominaisuuksien lisääminen
1. Laajenna tai tiivistä Varastonhallinta-osa.
2. Syötä Nettopaino-kenttään numero.
3. Syötä Taarapaino-kenttään numero.
4. Syötä Bruttosyvyys-kenttään numero.
5. Syötä Bruttoleveys-kenttään numero.
6. Syötä Bruttokorkeus-kenttään numero.
7. Syötä Tilavuus-kenttään numero.

## <a name="add-financial-dimensions"></a>Taloushallinnon dimensioiden lisääminen
1. Laajenna tai tiivistä Taloushallinnon dimensiot -osa.
2. Avaa haku valitsemalla BusinessUnit-kentässä avattavan valikon painike.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Avaa haku valitsemalla CostCenter-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku valitsemalla Osasto-kentässä avattavan valikon painike.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Avaa haku valitsemalla ItemGroup-kentässä avattavan valikon painike.
12. Etsi haluamasi tietue luettelosta ja valitse se.
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

