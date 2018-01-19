---
title: Tuotteen elinkaaren tila
description: Tuotteen elinkaaren tila kirjaa julkaistun tuotteen tai tuotevariantin elinkaaren tilan.
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: cvocph
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: 33130a4061f22335aeeffa69c478b693604393a9
ms.openlocfilehash: a57f306ba02c5758c39c4bd29d9a4fa0d7efbcd3
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2017

---

# <a name="product-lifecycle-state"></a>Tuotteen elinkaaren tila 

[!include[banner](../includes/banner.md)]


Tuotteen elinkaaren tila kirjaa julkaistun tuotteen tai tuotevariantin elinkaaren tilan. Tuotteen elinkaaren tilat määrittää käyttäjä, yleensä tuotepäällikkö tai tuotteen päätietojen hallinta. Tietty elinkaaren tila voi vaikuttaa tiettyihin liiketoimintaprosesseihin, kuten pääsuunnitteluun.   
 
Vapautettu tuote tai tuotevariantti voidaan liittää tuotteen elinkaaren tilaan, joka kirjaa, mikä on tietyn tuotteen tai variantin tämän hetkinen elinkaaren tila. Voit määrittää haluamasi määrän tuotteen elinkaaren tiloja määrittämällä tilalle nimen ja kuvauksen. Voit valita yhden elinkaarin tilan uusien vapautettujen tuotteiden oletustilaksi. Vapautetut tuotevariantit perivät luonnin yhteydessä tuotteen elinkaaren tilan vapautetulta päätuotteelta. Kun muutat vapautetun päätuotteen elinkaaren tilaa, voit halutessasi päivittää kaikki sellaisen aiemmin luodut variantit, joilla on sama alkuperäinen tila.  

## <a name="create-a-new-product-lifecycle-state"></a>Uuden tuotteen elinkaaren tilan luominen 
 
- Toista tai lue tehtäväopas **Uuden tuotteen elinkaaren tilan luominen**, kun haluat luoda uuden tuotteen elinkaaren tilan. 

-  Toista tai lue tehtäväopas **Tuotteen elinkaaren oletustilan luominen**, kun haluat luoda tuotteen elinkaaren oletustilan.   

## <a name="associate-product-lifecycle-states-to-released-products"></a>Tuotteen elinkaaren tilojen liittäminen vapautettuihin tuotteisiin  

Tuotteen elinkaaren tilan voi liittää eri tavoin vapautettuihin tuotteisiin tai tuotevariantteihin.

-  Kun uusi vapautettu tuote luodaan, oletusarvoinen **tuotteen elinkaaren tila** määritetään automaattisesti. 
-  Kun tuote vapautetaan yritykseen, oletusarvoinen **tuotteen elinkaaren tila** määritetään automaattisesti. 
-  Kun tuotevariantti vapautetaan yritykseen, yrityksessä vapautettuun päätuotteeseen liitetty **tuotteen elinkaaren tila** määritetään automaattisesti uuteen varianttiin. 

Voit päivittää tuotteen elinkaaren tilan manuaalisesti käyttämällä 

-    **Vapautetut tuotteet** -luettelosivua tai **tietonäkymää** 
-  **Vapautetut tuotevariantit** -luettelosivua tai **tietonäkymää**. 
-  Voit etsiä vanhentuneita tuotteita tai tuotevariantteja kysynnän ja liitetyn elinkaaren tilan mukaan.  

Saat lisätietoja tuotteen elinkaaren tilojen liittämisestä toistamalla tai lukemalla seuraavat tehtäväoppaat.

-  Toista tai lue **Tuotteen elinkaaren tilan määrittäminen vapautettuun päätuotteeseen** -tehtäväopas, jos haluat liittää tuotteen elinkaaren tilan vapautettuun päätuotteeseen. 

-  Toista tai lue **Tuotteen elinkaaren tilan määrittäminen vapautettuun tuotteeseen** -tehtäväopas, jos haluat liittää tuotteen elinkaaren tilan vapautettuun tuotteeseen. 

## <a name="impact-on-master-planning"></a>Vaikutus pääsuunnitteluun 

Tuotteen elinkaaren tilalla on vain yksi valvontamerkki: **On käytettävissä suunnitteluun**. Sen oletusasetus on **Kyllä** kaikissa luoduissa tuotteen elinkaaren tiloissa, mutta asetukseksi voidaan vaihtaa **Ei**. Kun **Ei** on valittu, liitetyt vapautetut tuotteet tai tuotevariantit 

-  jätetään pääsuunnittelun ulkopuolelle 
-  jätetään tuoterakennetason laskennan ulkopuolelle. 

Saat lisätietoja tavoista, joilla tuotteen elinkaaren tilan avulla voidaan jättää tuotteita pääsuunnittelun ja tuoterakennetason laskennan ulkopuolelle, toistamalla tai lukemalla tehtäväoppaan **Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle**.

> [!NOTE]
> Suorituskyvyn kannalta on suositeltavaa liittää kaikki vanhentuneet vapautetut tuotteet tai tuotevariantit sellaiseen tuotteen elinkaaren tilaan, jossa käyttö pääsuunnittelussa on poistettu käytöstä. Tämä kannattaa erityisesti käsiteltäessä tuotemääritysvariantteja, joita ei voi käyttää uudelleen.  
 
## <a name="default-migration-import-and-export"></a>Oletusarvoinen siirto, tuonti ja vienti 

Tietoyksiköt eivät tue tuotteen elinkaaren tiloja eikä elinkaaren tilaa voi määrittää muuttuvaksi tilaksi vapautettujen tuotetietoyksiköiden avulla.

-  Kaikkien tuotteiden ja tuotevarianttien elinkaaren tila on tyhjä aiemmista versioista siirrettäessä.  
-  Kun vapautettuja tuotteita tuodaan tietoyksikön avulla, elinkaaren oletustila otetaan käyttöön luonnin yhteydessä.  
-  Kun vapautettuja tuotevariantteja tuodaan tietoyksikön avulla, vapautetun päätuotteen elinkaaren tila tuodaan.   
 
## <a name="find-obsolete-products-and-products-variants"></a>Vanhentuneiden tuotteiden ja tuotevarianttien etsiminen 
 
Voit etsiä vanhentuneita vapautettuja tuotteita ja tuotevariantteja suorittamalla simulointianalyysin ja päivittää sitten niiden tuotteen elinkaaren tilan. Toista ja lue **Vanhentuneiden tuotevarianttien etsiminen ja tuotteen elinkaaren tilan määrittäminen** -tehtäväopas, jos haluat etsiä vanhentuneita tuotteita. Tässä tehtäväoppaassa kerrotaan, miten vanhentuneita julkaistuja tuotteita tai tuotevariantteja etsitään ja miten tuotteen elinkaaren tila liitetään vanhentuneisiin tuotteisiin. Siinä kerrotaan myös miten simulointituloksia tarkastellaan ja miten useita tuotteita ja tuotevariantteja liitetään uuteen tuotteen elinkaaren tilaan, kun päivitys suoritetaan ilman simulointia.  
 
Kun analyysi suoritetaan simulointitilassa, vanhentuneiksi tunnistetut tuotteet ja tuotevariantit näkyvät erillisessä lomakkeessa, jossa niitä on helppo tarkastella. Analyysi hakee tapahtumia ja tiettyjä päätietoja, joilla voi tunnistaa tuotteet, joilla ei ole ollut kysyntää muutettavan ajanjakson aikana ja joilla ei ole kysyntänä ilmeneviä päätietoja. Analyysin ulkopuolelle voidaan jättää uudet vapautetut tuotteet muutettavan ajanjakson ajalta. Kun analyysisimuloinnin tulos on odotettu, käyttäjä voi suorittaa analyysin ja määrittää kaikille analyysin vanhentuneiksi tunnistamille tuotteille uuden tuotteen elinkaaren tilan.  
 
> [!NOTE]
> Huomaa, että analyysi ja päivitykset on tehtävä samassa yrityksessä.  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Vapautettujen tuotteiden ja tuotevarianttien valinta- ja päivitysehdot 
 
Valitse ja päivitä vapautetut tuotteet ja tuotevariantit seuraavien ehtojen mukaisesti: 

-    Tuotteen tai tuotevariantin tuotteen elinkaaren tila ei saa olla sama kuin uusi toivottu tila. 
-  Tuote tai tuotevariantti luotiin muutamia päiviä aiemmin; päivien määrä perustuu valintaikkunassa annettuun arvoon. 
-  Tuotteella tai tuotevariantilla ei ole avoimia tuotantotilauksia (= tila < päättynyt). 
-  Tuotteella tai tuotevariantilla ei ole avoimia varastotapahtumia (= tila varasto-otto ReservPhysical–QuotationIssue tai tila vastaanotto Registrered–QuotationReceipt). 
-  Tuotteella tai tuotevariantilla ei ole varastotapahtumia tiettyjen päivien aikana. 
-  Tuotteella tai tuotevariantilla ei ole tulevaa kysyntää tai tarjontaennustetta.  
-  Tuotteelle tai tuotevariantille ei ole määritetty minimivarastotasoa nimikkeen kattavuudessa. 
-  Tuotteella tai tuotevariantilla ei ole aktiivista kiinteämääräistä kanban-sääntöä.  
-  Tuotteella tai tuotevariantilla ei ole huoltotilausriviä. 
-  Tuotteella tai tuotevariantilla ei ole aktiivisia tai tulevia myynti- tai ostosopimusrivejä. 
-  Tuotetta tai tuotevarianttia ei käytetä sellaisessa tuoterakenteessa, joka on liitetty ei-vanhentuneeseen hyväksyttyyn suunnittelussa käytettävissä olevaan tuotteen tai variantin tuoterakenneversioon.

## <a name="related-topics"></a>Liittyvät aiheet

-  Uuden tuotteen elinkaaren tilan luominen
-  Uuden tuotteen elinkaaren oletustilan luominen
-  Tuotteen elinkaaren tilan liittäminen vapautettuun päätuotteeseen
-  Tuotteen elinkaaren tilan liittäminen vapautettuun tuotteeseen
-  Vanhentuneiden tuotevarianttien etsiminen ja tuotteen elinkaaren tilan liittäminen
-  Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle

