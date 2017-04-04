---
title: "Kustannukset ohjaava mobiili työtilan toiminnot app for Microsoft Dynamics-365"
description: "Kustannuksella hallinta mobile workspace-center esimiehille cost voit nähdä kustannus center milloin tahansa ja missä tahansa."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Kustannukset ohjaava mobiili työtilan toiminnot app for Microsoft Dynamics-365

Kustannuksella hallinta mobile workspace-center esimiehille cost voit nähdä kustannus center milloin tahansa ja missä tahansa. 

<a name="prerequisites"></a>Edellytykset
-------------

| Edellytys                                                         | kuvaus                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lue Microsoft Dynamics-365 toimintojen mobiilien | [Toimintojen mobiilien Dynamics 365](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Työvaiheiden Dynamics 365                                          | Muista, että käytät ympäristössä, jossa on Microsoft Dynamics-365-version toimintoja 1611 ja päivittää toimia ympäristön Microsoft Dynamics 3 (marraskuu-2016). |
| Hotfix-korjauksen kt 3215650                                                    | Asentaa korjaustiedoston käyttöön työtilat, jotka toimitetaan Microsoft Dynamics-365 operaatioille.                                                                       |
| Kannettava laite, joka on asennettu toiminnot app for Dynamics-365 | Lataa mobile app myymälä toiminnot app for Dynamics-365.                                                                                                      |

## <a name="introduction"></a>Johdanto
Kustannusten hallinta mobile workspace sisältää nykyisen suorituskyvyn kustannuspaikkojen instant tutkimuksen vertaamalla toteutuneita kustannuksia budjetoituihin kustannuksiin vastaan. Voit siirtyä yksittäisten kustannuselementeistä tilat.

### <a name="example"></a>Esimerkki

Työntekijä saa kutsun kansainvälinen konferenssi. Organisaation on katettava kaikki matkakulut. Työntekijä kysyy hänen hallinta, hän voi osallistua kokoukseen. Esimiehen tulee nopeasti hänen Matkapuhelin mobiili työtilan hallinta kustannukset nähdä, onko hän talousarvion työntekijän osallistumaan kokoukseen.

### <a name="data-security"></a>Tietoturva

Kustannusten hallinta-työtilan tiedot suojataan käyttäjän tunnistetietojen mukaan. Kustannus center johtaja on sallittu vain Nähdäksesi tiedot omaan kustannuspaikka. Access Tietuetason tietoturva on hallittu Kustannuslaskenta-moduulin. Kustannukset kirjanpitäjät määrittää kustannukset mobile workspace Kustannuslaskenta-moduulin kokoonpanon hallinta. Työtilan toiminnot app for Microsoft Dynamics-365 julkaistaan, kun on käytettävissä toimintojen mobile app for Dynamics-365. Näin varmistetaan kaikkien kustannusten center johtajat organisaation katsomalla tiedot samassa muodossa.

### <a name="actions-views-and-links"></a>Toiminnot, näkymiä ja linkit

Kustannusten hallinta toimintojen app for mobile workspace Dynamics 365, sisältää seuraavat toimet, näkymät ja linkkejä:

-   Toimet 
    -   Valitse **kokoonpanot** voidaan valita asettelun.
    -   Valitse **kustannus-objektien** Valitse kustannuspaikat, jotka haluat suodattaa tiedot. **Huomautus:** -Kustannuslaskenta-moduulin käyttöoikeuden näytetään luettelossa.

<!-- -->

-   Mukaan, mitä on valittu **toimintojen** ja mitä on määritetty Kustannuslaskenta-moduulin, voit tarkastella seuraavia tietoja korteille. Huomaa, että summa tulee näkyviin samassa muodossa: Todellinen, budjetti, varianssi ja varianssi %. 
    -   Todellinen vs. budjetti (nykyhetkeen)
    -   Todellinen vs. muokattu budjetti (nykyhetkeen)
    -   Todellinen vs. budjetti (edelliseltä kaudelta)
    -   Todellinen vs. muokattu budjetti (edelliseltä kaudelta)
    -   Todellinen vs. budjetti (vuoden alusta)
    -   Todellinen vs. muokattu budjetti (vuoden alusta)

<!-- -->

-   Linkit
    -   Nykyisen jakson tiedot.
    -   Edellisen jakson tiedot.
    -   Kuluva vuosi tietoja.

Kun valitset linkkejä, Kustannustekijä per kortti tulee näkyviin. Korttien summa näkyy seuraavassa muodossa: Todellinen, budjetti, budjetin varianssin, vaihtelu % budjetin, muokattu budjetin, muokattu budjetin varianssin ja muokattu budjetin varianssin %.  [![kustannusten hallinta](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Aloittaminen
Matkaviestimen käytön kustannusten hallinta mobile app seuraavasti.

1.  Mobile app-myymälä, lataa ja asenna toiminnot app for Microsoft Dynamics-365.
2.  Käynnistä sovellus laitteen.
3.  Anna URL-osoitteesi Dynamics 365.
4.  Kirjoita Kirjaudu yritys. Esimerkiksi **USMF**.
5.  Ensimmäinen kerta, kun kirjaudut sisään, sinua pyydetään käyttäjänimeä ja salasanaa Microsoft Dynamics-365, tilin toimintoja varten. Anna tunnistetietosi. Kun kirjaudut sisään, näet yrityksen käytettävissä olevat työtilat.

Voit tarkastella mobiili sovellusten työtilat, haluttu työtilat on ensin julkaistava toiminnot app for Dynamics-365.

1.  Käynnistä Dynamics 365 operaatioille.
2.  Siirry **järjestelmän hallinta**&gt;**asennus**&gt;**järjestelmäparametrit**.
3.  Valitse **hallinta mobile app**.
4.  Valitse työtila ** kustannusten hallinta ** julkaista mobile platform.
5.  Valitse **julkaista työtilan**.
6.  Päivitä laitteesi on julkaistu työtilat.

## <a name="view-the-performance-of-your-cost-center"></a>Että kustannuspaikan suorituskyvyn tarkasteleminen
1.  Matkaviestimessä, valitse **kustannusten hallinta** työtila.
2.  Valitse **kustannusten objektin hallinta**.
3.  Valitse **toimintojen**.
4.  Valitse **Select configuration** voit valita asettelun hallinta kustannukset.
5.  Click **Done**.
6.  Valitse **toimintojen**.
7.  Valitse **Valitse kustannuskohde** Valitse kustannuspaikat, johon sinulla on oikeus käyttää.
8.  Click **Done**.
9.  Näytä kustannus-center yleistä suorituskykyä.
10. Valitse **tiedot valitun kauden**.
11. Näytä kustannukset yksittäisten osien suorituskykyä.
12. Voit myös etsiä tietyn kustannuselementeistä.



