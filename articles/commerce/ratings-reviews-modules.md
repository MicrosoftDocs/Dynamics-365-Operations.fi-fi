---
title: Luokitusten ja arvosteluiden moduulit
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Commercen tuotetietojen sivuilla käytettäviä luokitus- ja arviointimoduuleja.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 85fb1272103eed7d6e44635b7c20438471d96b34
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817727"
---
# <a name="ratings-and-reviews-modules"></a>Luokitusten ja arvosteluiden moduulit

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Commercen tuotetietojen sivuilla (PDP) käytettäviä luokitus- ja arviointimoduuleja.

## <a name="overview"></a>Yleiskatsaus

Sähköisen kaupankäynnin sivustojen luokitukset ja arvostelut auttavat asiakkaita saamaan tietoja tuotteista ennen ostopäätöksen tekemistä. Niiden avulla voi myös kerätä asiakkaiden tuotteita koskevaa palautetta. 

Luokitukset näkyvät tuoteluettelo-, luokkaluettelo- ja hakutulossivuilla sekä muilla sivuston sivuilla. 

Luokitusten histogrammit ja tuotearvostelut näytetään PDP-sivuilla. l**Kirjoita arvostelu** -painikkeen avulla asiakkaat voivat lähettää tuotetta koskevia luokituksia ja arvosteluja. Näitä PDP-toimintoja hallitsevat luokitus- ja tarkistusmoduulit.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Luokitusten ja arvosteluiden moduulit PDP-sivuilla 

Kolme moduulia näyttävät luokitukset ja arvostelut PDP-sivujen yhteenvedoissa seuraavasti:
- Kirjoita arvostelu -moduuli
- Tuotearvosteluluettelomoduuli
- Luokitusten histogrammin moduuli
 
Seuraavassa kuvassa näytetään, miltä luokitusten ja arvosteluiden moduulit näyttävät PDP-sivulla.

![Luokitusten ja arvosteluiden moduulit PDP-sivulla](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Lisätietoja PDP-mallien ja -asettelujen optimoimisesta niin, että voit jakaa luokitusten ja arvosteluiden moduulien määritykset useiden PDP-sivujen kanssa sähköisen kaupankäynnin sivustossa, on kohdassa [Mallien ja asettelujen yleiskatsaus](templates-layouts-overview.md).

Seuraavassa kuvassa on tietoja siitä, miten **Lisää moduuli** -valintaikkuna esittää luokitusten ja arvosteluiden moduulit Dynamics 365 Commerce -sovelluksessa.
![Lisää moduuli -valintaikkuna](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Kirjoita arvostelu -moduuli

Kirjoita arvostelu -moduuli sisältää **Kirjoita arvostelu** -painikkeen, jonka avulla käyttäjät voivat kirjautua sisään, määrittää luokituksen ja kirjoittaa tuotetta koskevan arvostelun. Tämän moduulin avulla käyttäjät voivat myös muokata aiemmin lähettämiään luokituksia ja arvosteluita. Tämä moduuli näkyy yleensä luokitusten histogrammi -ja tuotearvosteluluettelomoduulien yläpuolella PDP-sivulla.
Seuraavassa kuvassa on **Kirjoita arvostelu** -valintaikkuna, joka näkyy, kun asiakas valitsee **Kirjoita arvostelu** -kohdan. Asiakas voi tämän valintaikkunan avulla lähettää luokituksen ja arvostelun.
![Kirjoita arvostelu -valintaikkuna](media/rnr-eCommerce-write-review-module.png) Seuraavassa taulussa ovat kirjoita arvostelu -ominaisuus, joka on määritettävä luontityökalussa.
| Ominaisuuden nimi | Arvo        | Ominaisuuden kuvaus                 |
|---------------|--------------|--------------------------------------|
| Nimi          | Kirjoita arvostelu | Kirjoita arvostelu -moduulin nimi. |

### <a name="ratings-histogram-module"></a>Luokitusten histogrammin moduuli

Luokitusten histogrammin moduulissa on luokitusten histogrammi. Tämä moduuli tulee yleensä näkyviin Kirjoita arvostelu -moduulin ja tuotearvosteluluettelomoduulin väliin PDP-sivulla.
Luokitusten histogrammin moduulia ei tarvitse määrittää. Moduuli on ainoastaan lisättävä PDP-malliin. Seuraavissa kuvissa näkyy, miltä PDP-malli näyttää Dynamics 365 Commerce -sovelluksessa, kun luokitusten ja arvostelujen moduulit on määritetty näytettäväksi PDP-sivuilla.
![PDP-malli, kun luokitukset ja arvostelut on määritetty näytettäväksi PDP-sivuilla](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Tuotearvosteluluettelomoduuli

Tuotearvosteluluettelomoduulissa on tuotearvosteluluettelo sekä lajittelu-, suodatus- ja sivutusvaihtoehdot. Tämä moduuli tulee yleensä näkyviin luokitusten histogrammin moduulin jälkeen PDP-sivulla.
Seuraavassa taulukossa on tuotearvosteluluettelomoduulin ominaisuudet, jotka on määritettävä muokkaustyökalussa.

| Ominaisuuden nimi              | Arvo | Ominaisuuden kuvaus |
|----------------------------|-------| ---------------------|
| Kullakin sivulla näytettävät arvostelut | 10    | Niiden arvosteluiden määrä, jotka tulee näyttää kerralla PDP-sivulla. **Seuraava**- ja **Edellinen**-painikkeet ovat mukana, jotta käyttäjät voivat liikkua arvostelusivuilla. |

#### <a name="ratings-histogram--summary-view"></a>Luokitusten histogrammi – Yhteenvetonäkymä

Tuotearvosteluluettelomoduuli sisältää paikan, jossa voit lisätä luokitusten histogrammin moduulin. Seuraavassa kuvassa näkyy, miten voit lisätä luokitusten histogrammin moduulin tuotearvosteluluettelomoduuliin Dynamics 365 Commerce -sovelluksessa.

![Luokitusten histogrammin moduulin lisääminen tuotearvosteluluettelomoduuliin](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
