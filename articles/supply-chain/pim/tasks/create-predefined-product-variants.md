---
title: Luo ennalta määritetyt tuotevariantit
description: Tässä menettelyssä selvitetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä.
author: t-benebo
manager: tfehr
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acd2e3f1464dfed09ee24764270b06970b747d7c
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938199"
---
# <a name="predefined-product-variants"></a>Ennalta määritellyt tuotevariantit

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Esimerkkiskenaario: Luo ennalta määriteltyjä tuotevariantteja

Tässä esimerkkiskenaariossa näytetään tuotevariantien luonti päätuotteelle käyttämällä tuotedimensioiden yhdistelmiä.

### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Tämän skenaarion noudattaminen tässä ehdotettuja arvoja käyttämällä edellyttää, että demotiedot on asennettu ja että *USMF*-yritys on valittu.

### <a name="step-1-create-a-product-master"></a>Vaihe 1: Luo päätuote

Päätuotteen luominen:

1. Siirry kohtaan **Tuotetietojen hallinta > Tuotteet > Päätuotteet**.
1. Valitse **Uusi**.
1. Jos **Tuotenumero**-kentässä ei vielä ole numeroa näkyvissä, kirjoita arvo. Tämä vaaditaan vain, jos kentälle ei ole määritetty numerosarjaa.
1. Syötä **Tuotenimi** -kenttään nimi.
1. Valitse **Tuotedimensioryhmä**-kentästä tuotedimensioryhmä *SizeCol* (koko ja väri).
1. Luo ja avaa uusi päätuote valitsemalla **OK**.

### <a name="step-2-add-product-dimensions"></a>Vaihe 2: Lisää tuotedimensiot

Tässä esimerkissä havainnollistetaan, kuinka tuotedimensiot voi antaa käsin. Voit myös valita koko-, väri- tai tyyliryhmän, joka sisältää haluamasi tuotedimension arvot.

Tuotedimensioiden lisääminen:

1. Kun uusi päätuote on vielä avoinna, valitse **Tuotedimensiot** toimintoruudusta.
1. Avaa **Koko**-välilehti ja lisää ruudukkoon rivi valitsemalla työkaluriviltä **Uusi**. Tee uudelle riville seuraavat asetukset:
    - **Koko:** Valitse koon arvo.
    - **Nimi:** Syötä koolle nimi.
1. Valitse työkaluriviltä **Uusi** ja lisää toinen koko ruudukkoon, jossa on uusi **Koko** ja **Nimi**.
1. Avaa **Värit**-välilehti ja lisää ruudukkoon rivi valitsemalla työkaluriviltä **Uusi**. Tee uudelle riville seuraavat asetukset:
    - **Väri:** Valitse väriarvo.
    - **Nimi:** Syötä värille nimi.
1. Valitse työkaluriviltä **Uusi** ja lisää toinen väri ruudukkoon, jossa on uusi **Väri** ja **Nimi**.
1. Valitse **Tallenna**.
1. Voit palata uuteen päätuotteeseen sulkemalla sivun.

### <a name="step-3-generate-product-variants"></a>Vaihe 3: Luo tuotevariantit

> [!NOTE]
> Tässä osassa kuvataan, miten tuotevariantteja luodaan, kun *Muuttujaehdotukset-sivun parannukset* -toiminto ei ole käytössä. Seuraavassa osassa on tietoja siitä, miten tuotevariantteja luodaan, kun tämä ominaisuus on käytettävissä.

Tuotevarianttien luonti:

1. Kun uusi päätuote on vielä avoinna, valitse **Tuotevariantit** toimintoruudusta.
1. Valitse toimintoruudussa **Muuttujaehdotukset**.
1. Järjestelmä luo luettelon, joka sisältää kaikki mahdolliset tuotteeseen määritetyt koko- ja väriyhdistelmät. Valitse työkalurivillä **Valitse kaikki**.
    - Tässä esimerkissä valitse kaikki mahdolliset muuttujat. Jos haluat käyttää vain mahdollisen tuotedimensioyhdistelmän alijoukkoa, valitse vain tarvittavat valintaruudut.  
1. Valitse **Luo**.
1. Valitse **Tallenna**.

## <a name="improved-variant-suggestions"></a>Parannetut muuttujaehdotukset

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

*Muuttujaehdotukset-sivun parannukset* -ominaisuus parantaa **Muuttujaehdotukset**-sivua niiden yritysten suorituskykyyn ja käytettävyyteen liittyvien ongelmien käsittelemiseksi, joilla on suuri määrä tuotedimensioyhdistelmiä. Paranneltu prosessi, jossa valitaan tuotedimensioarvot, joiden perusteella muuttujaehdotuksia luodaan, nopeuttaa ja helpottaa asianmukaisten tuotevarianttien tunnistamista ja vapauttamista.

Tämä ominaisuus lisää seuraavat parannukset:

- **Varianttiehdotusten lykätty luominen::** **Varianttiehdotukset**-sivun ensimmäisellä avauskerralla ei enää näytetä ehdotuksia. Sen sijaan sinun on nimenomaisesti valittava haluamasi arvot ja luotava yhdistelmät valitsemalla **Ehdota**-painike. Näin prosessi on näkyvämpi ja vuorovaikutteisempi.
- **Dimension arvojen valitseminen:** Kun dimension arvoja on useita, käyttäjä haluaa yleensä luoda varianttiehdotuksia, jotka sisältävät vain joitakin arvoja (kuten uuden väri- tai tyylijoukon esittely). Tämän parannetun suunnittelun avulla käyttäjä voi valita ne dimension arvot, joille tuotevarianttiehdotukset halutaan luoda. Tämä kasvattaa suuresti ehdotettujen varianttien relevanssia ja parantaa sekä järjestelmän suorituskykyä että käyttäjän tuottavuutta.

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a>Muuttujaehdotus-sivun parannustoiminnon ottaminen käyttöön

Ennen kuin voit käyttää *Muuttujaehdotukset-sivun parannukset* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Tuotetietojen hallinta*
- **Ominaisuuden nimi:** *Muuttujaehdotukset-sivun parannukset*

### <a name="work-with-the-improved-variant-suggestions"></a>Paranneltujen muuttujaehdotusten käyttäminen

Tuotevarianttiehdotusten luominen, kun *Muuttujaehdotukset-sivun parannukset* -toiminto on käytössä:

1. Avaa tai luo päätuote ja lisää tarvittavat tuotedimensiot siihen edellisessä osassa kuvatulla tavalla.
1. Kun päätuote on avoinna, valitse **Tuotevariantit** toimintoruudusta.
1. Valitse toimintoruudussa **Muuttujaehdotukset**.
1. Valitse kullekin dimensiolle arvot, joita haluat käyttää.
1. Valitse yläreunan työkaluriviltä **Ehdota**.
1. Järjestelmä luo luettelon, joka sisältää kaikki mahdolliset valitut koko- ja väriyhdistelmät. Valitse **Ehdotetut muuttujat** -pikavälilehdessä kunkin käytettävän tuotedimensioyhdistelmän valintaruutu tai valitse **Valitse kaikki** työkalurivillä valitaksesi ne kaikki.  
1. Valitse **Luo** lisätäksesi muuttujat nykyiseen päätuotteeseen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
