---
title: Resurssien hallinnan mobiilityötilan käyttäminen
description: Tässä ohjeaiheessa on tietoja resurssien hallinnan mobiilityötilasta.
author: josaw1
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: afda807714f14efb1cbab4ecfdd273aac52f4558
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033149"
---
# <a name="use-the-asset-management-mobile-workspace"></a>Resurssien hallinnan mobiilityötilan käyttäminen

[!include [banner](../../includes/banner.md)]

Tässä aiheessa on tietoja **resurssien hallinnan** mobiilityötilasta. Tämä työtila antaa käyttäjien tarkastella ja luoda ylläpitopyyntöjä ja työtilauksia. Käyttäjät voivat myös tarkastella määritettyjä työtilaustöitä kalenteri- tai luettelonäkymässä. Myös käyttökohteita ja toiminnallisia sijainteja voidaan tarkastella ja etsiä.

## <a name="overview"></a>Yleiskuvaus

Resurssien hallinta on kehittynyt moduuli resurssien ja työtilausten hallintaan Dynamics 365 Supply Chain Managementissa. **Resurssien hallinnan** mobiilityötilassa käyttäjät voivat nopeasti tarkastella heille määritettyjä työtilaustöitä valitsemassaan mobiililaitteessa. Käyttäjät voivat myös luoda ja hallita ylläpitopyyntöjä, päivittää elinkaaren tilan sekä tarkastella resurssien ja toiminnallisen sijainnin tietoja omassa mobiililaitteeseen.

Käyttäjät voivat tehdä **resurssien hallinnan** mobiilityötilassa seuraavat tehtävät:

- Ylläpitopyyntöjen luonti, tarkastelu ja muokkaaminen, valokuvan ottaminen tai aiemmin otetun kuvan liittäminen ylläpitopyyntöön ja ylläpitopyynnön elinkaaren tilan muuttaminen. 
- Työtilausten luonti, tarkastelu ja muokkaaminen, valokuvan ottaminen tai aiemmin otetun kuvan liittäminen työtilaukseen, työtilauksen elinkaaren tilan muuttaminen ja työtilauksen töiden tarkastelu.
- Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä.
- Työtilauksen työn luonti, tarkastelu ja muokkaus, resurssilaskurien päivitys, ylläpidon tarkastuslistan tarkastelu, työtilauksen työn huomausten tarkastelu ja muokkaus sekä työtilauksen työssä tarvittavien työkalujen tarkastelu.
- Tietyn resurssin tai toiminnallisen sijainnin tarkastelu tai haku.

## <a name="prerequisites"></a>Edellytykset

**Resurssien hallinnan** mobiilityötilaa ei voi käyttää, ennen kuin järjestelmänvalvoja on määrittävät tarvittavat käyttäjä- ja työntekijätilit sekä julkaissut työtilan. Lisätietoja on kohdassa [Resurssien hallinnan mobiilityötilan määrittäminen](set-up-asset-management-mobile.md).

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen

Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:

- [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
- [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen

1. Käynnistä sovellus mobiililaitteessa.

1. Anna Dynamics 365 -URL-osoitteesi.

1. Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.

1. Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

    ![Työtilan valitseminen](media/am-mobile-01.png "Työtilan valitseminen")

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

1. Valitse **Oman työtilauksen töiden kalenteri**.

1. Valitse päivämäärä, jona haluat tarkastella työtilauksen töitä. Luettelossa on näkyvissä kunkin työtilauksen työn resurssin tunnus ja toiminnallisen sijainnin tunnus.

1. Saat työn tiedot näkyviin valitsemalla työtilauksen työn luettelossa: resurssin ja toiminnallisen sijainnin tiedot sekä muut siirtymislinkit, joilla voi avata seuraavat kohdat: **Liitteet**, **Tarkistusluettelot**, **Työkalut**, **Resurssilaskurit**, **Huomautukset** ja **Kirjauskansiot**.

    ![Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä](media/am-mobile-02.png "Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä")

## <a name="create-a-work-order-job"></a>Työtilauksen työn luominen

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

1. Valitse **Kaikki ylläpidon työtilaukset**.

1. Valitse työtilaus, jolle haluat luoda uuden työtilauksen.

1. Valitse **Lisää rivi** -painike.

1. Valitse **Resurssi**, jolle haluat luoda työtilauksen.

1. Valitse **Ylläpitotyön tyyppi**, **Ylläpitotyön tyypin variantti** ja **Toimiala**.

1. Valitse **Valmis**.

    ![Rivin lisäysnäyttö](media/am-mobile-03.png "Rivin lisäysnäyttö")


## <a name="add-attachment-to-a-work-order-job"></a>Liitteen lisääminen työtilauksen työhön

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

1. Valitse **Kaikki ylläpidon työtilaukset**.

1. Valitse työtilaus > työtilauksen työ, johon haluat lisätä liitteen.
    - Vaihtoehtoisesti voit valita myös aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.

1. Valitse **Liitteet** **Työtilauksen työn tiedot** -sivulla.

1. Näkyvissä on työtilauksen työssä jo olevat liitteet. Valitse **Lisää liite**.

1. Anna liitteelle **nimi** ja lisää **huomautukset**.

1. Valitse kuva mobiililaitteen kuvista valitsemalla **Valitse kuva** tai ota kuva valitsemalla **Ota kuva**.

1. Valitse **Valmis**.

    ![Työtilauksen työn liitteiden näyttäminen ja lisääminen](media/am-mobile-04.png "Työtilauksen työn liitteiden näyttäminen ja lisääminen")

## <a name="view-maintenance-checklist-on-a-work-order-job"></a>Työtilauksen työn ylläpidon tarkistuslistan tarkasteleminen

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

1. Valitse **Kaikki ylläpidon työtilaukset**.

1. Valitse työtilaus > työtilauksen työ, jonka tarkistusluetteloita haluat tarkastella.
    - Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.

1. Valitse **Tarkistusluettelot** **Työtilauksen työn tiedot** -sivulla.

1. Näkyviin tulee luettelo työtilauksen työhön liittyviä tarkistusluettelon rivejä. Avaa **Ohjeet** valitsemalla tarkistusluettelossa rivi ja lisää **Huomautukset**.

1. Palaa edelliselle sivulle valitsemalla Edellinen (**<**) -painike.

    ![Ylläpidon tarkistuslista ja rivin tiedot](media/am-mobile-05.png "Ylläpidon tarkistuslista ja rivin tiedot")

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Resurssilaskurien näyttäminen ja päivittäminen työtilauksen työssä

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

1. Valitse **Kaikki ylläpidon työtilaukset**.

1. Valitse työtilaus > työtilauksen työ, jonka resurssilaskureita haluat tarkastella.
    - Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.

1. Valitse **Resurssilaskurit** **Työtilauksen työn tiedot** -sivulla.

1. Näkyviin tulee luettelo työtilauksen työhön liittyviä resurssilaskureita. Päivitä laskurin arvo valitsemalla kynäkuvake resurssilaskurin rivillä.

1. Anna laskurin uusi arvo ja valitse **Valmis**.

    ![Resurssilaskureiden näyttäminen ja päivittäminen](media/am-mobile-06.png "Resurssilaskureiden näyttäminen ja päivittäminen")

## <a name="register-consumption-on-a-work-order-job"></a>Kulutuksen rekisteröinti työtilaus työssä

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

1. Valitse **Kaikki ylläpidon työtilaukset**.

1. Valitse työtilaus > työtilauksen työ, johon kulutuksen rekisteröinnit halutaan lisätä.
    - Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.

1. Valitse **Kirjauskansiot** **Työtilauksen työn tiedot** -sivulla.

1. Luo työtunnin rekisteröinnit valitsemalla **Lisää tunnit**.
    1. Valitse haussa **Luokka**.
    1. Anna **Tunnit**-kenttään työtilauksen työhön käytetyt työtunnit.
    1. Valitse sopiva **Rivin ominaisuus**.
    1. Valitse **Valmis**.

1. Luo nimikerekisteröinnit valitsemalla **Lisää nimikkeitä**.
    1. Valitse haussa **Nimiketunnus**.
    1. Valitse haussa **Toimipaikka**.
    1. Anna kulutettujen nimikkeiden **Määrä**.
    1. Valitse **Valmis**.

1. Luo kulurekisteröinnit valitsemalla **Lisää kulu**.
    1. Valitse haussa **Luokka**.
    1. Anna kulurekisteröintien määrä.
    1. Valitse haussa **Myyntivaluutta**.
    1. Anna kulurekisteröintien **Kustannushinta**.
    1. Valitse **Valmis**.

    ![Työtilauksen kirjauskansion päivittäminen](media/am-mobile-07.png "Työtilauksen kirjauskansion päivittäminen")

## <a name="update-lifecycle-state-on-a-work-order"></a>Työtilauksen elinkaaren tilan päivittäminen

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

1. Valitse **Kaikki ylläpidon työtilaukset**.

1. Valitse työtilaus, jonka elinkaaren tilan haluat päivittää.

1. Valitse **Päivitä tila** -painike näytön alareunassa.

1. Valitse luettelossa uusi elinkaaren tila.

1. Valitse **Valmis**.

    ![Työtilauksen elinkaaren tilan päivittäminen](media/am-mobile-08.png "Työtilauksen elinkaaren tilan päivittäminen")

## <a name="create-a-maintenance-request"></a>Luo ylläpitopyyntö

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

1. Valitse **Kaikki ylläpitopyynnöt**.

1. Valitse näytön alareunassa ensin **Toiminnot** ja sitten **Luo ylläpitopyyntö**.

1. Jos huoltopyyntöjen numerosarja otetaan käyttöön **resurssin hallinnassa**, **Ylläpitopyyntö**-kenttä piilotetaan, koska se täytetään automaattisesti. Jos **Ylläpitopyyntö**-kenttä on näkyvissä, anna ylläpitopyynnön tunnus.

1. Valitse **Ylläpitopyynnön tyyppi**.

1. Lisää ylläpitopyynnön **Kuvaus**.

1. Valitse **Resurssi**, jolle pyyntö luodaan.

1. Valitse ylläpitopyynnön **Palvelutaso**.

1. Valitse **Valmis**.

    ![Luo ylläpitopyyntö](media/am-mobile-09.png "Luo ylläpitopyyntö")

## <a name="add-attachment-to-a-maintenance-request"></a>Liitteen lisääminen ylläpitopyyntöön

1. Avaa **Resurssien hallinta** -työtila mobiililaitteessa.

1. Valitse **Kaikki ylläpitopyynnöt**.

1. Valitse ylläpitopyyntö, johon liite lisätään.

1. Valitse **Liitteet** näytön alareunassa.

1. Valitse **Lisää liitteet**.

1. Anna liitteelle **nimi** ja lisää **huomautukset**.

1. Valitse kuva mobiililaitteen kuvista valitsemalla **Valitse kuva** tai ota kuva valitsemalla **Ota kuva**.

1. Valitse **Valmis**.

    ![Liitteen lisääminen ylläpitopyyntöön](media/am-mobile-10.png "Liitteen lisääminen ylläpitopyyntöön")
