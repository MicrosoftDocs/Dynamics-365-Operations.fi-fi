---
title: Vuokrasopimuksen kirjaustilien määrittäminen
description: Tässä ohjeaiheessa luetellaan kirjaustilit, joita tarvitaan resurssin vuokratapahtumissa, sekä selitetään, miten tilit kirjataan Vuokrasopimuksen kirjausparametrit -sivulla.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 147d8cd93f9664039b2004b878dcaff96c8b6ce6
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726375"
---
# <a name="set-up-lease-posting-accounts"></a>Vuokrasopimuksen kirjaustilien määrittäminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa luetellaan kirjaustilit, joita tarvitaan resurssin vuokratapahtumissa, sekä selitetään, miten tilit kirjataan **Vuokrasopimuksen kirjausparametrit** -sivulla.

Jos haluat noudattaa 842 (ASC 842)- ja IFRS 16 -säädöksiä, sinun on ehkä luotava tilit tilikarttaan. Kuitenkaan kaikki tilit, jotka noudattavat ASC- ja IFRS-säädöksiä, eivät ole käyttöomaisuustilejä. ASC 842:n mukaisesti käyttöoikeusomaisuuserä on tallennettu sekä rahoitus- että käyttöleasingsopimuksiin. Nämä vuokrasopimukset ovat erillisiä käyttöomaisuudesta. (Voit silti ylläpitää käyttöoikeusomaisuuserää Käyttöomaisuuserät-kohdan avulla.)

Lisätietoja tilirakenteiden luomisesta on kohdassa [Tilirakenteiden luominen](../general-ledger/tasks/create-account-structures.md). Lisätietoja päätilin luomisesta on kohdassa [Päätilin luominen](../general-ledger/tasks/create-main-account.md).

Seuraavassa taulukossa on esimerkkejä tileistä, jotka on luotava vuokratuille resurssitapahtumille, jos niitä ei ole vielä luotu. IFRS 16:n mukaisesti käyttöleasingsopimuksia käytetään yhä alhaisen arvon vuokrasopimuksissa ja lyhytaikaisissa vuokrasopimuksissa.

| Kirjanpitotilin numero | Tilityyppi  | Tilin nimi                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Resurssi         | Ajoneuvo - käyttöoikeusomaisuuserä                                     |
| 180160                | Resurssi         | Rakennus - käyttöoikeusomaisuuserä                                    |
| 180250                | Resurssi         | Kumulatiivinen poisto - ajoneuvot                   |
| 180260                | Resurssi         | Kumulatiivinen poisto - rakennukset                  |
| 222300                | Velat     | Lyhytaikainen sitoumus - rahoitusleasingsopimukset                |
| 222310                | Tase | Lyhytaikainen sitoumus - käyttöleasingsopimukset              |
| 250200                | Velat     | Velkavekselit                                         |
| 250601                | Tase | Pitkäaikainen sitoumus - rahoitusleasingsopimukset                 |
| 250602                | Tase | Pitkäaikainen sitoumus - käyttöleasingsopimukset               |
| 250606                | Tase | Toteutumaton vuokra                                         |
| 300160                | Tase | Jakamaton voitto                                     |
| 604500                | Expense       | Vuokran kulu                                         |
| 604501                | Expense       | Ajoneuvon käyttöleasingsopimuksen kulu - koron lisäys  |
| 604502                | Expense       | Ajoneuvon käyttöleasingsopimuksen kulu - kuoletus        |
| 605200                | Expense       | Rakennuksen käyttöleasingsopimuksen kulu - koron lisäys |
| 605201                | Expense       | Rakennuksen käyttöleasingsopimuksen kulu - kuoletus       |
| 607101                | Expense       | Ajoneuvon vuokrasopimuksen kuoletuskulu                    |
| 607102                | Expense       | Rakennuksen vuokrasopimuksen kuoletuskulu                   |
| 607103                | Expense       | Arvonalentumiskulu - rahoitusleasingsopimukset                   |
| 607104                | Expense       | Arvonalentumiskulu - käyttöleasingsopimukset                 |
| 618910                | Expense       | Vuokrasopimuksen kulu - rahoitusleasingsopimukset                        |
| 618920                | Expense       | Muuttuvat maksut - rahoitusleasingsopimukset                    |
| 618930                | Expense       | Muuttuvat maksut - käyttöleasingsopimukset                  |
| 800600                | Expense       | Ajoneuvon vuokrasopimuksen korkokulu                        |
| 800601                | Expense       | Rakennuksen vuokrasopimuksen korkokulu                       |
| 801201                | Tase | Voitto ja tappio - vuokrasopimuksen muokkaaminen                      |

## <a name="configure-posting-accounts"></a>Kirjaustilien määrittäminen

Jos haluat liittää tilejä vuokrauskirjoihin ja -ryhmiin, jotka on jo luotu, määritä parametrit resurssin vuokrausta varten.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokrasopimuksen kirjausparametrit**.
2. Avaa **Tilit**-välilehdessä **Vuokrauksen tilit** -pikavälilehti. Määritä rahoitus- ja käyttöleasingsopimusten päätilit vastaavalle **kirjaustyypille**. Edellä olevassa taulukossa näkyvät käyttö- ja käyttöleasingsopimuksiin liittyvät tilit.

    > [!NOTE]
    > Tämä vaihe vaatii erillisten tilien määrittämistä sekä käyttö- että rahoitusleasingsopimusten jokaiselle kirjaustyypille lukuun ottamatta **Vuokrasopimuksen kulun vastatili**- ja **Vuokrasopimuksen lisäys/vähennys** -kohtia. IFRS 16:n kirjanpidon kehystä noudattavien yritysten on lisättävä päätili käyttöleasingsopimusta varten. Järjestelmä ei kuitenkaan käytä tätä tiliä, vaikka se on pakollinen kenttä, koska kaikki IFRS 16 -standardin mukaiset vuokrasopimukset luokitellaan rahoitusleasingsopimuksiksi.
    >[!NOTE]
    > **Vuokrasopimuksen lisäys/vähennys** -kohtaa käytetään kirjaustyyppinä resurssin lisämäärityksissä. Niitä ovat **alkuvaiheen välittömät menot, vuokrasopimukseen liittyvät kannustimet, vuokrasopimuksen ennakkomaksut ja purkamiskustannukset**, mutta kirjaus käyttöoikeusomaisuuserän päätiliin saa oletusarvoksi **vuokrasopimuksen resurssin**.        
    
3. Jos haluat valita tietyn vuokrasopimusryhmän, joka vastaa päätiliä, valitse **Tilikoodi**-kentässä **Ryhmä**. Valitse sitten **Tilin/ryhmän numero** -kentässä vuokrasopimusryhmä, joka liitetään päätiliin.
4. Jos haluat liittää tilikoodit hallinnollisiin kustannuksiin, jotka on määritetty järjestelmässä, valitse kulu **Toimeenpanokustannukset**-pikavälilehden **Kulun tyyppi** -kentässä. Määritä sitten kunkin kirjan rahoitus- ja käyttötilit.

    > [!NOTE]
    > Valittua rahoitus- tai käyttötiliä veloitetaan, kun ajoitetun kulun lasku kirjataan.
    > **Vuokrasopimuksen kulun vastatili** -kohtaa käytetään kirjaustyyppinä toimeenpanokustannusten tapahtumissa, mutta kirjaa määritettyyn **vastatiliin** **toimeenpanokustannusten maksuaikatauluriveillä** vuokrasopimuksen tiedoissa tai vuokrauskirjalomakkeessa.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
