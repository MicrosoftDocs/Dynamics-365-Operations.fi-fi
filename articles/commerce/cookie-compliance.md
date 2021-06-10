---
title: Evästeen yhteensopivuus
description: Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.
author: BrianShook
ms.date: 05/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8eb610eb819dee09a30368257e36dc88f855e985
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088384"
---
# <a name="cookie-compliance"></a>Evästeen yhteensopivuus

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään evästeiden yhteensopivuuden ja Microsoft Dynamics 365 Commercen oletuskäytäntöjen huomioitavia seikkoja.

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
| \_msdyn365___muid_                            | Käytetään, jos kokeilu on aktivoitu ympäristölle. Käytetään käyttäjätunnuksena kokeilutarkoituksiin. |
| \_msdyn365___exp_                             | Käytetään, jos kokeilu on aktivoitu ympäristölle. Käytetään suorituskyvyn kuormituksen tasaamisen mittarina.         |
| d365mkt                                       | Käytetään, jos sijaintiin perustuva tunnistus käyttäjän IP-osoitteen seuraamiseksi Commercen sijaintiehdotuksille on otettu käyttöön Commercen sivustonluontityökalussa kohdassa **Sivustoasetukset > Yleiset > Ota sijaintiin perustuva kaupan tunnistus käyttöön**.      |

Jos sivuston käyttäjä valitsee sivuston mahdolliset medialinkit, seuraavan taulukon evästeitä seurataan myös selaimessa.


| Toimialue                      | Eväste               | kuvaus                                                  | Lähde                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | LinkedIn-mainosten tunnusten synkronointi                                      | LinkedIn-syöte ja merkityksellisten tietojen tunniste                                |
| .linkedin.com               | li_sugr                  | Selaimen tunnus                                           | LinkedInin merkityksellisten tietojen tunniste, jos IP-osoitetta ei ole määritetyssä maassa |
| .linkedin.com               | BizographicsOptOut       | Määrittää ulkopuolelle jätetyn tilan kolmannen osapuolen seurantaa varten.              | LinkedInin vierasohjausobjektit ja toimialan pois jätetyt sivut           |
| .linkedin.com               | \_guid                    | Google Adsin selaintunniste.                            | LinkedIn-syöte                                                |
| .linkedin.com               | li_oatml                 | Jäsenen epäsuora tunniste konversioseurannalle, uudelleen kohdentamiselle ja analyysille. | LinkedInin mainonnan ja merkityksellisten tietojen tunnisteet                                |
| Useita ensimmäisen osapuolen toimialueita | li_fat_id                | Jäsenen epäsuora tunniste konversioseurannalle, uudelleen kohdentamiselle ja analyysille. | LinkedInin mainonnan ja merkityksellisten tietojen tunnisteet                                |
| .adsymptotic.com            | U                        | Selaimen tunnus                                           | LinkedInin merkityksellisten tietojen tunniste, jos IP-osoitetta ei ole määritetyssä maassa |
| .linkedin.com                | bcookie                  | Selaimen tunnuksen eväste                                            | LinkedIn-pyynnöt                                         |
| .linkedin.com                | bscookie                 | Suojattu selaineväste                                        | LinkedIn-pyynnöt                                         |
| .linkedin.com               | kieli                     | Määrittää oletussijainnit ja -kielen.                                 | LinkedIn-pyynnöt                                         |
| .linkedin.com                | lidc                     | Käytetään reititykseen.                                             | LinkedIn-pyynnöt                                         |
| .linkedin.com               | aam_uuid                 | Adoben yleisönhallintaeväste                                                     | Tunnuksen synkronoinnin asetus                                              |
| .linkedin.com               | \_ga                      | Google Analyticsin eväste                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google Analyticsin eväste                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google Analyticsin eväste                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Eväste sisältää kirjautuneena olevan käyttäjän käyttäjätunnuksen.  |   Facebook                                                           |
| .facebook.com               | datr                     | Tämän avulla tunnistat Internet-selaimen, jota käytetään yhteyden muodostamiseen Facebookiin sisäänkirjatuneesta käyttäjästä riippumatta. | Facebook                                                             |
| .facebook.com               | wd                       | Tallentaa selaimen ikkunan dimensiot ja Facebook käyttää sitä sivun hahmontamisen optimointiin. | Facebook                                                             |
| .facebook.com               | xs                       | Kaksinumeroinen luku, joka edustaa istunnon numeroa. Toinen osa on istunnon salainen koodi. |  Facebook                                                            |
| .facebook.com               | fr                       | Sisältää yksilöivän selaimen ja käyttäjätunnuksen, joita käytetään kohdistetussa mainonnassa. |  Facebook                                                            |
| .facebook.com               | sb                       | Käytetään Facebookin kaveriehdotusten parantamiseen.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Eväste sisältää kirjautuneena olevan käyttäjän käyttäjätunnuksen.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Eväste sisältää kirjautuneena olevan käyttäjän käyttäjätunnuksen.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Eväste sisältää sivut, kun käyttäjä valitsee Pinterest-painikkeen.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Eväste sisältää sivut, kun käyttäjä valitsee Pinterest-painikkeen.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Sisältää käyttäjätunnuksen ja aikaleiman, jolloin eväste luotiin. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Eväste sisältää sivut, kun käyttäjä valitsee Pinterest-painikkeen.      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Eväste sisältää sivut, kun käyttäjä valitsee Pinterest-painikkeen.      | Pinterest                                                             |
| .pinterest.com              | Paikallinen tallennussijainti            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Palvelualan työntekijät          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Sivuston käyttäjän evästeiden hyväksyntä sähköisen kaupankäynnin sivustossa 

Jos sähköisen kaupankäynnin sivuston ominaisuus tai moduuli käyttää ei-olennaista evästettä, sivuston käyttäjän hyväksyntä on saatava ennen evästeen seuraamista. Jotta sivuston käyttäjät voivat antaa evästeiden hyväksynnän sähköisen kaupankäynnin sivustossa, sivuston tekijän on lisättävä ja konfiguroitava evästeiden hyväksyntämoduuli sivun otsikkomoduulissa. Näin varmistetaan, että hyväksyntä pyydetään ja vastaanotetaan. Sivuston käyttäjän hyväksyntä on saatava, ennen kuin ei-olennaista evästettä käyttävä toiminto tai moduuli voidaan hahmontaa sivuston sivulla.

## <a name="additional-resources"></a>Lisäresurssit

[Helppokäyttöisyyden toiminnot ja ominaisuudet](accessibility.md)

[Yhteensopivuuden yleiskatsaus](compliance-overview.md)

[Lisää tietosuojakäytäntösivu](add-privacy-page.md)

[Seurattuihin sisällönmuutoksiin liittyvien käyttäjätunnusten korvaaminen](replace-IDs-tracked-changes.md)

[Evästeen hyväksyntämoduuli](cookie-consent-module.md) 
 
[Ylätunnistemoduuli](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
