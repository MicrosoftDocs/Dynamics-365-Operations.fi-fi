---
title: Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille
description: Tässä aiheessa kuvataan, kuinka määritetään tuotemäärän rajat yritysten (B2B) verkkokauppasivustoissa.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e9f14bc9aa6586e87f3e8ccb82e63d0ec2e46534
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799778"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka määritetään tuotemäärän rajat yritysten (B2B) verkkokauppasivustoissa.

Useimmilla tuotteilla on ryhmittelyn määrittävä mittayksikkö. Ryhmittely vaikuttaa siihen, miten tuotteita voidaan myydä. Joillakin tuotteilla saattaa olla määrille lisäryhmittelyitä. Tämä ryhmittely määrittää, voidaanko tuotteet myydä yksittäisinä yksikköinä vai ryhminä, ja se, onko olemassa vähimmäis- tai enimmäistilausmäärän raja, jota on noudatettava.

Määrän rajaustoiminnon avulla voidaan varmistaa, että Microsoft Dynamics 365 Commercessa (oletustilausasetuksissa tai Commercen sivuston muodostintyökalun sivuston asetuksissa) konfiguroituja vähimmäis-, enimmäis-, moni- ja vakiomääriä sovelletaan asiakastilauksiin, jotka tehdään verkkokauppasivustossa. Tuotemäärän rajoja ei tueta myyntipisteissä ja soittokeskuksissa.

Monet vähittäiskauppiaat tarjoavat asiakastilausten (eli erikoistilausten) mahdollisuuden täyttääkseen erilaisia eri tuote- ja palveluvaatimuksia. Seuraavassa on joitakin tyypillisiä skenaarioita:

- Asiakas haluaa, että tietyt tuotteet tai variantit myydään muutaman kappaleen erissä.
- Asiakas haluaa noutaa tuotteet myymälästä tai sijainnista, joka on eri kuin myymälä tai sijainti, josta asiakas osti nämä tuotteet. Myymälöiden pakkausstandardit eroavat kuitenkin online-myynnin jakelun pakkausstandardeista.
- Asiakas haluaa ostaa rajoitetun painoksen tuotteen, jolla on suurin mahdollinen määrä ostettavalle nimikkeelle.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Oletusarvoisten tilausasetusten ominaisuuden käyttöönottaminen Commerce headquarters -sovelluksessa

Ennen kuin tuotemäärän rajat voidaan määrittää, tilausten oletusasetusten ominaisuus on otettava käyttöön Commerce headquartersissa.

Noudata seuraavia ohjeita ottaaksesi oletusarvoisten tilausasetusten ominaisuuden käyttöön.

1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
1. Etsi ja valitse **Tue sivuston ja oletusarvoisia tilausasetuksia asiakastilauksessa** -ominaisuus.
1. Valitse oikeanpuoleisen ruudun alareunasta **Ota käyttöön nyt**. 

## <a name="define-quantity-settings"></a>Määräasetusten määrittäminen 

Voit määrittää määrän asetukset **Tilauksen oletusasetukset** -sivulla.

Voit määrittää määrän asetukset noudattamalla seuraavia vaiheita. 

1. Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Vapautetut tuotteet luokittain**.
1. Valitse vapautettu tuote.
1. Valitse toimintoruudussa **Hallitse varastoa** -välilehden **Tilauksen asetukset** -ryhmästä **Tilauksen oletusasetukset**. 
1. Määritä **Tilauksen oletusasetukset** -sivun **Myyntitilaus**-pikavälilehden **Myyntimäärä** -osassa uotteetn myyntimäärät:

    - **Kerrannainen** – Määrä, jonka mukaan tuotteen voi ostaa.
    - **Tilauksen vähimmäismäärä** – Ostettavan tuotteen vähimmäismäärä.
    - **Tilauksen enimmäismäärä** – Ostettavan tuotteen enimmäismäärä.
    - **Tilauksen vakiomäärä** – Oletusmäärä, joka syötetään automaattisesti, kun tuote valitaan.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Ota B2B-tilauksen määrärajatoiminto käyttöön Commercen sivustonmuodostimessa

Ota B2B-tilauksen määrärajatoiminto käyttöön Commercen sivustonmuodostimessa seuraavasti.

1. Siirry kohtaan **Sivuston asetukset \> Laajennukset**.
1. Valitse kohdan **Ota käyttöön tilausten määrärajat** avattavasta valikosta **Käytössä B2B-asiakkaille**. 

> [!NOTE] 
> Päivitetyt sivustonmuodostajan asetukset tulevat voimaan vasta, kun app.settings.json-tiedosto on päivitetty. Lisätietoja on ohjeaiheessa [SDK:n ja moduulikirjaston päivitykset](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Lisäresurssit

[B2B-verkkokauppasivuston määrittäminen](set-up-b2b-site.md)

[Organisaation mallinnushierarkioiden luominen B2B-organisaatioille](org-model.md)

[Liikekumppanikäyttäjien hallinta yritystenvälisen yhteistyön sähköisen kaupankäynnin sivustoissa](manage-b2b-users.md)

[Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]