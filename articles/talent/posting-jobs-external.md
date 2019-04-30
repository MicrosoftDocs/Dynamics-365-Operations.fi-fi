---
title: Työpaikkailmoitusten julkaiseminen Attractista ulkoisille urasivustoille
description: Tässä ohjeaiheessa kerrotaan, miten voit Dynamics 365 for Talent - Attractista julkaista töitä ulkoisille työhönoton sivustoille.
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
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
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 1653d1e28d02f8a9a4bea8df562ac98d7a350ed1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/15/2019
ms.locfileid: "993665"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Työpaikkailmoitusten julkaiseminen Attractista ulkoisille urasivustoille

[!include [banner](../includes/banner.md)]

Haluat saada työpaikkailmoituksesi mahdollisimman monen pätevän ehdokkaan näkyville kuin mahdollista. Työhönoton sivustot, kuten Broadbean, voi auttaa saavuttamaan tämän tavoitteen. Microsoft Dynamics 365 Talent: Attractin avulla voit nyt julkaista työpaikkoja Broadbeanissa, ja Microsoft tarjoaa koko ajan uusia mahdollisuuksia tällä alueella.

## <a name="post-jobs-to-broadbean"></a>Työpaikkojen julkaiseminen Broadbeaniin

Ennen kuin voit julkaista töitä Broadbeaniin, sinun on määritettävä Broadbean-integrointi.

> [!NOTE]
> - Voit julkaista töitä ulkoisille sivustoille vain jos sinulla on [kattava työhönottolaajennus](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - Tämä ominaisuus on tällä hetkellä vain esiversiossa. Voit halutessasi kokeilla sitä [ottamalla sen käyttöön Attractin järjestelmänvalvojan asetuksissa](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>Broadbean-integroinnin määritys

1. Kirjaudu Attractiin järjestelmänvalvojana.
2. Valitse **Asetukset**-painike (rataskuvake) sivun oikeassa yläkulmassa ja valitse sitten **Hallintakeskus**.
3. Ota integraatio käyttöön **Työpaikkailmoitussivun asetukset** -välilehden **Ota Broadbean-integrointi käyttöön** -osassa.
4. Muodosta yhteys Broadbeaniin ja anna tietosi kohdassa **Käyttäjätunnus, Asiakastunnus, Salaustunnus**.

> [!WARNING]
> Broadbean-tunnistetietosi ovat luottamuksellisia. Siksi tallenna ja jaa niitä vastuuntuntoisesti. Kaikki käyttäjät, joilla on järjestelmänvalvojan rooli Attractissa, voivat tarkastella näitä tunnistetietoja.

> [!NOTE]
> Microsoft ja Attract eivät ole mukana luomassa ja ylläpitämässä näitä arvoja. On omalla vastuullasi pitää ne ajan tasalla Attractissa ja selvittää mahdolliset ongelmat Broadbeanin kanssa.

### <a name="post-a-job-to-broadbean"></a>Työpaikan julkaiseminen Broadbeaniin

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
2. Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Näytä**.

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

### <a name="troubleshoot-the-broadbean-integration"></a>Broadbean-integroinnin vianmääritys

Jos sinulla on vaikeuksia julkaista työ Broadbeanissa, yritä seuraavia vaiheita.

1. Varmista, että Broadbean-tunnistetiedot, jotka olet määrittänyt Attractissa, ovat voimassa ja oikeelliset.
2. Jos tunnistetiedot ovat voimassa ja oikein, ota yhteyttä [Broadbeanin tukeen](https://www.broadbean.com/resources/support/).
3. Jos ongelma ei ratkea, ota yhteyttä [Microsoftin tukeen](./talent-support.md).
