---
title: Työpaikkojen julkaiseminen ulkoisille urasivustoille Attractista
description: 'Tässä ohjeaiheessa kerrotaan, miten voit Dynamics 365 Talent: Attractista julkaista töitä ulkoisille työhönoton sivustoille.'
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 2c822a1f799144bb9240fc0cbdeb6c5441e278af
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551400"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Työpaikkojen julkaiseminen ulkoisille urasivustoille Attractista

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract auttaa palkkaamaan työntekijöitä mahdollistamalla työpaikkojen julkaisemisen suoraan Attractista Broadbeaniin. Kun olet [luonut työpaikan](./creating-jobs-attract.md), sinun tarvitsee vain napsauttaa painiketta, jonka jälkeen työpaikka on työpaikan kaikkien mahdollisten ehdokkaiden nähtävillä Broadbeanissa.

Työpaikkojen julkaisemista varten Broadbeanissa tarvitaan soveltuva Broadbean-käyttöoikeus. Broadbean sisältää erilaisia tuotteita ja suunnitelmia. Jos haluat lisätietoja Broadbeanin käyttöoikeuksista ja hinnoittelusta, [ota yhteys Broadbeaniin](https://www.broadbean.com/contact-us/).

Jos olet järjestelmänvalvoja ja tarvitset lisätietoja Broadbeanin integroinnista Attractiin, katso [Ulkoisten työpaikkasivustojen asetusten määrittäminen](./attract-admin-job-board-settings.md).

## <a name="post-jobs-to-broadbean"></a>Työpaikkojen julkaiseminen Broadbeaniin

Kun Broadbean on otettu käyttöön, rekrytoijat ja järjestelmänvalvojat voivat julkaista sinne työpaikkailmoituksen. Ilmoituksessa on oltava URL-osoite työn hakemista varten.

1. Avaa Attractissa työ, jonka haluat julkaista Broadbeanissa.
2. Valitse **Ilmoitukset**-osassa **Julkaise nyt** -kuvaketta, joka lähettää tiedot Broadbeaniin.
3. Noudata Broadbean-ikkunan ohjeita.

Attract välittää Broadbeaniin seuraavat tiedot:

- Pyynnön tunnus
- Ammattinimike
- Työn kuvaus
- Työn sijainti
- Hakemuksen URL-osoite
- Työhönottajan tiedot

Kun Broadbean on suorittanut julkaisun, työn **Ilmoitukset**-osio Attractissa näyttää Broadbean-tilana **Julkaistu**.

> [!NOTE]
> - Broadbean edellyttää **Toimiala**-kentän. Tämän kentän oletusarvo on tällä hetkellä **IT**. Voit kuitenkin muuttaa arvoa oikeaan toimialaan Broadbean-työpaikkailmoituksen ikkunassa.
> - Kestää jonkin aikaa, kun Broadbean viimeistelee työn julkaisun kaikkiin valitsemiisi työpaikkailmoitussivustoihin. Näin voi olla vähäinen viive ennen kuin Attract näyttää työn tilan päivityksen.

### <a name="view-a-broadbean-job-posting"></a>Tarkastele Broadbean-työpaikkailmoitusta

Kun olet julkaissut työn Broadbeaniin, voit tarkastella sitä Attractista.

1. Avaa Attractissa työ, jota haluat tarkastella Broadbeanissa.
2. Valitse **Ilmoitukset**-välilehdessä Broadbeaniin viittaavat kolme pistettä (**...**) -painike ja valitse sitten **Näytä**.

Broadbean-työpaikkailmoitus näkyy uudessa ikkunassa.

### <a name="update-a-broadbean-job-posting"></a>Päivitä Broadbean-työpaikkailmoitus

Voit päivittää Broadbean-työpaikkailmoituksen kahdella tavalla.

1. Avaa Attractissa työ, jota haluat päivittää.
2. Valitse **Ilmoitukset**-osassa **Päivitä julkaisu** -kuvaketta, joka lähettää tiedot Broadbeaniin.
3. Muokkaa ilmoitusta Broadbean-ikkunassa.

–TAI–

1. Avaa Attractissa työ, jota haluat tarkastella Broadbeanissa.
2. Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Näytä**.
3. Muokkaa työn tietoja Broadbean-ikkunassa ja julkaise sitten työ uudelleen. Työn tietoja Attractissa ei muuteta.

### <a name="remove-a-broadbean-job-posting"></a>Poista Broadbean-työpaikkailmoitus

Voit poistaa työpaikkailmoituksen Broadbeanista tarpeen mukaan.

1. Avaa Attractissa työ, jonka haluat poistaa.
2. Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Poista julkaisu**.

Sen jälkeen, kun Broadbean poistaa työn, Broadbean-kohteessa Attractissa on **Julkaise nyt** -painike. Tämä painike ilmaisee, että työ on poistettu ja se voidaan julkaista uudelleen.

### <a name="troubleshoot-job-posting-to-broadbean"></a>Broadbeanissa julkaistavan työpaikkailmoituksen vianmääritys

Jos sinulla on vaikeuksia julkaista työ Broadbeanissa, yritä seuraavia vaiheita.

1. Varmista, että Broadbean-tunnistetiedot, jotka olet määrittänyt Attractissa, ovat voimassa ja oikeelliset.
2. Jos tunnistetiedot ovat voimassa ja oikein, ota yhteyttä [Broadbeanin tukeen](https://www.broadbean.com/resources/support/).
3. Jos ongelma ei ratkea, ota yhteyttä [Microsoftin tukeen](./talent-support.md).

## <a name="see-also"></a>Lisätietoja

[Työpaikkojen luominen](./creating-jobs-attract.md)

[Ulkoisten työpaikkasivustojen asetusten määrittäminen](./attract-admin-job-board-settings.md)
