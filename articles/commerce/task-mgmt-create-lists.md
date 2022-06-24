---
title: Tehtäväluetteloiden luominen ja tehtävien lisääminen
description: Tässä artikkelissa kerrotaan, miten tehtäväluettelot luodaan ja miten niihin lisätään tehtäviä Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a299be239d911e4605ed26625a313c93bd3020b8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881628"
---
# <a name="create-task-lists-and-add-tasks"></a>Tehtäväluetteloiden luominen ja tehtävien lisääminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten tehtäväluettelot luodaan ja miten niihin lisätään tehtäviä Microsoft Dynamics 365 Commerce -sovelluksessa.

*Tehtävä* määrittää tietyn työn tai toiminnon, joka on suoritettava tiettynä eräpäivänä tai ennen sitä. Dynamics 365 Commerce -sovelluksessa tehtävä voi sisältää eriteltyjä ohjeita ja tietoja yhteyshenkilöstä. Se voi sisältää myös linkkejä taustatoimintoihin, myyntipistetoimintoihin tai sivuston sivuihin. Tämä auttaa parantamaan tuottavuutta ja määrittämään kontekstin, jonka avulla tehtävän omistaja voi suorittaa tehtävän tehokkaasti.

*Tehtäväluettelo* on kokoelma tehtäviä, jotka on suoritettava liiketoimintaprosessin osana. Tehtäväluettelo voi olla esimerkiksi uudelle työntekijälle, jonka on suoritettava tehtävät perehdytyksen aikana, kassanhoitajalle, joka työskentelee iltavuoroissa tai tulevan lomakauden valmistelua varten. Commercessa kaikki tehtäväluettelot, joilla on tavoitepäivämäärä, voidaan määrittää halutulle määrälle myymälöitä tai työntekijöitä. Ne voidaan määrittää myös toistuviksi.

Sekä päälliköt että työntekijät voivat luoda tehtäväluetteloita Commercen taustatoiminnoissa ja määrittää ne tämän jälkeen myymäläjoukoille.

## <a name="create-a-task-list"></a>Tehtäväluettelon luominen

Voit luoda tehtäväluettelon seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.
1. Valitse **Uusi** ja anna arvot **Nimi**-, **Kuvaus** -ja **Omistaja**-kenttiin.
1. Valitse **Tallenna**.

## <a name="add-tasks-to-a-task-list"></a>Tehtävien lisääminen tehtäväluetteloon

Voit lisätä tehtäviä tehtäväluetteloon seuraavasti.
 
1. Lisää tehtävä valitsemalla olemassa olevan tehtäväluettelon **Tehtävät**-pikavälilehdessä **Uusi**.
1. Anna tehtävän nimi **Luo uusi tehtävä** -valintaikkunan **Nimi**-kenttään.
1. Anna positiivinen tai negatiivinen kokonaisluku **Eräpäivän vastakirjaus tavoitepvm:stä** -kenttään. Anna esimerkiksi **-2**, jos tehtävä on suoritettava kaksi päivää ennen tehtäväluettelon eräpäivää.
1. Anna **Huomautukset**-kenttään yksityiskohtaiset ohjeet.
1. Anna **Yhteyshenkilö**-kenttään sen aihepiirin asiantuntijan nimi, johon tehtävän omistaja voi ottaa yhteyttä tarvittaessa.
1. Anna **Tehtävän linkki** -kenttään linkki, joka perustuu tehtävän luonteeseen.

> [!TIP]
> Vaikka voit käyttää **Määritetty henkilölle** -kenttää, jos haluat määrittää tehtäviä jollekin tehtäväluettelon luomisen yhteydessä, on suositeltavaa välttää tehtävien määrittämistä tehtäväluettelon luomisen yhteydessä. Sen sijaan tehtävät kannattaa määrittää sen jälkeen, kun luettelo on luotu yksittäisille myymälöille.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Työntekijöiden tuottavuuden parantaminen tehtävälinkkien avulla

Commercen avulla tehtäviä voi linkittää tiettyihin myyntipistetoimintoihin, kuten myyntiraportin suorittaminen, online-koulutusvideon tarkasteleminen uuden työntekijän ohjauksen yhteydessä tai taustatoiminnon suorittaminen. Tämä ominaisuus auttaa tehtävän omistajia hankkimaan tiedot, joita he tarvitsevat tehtävän tehokasta suorittamista varten.

Voit lisätä linkkejä tehtävää luodessasi seuraavasti.

1. Valitse olemassa olevan tehtäväluettelon **Tehtävät**-pikavälilehdessä **Muokkaa**.
1. Valitse **Muokkaa tehtävää** -valintaikkunan **Tehtävän linkki** -kentässä vähintään yksi seuraavista vaihtoehdoista:

    - Valitse **Valikkovaihtoehto**, jos haluat määrittää taustatoiminnon, kuten Tuotteen myyntirakenteet.
    - Valitse **Myyntipistetoiminto**, jos haluat määrittää myyntipistetoiminnon. Se voi olla esimerkiksi myyntiraportti.
    - Valitse **URL-osoite**, jos haluat määrittää absoluuttisen URL-osoitteen.

Seuraavassa kuvassa on tehtävän linkkien valikoima **Muokkaa tehtävää** -valintaikkunassa.

![Tehtävän linkkien valitseminen Muokkaa tehtävää -valintaikkunassa.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Myyntipistetoiminnon määrittäminen niin, että se voidaan linkittää tehtävään

Jos haluat määrittää myyntipistetoiminnon niin, että se voidaan linkittää tehtävään, noudata seuraavia vaiheita.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipiste \> Myyntipistetoiminnot**.
1. Valitse **Muokkaa**, etsi myyntipistetoiminto ja valitse sitten toiminnon **Ota tehtävienhallinta käyttöön** -valintaruutu.

## <a name="additional-resources"></a>Lisäresurssit

[Tehtävien hallinnan yleiskatsaus](task-mgmt-overview.md)

[Tehtävien hallinnan määrittäminen](task-mgmt-configure.md)

[Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille](task-mgmt-assign-lists.md)

[Tehtävien hallinta myyntipisteessä](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
