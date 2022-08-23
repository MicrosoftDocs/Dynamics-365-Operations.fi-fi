---
title: Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä
description: Tässä artikkelissa annetaan ohjeita Azure Data Lake Storage Gen 2 -ratkaisun yhdistämiseen Dynamics 365 Commerce -ympäristön yksikkösäilöön. Tämä on pakollinen vaihe ennen tuotesuositusten käyttöönottoa.
author: bebeale
ms.date: 08/31/2020
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
ms.openlocfilehash: d7995e826a838796f714ced2f30220201a157f93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284742"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä

[!include [banner](includes/banner.md)]

Tässä artikkelissa annetaan ohjeita Azure Data Lake Storage Gen 2 -ratkaisun yhdistämiseen Dynamics 365 Commerce -ympäristön yksikkösäilöön. Tämä on pakollinen vaihe ennen tuotesuositusten käyttöönottoa.

Dynamics 365 Commerce -ratkaisussa suositusten, tuotteiden ja tapahtumien käsittelyyn tarvittavat tiedot koostetaan ympäristön yksikkösäilössä. Näiden tietojen muiden Dynamics 365:n palvelujen, kuten tietojen analytiikan, yritystietojen ja mukautettujen suositusten, käyttöön asettamista varten ympäristö on yhdistettävä asiakkaan omistamaan toisen sukupolven Azure Data Lake Storage Gen 2 -ratkaisuun.

Kun edellä mainitut vaiheet on suoritettu, kaikki ympäristön yksikkösäilön asiakastiedot peilataan automaattisesti asiakkaan Azure Data Lake Storage Gen 2 -ratkaisuun. Kun suositusominaisuudet on otettu käyttöön Commerce-pääkonttorin ominaisuuksienhallinnan työtilassa, suosituspinolle annetaan käyttöoikeus samaan Azure Data Lake Storage Gen 2 -ratkaisuun.

Asiakastiedot pysyvät koko prosessin ajan suojattuna ja asiakkaiden hallinnassa.

## <a name="prerequisites"></a>Edellytykset

Dynamics 365 Commerce -ympäristön yksikkösäilön on oltava yhdistettynä Azure Data Lake Gen Storage Gen2 -tiliin ja siihen liittyviin palveluihin.

Lisätietoja Azure Data Lake Storage Gen 2:sta ja sen määrityksestä: [Azure Data Lake Storage Gen 2:n virallinen dokumentaatio](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Määritysvaiheet

Tämä osa sisältää määritysvaiheet, jotka ovat tarpeen, jotta Azure Data Lake Storage Gen 2 voidaan ottaa käyttöön ympäristössä, joka liittyy tuotesuosituksiin.
Lisätietoja Azure Data Lake Storage Gen 2 -lisäosan käyttöön tarvittavista vaiheista on ohjeaiheessa [Määritä yksikkösäilö käytettäväksi Data Lakessa](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Azure Data Lake Storagen käyttöönotto ympäristössä

1. Kirjaudu ympäristön taustajärjestelmäportaaliin.
1. Etsi **Järjestelmäparametrit** ja siirry **Tietoyhteydet**-välilehteen. 
1. Määritä **Ota Data Lake -integrointi käyttöön** -parametrin arvoksi **Kyllä**.
1. Syötä sitten seuraavat vaaditut tiedot:
    1. **Sovellustunnus** // **Sovelluksen salauskoodi** // **DNS-nimi** – Tarvitaan siihen KeyVault-säilöön yhdistämistä varten, johon Azure Data Lake Storage -salauskoodi on tallennettu.
    1. **Salainen nimi** – KeyVaultiin tallennettu ja Azure Data Lake Storage -todennukseen käytetty salainen nimi.
1. Tallenna muutoksesi sivun vasemmassa yläkulmassa.

Seuraavassa kuvassa näkyy esimerkki Azure Data Lake Storage -määrityksessä.

![Esimerkki Azure Data Lake Storage -määrityksestä.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Azure Data Lake Storage -yhteyden testaaminen

1. Testaa yhteys KeyVaultiin **Testaa Azure Vault** -linkin avulla.
1. Testaa yhteys Azure Data Lake Storageen käyttämällä **Testaa Azure-tallennustila** -linkin avulla.

> [!NOTE]
> Jos toinen edellä mainituista testeistä epäonnistuu, varmista, että kaikki edellä lisätyt KeyVault-tiedot ovat oikein. Kokeile sen jälkeen uudelleen.

Kun kaikki yhteystestit ovat onnistuneet, sinun on otettava yksikkötallennustilan automaattinen päivitys käyttöön.

Ota yksikkötallennustilan päivitys käyttöön seuraavia vaiheita noudattamalla.

1. Etsi kohdetta **Entiteettitallennustila**.
1. Siirry vasemmalla olevassa luettelossa **RetailSales**-kirjaukseen ja valitse **Muokkaa**.
1. Varmista, että **Automaattinen päivitys käytössä** -kohdan arvoksi on määritetty **Kyllä**, valitse **Päivitys** ja sitten **Tallenna**.

Seuraavassa kuvassa näkyy esimerkki yksikkösäilöstä, jossa automaattinen päivitys on käytössä.

![Esimerkki yksikkötallennustilasta, jossa automaattinen päivitys on käytössä.](./media/exampleADLSConfig2.png)

Azure Data Lake Storage on nyt määritetty ympäristölle. 

Jos et ole vielä suorittanut niitä, suorita ympäristön [tuotesuositusten ja mukautusten käyttöönoton](enable-product-recommendations.md) vaiheet.

## <a name="additional-resources"></a>Lisäresurssit

[Yksikkösäilön määrittäminen saataville Data Lake -säilönä](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
