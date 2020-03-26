---
title: ADLS:n käyttöönotto Dynamics 365 Commerce -ympäristössä
description: Tässä ohjeaiheessa selitetään, miten voit ottaa Azure Data Lake Storagen (ADLS:n) käyttöön Dynamics 365 Commerce -ympäristöä varten. Tämä on edellytys tuotesuositusten käyttöönotolle.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 553e1512ba72559923403eef741ce08222172a09
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127764"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>ADLS:n käyttöönotto Dynamics 365 Commerce -ympäristössä

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa selitetään, miten voit ottaa Azure Data Lake Storagen (ADLS:n) käyttöön Dynamics 365 Commerce -ympäristöä varten. Tämä on edellytys tuotesuositusten käyttöönotolle.

## <a name="overview"></a>Yleiskatsaus

Dynamics 365 Commerce -ratkaisussa kaikkia tuote- ja tapahtumatietoja seurataan ympäristön yksikkösäilöön. Näiden tietojen muiden Dynamics 365:n palvelujen, kuten tietojen analytiikan, yritystietojen ja mukautettujen suositusten, käyttöön asettamista varten ympäristö on yhdistettävä asiakkaan omistamaan toisen sukupolven Azure Data Lake Storage (ADLS) -ratkaisuun.

Koska ADLS on määritetty ympäristössä, kaikki tarvittavat tiedot peilataan yksikkösäilöstä samalla, kun ne ovat edelleen suojattuja ja asiakkaan valvonnassa.

Jos myös tuotesuositukset tai mukautetut suositukset ovat käytössä ympäristössä, tuotesuositusten pinolle myönnetään käyttöoikeus ADLS:n varattuun kansioon asiakastietojen noutamista ja niihin perustuvien suositusten laskemista varten.

## <a name="prerequisites"></a>Edellytykset

Asiakkailla on oltava ADLS määritettynä omistamassaan Azure-tilauksessa. Tässä ohjeaiheessa ei käsitellä Azure-tilauksen hankkimista eikä ADLS-yhteensopivan säilötilin määrittämistä.

Lisätietoja ADLS:stä on kohdassa [ADLS:n virallinen dokumentaatio](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Määritysvaiheet

Tässä osassa käsitellään ADLS:n ympäristössä käyttöön ottamisen edellyttämät määritysvaiheet.

### <a name="enable-adls-in-the-environment"></a>ADLS:n käyttöönotto ympäristössä

1. Kirjaudu ympäristön taustajärjestelmäportaaliin.
1. Etsi **Järjestelmäparametrit** ja siirry **Tietoyhteydet**-välilehteen. 
1. Määritä **Ota Data Lake -integrointi käyttöön** -parametrin arvoksi **Kyllä**.
1. Määritä **Data Laken vähittäinen päivitys** -parametrin arvoksi **Kyllä**.
1. Syötä sitten seuraavat vaaditut tiedot:
    1. **Sovellustunnus** // **Sovelluksen salauskoodi** // **DNS-nimi** – Tarvitaan siihen KeyVault-säilöön yhdistämistä varten, johon ADLS-salauskoodi on tallennettu.
    1. **Salainen nimi** – KeyVaultiin tallennettu ja ADLS-todennukseen käytetty salainen nimi.
1. Tallenna muutoksesi sivun vasemmassa yläkulmassa.

Seuraavassa kuvassa näkyy esimerkki ADLS-määrityksessä.

![Esimerkki ADLS-määrityksestä](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>ADLS-yhteyden testaaminen

1. Testaa yhteys KeyVaultiin **Testaa Azure Vault** -linkin avulla.
1. Testaa yhteys ADLS:ään käyttämällä **Testaa Azure-tallennustila** -linkin avulla.

> [!NOTE]
> Jos testit epäonnistuvat, tarkista uudelleen, että kaikki edellä lisätyt KeyVault-tiedot ovat oikein. Kokeile sen jälkeen uudelleen.

Kun kaikki yhteystestit ovat onnistuneet, sinun on otettava yksikkötallennustilan automaattinen päivitys käyttöön.

Ota yksikkötallennustilan päivitys käyttöön seuraavia vaiheita noudattamalla.

1. Etsi kohdetta **Entiteettitallennustila**.
1. Siirry vasemmalla olevassa luettelossa **RetailSales**-kirjaukseen ja valitse **Muokkaa**.
1. Varmista, että **Automaattinen päivitys käytössä** -kohdan arvoksi on määritetty **Kyllä**, valitse **Päivitys** ja sitten **Tallenna**.

Seuraavassa kuvassa näkyy esimerkki yksikkösäilöstä, jossa automaattinen päivitys on käytössä.

![Esimerkki yksikkötallennustilasta, jossa automaattinen päivitys on käytössä](./media/exampleADLSConfig2.png)

ADLS on nyt määritetty ympäristölle. 

Jos et ole vielä suorittanut niitä, suorita ympäristön [tuotesuositusten ja mukautusten käyttöönoton](enable-product-recommendations.md) vaiheet.

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Ota tuotesuositukset käyttöön](enable-product-recommendations.md)

[Ota kohdennetut suositukset käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

[Suositusluettelojen lisääminen sähköisen kaupankäynnin sivustoon](add-reco-list-to-page.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)


