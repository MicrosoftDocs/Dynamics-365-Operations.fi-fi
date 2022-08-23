---
title: Tavujärjestysmerkkejä luoduissa tiedostoissa estävien ER-määritysten suunnitteleminen
description: Tässä artikkelissa käsitellään sähköisen raportoinnin (ER) muotojen määrittäminen luomaan raportteja, jotka estävät tavujärjestysmerkit.
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: EROperationDesigner
ms.openlocfilehash: fa66edef7e39c72d4859a21a1474096f7bc1c1dd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278793"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>Tavujärjestysmerkkejä luoduissa tiedostoissa estävien ER-määritysten suunnitteleminen

[!include [banner](../includes/banner.md)]

[Sähköisen raportoinnin (ER)](general-electronic-reporting.md) [ratkaisu](er-quick-start1-new-solution.md) voidaan suunnitella luomaan lähteviä asiakirjoja. Teksti- tai XML-tiedostojen kaltaisten asiakirjojen luominen edellyttää, että ratkaisussa on oltava ER-[määritys](general-electronic-reporting.md#Configuration), joka sisältää ER-muoto-osan. Luotujen tiedostojen merkkijoukon ilmaisevan [merkkikoodaus](/windows/win32/intl/character-sets) edellyttää, että ER-muoto sisältää **Yleinen\\Tiedosto**-muotoelementin. ER-muoto-osan määritetään avaamalla ER-määrityksen [luonnos](general-electronic-reporting.md#component-versioning) ER-muodon suunnittelutoiminnossa ja lisäämällä **Yleinen\\Tiedosto**-elementti. **Koodaus**-kenttään määritetään niiden lähtevien tiedostojen koodaus, jotka luodaan suorituksen aikana tätä osaa käyttämällä.

> [!NOTE]
> Jos muodon sisältämän koodauksen nimi on virheellinen, seurauksena on virhe, kun muutokset tallennetaan muotoasetuksiin.

![Juurielementin lisääminen Muodon suunnittelija -sivulla.](./media/er-suppress-bom-characters-image1.gif)

Jos koodaukseksi määritettään **UTF-8**, **UTF-16** tai **UTF-32**, **Estä tavujärjestysmerkit**-vaihtoehto on käytettävissä. Kun asetuksena on **Kyllä**, [tavujärjestysmerkit](/globalization/encoding/byte-order-mark) estetään lähtevissä tiedostoissa, jotka luodaan suorituksen aikana suoritettaessa muokattavaa ER-muotoa.

> [!NOTE]
> Jos **Koodaus**-kenttä jätetään tyhjäksi, **UTF-8**-oletuskoodausta käytetään.

![Estä tavujärjestysmerkit -vaihtoehdon määrittäminen Muodon suunnittelija -sivulla.](./media/er-suppress-bom-characters-image2.gif)

Toiminnon tarkastelu suorituksen aikana edellyttää soveltuvan menettelyn suorittamista. Voit noudattaa esimerkiksi artikkelin [ER-muotojen XML-elementtien suorittamisen lykkääminen](er-defer-xml-element.md) vaiheita. Kun kyseisen artikkelin [Muodon muokkaaminen siten, että laskeminen perustuu luotuun tulokseen](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) -osan vaiheet on suoritettu, tee seuraavat lisävaiheet:

1. UTF-koodauksen määrittäminen:

    1. Valitse **Yleinen\\Tiedosto**-tyypin **Raportti**-elementti.
    2. Määritä **Koodaus**-kenttään **UTF-8**-koodaus.

2. Luo XML-tiedosto, joka sisältää tavujärjestysmerkin:

    1. Sisällytä tavujärjestysmerkit luotuihin XML-tiedostoihin määrittämällä **Estä tavujärjestysmerkit** -asetukseksi **Ei**.
    2. Suorita artikkelin [ER-muotojen XML-elementtien suorittamisen lykkääminen](er-defer-xml-element.md) osassa [XML-elementin suorittamisen lykkääminen siten, että käytetään laskettua summaa](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) olevat vaiheet ja tallenna luotu tiedosto nimellä **SampleXmlReport.xml**.

3. Luo XML-tiedosto, joka ei sisällä tavujärjestysmerkkiä:

    1. Estä tavujärjestysmerkit luoduissa XML-tiedostoissa määrittämällä **Estä tavujärjestysmerkit** -asetukseksi **Kyllä**.
    2. Suorita artikkelin [ER-muotojen XML-elementtien suorittamisen lykkääminen](er-defer-xml-element.md) osassa [XML-elementin suorittamisen lykkääminen siten, että käytetään laskettua summaa](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) olevat vaiheet ja tallenna luotu tiedosto nimellä **SampleXmlReport (1).xml**.

4. Vertaa luotuja tiedostoja tiedostovertailun apuohjelmassa.

    Ensimmäinen ero on nähtävissä tiedoston otsikossa. SampleXmlReport.xml-tiedosto sisältää tavujärjestysmerkin, mutta sitä ei ole SampleXmlReport (1).xml-tiedostossa.

    ![Luotujen tiedostojen vertaaminen tiedostovertailun apuohjelmalla.](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Lisätietoja

- [Sähköisen raportoinnin muotojen XML-elementtien suorittamisen lykkääminen](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
