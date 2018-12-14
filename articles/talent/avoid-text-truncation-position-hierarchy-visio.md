---
title: "Tekstin katkaisemisen välttäminen toimihierarkiassa ja vienti Visioon"
description: "Tässä ohjeaiheessa kerrotaan, miten voi ratkaista henkilöiden ja toimien nimien katkaisemisongelman, kun asiakkaat tarkastelevat toimihierarkiaa Microsoft Dynamics 365 for Talentissa. Tekstin katkaisemisen voi vaikeuttaa näyttökuvan ottamista hierarkiasta tai sen tulostamista."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: b688a396e3b384aedb06c470b1634150ae7aa038
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---

# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Tekstin katkaisemisen välttäminen toimihierarkiassa ja vienti Visioon

[!include [banner](includes/banner.md)]

**Ongelma**

Kun asiakas tarkastelee, toimihierarkiaa Microsoft Dynamics 365 for Talentissa, henkilöiden ja toimien nimet on katkaistu. Tämän vuoksi näyttökuvan ottaminen hierarkiasta tai hierarkian tulostaminen jakamista varten voi olla hankalaa.

![Toimihierarkia](media/position-h.png)

**Syy**

Tämä on suunniteltu ominaisuus.

**Tarkkuus**

Tekstin koon muuttaminen ei valitettavasti ole yksinkertaista. Voit kuitenkin viedä toimihierarkian Talentista ja tuoda sen Microsoft Visioon. Vaikka seuraava artikkeli kirjoitettiin Microsoft Dynamics AX 2012:ta varten, samaa prosessia käytetään Talentissa: [Toimihierarkian vieminen Microsoft Visioon](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Vie hierarkia Visioon seuraavien ohjeiden mukaisesti.

1. Avaa Talentissa **Toimet**-luettelosivu.

    Jos haluat sisällyttää muita tietoja organisaation rakennekaavioon, lisää kenttiä **Toimet**-luetteloon. jotta ne ovat käytettävissä, kun käytät ohjattua toimintoa myöhemmin tämän menettelyn aikana.

2. Valitse toimintoruudussa ensin **Avaa Microsoft Officessa** -painike ja sitten **Vie Exceliin** -kohdassa **Toimet**. Voit vaihtoehtoisesti painaa näppäinyhdistelmää Ctrl+T.

    ![Toimet-luettelosivun vieminen Exceliin](media/org-admin.png)

3. Tallenna viety Excel-tiedosto.

    ![Vie Exceliin -valintaikkuna](media/export-excel.png)

4. Valitse Visiossa ensin **Visio - Luo uusi** ja sitten **Yritys**-malliluokka.

    ![Uusi kaavio](media/new.png)

5. Valitse ensin **organisaatiokaavion ohjattu toiminto** ja sitten **Luo**.

    ![Organisaatiokaavion ohjatun toiminnon valintaikkuna](media/orgchart-wizard.png)

6. Valitse ensin **Tiedostoon tai tietokantaan jo tallennetut tiedot** ja sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 1](media/orgchart-wizard7.png)

7. Valitse ensin **Teksti-, Org Plus (\*.txt)- tai Excel-tiedosto** ja sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 2](media/orgchart-wizard3.png)

8. Siirry toimihierarkian sisältävään Excel-tiedostoon, valitse se ja valitse sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 3](media/orgchart-wizard2.png)

9. Määritä **Nimi**-kentän arvoksi **Toimi** ja **Raportoi:**-kentän arvoksi **Raportoi toimella**. Valitse sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 4](media/orgchart-wizard1.png)

10. Valitse kussakin solmussa näytettävät kentät ja valitse sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 5](media/orgchart-wizard5.png)

11. Lisää **Toimi**-sarake **Muokkaa tietokenttien muotoa** -luetteloon ja valitse sitten **Seuraava**.

    ![Organisaatiokaavion ohjattu toiminto 6](media/orgchart-wizard6.png)

12. Kuvia ei ole tällä hetkellä käytettävissä. Valitse tämän vuoksi seuraavalla sivulla **Seuraava**.
13. Valitse **Haluan, että ohjattu toiminto jakaa organisaatiokaavio automaattisesti sivuille**.

    ![Organisaatiokaavion ohjattu toiminto 7](media/orgchart-wizard4.png)

14. Valitse **Valmis**.

    Jos jotkin toimet eivät ole rakenteessa, sinua pyydetään sisällyttämään ne kaavioon.

Visiossa muodostettavassa kaaviossa jokainen esimies näkyy erillisessä laskentataulukossa.

Kun Visio-tiedosto luodaan, kussakin solmussa näkyvät ne tiedot, jotka perustuvat kaavioon sisällytettäväksi valittuihin kenttiin.

![Hierarkiakaavio](media/hierarchy.png)

**Lisäasetus**

Talentissa joitakin hierarkiaan liittyviä tietoja voi olla mahdollista katsoa **Ihmiset**-työtilassa.

