---
title: Siirtymisvalikkomoduuli
description: Tässä ohjeaiheessa on tietoja siirtymisvalikkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 1af1fc03ead21150415295d83d292afe0110e5bd
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109679"
---
# <a name="navigation-menu-module"></a>Siirtymisvalikkomoduulit

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja siirtymisvalikkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Siirrymisvalikkomoduulien ensisijainen tarkoitus on antaa sivuston käyttäjille mahdollisuus selata tuotteita ja sivuston sivuja kanavan siirtymishierarkian mukaan. Hierarkia määritetään Dynamics 365 Commerce Headquarters -sovelluksessa. Siirtymisvalikkomoduulissa määritetyt nimikkeet näkyvät sivuston otsikon navigointitoiminnossa. Siirtymisvalikkomoduulit tukevat myös staattisia valikon vaihtoehtoja, joka sisältävät linkit muille sivuille sähköisen kaupankäynnin sivustossa.

Navigointivalikkomoduuli voidaan lisätä sivun ylätunnistemoduuliin. Fabrikam-teeman siirtymisvalikossa on näkyvissä kaksi tasoa oletusarvoisesti. Starter (aloitus) -teeman siirtymisvalikossa on näkyvissä kolme tasoa oletusarvoisesti. Jos haluat vaihtaa tasojen määrän, teemalle on määritettävä näkymän laajennus.

Seuraavassa kuvassa on esimerkki Fabrikam-sivuston siirtymisvalikosta, jossa on kaksi luokkahierarkian tasoa ja joitakin staattisia valikon vaihtoehtoja.
![Esimerkki siirtymisvalikkomoduulista.](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Siirtymisvalikkomoduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Lähde                  | **Vähittäismyynti**, **Manuaalinen luominen**, **Vähittäismyynti ja manuaalinen luominen** | **Vähittäismyynti**-arvon ansiosta Commerce Headquarters -sovelluksen kanavan siirtymishierarkia voidaan näyttää siirtymisvalikossa. **Manuaalisen luominen** -arvo sallii staattisten valikon vaihtoehtojen kuratoinnin. **Vähittäismyynti ja manuaalinen luominen** -arvo sallii näiden yhdistämisen. |
| Näytä luokan kuvat | **Tosi** vai **Epätosi**    | Kun tämä ominaisuus on käytössä, tämä ominaisuus näyttää siirtymisvalikon luokan kuvat Commerce Headquarters -sovelluksessa määritetyllä tavalla. Lisätty Commercen versioon 10.0.14. |
| Näytä mainoskuvat | **Tosi** vai **Epätosi** | Kun tämä ominaisuus on käytössä, kampanjat voidaan konfiguroida kuvien, linkkien ja tekstin avulla. Tämä ominaisuus on lisätty Commerce-version 10.0.17 julkaisuun. |
|Lisää luokan markkinointisisältö | Teksti, kuva tai linkki | Kun **Näytä markkinointikuvat**-ominaisuus on käytössä, voit lisätä siirtymisvalikkoon tekstiä, kuvia tai linkkejä kampanjasisällöksi. |
| Ota monitasoinen siirtymisvalikko käyttöön | **Tosi** vai **Epätosi** | Jos tämä ominaisuus on otettu käyttöön, siirtymisvalikossa näkyy monta siirtymishierarkian tasoa. Tämä ominaisuus on käytettävissä Commerce-version 10.0.15 julkaisussa. |
| Tasojen määrä | kokonaisluku | Tämä ominaisuus määrittää, kuinka monta tasoa voidaan näyttää, jos **Ota monitasoinen siirtymisvalikko käyttöön** -ominaisuuden arvoksi on määritetty **Tosi**. |
| Staattinen valikon vaihtoehto| Arvomatriisi| Staattisia valikon vaihtoehtoha, jotka liittävät valikon vaihtoehdon nimen ja linkin staattisen sivuston sivuun. Voit luoda valikon vaihtoehtoja muiden valikon vaihtoehtojen alle. Oletusarvoisesti staattinen valikko näkyy juuri tasolla. Se liitetään kanavan siirtymishierarkiaan, jos se on olemassa. |
| Näytä päävalikko | **Tosi** vai **Epätosi** | Jos tämä ominaisuus on otettu käyttöön, siirtymisvalikko voidaan määrittää mukautetussa juuressa (kuten **Osta nyt**). Tämä ominaisuus on saatavana Dynamics 365 Commercen versiossa 10.0.15. |
| Päävalikko | merkkijono | Tällä ominaisuudella voi määrittää mukautetun juuren teksti, jos **Näytä päävalikko** -ominaisuudeksi on määritetty **Tosi**. |

Seuraavassa kuvassa näkyy esimerkki Fabrikam-sivuston siirtymisvalikossa näkyvästä luokan kuvasta.
![Esimerkki siirtymisvalikkomoduulista ja luokan kuvista.](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Siirtymisvalikkomoduulin lisääminen ylätunnistemoduuliin

Lisätietoja siirtymisvalikkomoduulin lisäämisestä ylätunnistemoduuliin on kohdassa [Ylätunnistemoduuli](author-header-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Navigointipolkumoduuli](add-breadcrumb.md)

[Sivuston valitsinmoduuli](site-selector.md)

[Ostoruutumoduuli](add-buy-box.md)

[Evästeen yhteensopivuus](cookie-compliance.md)

[Ylätunnistemoduuli](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
