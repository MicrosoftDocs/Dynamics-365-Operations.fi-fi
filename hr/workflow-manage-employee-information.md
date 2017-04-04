---
title: "Työnkulkujen avulla voit hallita työntekijätiedot"
description: "Tässä ohjeaiheessa kerrotaan, miten voit henkilöstöhallinnon työnkulun kyvyn hallita työntekijöiden tietoja. Voit liittää toimeen työnkulun ja hyväksynnän työnkulku, joka käynnistetään, kun työntekijät muuttavat niiden tietueen määrittäminen."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Työnkulkujen avulla voit hallita työntekijätiedot

Tässä ohjeaiheessa kerrotaan, miten voit henkilöstöhallinnon työnkulun kyvyn hallita työntekijöiden tietoja. Voit liittää toimeen työnkulun ja hyväksynnän työnkulku, joka käynnistetään, kun työntekijät muuttavat niiden tietueen määrittäminen.

Henkilöstöhallinnon työnkulun-ominaisuus sisältää useita työnkulkuja henkilöstöhallinnon tehtävät hallinnalle. Lisäksi lukuisat vaihtoehdot ovat käytettävissä, jotta voit muokata tietyn työnkulkuja ja kytkeä raportointihierarkian. Työnkulut ovat käytettävissä vakiotyyppisiä työntekijätiedot muutosten hallintaan. Työnkulku voi liittää toimeen. Tämän jälkeen työntekijät muuttaa niiden työntekijätietuetta, jos työnkulku on aloitettu, joka edellyttää hyväksyntää, ennen kuin uusia tietoja on tallennettu. Työnkulut ovat valmiiksi määritettyjä seuraavantyyppisiä tietoja, joiden avulla voit tehokkaasti hallita muutoksia ja säilyttää työntekijöiden tiedot tarkasti:

-   Tunnusnumerot
-   Kurssit
-   Koulutus
-   Kuva
-   Lainatut nimikkeet
-   Ammattikokemus
-   Projektikokemus
-   Osaamisalueet
-   Luottamustoimet
-   Henkilöstöhallinnon toiminnot
-   Kurssille ilmoittautuminen

Kun työntekijät palkataan, siirretty tai lopetettu, työnkulku voi sisältää tarkistusprosessia. Tällä tavalla voit tarkistaa asiakirjan tai osana työnkulku voidaan määrittää toiminnon käyttöehdot. Kun tarkistus on valmis, asiakirja tai toiminto on valmis ja viimeinen hyväksyntävaihe siirtyy työnkulun.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Liitä työnkulku toimihierarkia
Voit liittää minkä tahansa hierarkian, jonka määrittää työnkulun. Esimerkiksi jos toimeen liittyvää raportointia hierarkia matriisi, voit määrittää työnkulun, joka reitittää kulut tiettyyn projektiin projektin liidin sen sijaan, että työntekijä, joka liittyy kyseisen toimen johtaja. Voit luoda uuden työnkulun tai muokata aiemmin luotu työnkulku **henkilöstöhallinnon työnkulun** -sivulla **uusi**. Valitse luettelosta voit käynnistää työnkulun suunnitteluikkunassa työnkulun. Voit luoda uuden työnkulun tai muuttaa aiemmin luodun työnkulun vaiheet suunnittelija. Kun muutat aiemmin luotu työnkulku, muutokset tallennetaan uutena versiona. Siksi voit aina palata edelliseen versioon Jos haluat.

## <a name="configure-a-human-resources-workflow"></a>Henkilöstöhallinnon työnkulun määrittäminen
Määrittää perus työnkulun, joka käynnistyy, kun työntekijät pyytää muutoksia heidän henkilökohtaiset tunnistetiedot, toimi seuraavasti.

1.  - **Henkilöstöhallinnon työnkulkuja** -sivulla **uusi**.
2.  Valitse-luettelosta käytettävissä olevat työnkulut **tunnuslukujen**.
3.  Valitse **suorittaa** voit käynnistää työnkulun suunnitteluikkunassa ja kirjoita käyttäjänimi ja salasana, kun sinua pyydetään.
4.  Vedä **Hyväksy tunnusnumero** elementin designer piirtoalustaan luettelon työnkulun elementeistä.
5.  Hyväksynnän elementti muodostaa **käynnistää** ja **loppu**.
6.  Kaksoisnapsauta **Hyväksy elementin**, ja sitten hiiren kakkospainiketta ja valitse **ominaisuudet**.
7.  Voit lisätä kohteen työohjeita seuraavasti:
    1.  Valitse **tehtävän**, ja valitse sitten **hierarkian** Valitse tehtävätyyppi.
    2.  Alla **hierarkian**, valinta **voidaan määrittää hierarkian**.
    3.  Pysäytysehdon Lisää ja sulje sivu.

8.  Täytä lisäohjeita (muita varoituksia on olemassa).
9.  Valitse **Tallenna ja sulje**. Kun valintaikkuna avautuu, ja valitse Uusi työnkulun aktivoiminen **Aktivoi**.
10. Siirry **henkilöstöhallinnon**&gt;**toimien**&gt;**sijoittaa luokkahierarkian tyypit**.
11. Valitse **matriisin**.
12. Lisää **työntekijän tunnusnumero** työnkulun luetteloon.



