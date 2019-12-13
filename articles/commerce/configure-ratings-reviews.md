---
title: Määritä luokitukset ja arvostelut
description: Tässä ohjeaiheessa kerrotaan, miten sähköisen kaupankäynnin sivusto määritetään niin, että se näyttää asiakasluokituksia ja -arvostelut Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770478"
---
# <a name="configure-ratings-and-reviews"></a>Määritä luokitukset ja arvostelut

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten sähköisen kaupankäynnin sivusto määritetään niin, että se näyttää asiakasluokituksia ja -arvostelut Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Sähköisen kaupankäynnin sivustojen luokitukset ja arvostelut auttavat asiakkaita saamaan tietoja tuotteista ennen ostopäätöksen tekemistä. NIiden avulla saadaan selville, mitä muut asiakkaat ajattelevat kyseisistä tuotteista. Sähköisen kaupankäynnin sivustoissa luokitukset ja arvostelut ovat myös keino, jolla kerätään asiakaspalautetta tuotteista. 

Luokitukset näkyvät tuoteluettelo-, luokkaluettelo- ja hakutulossivuilla sekä muilla sivuston sivuilla. Luokitusten histogrammit ja tuotearvostelut näytetään tuotetietosivuilla (PDP:t). l**Kirjoita arvostelu** -painikkeen avulla asiakkaat voivat lähettää tuotetta koskevia luokituksia ja arvosteluja.

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

![Kirjoita arvostelu -valintaikkuna](media/rnr-eCommerce-write-review-module.png)

Seuraavassa taulukossa on Kirjoita arvostelu -moduulin ominaisuus, joka on määritettävä muokkaustyökalussa.

| Ominaisuuden nimi | Arvo        | Ominaisuuden kuvaus                 |
|---------------|--------------|--------------------------------------|
| Nimi          | Kirjoita arvostelu | Kirjoita arvostelu -moduulin nimi. |

### <a name="ratings-histogram-module"></a>Luokitusten histogrammin moduuli

Luokitusten histogrammin moduulissa on luokitusten histogrammi. Tämä moduuli tulee yleensä näkyviin Kirjoita arvostelu -moduulin ja tuotearvosteluluettelomoduulin väliin PDP-sivulla.

Luokitusten histogrammin moduulia ei tarvitse määrittää. Moduuli on ainoastaan lisättävä PDP-malliin. 

Seuraavissa kuvissa näkyy, miltä PDP-malli näyttää Dynamics 365 Commerce -sovelluksessa, kun luokitusten ja arvostelujen moduulit on määritetty näytettäväksi PDP-sivuilla.

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

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Sivuston määrittäminen niin, että se näyttää luokitukset ja arvostelut

Luokitusten ja arvostelujen määrityksen arvot, kuten vuokraajan tunnus, arvostelun tekstin pituus ja luokituksen otsikon pituus, määritetään sivustotasolla. 

Voit määrittää sivuston näyttämään luokitukset ja arvostelut seuraavasti. 

1. Siirry kohtaan **Aloitus \> Sivustot**.
1. Valitse sivuston nimi. 
1. Siirry kohtaan **Sivuston hallinta \> Laajennettavuus**. 
1. Syötä **Arvostelun tekstin enimmäispituus** -kenttään arvostelun tekstin merkkien enimmäismäärä (esimerkiksi **1 000**). 
1. Syötä **Arvostelun otsikon enimmäispituus** -kenttään arvostelun otsikoiden merkkien enimmäismäärä (esimerkiksi **55**). 
1. Valitse **Tallenna ja julkaise**. 

Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.

![Sivuston määrittäminen niin, että se näyttää luokitukset ja arvostelut](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Tuoteluokituksen linkittäminen PDP:n Arvostelut-osaan

Tuoteluokitus näkyy PDP:n yläosassa olevan tuotteen otsikon alla. Tuoteluokitus voidaan määrittää niin, että se on linkitetty saman PDP:n **Arvostelut**-osaan. 

Voit linkittää tuoteluokituksen PDP:n osan **Arvostelut**-osaan seuraavasti.

1. Avaa PDP-malli. 
1. Siirry kohtaan **Ostoruudun säilömoduulin asetukset**.
1. Valitse **Ostoruutu**-kohdassa **Tuoteluokitukset** ja valitse sitten **Linkitä napsautus täydellisten arviointien moduuliin** -valintaruutu.

Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.

![Tuoteluokituksen linkittäminen PDP:n Arvostelut-osaan](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Tietosuoja- ja käytäntösivun linkin määrittäminen

Voit määrittää tietosuoja- ja käytäntösivun linkin seuraavasti.

1. Siirry kohtaan **Aloitus \> Sivustot**.
1. Valitse sivuston nimi. 
1. Siirry kohtaan **Sivuston hallinta \> Laajennettavuus**
1. Valitse **Reitit**-välilehdessä **RNR - tietosuoja ja käytäntö** -kohdassa **Lisää linkki**. Jos linkki on jo syötetty ja haluat korvata sen, valitse linkki. 
1. Valitse **Lisää linkki** -valintaikkunassa tietosuoja-ja käytäntösivun linkki ja valitse sitten **OK**. 
1. Valitse **Tallenna ja julkaise**. 

Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.

![Tietosuoja- ja käytäntösivun linkin määrittäminen](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Osallistu käyttääksesi luokituksia ja arvosteluja](opt-in-ratings-reviews.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Tuoteluokitusten synkronoiminen Dynamics 365 Retailissa](sync-product-ratings.md)
