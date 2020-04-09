---
title: Ylätunnistemoduuli
description: Tässä ohjeaiheessa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.
author: anupamar
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025654"
---
# <a name="header-module"></a>Ylätunnistemoduuli


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Dynamics 365 Commercessa sivun ylätunniste koostuu useita moduuleista, kuten ylätunniste-, siirtymisvalikko-, haku-, mainosbanneri- ja evästehyväksyntämoduuleista. 

Ylätunnistemoduuli sisältää sivuston logon, linkit siirtymishierarkiaan, linkit muille sivuston sivuille, ostoskorisymbolin, toivelistasymbolin, kirjautumisvaihtoehdot ja hakupalkin. Ylätunnistemoduuli optimoidaan automaattisesti sitä laitetta varten, jolla sivustoa tarkastellaan (eli pöytätietokonetta tai mobiililaitetta varten). Esimerkiksi mobiililaitteessa siirtymispalkki tiivistetään **Valikko**-painikkeeksi (jossa on useita *viivoja*).

## <a name="properties-of-a-header-module"></a>Ylätunnistemoduulin ominaisuudet

Ylätunnistemoduuli tukee **Logon kuva**-, **Logon linkki**- ja **Oman tilin linkit** -ominaisuuksia. 

**Logon kuva**- ja **Logon linkki** -ominaisuuksilla määritetään sivulla oleva logo. Lisätietoja on kohdassa [Logon lisääminen](add-logo.md). 

**Oman tilin linkit** -ominaisuudella voidaan määrittää ne tilisivut, joiden pikalinkit sivuston omistaja haluaa näyttää ylätunnisteessa.

## <a name="modules-that-are-available-in-a-header-module"></a>Ylätunnistemoduulin käytettävissä olevat moduulit

Seuraavia moduuleja voi käyttää ylätunnistemoduulissa:

- **Siirtymisvalikko** – Siirtymisvalikko edustaa kanavan siirtymishierarkiaa ja muita staattisia siirtymislinkkejä. Kanavan siirtymishierarkia voidaan määrittää Dynamics 365 Commerce -sovelluksessa. Siirtymisvalikossa on **Siirtymisen lähde** -ominaisuus, jolla määritetään Retail Serverin siirtymisvalikon vaihtoehdot ja staattiset valikkovaihtoehdot lähteeksi. Jos staattiset valikkovaihtoehdot määritetään lähteeksi, sivuston muille sivulle voidaan antaa suhteelliset linkit. Määritetyt nimikkeet näkyvät tämän jälkeen ylätunnisteen siirtymistoiminnossa. 
- **Haku** – Hakumoduulin avulla käyttäjät voivat etsiä tuotteita hakusanojen avulla. Oletushakusivun URL-osoite ja hakukyselyn parametrit on annettava valitsemalla **Sivuston asetukset \> Laajennukset**. Hakumoduulissa on ominaisuuksia, joiden avulla voit estää hakupainikkeen tai -selitteen tarvittaessa. Hakumoduuli tukee myös automaattisia ehdotuksia, kuten tuotteen, avainsanan ja luokan hakutuloksia.

## <a name="create-a-header-module-for-a-page"></a>Sivun ylätunnistemoduulin luominen

Voit luoda ylätunnistemoduulin seuraavasti.

1. Luo **Ylätunnisteosa**-niminen osa ja lisää siihen säilömoduuli.
1. Määritä säilömoduulin ominaisuusruudun **Leveys**-ominaisuudeksi **Täytä säilö**.
1. Lisää mainosbanneri- ja evästehyväksyntämoduulit säilömoduuliin.
1. Lisää osaan toinen säilömoduuli ja määritä **Leveys**-ominaisuudeksi **Täytä säilö**.
1. Lisää ylätunnistemoduuli toiseen säilömoduuliin.
1. Lisää siirtymisvalikkomoduuli ylätunnistemoduulin **Siirtymisvalikko**-paikkaan. 
1. Määritä siirtymisvalikkomoduulin ominaisuusruudussa siirtymisvalikkomoduulin ominaisuudet.
1. Lisää hakumoduuli ylätunnistemoduulin **Haku**-paikkaan. 
1. Määritä hakumoduulin ominaisuusruudussa hakumoduulin ominaisuudet. 
1. Tallenna sivuosa, lopeta sen muokkaus ja julkaise se. 

Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.

1. Lisää oletussivun **Otsikko**-paikassa ylätunnisteeseen ylätunnistemoduulin sisältävä ylätunniste-sivuosa.
1. Tallenna malli, lopeta sen muokkaus ja julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
