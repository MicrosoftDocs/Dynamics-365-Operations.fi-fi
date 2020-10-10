---
title: "\"Osta samankaltaisia tyylejä\" -suositusten käyttöönotto"
description: Tässä ohjeaiheessa kuvataan, kuinka voit ottaa käyttöön "Osta samankaltaisia tyylejä" -tuotesuositukset Microsoft Dynamics 365 Commercessa.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818371"
---
# <a name="enable-shop-similar-looks-recommendations"></a>"Osta samankaltaisia tyylejä" -suositusten käyttöönotto

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka voit ottaa käyttöön "Osta samankaltaisia tyylejä" -tuotesuositukset Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yhteenveto

Dynamics 365 Commercen "Osta samankaltaisia tyylejä" -suositusominaisuus, joka käyttää tekoälyä ja koneoppimista (AI-ML) antaakseen suosituksia visuaalisesti vastaavista tuotteista asiakkaille. Tekemällä "Osta samankaltaisia tyylejä" -suosituksia kaikille Commercen kanaville vähittäiskauppiaat voivat lisätä asiakastyytyväisyyttä auttamalla asiakkaita löytämään haluamansa helposti.

"Osta samankaltaisia tyylejä" -suositusten toiminnallisuus käyttää siementuotevalikoimien tuotekuvia etsimään ja suosittelemaan visuaalisesti samanlaisia tuotteita jälleenmyyjän tuoteluettelosta. 

"Osta samankaltaisia tyylejä" -suositukset ovat saatavilla sekä myyntipisteissä (POS) ja sähköisen kaupankäynnin kokemuksissa.

### <a name="example-scenarios"></a>Esimerkkiskenaariot

- Asiakas tarkastelee mustaa raidallista puseroa ja saa suosituksen samanlaisesta punaisesta puserosta. Asiakas valitsee suositellun tuotteen alun perin tarkasteltujen tuotteiden asemesta ja saa sen jälkeen suosituksia samankaltaisista tuotteista punaisina. 
- Asiakas käyttää "Osta samankaltaisia tyylejä" -suosituksia löytääkseen korvakorut pariksi sormukselle, jonka asiakas on kiinnostunut ostamaan.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Ota "Osta samankaltaisia tyylejä" -suositukset käyttöön Commerce Headquarters -sovelluksessa

Tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Gen2:een.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin jälleenmyyjät voivat alkaa näyttää "Osta samankaltaisia tyylejä" -suosituksia asiakkaille, seuraavia vaiheita on kaksi:

- [Ota tuotesuositukset käyttöön](enable-product-recommendations.md) Commerce Headquarters -sovelluksessa.
- Varmista, että mediasisältöpalvelin tukee HTTPS-puheluja.

Jotta suositukset-moduuli voi käyttää tuotekuvia, jälleenmyyjien on luotava tuotteen URL-osoitteet. Luo tuotteen URL-osoitteet Commerce headquartersissa seuraavasti.

1. Siirry kohtaan **Tuotekuvat**.
1. Valitse Toimintoruudussa **Määritä mediasisältömalli**.
1. Valitse **Määritä mediasisältömallin** ominaisuudet-ruudun **Median URL-osoitteet** -kohdasta **Luo URL-osoitteita**.

> [!NOTE]
> Kun otat käyttöön "Osta samankaltaisia tyylejä" -suositukset-toiminnon, tuotesuositusluetteloiden luontiprosessi alkaa. Enintään yksi päivä saattaa olla tarpeen, ennen kuin nämä luettelot ovat käytettävissä ja näkyvissä verkossa ja myyntipisteissä.

Jos haluat ottaa käyttöön "Osta samankaltaisia tyylejä" -suositukset-toiminnon Commerce Headquarters -sovelluksessa, toimi seuraavasti.

1. Mene **Toimintojen hallintaan**.
1. Etsi ja valitse käytettävissä olevien toimintojen luettelosta **Osta samankaltaisia tyylejä**.
1. Ota palvelu käyttöön valitsemalla oikeanpuoleisesta ruudusta **Ota käyttöön**.

Seuraavassa kuvassa näkyy **Osta samankaltaisia tyylejä** -ominaisuus, joka sijaitsee Commerce Headquarters -sovelluksen **toimintojen hallinta** -sivulla.

![Commerce headquartersin toimintojen hallinta -sivun Osta samankaltaisia tyylejä -ominaisuus](./media/enableshopsimilarlooks.png)

Kun edeltävät tehtävät on suoritettu, POS-päätteisiin päivittyy automaattisesti asiayhteyteen liittyvä **Osta samankaltaisia tuotteita** - paneeli. Kun valitset **Näytä lisää**, POS-päätteen käyttäjät voidaan viedä erityiseen "Osta samankaltaisia tyylejä" -sivulle, jota voidaan suodattaa edelleen.

> [!NOTE]
> Muihin tuotesuosituksiin ei vaikuta, jos poistat "Osta samankaltaisia tyylejä" -suositukset käytöstä. Lisätietoja tuotesuosituksista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Osta samankaltaisia tyylejä -painikkeen lisääminen tuotetieto sivuille Commerce site builderin avulla

Kun olet ottanut käyttöön "osta samankaltaisia lookkeja" -suositukset-toiminnon Commerce Headquarters -sovelluksessa, Commerce site Builderin vaihtoehdon avulla jälleenmyyjät voivat lisätä **Osta samankaltaisia tyylejä** -painikkeen osto-ruutuun millä tahansa tuotetietosivulla (PDP). Asiakas, joka valitsee tämän painikkeen, viedään omistautuneelle "Osta samankaltaisia tyylejä" -sivulle, joka palauttaa visuaalisesti samankaltaiset tuotteet. Tällöin asiakas voi suodattaa tuotteita käyttämällä valitsimia.

Noudata seuraavia ohjeita **Osta samankaltaisia tyylejä** -painikkeen lisäämiseksi tuotetietosivuille (PDP) Commerce site builderin avulla.

1. Avaa aiemmin luotu sivustonluontisivu, joka sisältää ostolaatikkomoduulin.
1. Valitse vasemmasta siirtymisruudusta ostolaatikkomoduuli.
1. Valitse oikeanpuoleisesta siirtymisruudusta **Ota käyttöön Osta samankaltaisia tyylejä -linkki** -valintaruutu.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**. Kun sivu on julkaistu, PDP:n mukana tulee **Osta samankaltaisia tyylejä** -painike.

Seuraavassa kuvassa on **Ota käyttöön Osta samankaltaisia tyylejä -linkki** -valintaruutu ja **Osta samankaltaisia lookkeja** -painike esimerkiksi PDP:n sivustomuodostimessa.

![Ota käyttöön Osta samankaltaisia tyylejä -linkki -valintaruutu ja Osta samanlaisia lookkeja -painike PDP:n sivustomuodostimessa](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)
