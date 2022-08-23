---
title: Vastaavien tuotteiden kuvaukseen perustuvien suositusten ottaminen käyttöön
description: Tässä artikkelissa kuvataan, kuinka voit ottaa käyttöön "Tuotteet, joissa samankaltainen kuvaus" -tuotesuositukset Microsoft Dynamics 365 Commercessa.
author: bebeale
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: c15122d15660144f46528bd8c575029bf9d966c6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274975"
---
# <a name="enable-shop-similar-description-recommendations"></a>Vastaavien tuotteiden kuvaukseen perustuvien suositusten ottaminen käyttöön

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka voit ottaa käyttöön "Tuotteet, joissa samankaltainen kuvaus" -tuotesuositukset Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commercen "Tuotteet, joissa samankaltainen kuvaus" -suositusominaisuus, joka käyttää tekoälyä ja koneoppimista (AI-ML) antaakseen suosituksia tuotteista, joiden kuvaukset ovat samankaltaisia, kuin mitä asiakas etsii. Tekemällä "Tuotteet, joissa samankaltainen kuvaus" -suosituksia kaikille Commercen kanaville vähittäiskauppiaat voivat auttaa asiakkaita löytämään haluamansa helposti.

"Tuotteet, joissa samankaltainen kuvaus" -suositusten toiminnallisuus käyttää alkuperäisen tuotteen nimeä ja kuvausta etsimään ja suosittelemaan samanlaisia tuotteita jälleenmyyjän tuoteluettelosta.

"Tuotteet, joissa samankaltainen kuvaus" -suositukset ovat saatavilla sekä myyntipisteissä (POS) ja sähköisen kaupankäynnin kokemuksissa.

## <a name="example-scenarios"></a>Esimerkkiskenaariot

Seuraavissa esimerkkiskenaarioissa kuvataan, millaisia suosituksia "Tuotteet, joissa samankaltainen kuvaus" -toiminnoilla voi olla:

- Asiakas katselee retrotyylisiä paksusankaisia silmälaseja ja saa joukon suosituksia muista samantapaisista laseista, joissa on sama tyyli, vähittäismyyjän toimialan mukaisesti.
- Asiakas käyttää "Tuotteet, joissa samankaltainen kuvaus" -suosituksia löytääksen samankaltaisia kahvimakuja kuin mitä hän vähittäismyyjältä aiemmin osti.

## <a name="set-up-shop-similar-description-recommendations"></a>"Tuotteet, joissa samankaltainen kuvaus" -suositusten määrittäminen

Tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Storage Gen2:een.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin asiakkaille voidaan näyttää "Tuotteet, joissa samankaltainen kuvaus" -suositukset, sinun on täytettävä seuraavat edellytykset:

- [Ota tuotesuositukset käyttöön](enable-product-recommendations.md) Commerce Headquarters -sovelluksessa.
- Varmista, että mediasisältöpalvelin tukee HTTPS-puheluja.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>Ota "Tuotteet, joissa samankaltainen kuvaus" -suositusten ominaisuus käyttöön

Jos haluat ottaa käyttöön "Tuotteet, joissa samankaltainen kuvaus" -suositukset-toiminnon Commerce headquarters -sovelluksessa, toimi seuraavasti.

1. Etsi ja valitse **Tuotteet, joissa samankaltainen kuvaus** **Toimintohallinta**-työtilan käytettävissä olevien ominaisuuksien luettelosta.
1. Valitse oikeanpuoleisesta ruudusta **Ota käyttöön**.

> [!NOTE]
> Kun otat ominaisuuden käyttöön, järjestelmä alkaa luoda tuotesuositusluetteloita. Saattaa kulua vuorokausi, ennen kuin nämä luettelot ovat käytettävissä ja näkyvissä verkossa ja myyntipisteissä.
>
> Jos poistat toiminnon käytöstä, se ei vaikuta muuntyyppisiin tuotesuosituksiin. Lisätietoja tuotesuosituksista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Tuotteet, joissa samankaltainen kuvaus -painikkeen lisääminen tuotetietosivuille

Kun olet ottanut käyttöön "Tuotteet, joissa samankaltainen kuvaus" -suositukset-toiminnon Commerce headquarters -sovelluksessa, voit lisätä **Tuotteet, joissa samankaltainen kuvaus** -painikkeen ostoruutuun millä tahansa tuotetietosivulla (PDP). Asiakas, joka valitsee tämän painikkeen, viedään erilliselle **Tuotteet, joissa samankaltainen kuvaus** -sivulle, joka näyttää samankaltaiset tuotteet. Näin asiakas voi suodattaa tuotteita käyttämällä valitsimia.

Noudata seuraavia ohjeita **Tuotteet, joissa samankaltainen kuvaus** -painikkeen lisäämiseksi tuotetietosivuille (PDP) Commercen sivustonmuodostimen avulla.

1. Avaa aiemmin luotu sivustonluontisivu, joka sisältää ostolaatikkomoduulin.
1. Valitse vasemmasta siirtymisruudusta ostolaatikkomoduuli.
1. Valitse oikeanpuoleisesta ruudusta **Ota käyttöön Tuotteet, joissa samankaltainen kuvaus -linkki** -valintaruutu.
1. Valitse **Tallenna**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen. Kun sivu on julkaistu, PDP sisältää **Tuotteet, joissa samankaltainen kuvaus** -painikkeen.

Seuraavassa kuvassa on **ota käyttöön Tuotteet, joissa samankaltainen kuvaus -linkki** -valintaruutu ja **Tuotteet, joissa samankaltainen kuvaus** -painike esimerkkituotetietosivulla sivustomuodostimessa.

![Ota käyttöön Tuotteet, joissa samankaltainen kuvaus -linkin valintaruutu ja Tuotteet, joissa samankaltainen kuvaus -painike tuotetietosivulla sivuston luontiohjelmassa.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Ota tuotesuositukset käyttöön](enable-product-recommendations.md)

[Vastaavien tuotteiden ostosuositusten ottaminen käyttöön](shop-similar-looks.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
