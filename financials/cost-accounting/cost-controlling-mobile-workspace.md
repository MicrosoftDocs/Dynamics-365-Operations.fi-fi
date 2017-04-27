---
title: "Kustannusseurannan mobiilityötila Microsoft Dynamics 365 for Operations -sovellusta varten"
description: "Kustannusten hallinnan mobiilityötilan avulla kustannuspaikan päälliköt näkevät kustannuspaikan suorituskyvyn missä tahansa ja milloin tahansa."
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

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Kustannusseurannan mobiilityötila Microsoft Dynamics 365 for Operations -sovellusta varten

Kustannusten hallinnan mobiilityötilan avulla kustannuspaikan päälliköt näkevät kustannuspaikan suorituskyvyn missä tahansa ja milloin tahansa. 

<a name="prerequisites"></a>Edellytykset
-------------

| Edellytys                                                         | kuvaus                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lue Microsoft Dynamics 365 for Operations -mobiiliympäristöstä | [Dynamics 365 for Operations -mobiiliympäristö](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Varmista, että käytössäsi on ympäristö, johon on asennettu Microsoft Dynamics 365 for Operations -versio 1611 sekä Microsoft Dynamics for Operations ympäristöpäivitys 3 (Marraskuu 2016). |
| Hotfix-korjaus KB 3215650                                                    | Asenna korjaustiedosto ottaaksesi käyttöön työtilat, jotka toimitetaan Microsoft Dynamics 365 for Operationsissa.                                                                       |
| Mobiililaite, johon on asennettu Dynamics 365 for Operations -sovellus | Lataa mobiilisovelluskaupasta Microsoft Dynamics 365 for Operations -sovellus.                                                                                                      |

## <a name="introduction"></a>Johdanto
Kustannusten hallinnan mobiilityötila sisältää kustannuspaikkojen nykyisen suorituskyvyn välittömän näkymän vertaamalla toteutuneita kustannuksia budjetoituihin kustannuksiin. Voit porautua yksittäisten kustannuselementtien tiloihin.

### <a name="example"></a>Esimerkki

Työntekijä saa kutsun kansainväliseen konferenssiin. Organisaation on katettava kaikki matkakulut. Työntekijä kysyy esimieheltään, voiko hän osallistua kokoukseen. Esimies avaa nopeasti kustannuslaskennan mobiilityötilan puhelimessaan nähdäkseen, onko budjetissa varaa työntekijän osallistumiseen kokoukseen.

### <a name="data-security"></a>Tietoturva

Kustannusten hallinnan työtilan tiedot suojataan käyttäjän tunnistetietojen mukaan. Kustannuspaikan johtajan on sallittu nähdä vain tiedot omasta kustannuspaikastaan. Käyttöoikeustason tietoturva on hallittu Kustannuslaskenta-moduulissa. Kustannusten kirjanpitäjät määrittävät kustannusseurannan mobiilityötilan Kustannuslaskenta-moduulissa. Kun työtila on julkaistu Microsoft Dynamics 365 for Operations -sovellukseen, se on saatavissa Dynamics 365 for Operations -mobiilisovelluksessa. Näin varmistetaan, että kaikkien kustannuspaikkojen johtajat organisaatiossa näkevät tiedot samassa muodossa.

### <a name="actions-views-and-links"></a>Toiminnot, näkymät ja linkit

Kustannusten hallinnan Dynamics 365 for Operations -mobiilityötila tarjoaa seuraavat toiminnot, näkymät ja linkit:

-   Toimet 
    -   Valitse **Konfiguroinnit** valitaksesi asettelun.
    -   Valitse **Kustannusobjektit** valitaksesi kustannuspaikat, joiden tiedot haluat suodattaa. **Huomautus:** Luettelo näytetään Kustannuslaskenta-moduulissa määritettyjen käyttöoikeuksien mukaan.

<!-- -->

-   Sen mukaan, mitä on valittu **Toiminnot**-kohdassa ja mitä on määritetty Kustannuslaskenta-moduulissa, voit tarkastella seuraavia tietoja korteissa. Huomaa, että summa tulee näkyviin samassa muodossa: Todellinen, budjetti, varianssi ja varianssi %. 
    -   Todellinen vs. budjetti (nykyinen kausi)
    -   Todellinen vs tarkistettu budjetti (nykyinen kausi)
    -   Todellinen vs. budjetti (edellinen kausi)
    -   Todellinen vs tarkistettu budjetti (edellinen kausi)
    -   Todellinen vs. budjetti (vuoden alusta)
    -   Todellinen vs tarkistettu budjetti (vuoden alusta)

<!-- -->

-   Linkit
    -   Kuluvan kauden tiedot.
    -   Edellisen kauden tiedot.
    -   Kuluvan vuoden tiedot.

Kun valitset linkkejä, Kustannustekijä per kortti tulee näkyviin. Korttien summa näkyy seuraavassa muodossa: Todellinen, budjetti, budjetin varianssi, budjetin varianssi %, muokattu budjetti, muokattu budjetin varianssi ja muokattu budjetin varianssi %.  [![cost-controlling](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Aloittaminen
Aloita kustannuslaskennan mobiilisovelluksen käyttö mobiililaitteellasi seuraamalla näitä ohjeita.

1.  Lataa mobiilisovelluskaupasta Microsoft Dynamics 365 for Operations -sovellus.
2.  Käynnistä sovellus laitteessa.
3.  Anna Dynamics 365 -URL-osoitteesi.
4.  annan yritys, johon kirjaudutaan. Kirjoita esimerkiksi **USMF**.
5.  Ensimmäinen kerta, kun kirjaudut sisään, sinulta pyydetään Microsoft Dynamics 365 for Operations -tilisi käyttäjänimeä ja salasanaa. Kirjota tunnistetiedot. Kun olet kirjautunut sisään, näet yrityksen käytettävissä olevat työtilat.

Jotta voit tarkastella mobiilisovelluksessa työtiloja, halutut työtilat on ensin julkaistava Dynamics 365 for Operationsiin.

1.  Käynnistä Dynamics 365 for Operations.
2.  Valitse **Järjestelmän hallinta** &gt; **Asetukset** &gt; **järjestelmän parametrit**.
3.  Valitse **Hallitse mobiilisovellusta**.
4.  Valitse työtila ** Kustannusten hallinta **julkaistaksesi mobiiliympäristöön.
5.  Valitse **Julkaise työtila**.
6.  Päivitä laitteesi nähdäksesi julkaistut työtilat.

## <a name="view-the-performance-of-your-cost-center"></a>Kustannuspaikan suorituskyvyn tarkasteleminen
1.  Valitse mobiililaitteessasi **Kustannusten hallinta** -työtila.
2.  Valitse **Kustannusobjektin hallinta**.
3.  Valitse **Toimenpiteet**.
4.  Valitse **Valitse konfigurointi** valitaksesi kustannusten hallinnan asettelun.
5.  Valitse **Valmis**.
6.  Valitse **Toimenpiteet**.
7.  Valitse **Valitse kustannusobjekti** valitaksesi kustannuspaikat, joihin sinulla on käyttöoikeus.
8.  Valitse **Valmis**.
9.  Kustannuspaikan yleisen suorituskyvyn tarkasteleminen.
10. Valitse **Kuluvan kauden tiedot**.
11. Yksittäisten kustannuselementtien suorituskyvyn tarkasteleminen.
12. Voit myös etsiä tiettyjä kustannuselementtejä.



