---
title: "Käytettävissä olevan varaston mobiilityötila Microsoft Dynamics 365 for Operations -sovellusta varten"
description: "Käytettävissä olevan varaston mobiilityötila auttaa syventämään näkemyksiä varatusta ja käytettävissä olevasta varastosta mobiilisti milloin tahansa ja missä tahansa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Käytettävissä olevan varaston mobiilityötila Microsoft Dynamics 365 for Operations -sovellusta varten

Käytettävissä olevan varaston mobiilityötila auttaa syventämään näkemyksiä varatusta ja käytettävissä olevasta varastosta mobiilisti milloin tahansa ja missä tahansa. 

<a name="prerequisites"></a>Edellytykset
-------------

| Edellytys                                                         | kuvaus                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lue Microsoft Dynamics 365 for Operations -mobiiliympäristöstä | [Dynamics 365 for Operations -mobiiliympäristö](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Ympäristö, johon on asennettu Microsoft Dynamics 365 for Operations -versio 1611 sekä Microsoft Dynamics for Operations ympäristöpäivitys 3 (Marraskuu 2016) |
| Hotfix-korjaus KB 3215650                                                    | Asenna korjaustiedosto ottaaksesi käyttöön työtilat, jotka toimitetaan Microsoft Dynamics 365 for Operationsissa.                                       |
| Mobiililaite, johon on asennettu Dynamics 365 for Operations -sovellus | Lataa mobiilisovelluskaupasta Microsoft Dynamics 365 for Operations -sovellus.                                                                           |

## <a name="introduction"></a>Johdanto
Yleensä yrityksillä on useita varaston toimituksia ja vastaanottoja joka päivä. Näiden siirrot muuttavat jatkuvasti käytettävissä olevan varaston tilaa. Käytettävissä olevan varaston mobiilityötilassa näet koko yrityksen käytettävissä olevan varaston tilan, jolloin voit hyödyntää uusimpia varastotietoja haluamassasi mobiililaitteessa. Riippumatta siitä, työskenteletkö fyysisessä varastossa, ostossa, myynnissä, tuotannossa, yrityksen johdossa tai muussa roolissa, voit käyttää käytettävissä olevan varaston tietoja milloin tahansa ja missä tahansa. Mobiilityötila mahdollistaa käytettävissä olevan varaston reaaliaikaisen tilan eri toimipisteissä, ja voit tarkastella käytettävissä olevaa varastoa eri toimipisteissä, nykyisiä materiaalivarauksia ja varaamatonta käytettävissä olevaa varastoa. Voit myös syöttää nimikenumeron suorittaaksesi kyselyjä käytettävissä olevaan varastoon ja suorittaa suodatetun haun varastotuotteille ja varianteille. Erityisesti mobiilityötilassa on nämä ominaisuudet:

-   Voit etsiä tuotenumerolla tai tuotteen nimellä löytääksesi tuotteita ja tarkastellaksesi niiden käytettävissä olevan varaston tilaa.
-   Voit tarkastella valittujen tuotteiden osalta seuraavia tietoja:
    -   Käytettävissä oleva varasto toimipaikan mukaan
    -   Käytettävissä oleva varasto fyysisten varastojen mukaan
    -   Käytettävissä oleva varasto sijaintien mukaan
    -   Käytettävissä oleva varasto erän mukaan (eräohjatuille tuotteille)
    -   Käytettävissä oleva varasto varastotilan mukaan

<!-- -->

-   Tuotteen varastosaldo näkyy seuraavilla tavoilla:
    -   Fyysisen varaston mukaan (tämä näkymä edustaa kokonaismäärää).
    -   Fyysisen varaston varattujen mukaan (tämä näkymä edustaa varattua määrää).
    -   Käytettävissä olevan fyysisen varaston mukaan (tämä näkymä edustaa varaamatonta käytettävissä olevaa määrää).

## <a name="get-started"></a>Aloittaminen
Voit aloittaa käytön mobiililaitteessa seuraavasti:

1.  Lataa mobiilisovelluskaupasta Microsoft Dynamics 365 for Operations -sovellus.
2.  Käynnistä sovellus laitteessa.
3.  Anna Dynamics 365 -URL-osoitteesi.
4.  annan yritys, johon kirjaudutaan. Kirjoita esimerkiksi **USMF**.
5.  Ensimmäinen kerta, kun kirjaudut sisään, sinulta pyydetään Microsoft Dynamics 365 for Operations -tilisi käyttäjänimeä ja salasanaa. Kirjota tunnistetiedot. Kun olet kirjautunut sisään, näet yrityksen käytettävissä olevat työtilat.

Jotta voit tarkastella mobiilisovelluksessa työtiloja, halutut työtilat on ensin julkaistava Dynamics 365 for Operationsiin.

1.  Käynnistä Dynamics 365 for Operations.
2.  Valitse **Järjestelmän hallinta** &gt; **Asetukset** &gt; **järjestelmän parametrit**.
3.  Valitse **Hallitse mobiilisovellusta**.
4.  Valitse työtila julkaistaksesi mobiiliympäristöön.
5.  Valitse **Julkaise työtila**.
6.  Päivitä laitteesi nähdäksesi julkaistut työtilat.

## <a name="view-the-onhand-inventory-for-a-product"></a>Näytä tuotteen käytettävissä oleva varasto
1.  Valitse mobiililaitteessasi **Käytettävissä oleva varasto** -työtila.
2.  Valitse **Tarkistaa käytettävissä oleva varasto nimikkeelle**. Näet luettelon tuotteista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta tätä määrää voi muuttaa. Lisätietoja on valmistelun käsikirjassa.
3.  Jos nimike ei ole luettelossa, valitse **Hae lisää** tehdäksesi online-haun Dynamics 365 for Operationsissa. Etsi tuotteen numeron mukaan tai vaihda hakuun tuotteen nimen mukaan.
4.  Valitse tuote. Jos nimikkeellä on kuva, kuva näkyy.
5.  Valitse jokin seuraavista vaihtoehdoista tarkastellaksesi käytettävissä olevan varaston tilaa:
    -   Näytä käytettävissä oleva varasto toimipaikan mukaan
    -   Näytä käytettävissä oleva varaston fyysisen varaston mukaan
    -   Näytä käytettävissä oleva varasto sijaintien mukaan
    -   Näytä käytettävissä oleva varasto erän mukaan (eräohjatuille tuotteille)
    -   Näytä käytettävissä oleva varasto varaston tilan mukaan

    Tuotteen varastosaldo näkyy seuraavilla tavoilla:
    -   Fyysisen varaston mukaan (tämä näkymä edustaa kokonaismäärää).
    -   Fyysisen varaston varattujen mukaan (tämä näkymä edustaa varattua määrää).
    -   Käytettävissä olevan fyysisen varaston mukaan (tämä näkymä edustaa varaamatonta käytettävissä olevaa määrää).




