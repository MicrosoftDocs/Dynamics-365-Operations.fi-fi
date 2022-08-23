---
title: Ota käyttöön kohdennetut tuotesuositukset
description: Tässä artikkelissa kuvataan, miten mukautettuja tuotesuosituksia voidaan käyttää Microsoft Dynamics 365 Commerce -asiakkaille.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: f626704b41b9d22f6b2ff55dd4ffe1037559a83a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283611"
---
# <a name="enable-personalized-recommendations"></a>Kohdennettujen suositusten ottaminen käyttöön

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, miten mukautettuja tuotesuosituksia voidaan käyttää Microsoft Dynamics 365 Commerce -asiakkaille.

Dynamics 365 Commerce -ohjelmassa jälleenmyyjät voivat tehdä mukautettuja tuotesuosituksia (eli personointeja). Näin henkilökohtaiset suositukset voidaan sisällyttää asiakaskokemukseen verkossa ja myyntipisteessä (POS). Kun mukautustoiminto on käytössä, järjestelmä voi liittää käyttäjän osto- ja tuotetiedot ja luoda yksilöllisiä tuotesuosituksia.

## <a name="personalization-prerequisites"></a>Mukauttamisen edellytykset

Ennen kuin teet mukautettuja tuotesuosituksia asiakkaiden käyttöön, huomaa, että tuotesuosituksia tuetaan vain niiden Commerce-käyttäjien osalta, jotka ovat siirtyneet käyttämään tallennustilaa Azure Data Lake -säilössä. Ennen kuin asiakkaat voivat vastaanottaa mukautettuja tuotesuosituksia, jälleenmyyjien on [otettava tuotesuositukset käyttöön](enable-product-recommendations.md).

> [!NOTE]
> Ottamalla käyttöön tuotesuositukset otat myös mukauttamisen käyttöön. Jos kuitenkin poistat mukauttamisen käytöstä, et poista käytöstä muita tuotesuosituksia.

Lisätietoja tuotesuosituksista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).

## <a name="turn-on-personalization"></a>Ota käyttöön mukautukset

Mukautukset otetaan käyttöön seuraavasti.

1. Hae **Ominaisuuksien hallinta** Commercen pääkonttoriversiossa.
1. Avaa käytettävissä olevien ominaisuuksien luettelo valitsemalla **Kaikki**. 
1. Kirjoita hakuruutuun **Suositukset**.
1. Valitse **Kohdennetut tuotesuositukset** -ominaisuus.
1. Valitse **Kohdennetut tuotesuositukset** -ominaisuusruudussa **Ota käyttöön nyt**.

![Mukautusten ottaminen käyttöön.](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> Kun mukautus otetaan käyttöön, mukautettujen tuotesuositusluetteloiden luontiprosessi aloitetaan. Enintään yksi päivä saattaa olla tarpeen, ennen kuin nämä luettelot ovat käytettävissä ja näkyvissä verkossa ja POS-sovelluksessa.

## <a name="personalized-lists"></a>Mukautetut luettelot

Tietokoneella luotujen luetteloiden mukautuksen lisäksi suosituspalvelu mahdollistaa tuotekehityskokemuksen mukauttamisen sekä verkossa että myyntipisteessä.

Kun mukauttaminen on otettu käyttöön, jälleenmyyjät voivat näyttää asiakkaan henkilökohtaiset poiminnat -luettelot online-tilassa tai Suositeltava asiakkaalle -luetteloissa kassapäätteissä. Lisäksi jälleenmyyjät voivat soveltaa mukauttamista olemassa oleviin tuotesuositusluetteloihin ja tarjota todennettujen käyttäjien yleisiä tietosuojasäännöksiä (GDPR). Jos poistat mukauttamisen käytöstä, poistat myös nämä ominaisuudet käytöstä.

### <a name="online-picks-for-you-lists"></a>Poiminnat sinulle -luettelot verkosta

Poimittu sinulle -luettelo on tekoälykoneoppimisluettelo (AI-ML), joka näyttää todennetun käyttäjän mukautetun luettelon ehdotetuista tuotteista. Tämä luettelo perustuu käyttäjän monikanavaiseen ostohistoriaan. Mukautetut suositukset päivitetään dynaamisesti, kun käyttäjä tekee enemmän ostoksia. Tämäntyyppinen luettelo tukee myös luokkasuodatusta, jolloin vähittäiskauppiaat voivat näyttää siirtymishierarkioiden perusteella parhaimmistoa.

Ennen kuin Poiminnat sinulle -luettelo voi näkyä verkkokaupan sivulla, seuraavien käyttäjävaatimusten on täytyttävä:

- Käyttäjien on oltava kirjautuneena sisään. Anonyymit käyttäjät eivät näe mukautettuja suosituksia.
- Käyttäjillä on oltava vähintään yksi osto tilillään.
- Käyttäjien on valittava, jotta he saavat henkilökohtaisia suosituksia.

Seuraavassa kuvassa on esimerkki verkkokaupan sivulla olevasta Poiminnat sinulle -luettelosta.

![Poiminnat sinulle -luettelot verkosta.](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>Suositeltava asiakkaalle-luettelot POS-sovelluksessa

Vähittäiskauppiaat voivat mukauttaa aiemmin luotuja asiakastietosivuja ja lisätä niiden clienteling-kokemusta lisäämällä asia yhteyteen Suositeltava asiakkaalle -luettelon.

Seuraavassa kuvassa on esimerkki kassapäätteessä olevasta Suositeltu asiakkaalle -luettelosta.

![Suositeltava asiakkaalle -luettelot POS-sovelluksessa.](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Käytä mukauttamista aiemmin luotuihin suositusluetteloihin

Jälleenmyyjät voivat soveltaa mukauttamista aiemmin luotuihin suositusluetteloihin, kuten Uusi, Trendit, Myydyin, Ihmiset pitivät myös ja Usein ostetut yhdessä. Kun mukauttamista käytetään aiemmin luoduissa luetteloissa, nimikkeet, jotka on aiemmin ostettu kirjautuneen käyttäjän toimesta, poistetaan näistä luetteloista. Sekä anonyymeille käyttäjille että käyttäjille, jotka ovat jättäytymässä yksilöllisten suositusten vastaanottamisesta, näytetään aiemmin luotujen luetteloiden oletusversiot. Siksi vähittäiskauppiaiden ei tarvitse ylläpitää erillisiä sivukokemuksia manuaalisesti.

Esimerkiksi kirjautuneena oleva käyttäjä on jo ostanut mustan kellon ja ruskeat työsaappaat, jotka näkyvät seuraavassa kuvassa Trendit - oletus -luettelossa. Siksi käyttäjä näkee uusia tuotteita näiden tuotteiden sijasta, kuten Trendit - mukautettu -luettelossa näkyy.

![Mukauttamisen ottaminen käyttöön.](./media/applypersonalization.png)

Jos haluat käyttää mukauttamista aiemmin luotuun suositusluetteloon Commercen sivustonluontityökalussa, toimi seuraavasti.

1. Avaa aiemmin luotu sivustonluontisivu, joka sisältää tuotekokoelmamoduulin.
1. Valitse vasemmasta siirtymisruudusta tuotekokoelmamoduuli.
1. Valitse luettelo oikeanpuoleisessa siirtymisruudussa **Tuotteet**-kohdan alta.
1. Valitse luettelotyyppi **Valitse tuoteluettelon konfigurointi** -valintaikkunan **Tyyppi**-kohdasta.
1. Valitse **Käytä mukauttamista** -valintaruutu ja valitse sitten **OK**.

    ![Mukauttamisen kohdistaminen trendiluetteloon.](./media/ApplyPersonalizationToTrending.PNG)

1. Tallenna sivu, lopeta sen muokkaus ja sitten julkaise se. Kun sivu on julkaistu, kirjautuneet käyttäjät näkevät mukautetut trendiluettelot.

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Ota tuotesuositukset käyttöön](enable-product-recommendations.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
