---
title: Resurssien hallinnan mobiilityötila
description: Tässä ohjeaiheessa on tietoja resurssien hallinnan mobiilityötilasta.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 525f21d076027f1bf339e59fd0e346706044839c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426901"
---
# <a name="asset-management-mobile-workspace"></a>Resurssien hallinnan mobiilityötila

[!include [banner](../../includes/banner.md)]


Tässä ohjeaiheessa on tietoja resurssien hallinnan mobiilityötilasta. Tämä työtila antaa käyttäjien tarkastella ja luoda ylläpitopyyntöjä ja työtilauksia. Käyttäjät voivat myös tarkastella määritettyjä työtilaustöitä kalenteri- tai luettelonäkymässä. Myös käyttökohteita ja toiminnallisia sijainteja voidaan tarkastella ja etsiä.


## <a name="overview"></a>Yleiskuvaus

Resurssien hallinta on kehittynyt moduuli resurssien ja työtilausten hallintaan Dynamics 365 Supply Chain Managementissa. **Resurssien hallinnan** mobiilityötilassa käyttäjät voivat nopeasti tarkastella heille määritettyjä työtilaustöitä valitsemassaan mobiililaitteessa. Käyttäjät voivat myös luoda ja hallita ylläpitopyyntöjä, päivittää elinkaaren tilan sekä tarkastella resurssien ja toiminnallisen sijainnin tietoja omassa mobiililaitteeseen.

Käyttäjät voivat tehdä **resurssien hallinnan** mobiilityötilassa seuraavat tehtävät:

- Ylläpitopyyntöjen luonti, tarkastelu ja muokkaaminen, valokuvan ottaminen tai aiemmin otetun kuvan liittäminen ylläpitopyyntöön ja ylläpitopyynnön elinkaaren tilan muuttaminen. 
- Työtilausten luonti, tarkastelu ja muokkaaminen, valokuvan ottaminen tai aiemmin otetun kuvan liittäminen työtilaukseen, työtilauksen elinkaaren tilan muuttaminen ja työtilauksen töiden tarkastelu.
- Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä.
- Työtilauksen työn luonti, tarkastelu ja muokkaus, resurssilaskurien päivitys, ylläpidon tarkastuslistan tarkastelu, työtilauksen työn huomausten tarkastelu ja muokkaus sekä työtilauksen työssä tarvittavien työkalujen tarkastelu.
- Tietyn resurssin tai toiminnallisen sijainnin tarkastelu tai haku.


## <a name="prerequisites"></a>Edellytykset

Edellytykset vaihtelevat sen mukaan, mikä Dynamics 365 Supply Chain Managementin versio on otettu käyttöön organisaatiossa.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-supply-chain-management"></a>Edellytykset, jos käytössä on Microsoft Dynamics 365 Supply Chain Management 
Jos Microsoft Dynamics 365 Supply Chain Management on otettu käyttöön organisaatiossa, järjestelmänvalvojan on julkaistava **Resurssien hallinta** -mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen
Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:

- [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
- [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen
1. Käynnistä sovellus mobiililaitteessa.

2. Anna Dynamics 365 -URL-osoitteesi.

3. Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.

4. Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

![Kuva 1](media/am-mobile-01.png)


## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

2. Valitse **Oman työtilauksen töiden kalenteri**.

3. Valitse päivämäärä, jona haluat tarkastella työtilauksen töitä. Luettelossa on näkyvissä kunkin työtilauksen työn resurssin tunnus ja toiminnallisen sijainnin tunnus.

4. Saat työn tiedot näkyviin valitsemalla työtilauksen työn luettelossa: resurssin ja toiminnallisen sijainnin tiedot sekä muut siirtymislinkit, joilla voi avata seuraavat kohdat: **Liitteet**, **Tarkistusluettelot**, **Työkalut**, **Resurssilaskurit**, **Huomautukset** ja **Kirjauskansiot**.

![Kuva 2](media/am-mobile-02.png)


## <a name="create-a-work-order-job"></a>Työtilauksen työn luominen

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

2. Valitse **Kaikki ylläpidon työtilaukset**.

3. Valitse työtilaus, jolle haluat luoda uuden työtilauksen.

4. Valitse **Lisää rivi** -painike.

5. Valitse **Resurssi**, jolle haluat luoda työtilauksen.

6. Valitse **Ylläpitotyön tyyppi**, **Ylläpitotyön tyypin variantti** ja **Toimiala**.

7. Valitse **Valmis**.

![Kuva 3](media/am-mobile-03.png)


## <a name="add-attachment-to-a-work-order-job"></a>Liitteen lisääminen työtilauksen työhön

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

2. Valitse **Kaikki ylläpidon työtilaukset**.

3. Valitse työtilaus > työtilauksen työ, johon haluat lisätä liitteen.
    - Vaihtoehtoisesti voit valita myös aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.

4. Valitse **Liitteet** **Työtilauksen työn tiedot** -sivulla.

5. Näkyvissä on työtilauksen työssä jo olevat liitteet. Valitse **Lisää liite**.

6. Anna liitteelle **nimi** ja lisää **huomautukset**.

7. Valitse kuva mobiililaitteen kuvista valitsemalla **Valitse kuva** tai ota kuva valitsemalla **Ota kuva**.

8. Valitse **Valmis**.

![Kuva 4](media/am-mobile-04.png)


## <a name="view-maintenance-checklist-on-a-work-order-job"></a>Työtilauksen työn ylläpidon tarkistuslistan tarkasteleminen

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

2. Valitse **Kaikki ylläpidon työtilaukset**.

3. Valitse työtilaus > työtilauksen työ, jonka tarkistusluetteloita haluat tarkastella.
    - Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.

4. Valitse **Tarkistusluettelot** **Työtilauksen työn tiedot** -sivulla.

5. Näkyviin tulee luettelo työtilauksen työhön liittyviä tarkistusluettelon rivejä. Avaa **Ohjeet** valitsemalla tarkistusluettelossa rivi ja lisää **Huomautukset**.

6. Palaa edelliselle sivulle valitsemalla Edellinen (**<**) -painike.

![Kuva 5](media/am-mobile-05.png)


## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Resurssilaskurien näyttäminen ja päivittäminen työtilauksen työssä

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

2. Valitse **Kaikki ylläpidon työtilaukset**.

3. Valitse työtilaus > työtilauksen työ, jonka resurssilaskureita haluat tarkastella.
    - Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.

4. Valitse **Resurssilaskurit** **Työtilauksen työn tiedot** -sivulla.

5. Näkyviin tulee luettelo työtilauksen työhön liittyviä resurssilaskureita. Päivitä laskurin arvo valitsemalla kynäkuvake resurssilaskurin rivillä.

6. Anna laskurin uusi arvo ja valitse **Valmis**.

![Kuva 6](media/am-mobile-06.png)


## <a name="register-consumption-on-a-work-order-job"></a>Kulutuksen rekisteröinti työtilaus työssä

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

2. Valitse **Kaikki ylläpidon työtilaukset**.

3. Valitse työtilaus > työtilauksen työ, johon haluat lisätä kulutuksen rekisteröintejä.
    - Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.

4. Valitse **Kirjauskansiot** **Työtilauksen työn tiedot** -sivulla.

5. Luo työtunnin rekisteröinnit valitsemalla **Lisää tunnit**.
    1. Valitse haussa **Luokka**.
    2. Anna **Tunnit**-kenttään työtilauksen työhön käytetyt työtunnit.
    3. Valitse sopiva **Rivin ominaisuus**.
    4. Valitse **Valmis**.

6. Luo nimikerekisteröinnit valitsemalla **Lisää nimikkeitä**.
    1. Valitse haussa **Nimiketunnus**.
    2. Valitse haussa **Toimipaikka**.
    3. Anna kulutettujen nimikkeiden **Määrä**.
    4. Valitse **Valmis**.

7. Luo kulurekisteröinnit valitsemalla **Lisää kulu**.
    1. Valitse haussa **Luokka**.
    2. Anna kulurekisteröintien määrä.
    3. Valitse haussa **Myyntivaluutta**.
    4. Anna kulurekisteröintien **Kustannushinta**.
    5. Valitse **Valmis**.

![Kuva 7](media/am-mobile-07.png)


## <a name="update-lifecycle-state-on-a-work-order"></a>Työtilauksen elinkaaren tilan päivittäminen

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

2. Valitse **Kaikki ylläpidon työtilaukset**.

3. Valitse työtilaus, jonka elinkaaren tilan haluat päivittää.

4. Valitse **Päivitä tila** -painike näytön alareunassa.

5. Valitse luettelossa uusi elinkaaren tila.

6. Valitse **Valmis**.

![Kuva 8](media/am-mobile-08.png)


## <a name="create-a-maintenance-request"></a>Luo ylläpitopyyntö

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

2. Valitse **Kaikki ylläpitopyynnöt**.

3. Valitse näytön alareunassa ensin **Toiminnot** ja sitten **Luo ylläpitopyyntö**.

4. Jos huoltopyyntöjen numerosarja otetaan käyttöön **resurssin hallinnassa**, **Ylläpitopyyntö**-kenttä piilotetaan, koska se täytetään automaattisesti. Jos **Ylläpitopyyntö**-kenttä on näkyvissä, anna ylläpitopyynnön tunnus.

5. Valitse **Ylläpitopyynnön tyyppi**.

6. Lisää ylläpitopyynnön **Kuvaus**.

7. Valitse **Resurssi**, jolle pyyntö luodaan.

8. Valitse ylläpitopyynnön **Palvelutaso**.

9. Valitse **Valmis**.

![Kuva 9](media/am-mobile-09.png)


## <a name="add-attachment-to-a-maintenance-request"></a>Liitteen lisääminen ylläpitopyyntöön

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

2. Valitse **Kaikki ylläpitopyynnöt**.

3. Valitse ylläpitopyyntö, johon liite lisätään.

4. Valitse **Liitteet** näytön alareunassa.

5. Valitse **Lisää liitteet**.

6. Anna liitteelle **nimi** ja lisää **huomautukset**.

7. Valitse kuva mobiililaitteen kuvista valitsemalla **Valitse kuva** tai ota kuva valitsemalla **Ota kuva**.

8. Valitse **Valmis**.

![Kuva 10](media/am-mobile-10.png)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]