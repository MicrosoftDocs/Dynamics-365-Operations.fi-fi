---
title: "Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumasivulle"
description: "Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä näytön asettelun suunnittelutoimintoa Microsoft Dynamics 365 for Operationsissa."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 590a009fa4afaf8020b9905020266c4b7293d228
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumasivulle

[!include[banner](includes/banner.md)]


Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä näytön asettelun suunnittelutoimintoa Microsoft Dynamics 365 for Operationsissa.

Voit näyttää tuotesuosituksia myyntipisteen laitteessa, kun käytät Microsoft Dynamics 365 for Operationsia. *Suositukset* ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella. Voit näyttää tuotteen suosituksi lisäämällä ohjausobjektin tapahtumanäytölle näytön asettelun suunnittelutoiminnon avulla.

## <a name="open-layout-designer"></a>Avaa asettelun suunnittelutoiminto
1.  Siirry kohtaan **Vähittäismyynti ja kauppa** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **POS** &gt; **Näytön asettelut**.
2.  Pikasuodattimen avulla voit etsiä näyttöä, johon haluat lisätä ohjausobjektin. Voit esimerkiksi suodattaa **Näyttöasettelun tunnus** -kentässä arvolla "F2CP16:9M".
3.  Etsi haluamasi tietue luettelosta ja valitse se. Valitse esimerkiksi "Nimi: F2CP16:9M Näyttöasettelun tunnus: F2CP16:9M'.
4.  Valitse **Asettelun suunnittelutoiminto**.
5.  Noudata kehotteita asettelun suunnittelutoiminnon käynnistämiseksi. Tunnistetietoja kysyttäessä anna samat tunnistetiedot, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettiin **Näytön asettelut** -sivulla.
6.  Kun kirjaudut, tulee sivu, joka on samanlainen kuin alla oleva. Asettelu on erilainen riippuen oman myymälän tekemistä mukautuksista.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Valitse näyttöasetus
-----------------------

Käytettävissä on kaksi asetusta. Valitse vaihtoehto, joka sopii parhaiten myymälällesi ja noudata ohjeita loppuun viimeistelläksesi ohjausobjektin määrittämisen. Asetukset ovat:
-   Suositukset ovat aina näkyvissä.
-   A **Suositukset**-välilehti näkyy oikealla puolella näytön ruudukossa.

#### <a name="to-make-recommendations-always-visible"></a>Saat suositukset aina näkyville:

1.  Pienennä tapahtumarivien tiedot -alueen korkeutta niin, että se on samalla korkeudella kuin asiakaspaneeli vasemmalla puolellaan. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Vasemmanpuoleisesta valikosta vedä ja pudota suosituksien ohjausobjekti Tapahtumarivin tiedot -alueen ja painikeruudukon väliin näytön alareunassa keskellä. Muuta ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan. [](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.
4.  Siirry Dynamics 365 for Operationsissa kohtaan **Vähittäismyynti ja kauppa** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.
5.  Valitse luettelossa **1090, kassakoneet**.
6.  Valitse **Suorita nyt**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Lisää Suositukset-välilehti painikeruudukkoon näytön oikealla puolella seuraavasti:

1.  Napsauta hiiren kakkospainikkeella tyhjää tilaa sivun oikeassa reunassa painikeruudukon viimeisen välilehden alapuolella.
2.  Valitse **Mukauta**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Valitse **Uusi välilehti**.
4.  Etsi juuri lisäämäsi uusi välilehti. Saatat joutua vierittämään näyttöä alaspäin.
5.  Valitse avattavassa **Sisältö**-valikossa **Suositellut tuotteet**. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  Kirjoita **Otsikko**-kenttään suositusten välilehden nimi. Kirjoita esimerkiksi 'Suositellut tuotteet'.
7.  Valitse **Kuva**-kentässä välilehdessä näytettävä kuva.
8.  Valitse **OK**. Painikeruudukkoon tulee uusi välilehti.
9.  Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.
10. Siirry Dynamics 365 for Operationsissa kohtaan **Vähittäismyynti ja kauppa** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.
11. Valitse luettelossa **1090, kassakoneet**.
12. Valitse **Suorita nyt**.


<a name="see-also"></a>Lisätietoja
--------

[Mukautettujen tuotesuositusten yleiskuvaus](personalized-product-recommendations.md)




