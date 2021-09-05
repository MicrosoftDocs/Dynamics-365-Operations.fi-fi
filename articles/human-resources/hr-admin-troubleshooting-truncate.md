---
title: Tekstin katkaisun välttäminen toimihierarkiassa ja Visio-viennissä
description: Tässä aiheessa käsitellään toimihierarkian henkilöiden ja toimien nimien katkeamisongelmaa Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a9a8d22df0416ef417a6216c3131bfb6d40d200
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413532"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Tekstin katkaisun välttäminen toimihierarkiassa ja Visio-viennissä

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Varasto-otto**

Kun asiakas tarkastelee, toimihierarkiaa Microsoft Dynamics 365 Human Resourcesissa, henkilöiden ja toimien nimet on katkaistu. Tämän vuoksi näyttökuvan ottaminen hierarkiasta tai hierarkian tulostaminen jakamista varten voi olla hankalaa.

![Toimihierarkia.](media/position-h.png)

**Syy**

Tämä on suunniteltu ominaisuus.

**Ratkaisu**

Tekstin koon muuttaminen ei valitettavasti ole yksinkertaista. Voit kuitenkin viedä toimihierarkian Human Resourcesista ja tuoda sen Microsoft Visioon. Vaikka seuraava artikkeli kirjoitettiin Microsoft Dynamics AX 2012:ta varten, samaa prosessia käytetään Human Resourcesissa: [Toimihierarkian vieminen Microsoft Visioon](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Vie hierarkia Visioon seuraavien ohjeiden mukaisesti.

1. Avaa Human Resourcesissa **Toimet**-luettelosivu.

    Jos haluat sisällyttää muita tietoja organisaation rakennekaavioon, lisää kenttiä **Toimet**-luetteloon. jotta ne ovat käytettävissä, kun käytät **organisaation ohjattua kaaviotoimintoa** myöhemmin tämän menettelyn aikana.

2. Valitse toimintoruudussa ensin **Avaa Microsoft Officessa** -painike ja sitten **Vie Exceliin** -kohdassa **Toimet**. Voit vaihtoehtoisesti painaa näppäinyhdistelmää Ctrl+T.

    ![Toimet-luettelosivun vieminen Exceliin.](media/org-admin.png)

3. Tallenna viety Excel-tiedosto.

    ![Vie Exceliin -valintaikkuna.](media/export-excel.png)

4. Valitse Visiossa ensin **Visio - Luo uusi** ja sitten **Yritys**-malliluokka.

    ![Uusi kaavio.](media/new.png)

5. Valitse ensin **organisaatiokaavion ohjattu toiminto** ja sitten **Luo**.

    ![Organisaatiokaavion ohjatun toiminnon valintaikkuna.](media/orgchart-wizard.png)

6. Valitse ensin **Tiedostoon tai tietokantaan jo tallennetut tiedot** ja sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 1.](media/orgchart-wizard7.png)

7. Valitse ensin **Teksti-, Org Plus (\*.txt)- tai Excel-tiedosto** ja sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 2.](media/orgchart-wizard3.png)

8. Siirry toimihierarkian sisältävään Excel-tiedostoon, valitse se ja valitse sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 3.](media/orgchart-wizard2.png)

9. Määritä **Nimi**-kentän arvoksi **Toimi** ja **Raportoi:**-kentän arvoksi **Raportoi toimella**. Valitse sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 4.](media/orgchart-wizard1.png)

10. Valitse kussakin solmussa näytettävät kentät ja valitse sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 5.](media/orgchart-wizard5.png)

11. Lisää **Toimi**-sarake **Muokkaa tietokenttien muotoa** -luetteloon ja valitse sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 6.](media/orgchart-wizard6.png)

12. Kuvia ei ole tällä hetkellä käytettävissä. Valitse tämän vuoksi seuraavalla sivulla **Seuraava**.
13. Valitse **Haluan, että ohjattu toiminto jakaa organisaatiokaavio automaattisesti sivuille**.

    ![Organisaatiokaavion ohjattu toiminto 7.](media/orgchart-wizard4.png)

14. Valitse **Valmis**.

    Jos jotkin toimet eivät ole rakenteessa, sinua pyydetään sisällyttämään ne kaavioon.

Visiossa muodostettavassa kaaviossa jokainen esimies näkyy erillisessä laskentataulukossa.

Kun Visio-tiedosto luodaan, kussakin solmussa näkyvät ne tiedot, jotka perustuvat kaavioon sisällytettäväksi valittuihin kenttiin.

![Hierarkiakaavio.](media/hierarchy.png)

**Lisäasetus**

Human Resourcesissa joitakin hierarkiaan liittyviä tietoja voi olla mahdollista katsoa **Ihmiset**-työtilassa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
