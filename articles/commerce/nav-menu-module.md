---
title: Siirtymisvalikkomoduuli
description: Tässä ohjeaiheessa on tietoja siirtymisvalikkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4412107"
---
# <a name="navigation-menu-module"></a>Siirtymisvalikkomoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja siirtymisvalikkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Siirrymisvalikkomoduulien ensisijainen tarkoitus on antaa sivuston käyttäjille mahdollisuus selata tuotteita ja sivuston sivuja kanavan siirtymishierarkian mukaan. Hierarkia määritetään Dynamics 365 Commerce Headquarters -sovelluksessa. Siirtymisvalikkomoduulissa määritetyt nimikkeet näkyvät sivuston otsikon navigointitoiminnossa. Siirtymisvalikkomoduulit tukevat myös staattisia valikon vaihtoehtoja, joka sisältävät linkit muille sivuille sähköisen kaupankäynnin sivustossa.

Navigointivalikkomoduuli voidaan lisätä sivun ylätunnistemoduuliin. Fabrikam-teeman siirtymisvalikossa on näkyvissä kaksi tasoa oletusarvoisesti. Starter (aloitus) -teeman siirtymisvalikossa on näkyvissä kolme tasoa oletusarvoisesti. Jos haluat vaihtaa tasojen määrän, teemalle on määritettävä näkymän laajennus.

Seuraavassa kuvassa on esimerkki Fabrikam-sivuston siirtymisvalikosta, jossa on kaksi luokkahierarkian tasoa ja joitakin staattisia valikon vaihtoehtoja.
![Esimerkki siirtymisvalikkomoduulista](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Siirtymisvalikkomoduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Lähde                  | **Vähittäismyynti**, **Manuaalinen luominen**, **Vähittäismyynti ja manuaalinen luominen** | **Vähittäismyynti**-arvon ansiosta Commerce Headquarters -sovelluksen kanavan siirtymishierarkia voidaan näyttää siirtymisvalikossa. **Manuaalisen luominen** -arvo sallii staattisten valikon vaihtoehtojen kuratoinnin. **Vähittäismyynti ja manuaalinen luominen** -arvo sallii näiden yhdistämisen. |
| Näytä luokan kuvat | **Tosi** vai **Epätosi**    | Kun tämä ominaisuus on käytössä, tämä ominaisuus näyttää siirtymisvalikon luokan kuvat Commerce Headquarters -sovelluksessa määritetyllä tavalla. Lisätty Commercen versioon 10.0.14. |
| Ota monitasoinen siirtymisvalikko käyttöön | **Tosi** vai **Epätosi** | Jos tämä ominaisuus on otettu käyttöön, siirtymisvalikossa näkyy monta siirtymishierarkian tasoa. Tämä ominaisuus on saatavana Dynamics 365 Commercen versiossa 10.0.15. |
| Tasojen määrä | kokonaisluku | Tämä ominaisuus määrittää, kuinka monta tasoa voidaan näyttää, jos **Ota monitasoinen siirtymisvalikko käyttöön** -ominaisuuden arvoksi on määritetty **Tosi**. |
| Staattinen valikon vaihtoehto| Arvomatriisi| Staattisia valikon vaihtoehtoha, jotka liittävät valikon vaihtoehdon nimen ja linkin staattisen sivuston sivuun. Voit luoda valikon vaihtoehtoja muiden valikon vaihtoehtojen alle. Oletusarvoisesti staattinen valikko näkyy juuri tasolla. Se liitetään kanavan siirtymishierarkiaan, jos se on olemassa. |
| Näytä päävalikko | **Tosi** vai **Epätosi** | Jos tämä ominaisuus on otettu käyttöön, siirtymisvalikko voidaan määrittää mukautetussa juuressa (kuten **Osta nyt**). Tämä ominaisuus on saatavana Dynamics 365 Commercen versiossa 10.0.15. |
| Päävalikko | merkkijono | Tällä ominaisuudella voi määrittää mukautetun juuren teksti, jos **Näytä päävalikko** -ominaisuudeksi on määritetty **Tosi**. |

Seuraavassa kuvassa näkyy esimerkki Fabrikam-sivuston siirtymisvalikossa näkyvästä luokan kuvasta.
![Esimerkki siirtymisvalikkomoduulista ja luokan kuvista](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Siirtymisvalikkomoduulin lisääminen ylätunnistemoduuliin

Lisätietoja siirtymisvalikkomoduulin lisäämisestä ylätunnistemoduuliin on kohdassa [Ylätunnistemoduuli](author-header-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Navigointipolkumoduuli](add-breadcrumb.md)

[Toimipaikan valitsinmoduuli](site-selector.md)

[Ostoruutumoduuli](add-buy-box.md)

[Evästeen yhteensopivuus](cookie-compliance.md)

[Ylätunnistemoduuli](author-header-module.md)
