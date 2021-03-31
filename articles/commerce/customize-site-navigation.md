---
title: Sivuston selauksen mukauttaminen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan mukautettu online-siirtymishierarkia, jonka avulla tuotteita voidaan järjestellä Microsoft Dynamics 365 Commerce -sivuston selaamista varten.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cfd0a9559eb2b596adb822b228929e6855711bb4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222606"
---
# <a name="customize-site-navigation"></a>Sivuston selauksen mukauttaminen


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten luodaan mukautettu online-siirtymishierarkia, jonka avulla tuotteita voidaan järjestellä Microsoft Dynamics 365 Commerce -sivuston selaamista varten.

## <a name="overview"></a>Yleiskuvaus

Verkkomyymälöissä asiakkaat yleensä voivat etsiä ja selata tuotteita siirtymällä tuoteluokissa. Tätä ominaisuutta käytetään yleensä sivun yläosassa olevien välilehtien tai vasemmalla olevan siirtymispalkin avulla. Dynamics 365 Commerce -sovelluksessa voit luoda luokan siirtymisen ja eri luokkien tuotteiden hierarkiarakenteen ja hallita sitä.

## <a name="create-a-channel-navigation-hierarchy"></a>Luo kanavan siirtymishierarkia

Voit luoda kanavan siirtymishierarkian seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Luokka- ja tuotehallinta**.
1. Valitse **Luokan hierarkiat** ja valitse sitten **Uusi**.
1. Anna hierarkialle nimi.

    > [!NOTE]
    > Luotu ylin luokka on luokan juurisolmu. Se ei näy sivustossa. Jos haluat luoda luokkahierarkian, jossa yksi ylätason solmu näkyy sivustossa, luo luokka ja nimeä se juuriluokan alitasoksi.

1. Valitse **Uusi luokka solmu** ja anna luokan nimi.
1. Jatka rinnakkais- ja alitasojen luomista halutulla tavalla.

Voit nyt määrittää tuotteita kuhunkin ylätason luokkaan luotuun luokkaan.

## <a name="customize-the-order-of-categories"></a>Luokkien järjestyksen mukauttaminen

Oletusarvoisesti määrittämäsi luokat näkyvät sivustossa aakkosjärjestyksessä. Voit kuitenkin mukauttaa luokkien näyttöjärjestystä.

## <a name="assign-a-category-hierarchy-type"></a>Määritä luokkahierarkiatyyppi

1. Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Luokka- ja tuotehallinta**.
1. Valitse **Luokkahierarkiat**.
1. Valitse toimintoruudun **Luokkahierakia**-välilehden **Määritys**-ryhmässä **Liitä hierarkiatyyppi**.
1. Valitse **Uusi**.
1. Valitse **Luokkahierarkian tyyppi** -kentässä **Kanavan siirtymishierarkia**.
1. Valitse **Luokkahierarkia**-kentässä aiemmin valittu kanavan siirtymishierarkia.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Uusien tai päivitettyjen siirtymishierarkioiden julkaiseminen

Voit määrittää siirtymishierarkian käyttöön verkkomyymälässä seuraavasti.

1. Valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.
1. Valitse vasemmanpuoleisesta puusta verkkomyymälä.
1. Valitse **Julkaise kanavan päivitykset**.
1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Etsi luettelosta **Työ 1040** ja valitse se.
1. Valitse **Suorita nyt**.
1. Toista vaiheet 5 ja 6 töille 1070 ja 1150.

## <a name="show-categories-on-your-site"></a>Luokkien näyttäminen sivustossa

Jos haluat näyttää luokkahierarkian verkkomyymälässä, lisää siirtymisvalikkomoduuli sopivaan sijaintiin mallissa tai osassa. Tämä siirtymisvalikkomoduuli näyttää nyt siirtymishierarkian, jos olet julkaissut siirtymishierarkian kanavassa, johon sivusto on sidottu.

> [!NOTE]
> Myymälän moduulikirjastoon sisältyvän siirtymisvalikkomoduulin avulla käyttäjät voivat siirtyä vain luokissa, joissa ei ole aliluokkia. Jos asiakkaiden on voivat siirtyä luokissa, joissa on aliluokkia, mukauta siirtymisvalikkomoduulia.

## <a name="add-custom-navigation-options"></a>Mukautettujen siirtymisvaihtoehtojen lisääminen

Siirtymisvalikossa voit lisätä siirtymisvaihtoehtoja, jotka eivät ole tuoteluokkahierarkian osa. Esimerkiksi tuoteluokkaluettelon loppuun voit lisätä **Ota yhteyttä** -nimikkeen, joka vie sivustolle luodulle yhteydenottosivulle.

Voit lisätä siirtymisvalikkoon mukautettuja siirtymisvaihtoehtoja seuraavasti.

1. Valitse mukautettavassa mallissa tai osassa siirtymisvalikkomoduuli.
1. Valitse ominaisuusruudun **Tiedot**-välilehdessä **Lisää nimike**, jos haluat luoda uuden sisällönhallintajärjestelmän (CMS) siirtymisnimikkeen.
1. Anna linkin teksti ja URL-osoite.
1. Toista vaiheet 2 ja 3 ja lisää mukautettuja siirtymisvaihtoehtoja.
1. Kun olet valmis, tallenna malli tai osa valitsemalla **Tallenna** ja tarkista se sitten valitsemalla **Viimeistele muokkaus**.

## <a name="additional-resources"></a>Lisäresurssit

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Mallien käyttö](work-with-templates.md)

[Esimääritettyjen asettelujen käyttö](work-with-layouts.md)

[Katkelmien käyttäminen](work-with-fragments.md)

[Moduulien käyttäminen](work-with-modules.md)

[Sivun URL-osoitteen luominen](create-page-url.md)

[Julkaisuryhmien kanssa työskenteleminen](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]