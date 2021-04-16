---
title: Tuotteen elinkaaren tila – yleiskatsaus
description: Tuotteen elinkaaren tila kirjaa julkaistun tuotteen tai tuotevariantin elinkaaren tilan.
author: cvocph
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 1def67750fe6328087fe6bf7eeb22105232390fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820199"
---
# <a name="product-lifecycle-state-overview"></a>Tuotteen elinkaaren tila – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tuotteen elinkaaren tila kirjaa julkaistun tuotteen tai tuotevariantin elinkaaren tilan. Tuotteen elinkaaren tilat määrittää käyttäjä, yleensä tuotepäällikkö tai tuotteen päätietojen hallinta. Tietty elinkaaren tila voi vaikuttaa tiettyihin liiketoimintaprosesseihin, kuten pääsuunnitteluun.

Vapautettu tuote tai tuotevariantti voidaan liittää tuotteen elinkaaren tilaan, joka kirjaa, mikä on tietyn tuotteen tai variantin tämän hetkinen elinkaaren tila. Voit määrittää haluamasi määrän tuotteen elinkaaren tiloja määrittämällä tilalle nimen ja kuvauksen. Voit valita yhden elinkaarin tilan uusien vapautettujen tuotteiden oletustilaksi. Vapautetut tuotevariantit perivät luonnin yhteydessä tuotteen elinkaaren tilan vapautetulta päätuotteelta. Kun muutat vapautetun päätuotteen elinkaaren tilaa, voit halutessasi päivittää kaikki sellaisen aiemmin luodut variantit, joilla on sama alkuperäinen tila.  

## <a name="create-a-new-product-lifecycle-state"></a>Luo uusi tuotteen elinkaaren tila

- Lisätietoja uuden tuotteen elinkaaren tilasta on kohdassa [Uuden tuotteen elinkaaren tilan luominen](tasks/new-product-lifecycle-state.md).

- Lisätietoja oletusarvoisesta tuotteen elinkaaren tilasta on kohdassa [Oletusarvoisen tuotteen elinkaaren tilan luominen](tasks/default-product-lifecycle-state.md).

## <a name="associate-product-lifecycle-states-to-released-products"></a>Tuotteen elinkaaren tilojen liittäminen vapautettuihin tuotteisiin  

Tuotteen elinkaaren tilan voi liittää eri tavoin vapautettuihin tuotteisiin tai tuotevariantteihin.

- Kun uusi vapautettu tuote luodaan, oletusarvoinen **tuotteen elinkaaren tila** määritetään automaattisesti.
- Kun tuote vapautetaan yritykseen, oletusarvoinen **tuotteen elinkaaren tila** määritetään automaattisesti.
- Kun tuotevariantti vapautetaan yritykseen, yrityksessä vapautettuun päätuotteeseen liitetty **tuotteen elinkaaren tila** määritetään automaattisesti uuteen varianttiin.

Voit päivittää tuotteen elinkaaren tilan manuaalisesti käyttämällä

- **Vapautetut tuotteet** -luettelosivua tai **tietonäkymää**
- **Vapautetut tuotevariantit** -luettelosivua tai **tietonäkymää**.
- Voit etsiä vanhentuneita tuotteita tai tuotevariantteja kysynnän ja liitetyn elinkaaren tilan mukaan.  

Lisätietoja:

- Lisätietoja tuotteen elinkaaren tilan liittämisestä vapautettuun päätuotteeseen on kohdassa [Tuotteen elinkaaren tilan määrittäminen vapautettuun päätuotteeseen](tasks/product-lifecycle-state-released-product-master.md).

- Lisätietoja tuotteen elinkaaren tilan liittämisestä vapautustuotteeseen on kohdassa [Tuotteen elinkaaren tilan määrittäminen vapautettuun tuotteeseen](tasks/product-lifecycle-state-released-product.md).

## <a name="impact-on-master-planning"></a>Vaikutus pääsuunnitteluun

Tuotteen elinkaaren tilalla on vain yksi valvontamerkki: **On käytettävissä suunnitteluun**. Sen oletusasetus on **Kyllä** kaikissa luoduissa tuotteen elinkaaren tiloissa, mutta asetukseksi voidaan vaihtaa **Ei**. Kun **Ei** on valittu, liitetyt vapautetut tuotteet tai tuotevariantit

- jätetään pääsuunnittelun ulkopuolelle
- jätetään tuoterakennetason laskennan ulkopuolelle.

Lisätietoja tavoista tuotteen elinkaaren tilan käyttämisestä tuotteiden poisjättämiseeen pääsuunnittelusta ja tuoterakennetason laskennasta [Tuotteen elinkaaren tilan luonti jättämään tuotteita pääsuunnittelun ulkopuolelle](tasks/exclude-products-master-planning.md).

> [!NOTE]
> Suorituskyvyn kannalta on suositeltavaa liittää kaikki vanhentuneet vapautetut tuotteet tai tuotevariantit sellaiseen tuotteen elinkaaren tilaan, jossa käyttö pääsuunnittelussa on poistettu käytöstä. Tämä kannattaa erityisesti käsiteltäessä tuotemääritysvariantteja, joita ei voi käyttää uudelleen.  

## <a name="default-migration-import-and-export"></a>Oletusarvoinen siirto, tuonti ja vienti

Tietoyksiköt tukevat tuotteen elinkaaren tiloja ja elinkaaren tilaa voidaan asettaa muuttuvaan tilaan joko vapautetun tuotteen tietoyksikön tai julkaisun varianttitietoyksikön kautta.

## <a name="find-obsolete-products-and-products-variants"></a>Vanhentuneiden tuotteiden ja tuotevarianttien etsiminen

Voit etsiä vanhentuneita vapautettuja tuotteita ja tuotevariantteja suorittamalla simulointianalyysin ja päivittää sitten niiden tuotteen elinkaaren tilan. Lisätietoja vanhentuneiden tuotteiden etsimisestä on kohdassa [Vanhentuneiden tuotevarianttien etsiminen ja tuotteen elinkaaren tilan määrittäminen](tasks/obsolete-product-variants.md). Tässä aiheessa käsitellään vanhentuneiden vapautettujen tuotteiden tai tuotevarianttien etsimisestä ja tuotteen elinkaaren tilan liittämistä vanhentuneisiin tuotteisiin. Siinä kerrotaan myös miten simulointituloksia tarkastellaan ja miten useita tuotteita ja tuotevariantteja liitetään uuteen tuotteen elinkaaren tilaan, kun päivitys suoritetaan ilman simulointia.  

Kun analyysi suoritetaan simulointitilassa, vanhentuneiksi tunnistetut tuotteet ja tuotevariantit näkyvät erillisessä lomakkeessa, jossa niitä on helppo tarkastella. Analyysi hakee tapahtumia ja tiettyjä päätietoja, joilla voi tunnistaa tuotteet, joilla ei ole ollut kysyntää muutettavan ajanjakson aikana ja joilla ei ole kysyntänä ilmeneviä päätietoja. Analyysin ulkopuolelle voidaan jättää uudet vapautetut tuotteet muutettavan ajanjakson ajalta. Kun analyysisimuloinnin tulos on odotettu, käyttäjä voi suorittaa analyysin ja määrittää kaikille analyysin vanhentuneiksi tunnistamille tuotteille uuden tuotteen elinkaaren tilan.  

> [!NOTE]
> Huomaa, että analyysi ja päivitykset on tehtävä samassa yrityksessä.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Vapautettujen tuotteiden ja tuotevarianttien valinta- ja päivitysehdot

Valitse ja päivitä vapautetut tuotteet ja tuotevariantit seuraavien ehtojen mukaisesti:

- Tuotteen tai tuotevariantin tuotteen elinkaaren tila ei saa olla sama kuin uusi toivottu tila.
- Tuote tai tuotevariantti luotiin muutamia päiviä aiemmin; päivien määrä perustuu valintaikkunassa annettuun arvoon.
- Tuotteella tai tuotevariantilla ei ole avoimia tuotantotilauksia (= tila < päättynyt).
- Tuotteella tai tuotevariantilla ei ole avoimia varastotapahtumia (= tila varasto-otto ReservPhysical–QuotationIssue tai tila vastaanotto Registrered–QuotationReceipt).
- Tuotteella tai tuotevariantilla ei ole varastotapahtumia tiettyjen päivien aikana.
- Tuotteella tai tuotevariantilla ei ole tulevaa kysyntää tai tarjontaennustetta.  
- Tuotteelle tai tuotevariantille ei ole määritetty minimivarastotasoa nimikkeen kattavuudessa.
- Tuotteella tai tuotevariantilla ei ole aktiivista kiinteämääräistä kanban-sääntöä.  
- Tuotteella tai tuotevariantilla ei ole huoltotilausriviä.
- Tuotteella tai tuotevariantilla ei ole aktiivisia tai tulevia myynti- tai ostosopimusrivejä.
- Tuotetta tai tuotevarianttia ei käytetä sellaisessa tuoterakenteessa, joka on liitetty ei-vanhentuneeseen hyväksyttyyn suunnittelussa käytettävissä olevaan tuotteen tai variantin tuoterakenneversioon.

## <a name="related-topics"></a>Liittyvät aiheet

- [Luo uusi tuotteen elinkaaren tila](tasks/new-product-lifecycle-state.md)
- [Luo tuotteen elinkaaren oletustila](tasks/default-product-lifecycle-state.md)
- [Tuotteen elinkaaren tilan määrittäminen vapautetulle päätuotteelle](tasks/product-lifecycle-state-released-product-master.md)
- [Tuotteen elinkaaren tilan määrittäminen vapautetulle tuotteelle](tasks/product-lifecycle-state-released-product.md)
- [Vanhentuneiden tuotevarianttien etsiminen ja tuotteen elinkaaren tilan määrittäminen](tasks/obsolete-product-variants.md)
- [Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]