---
title: Evästeen yhteensopivuus
description: Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411871"
---
# <a name="cookie-compliance"></a>Evästeen yhteensopivuus

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.

## <a name="overview"></a>Yleiskuvaus

Yksityisyys on tärkeä tekijä aina, kun käytetään verkkokaupan asiakkaisiin vaikuttavia seurantatekniikoita. Tietosuojan yhteensopivuusstandardien noudattaminen, kuten yleinen tietosuoja-asetus (GDPR) Euroopan unionin (EU) alueella, on otettava huomioon sähköisessä tietosuojaohjeessa, jokaisella sivustolla, joka on käytössä tällä hetkellä. Koska monet sähköisen kaupankäynnin sivustot ovat oletusarvoisesti yleisesti saatavilla, on tärkeää, että tarkistat verkkokauppasivustosi yhteensopivuusstandardit.

Saat lisätietoja perusperiaatteista, joita Microsoft käyttää evästeiden noudattamiseen, käymällä [Microsoft Trust Centerissä](https://www.microsoft.com/trust-center). Tällä sivustolla voit myös saada lisätietoja yhteensopivuus- ja yksityisyysasioista.

Seuraavassa taulukossa on viiteluettelo evästeitä, joita Dynamics 365 Commerce -sivustot tällä hetkellä sijoittavat.

| Evästeen nimi                               | Käyttö                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Tallentaa Microsoft Azure Active Directoryn (Azure AD) kertakirjautumisen todentamisevästeet. Tallentaa salatut käyttäjän objektitiedot (nimen, sukunimen ja sähköpostiosoitteen). |
| &#95;msdyn365___cart&#95;                           | Tallentaa ostoskorin tunnukset, jolla saadaan luettelo ostoskoriesiintymään lisätyistä tuotteista. |
| &#95;msdyn365___ucc&#95;                            | Evästeiden vaatimustenmukainen hyväksynnän seuranta.                          |
| ai_session                                  | Määrittää, kuinka moni käyttäjän tehtäväistunto on sisältänyt tiettyjä sivuja ja sovelluksen toimintoja. |
| ai_user                                     | Määrittää, kuinka moni henkilö on käyttänyt sovellusta ja sen toimintoja. Käyttäjien laskennassa käytetään anonyymeja tunnuksia. |
| b2cru                                       | Tallentaa uudelleenohjauksen URL-osoitteen dynaamisesti.                              |
| JSESSESSIID                                  | Adyen-maksuyhdistin käyttää käyttäjäistunnon tallentamiseen.       |
| OpenIdConnect.nonce.&#42;                       | Todennus                                               |
| x-ms-cpim-cache:.&#42;                          | Käytetään pyynnön tilan ylläpitämiseen.                      |
| x-ms-cpim-csrf                              | Jaetun julkaisuoikeuspyynnön väärentämisen (CRSF) tunnus, jota käytetään CRSF-väärennökseltä suojautumiseen.     |
| x-ms-cpim-dc                                | Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään. |
| x-ms-cpim-rc.&#42;                              | Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään. |
| x-ms-cpim-slice                             | Käytetään reitittämään pyyntöjä sopivaan tuotannon todennuspalvelinesiintymään. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Käytetään kertakirjautumisistunnon ylläpitämiseen.                        |
| x-ms-cpim-trans                             | Käytetään tapahtumien seurantaan (kuluttajakauppasivustossa todennettavien avoimien välilehtien määrä), mikä sisältää myös nykyisen tapahtuman. |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Sivuston käyttäjän evästeiden hyväksyntä sähköisen kaupankäynnin sivustossa 

Jos sähköisen kaupankäynnin sivuston ominaisuus tai moduuli käyttää ei-olennaista evästettä, sivuston käyttäjän hyväksyntä on saatava ennen evästeen seuraamista. Jotta sivuston käyttäjät voivat antaa evästeiden hyväksynnän sähköisen kaupankäynnin sivustossa, sivuston tekijän on lisättävä ja konfiguroitava evästeiden hyväksyntämoduuli sivun otsikkomoduulissa. Näin varmistetaan, että hyväksyntä pyydetään ja vastaanotetaan. Sivuston käyttäjän hyväksyntä on saatava, ennen kuin ei-olennaista evästettä käyttävä toiminto tai moduuli voidaan hahmontaa sivuston sivulla.

## <a name="additional-resources"></a>Lisäresurssit

[Helppokäyttöisyyden toiminnot ja ominaisuudet](accessibility.md)

[Yhteensopivuuden yleiskatsaus](compliance-overview.md)

[Lisää tietosuojakäytäntösivu](add-privacy-page.md)

[Seurattuihin sisällönmuutoksiin liittyvien käyttäjätunnusten korvaaminen](replace-IDs-tracked-changes.md)

[Evästeen hyväksyntämoduuli](cookie-consent-module.md) 
 
[Ylätunnistemoduuli](author-header-module.md)
