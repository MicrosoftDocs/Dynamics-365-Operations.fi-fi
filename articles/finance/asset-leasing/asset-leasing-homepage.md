---
title: Resurssin vuokrauksen aloitussivu
description: Tässä artikkelissa on yleiskatsaus resurssin vuokrauksen dokumentaatiosta ja linkit tiettyihin ohjeaiheisiin.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeasingWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom:
- "4464"
- intro-internal
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fa27e20bc0c0ff5c639dfb2d079adef8926f535f
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069344"
---
# <a name="asset-leasing-home-page"></a>Resurssin vuokrauksen aloitussivu

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan resurssin vuokrauksen ohjeaiheet ja linkit tiettyihin ohjeaiheisiin. 

Omaisuuden leasing on lisäominaisuus, jolla hallitaan, seurataan ja automatisoidaan vuokratun omaisuuden rahoitustapahtumia Microsoft Microsoft Dynamics 365 Financessa. Omaisuuden leasing noudattaa kansainvälisiä kirjanpitostandardeja (IFRS 16) ja US GAAP -standardeja (ASC 842). Omaisuuden leasing tallentaa ja käsittelee tärkeimmät vuokrasopimuksia koskevat tiedot ja auttaa luomaan kirjauskansiovientejä koko leasingsopimuksen elinkaaren ajan alkukirjaamisesta, ja kuukausittaisista kirjauskansiovienneistä arvonalennukseen ja leasingsopimuksen päättymiseen.

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää **Toimintojen hallinnan** työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Etsi ja valitse **Ominaisuuksien hallinta** -työtilassa toiminto, jonka nimi on **Käyttöomaisuuden vuokraus** ja napsauta sitten **Ota käyttöön nyt** -painiketta.

## <a name="asset-leasing-topics"></a>Resurssin vuokrauksen ohjeaiheet
Seuraava artikkeli auttaa resurssin vuokrauksen määrittämisessä ja käyttämisessä. 

 - [Resurssin vuokrauksen aloittaminen](asset-leasing-quick-start.md) – Tässä artikkelissa kerrotaan resurssin vuokrauksen yleisiä ominaisuuksia. Se sisältää myös ohjelmiston ja dokumentaation termit ja kertoo niistä.
 
 ### <a name="set-up-asset-leasing"></a>Resurssin vuokrauksen määrittäminen
 Tämän ohjeaiheiden ryhmän avulla voit määrittää resurssin vuokrauksen tavalla, joka on optimaalinen organisaation liiketoimintatilanteen kannalta.  
  
  - [Vuokrasopimuksen parametrien määrittäminen](config-lease-parameters.md) 
  - [Vuokrasopimuskirjan määrittäminen](set-up-lease-books.md)
  - [Vuokraryhmän luominen](create-lease-group.md)
  - [Indeksin hintojen määrittäminen](set-up-index-rate-types.md)
  - [Kulutyyppien määrittäminen](set-up-expense-types.md)
  - [Vuokrakirjauskansioiden nimien määrittäminen](set-up-lease-journal-names.md)
  - [Vuokrauksen kirjaustilien määrittäminen](set-up-lease-posting-accts.md)
  - [Numerosarjojen määrittäminen](leasing-number-sequences.md)
  - [Määritä käyttäjärooleja](lease-user-roles.md)

### <a name="manage-asset-leases"></a>Käyttöomaisuuden vuokrasopimusten hallinta
Tämä ohjeaiheen ryhmä kuvaa vuokrasopimusten lisäämisen, maksujen luomisen, vuokrasopimusten muokkaamisen, vuokrasopimuksen tietojen tuomisen ja käyttöoikeusomaisuuserän arvonalenemisen. 

 - [Vuokrasopimuksen lisääminen tai kopioiminen](add-lease.md)
 - [Maksulaskun luominen](create-payment-invoice.md)
 - [Käyttöoikeusomaisuuserän poiston tallentaminen](record-rou-asset-depreciation.md)
 - [Kirjattujen vuokratapahtumien palauttaminen](reverse-posted-lease-trans.md)
 - [Vuokrauksen muokkaaminen](adjust-lease.md)
 - [Käyttöoikeusomaisuuserän arvon alentaminen](impair-rou-asset.md)
 - [Kirjattujen vuokratapahtumien palauttaminen](reverse-posted-lease-trans.md)
 - [Käyttöoikeusomaisuuserän arvon alentaminen](impair-rou-asset.md)
 - [Vuokrauksen yhdistäminen käyttöomaisuuserään](associate-lease-with-fixed-asset.md)
 - [Vuokrausten tallentaminen ulkomaan valuuttana](record-leases-foreign-currency.md)
 - [Indeksikorkoon sidottujen vuokrauksen maksujen uudelleenarvostus](revalue-payments-tied-2-index-rate.md)
 - [Lyhytaikaisen vuokrasopimusvelan osan uudelleenluokitteleminen](reclassify-st-lease-liability.md)
 - [Velka-, resurssi- ja kulutapahtumien tarkasteleminen](view-asset-transactions.md)
 - [Yhdistämisvälin toiminto](compound-interval-functionality.md)
 - [Kuukausittaisten kirjauskansiovientien vahvistaminen erätoimintona](confirm-payment-schedules-in-batch.md)
 - [Kuukausittaisten kirjauskansiovientien luominen erätoimintona](create-monthly-journals-batch.md)
 - [Kaksoisraportointi](dual-reporting.md)
 - [Vuokrauksen työnkulun määrittäminen](set-up-lease-wrkflw.md)
 - [Vuokrauksen hyväksyntätyönkulkujen käyttäminen](use-create-lease-wrkflw.md)
 - [Vuokrauksen hallinta vuokrauksen tuonnin kehyksen kautta](manage-leases-thru-imprt-framewrk.md)
 
### <a name="asset-leasing-reporting"></a>Resurssin vuokrauksen raportoiminen
Tässä artikkelissa esitellään resurssin vuokrauksen käytettävissä olevat raportit. 

 - [Resurssin vuokrauksen raportit](asset-leasing-rprts.md)
 

## <a name="additional-resources"></a>Lisäresurssit

### <a name="whats-new-and-in-development"></a>Uudet ja kehitteillä olevat toiminnot

Siirry [Microsoft Dynamics 365:n julkaisusuunnitelmiin](/dynamics365/release-plans/), kun haluat nähdä, millaisia uusia toimintoja on suunniteltu. 

### <a name="blogs"></a>Blogit

[Microsoft Dynamics 365 -blogissa](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) ja [Microsoft Dynamics 365 talous- ja toimintosovellusten taloushallinnon blogissa](https://community.dynamics.com/365/financeandoperations/b/financials) on mielipiteitä, uutisia ja muita tietoja.

[Microsoft Dynamics Operations -kumppaniyhteisön blogista](https://community.dynamics.com/partner/b/operationspartnercommunityblog) Microsoft Dynamics -kumppanit saavat keskitetysti tietoja Dynamics 365:n uutuuksista ja suosituista aiheista.

### <a name="videos"></a>Videot

Tutustu [Microsoft Dynamics 365 YouTube -kanavan](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) ohjevideoihin. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

