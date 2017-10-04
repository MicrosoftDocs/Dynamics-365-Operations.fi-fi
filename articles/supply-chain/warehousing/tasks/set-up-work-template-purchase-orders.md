--- 
title: "Määritä työmalli ostotilauksia varten"
description: "Tässä menettelyssä käsitellään vastaanotettujen nimikkeiden poispanossa käytettävän yksinkertaisen työmallin määrittämistä."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: aa561d558827e78529ef797b6df6dd3c1dcce34d
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Määritä työmalli ostotilauksia varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään vastaanotettujen nimikkeiden poispanossa käytettävän yksinkertaisen työmallin määrittämistä. Työmallit määrittävät varastotyöntekijälle mobiililaitteessa näytettävät ohjeet, kun nimikkeitä siirretään vastaanotosta. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoissa mainituilla tiedoilla. Luo työpoolin tunnus ennen tämän opastuksen aloittamista. Tässä esimerkissä käytetään Saapuva-asetuksessa kutsuttua työpoolin tunnusta. Tämä menettely on tarkoitettu varastopäällikölle.

1. Valitse Varastonhallinta > Asetukset > Työ > Työmallit.
2. Valitse Työtilaustyyppi-kentässä Ostotilaukset.

## <a name="create-a-work-template-header"></a>Luo työmallin otsikko
1. Valitse Uusi.
2. Syötä Järjestysnumero-kenttään numero.
    * Työmallit arvioidaan tässä järjestyksessä. Voit tarvittaessa muuttaa järjestystä.  
3. Kirjoita Työmalli-kenttään arvo.
    * Tämä on mallin yksilöivä tunniste.  
4. Kirjoita Työmallin kuvaus -kenttään arvo.
    * Voimassaoleva-asetusta ei voi valita, ennen kuin mallin tarvitsevat tiedot on annettu ja Tallenna on valittu.  
    * Ostotilaus-tyypin työtilausta ei voi käsitellä automaattisesti, joten jätä Käsittele automaattisesti -asetuksen valinnaksi Ei.  
5. Kirjoita Työpoolin tunnus -kenttään arvo.
    * Työpoolin tunnuksilla voi järjestää työt ryhmiksi. Tässä määritetty arvo on tällä mallilla luotavien töiden oletusarvo.  
6. Lisää Työn prioriteetti -kenttään 1.
    * Tämä ilmaisee työn tärkeyden ja tässä määritetty arvo on tällä mallilla luotavien töiden oletusarvo.  
7. Valitse Tallenna.
    * Muokkaa kyselyä -painike tulee käytettäväksi, kun työmallin otsikko on tallennettu.  

## <a name="set-up-the-query-for-the-work-template"></a>Määritä työmallin kysely
1. Valitse Muokkaa kyselyä.
    * Määritettävä rajoitus aiheuttaa sen, että mallia voi käyttää vain tietyssä varastossa.  
2. ValitseLisää.
3. Merkitse valittu rivi luettelossa.
4. Kirjoita Kenttä-kenttään varasto.
5. Kirjoita arvo Ehdot-kenttään.
6. Valitse OK.
7. Valitse Kyllä.

## <a name="set-work-template-details"></a>Määritä työmallin tiedot
1. Valitse Uusi.
2. Valitse Työtyyppi-kentässä Keräilyt.
3. Kirjoita Työluokan tunnus -kenttään osto.
    * Tässä määritetty työluokka on kaikkien tällä mallilla luotujen Keräily-tyypin työrivien oletus. Työluokkaa ei voi ohittaa työtilausriveiltä. Työluokilla ohjataan ja/tai rajoitetaan työtilausrivityyppejä, joita varastotyötekijä voi käsitellä mobiililaitteessa.  
4. Valitse Uusi.
5. Valitse Työtyyppi-kentässä Määritä.
6. Kirjoita Työluokan tunnus -kenttään arvo.
    * Keräily- ja määritysohjeet kuuluvat yhteen. Jokaisella keräily/määritys-joukolla on oltava sama työluokka. Käytä samaa, keräilyohjeessa ilmoitettua työluokkaa.  
7. Valitse Tallenna.
    * Huomaa, että Voimassaoleva-valinta on nyt valittuna.  

