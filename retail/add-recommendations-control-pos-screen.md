---
title: "Tapahtuman sivulla on POS-laitteen suositusten ohjausobjektin lisääminen"
description: "Tässä ohjeaiheessa kuvataan suosituksia ohjausobjektin lisääminen tapahtuman näytön kohtaa myynti (POS)-laitteen käyttämällä näytön asettelun suunnittelutoiminto Microsoft Dynamics-365-toimintoja varten."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Tapahtuman sivulla on POS-laitteen suositusten ohjausobjektin lisääminen

Tässä ohjeaiheessa kuvataan suosituksia ohjausobjektin lisääminen tapahtuman näytön kohtaa myynti (POS)-laitteen käyttämällä näytön asettelun suunnittelutoiminto Microsoft Dynamics-365-toimintoja varten.

Voit näyttää tuotteen suosituksia POS-laitetta käytettäessä toimintoja Microsoft Dynamics-365. *Suosituksia* kohteita asiakas mahdollisesti kiinnostuneita mukaan ostohistorian, niiden haluavansa luettelon kohteet ja kohteet, joita muut asiakkaat ostaa online- ja Tiili ja laastin kaupat. Näyttää tuotteen suosituksia, tarvitset lisää ohjausobjektin tapahtuman näytön näytön asettelun suunnittelutoiminnon avulla.

## <a name="open-layout-designer"></a>Avaa Layout suunnittelu
1.  Siirry **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS**&gt;**näytön asettelun**.
2.  Pika-suodattimen avulla voit etsiä näytön, johon haluat lisätä ohjausobjektin. Esimerkiksi suodattaa **näytön Asettelutunnus** -kentän arvo on "F2CP16:9M" avulla.
3.  Etsi haluamasi tietue luettelosta ja valitse se. Valitse esimerkiksi "nimi: F2CP16:9M näyttöasettelun tunnus: F2CP16:9M'.
4.  Valitse **asettelun suunnittelutoiminto**.
5.  Noudata asettelun suunnittelutoiminto käynnistämiseen. Tunnistetietoja kysyttäessä tunnistetietoja, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettävissä **näytön asettelun** sivulla.
6.  Kun kirjaudut, tulee sivu, joka on samanlainen kuin. Asettelu on erilainen riippuen oman myymälän tehdyt mukautukset.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Valitse Näytä-vaihtoehto
-----------------------

Kaksi asetuksista ovat käytettävissä. Valitse vaihtoehto, joka sopii parhaiten myymälä ja noudata ohjeita loppuun ohjausobjektin määrittäminen. On kaksi vaihtoehtoa:
-   Suositukset ovat aina näkyvissä.
-   A **suosituksia** välilehti näkyy oikealla puolella näytön ruudukossa.

#### <a name="to-make-recommendations-always-visible"></a>Suosituksia aina näkyvissä

1.  Pienennä sen korkeutta tapahtuman rivien tiedot alueen niin, että se on samalla korkeudella kuin asiakkaan paneelin vasemmalla puolellaan. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Vasemmanpuoleisesta valikosta vedä ja pudota suosituksia ohjausobjektin tapahtuman rivin tiedot-alueeseen – painikeruudukko-tapahtuman näytön alareunassa keskellä. Muuttaa ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan. [](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Valitse **X** Tallenna ja poistu asettelun suunnittelutoiminto.
4.  Siirry Dynamics työvaiheiden 365, **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**jakelu aikataulut**.
5.  Valitse-luettelosta **1090 Rekisteröi**.
6.  Valitse **suorittaa nyt**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Lisää painike näytön oikealla puolella olevaan ruudukkoon suositukset-välilehti

1.  Napsauta hiiren kakkospainikkeella tyhjää tilaa-sivun oikeassa reunassa sijaitseva painikeruudukon viimeisen välilehden alapuolella.
2.  Valitse **mukauttaa**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Valitse **uuden välilehden**.
4.  Etsi juuri lisäämäsi uuden välilehden. Saatat joutua vierittämään näyttöä alaspäin.
5.  - **Sisältö** avautuva, valitse **suositellaan tuotteita**. [![PIC-6](./media/pic-6.png)](./media/pic-6.png)
6.  - **Nimi** suositukset-välilehden nimi-kenttään. Kirjoita esimerkiksi 'Suositellut tuotteet'.
7.  - **Kuvan** Valitse kuva-välilehden-kenttään.
8.  Click **OK**. Painikeruudukon tulee uusi välilehti.
9.  Valitse **X** Tallenna ja poistu asettelun suunnittelutoiminto.
10. Siirry Dynamics työvaiheiden 365, **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**jakelu aikataulut**.
11. Valitse-luettelosta **1090 Rekisteröi**.
12. Valitse **suorittaa nyt**.


<a name="see-also"></a>Lisätietoja
--------

[Omat suositukset tuotekuvaus](personalized-product-recommendations.md)


