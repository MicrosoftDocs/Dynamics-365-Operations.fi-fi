---
title: Elämäntapahtumatyyppien määrittäminen
description: Microsoft Dynamics 365 Human Resources käyttää elinkaaritapahtumatyyppejä määrittämään työntekijän etujen rekisteröimisen päivittämistapahtumat.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f8f81d6cc00154ca85b41294f4ae2ecb52c908c4
ms.sourcegitcommit: 8592c661b41f9cef8b7ef2863a3b97bf49a4e6f9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/26/2021
ms.locfileid: "7423354"
---
# <a name="configure-life-event-types"></a>Elämäntapahtumatyyppien määrittäminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources käyttää elinkaaritapahtumatyyppejä sellaisten tapahtumien määrittämiseen, joissa työntekijän etujen rekisteröiminen päivitetään. Esimerkiksi avioliiton solmiminen tai lapsen saaminen. Kukin elinkaaritapahtumatyypin tunnus voidaan liittää vain yhteen elinkaaritapahtumatyyppiin. Jos esimerkiksi luot elinkaaritapahtuman tunnuksen nimeltä "osoitteenmuutos", joka liittyy elinkaaritapahtumatyyppiin työntekijän osoitteenmuutos, et voi luoda toista tunnusta, jonka nimi on työntekijän osoitteenmuutos ja liittää sitä elinkaaritapahtumatyyppiin työntekijän osoitteenmuutos. Jos elinkaaritapahtumatyyppiä ei ole liitetty suunnitelmatyyppiin, elinkaaritapahtumatyyppi ei käynnistä elinkaaritapahtumaa. Lisätietoja on kohdassa [Suunnitelmatyyppien luominen](hr-benefits-setup-plan-types.md).

## <a name="create-a-life-event-type"></a>Elinkaaritapahtumatyypin luominen

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Elinkaaritapahtumatyypit**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Elinkaaritapahtuman tyypin tunnus** | Elämäntapahtumatyypin yksilöllinen tunniste. |
   | **Kuvaus** | Elinkaaritapahtumatyypin kuvaus. |
   | **Elinkaaritapahtuman tyyppi** | Työntekijän eturekisteröinnin päivittämisen katalysaattori. Luettelo elinkaaritapahtumista on alla kohdassa [Elinkaaritapahtumat](hr-benefits-setup-payment-frequencies.md?life-events). |

4. Valitse **Tallenna**.

## <a name="view-attached-plans"></a>Tarkastele liitettyjä suunnitelmia

Voit tarkastella valittuun elinkaaritapahtumatyyppiin liitettyjen suunnitelmien luetteloa. Elinkaaritapahtumat liitetään suunnitelmatyyppiin, ja suunnitelmatyypit liitetään suunnitelmaan.

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Elinkaaritapahtumatyypit**.

2. Valitse **Toiminnot**.

3. Valitse **Liitetyt suunnitelmat**.

## <a name="life-events"></a>Elinkaaritapahtumat

Voit valita seuraavista elinkaaritapahtumista, kun luot elinkaaritapahtumatyypin:

| Elinkaaritapahtuma | Toimipaikka | Käynnistin |
| --- | --- | --- |
| **Siviilisäädyn muutos** | Työntekijä > profiili > henkilökohtaiset tiedot > siviilisääty| Siviilisäädyn muutos |
| **Työllisyystilanteen muutos** |<br><ul><li>Työntekijä > Työsuhde</li><li>Työsuhdehistoriasivu</li></ul> | Jos työntekijällä on aiemmin luodut työsuhdetiedot, uusien työsuhdetietojen luominen eri työsuhteen tilalla käynnistää elinkaaritapahtuman.  Myös aiemmin luotujen työsuhdetietojen päivittäminen eri työsuhteen tilalla käynnistää elinkaaritapahtuman.  |
| **Työntekijän osoitteen muutos** |<br><ul><li>Työntekijä > Profiili > Osoitteet</li><li>Työntekijä > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Osoite</li></ul> | Osoitteen muutos. Osoitteen on oltava **ensisijainen**, jotta se käynnistää elinkaaritapahtuman. |
| **Huollettavan muutos** |<br><ul><li>Työntekijä > Profiili > Henkilökohtaiset yhteystiedot > Henkilökohtaiset yhteyshenkilöt/li><li>Työntekijän itsepalvelu</li></ul> | Lisää henkilökohtainen yhteyshenkilö määrittäen hänet riippuvaisena ja määrittäen **Voimassaolo alkaa** -arvon. Päivitä henkilökohtaisen yhteyshenkilön riippuvaiset **Voimassaolo alkaa** -tiedot. Henkilökohtaisen yhteyshenkilön suhteen on oltava lapsi, puoliso, avopuoliso tai entinen puoliso.  |
| **Syntymä tai adoptio (huollettava)** |<br><ul><li>Työntekijä > Profiili > Henkilökohtaiset yhteystiedot > Henkilökohtaiset yhteyshenkilöt</li><li>Työntekijän itsepalvelu > Muokkaa henkilökohtaisia tietoja > Henkilökohtaiset yhteyshenkilöt</li></ul>| **Syntymäpäivämäärä** tai **Adoptiopäivämäärä** lisätään tai päivitetään. Lapsen **Syntymäpäivämäärä** on pakollinen. |
| **Kattavuuden menetys (puoliso/asuinkumppani)** | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot > Kattavuuden menetys | Henkilökohtaista kontaktia varten valitun **Kattavuuden menetys** sekä **Voimaantulopäivämäärä** |
| Asuinkumppanin työsuhteen muutos | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot > Toimessa | Henkilökohtaisen yhteyshenkilön luominen ja **Toimessa**-asetuksen määrittäminen arvoon **Kyllä**. Henkilökohtaisen yhteyshenkilön päivittäminen ja **Toimessa**-arvon muuttaminen.  |
| **Virkavapaa (puoliso/asuinkumppani)** | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot > Virkavapaa | Luotu henkilökohtainen yhteyshenkilö **Virkavapaan voimaantulopäivä** on määritetty. Henkilökohtaisen yhteyshenkilön **Virkavapaa** on päivitetty. Henkilökohtaisen yhteyshenkilön **Virkavapaan voimaantulopäivä** on päivitetty.  |
| **Muutos kattavuudessa (toimi)** |<br><ul><li>Työntekijä > Toimimääritys > Työntekijöiden toimimääritykset</li><li>Toimet > Toimet</li></ul>| Muuta työntekijän toimen määritystietueissa olevaa paikkaa. Työntekijän toimen määrityksen muutos. |
| **Muutos kattavuudessa (palkka)** |<br><ul><li>Työntekijä > Kompensaatio > Kiinteä suunnitelma</li><li>Työntekijä > Henkilökohtaiset tiedot > Etuuksien vuosipalkka</li></ul>| Jos Etujen hallinta > Human Resourcesin jaetut parametrit > Edut > Etuuksien vuosipalkka ei ole käytössä, Työntekijä > Kompensaatio > Kiinteä suunnitelma päivittäminen luo elinkaaritapahtuman. Jos Etujen hallinta > Human Resourcesin jaetut parametrit > Edut > Etuuksien vuosipalkka on käytössä, Työntekijä > Henkilökohtaiset tiedot > Etuuksien vuosipalkka päivittäminen luo elinkaaritapahtuman. |
| **Medicare (työntekijä/huollettava)** | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot > Medicaren voimaantulopäivä | Henkilökohtaisen yhteyshenkilön **Medicaren voimaantulopäivän** lisääminen tai päivittäminen luo tämän elinkaaritapahtuman. |
| **Tuomioistuimen määräämä tuki** | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettava > Tuomioistuimen määräämä tuki (QMSCO/QDRO) ja voimaantulopäivät | Henkilökohtaisen yhteyshenkilön luomisen yhteydessä luodaan elinkaaritapahtuma, jos **Tuomioistuimen määräämä tuki** -kohdan arvona on **Kyllä**. **Tuomioistuimen määräämä tuki**- tai **Tuomioistuimen määräämä vanhentumispäivä** -kohtien päivittäminen käynnistää myös elinkaaritapahtuman. |
| **Kuollut** | Työntekijä > profiili > henkilökohtaiset tiedot > Kuolinpäivämäärä | **Kuolinpäivämäärä** annetaan tai päivitetään. |
| **Todiste vakuutuksesta** | Työntekijä > Työntekijä > Versiot > Työhistoria > Päivämäärän hallinta > Etutiedot | **Todiste vakuutuskelpoisuudesta** -kohdan arvoksi asetetaan **Kyllä**. **Todiste vakuutuskelpoisuudesta -tarkistuspäivämäärä** määritetään. |
| **Edunsaaja** | Työntekijä > Profiili > Henkilökohtaiset yhteystiedot > Henkilökohtaiset yhteyshenkilöt | Henkilökohtainen yhteyshenkilö lisätään ja **Edunsaaja**- ja **Voimaantulopäivämäärä**-kentät täytetään. Henkilökohtaisen yhteyshenkilön tyypin on oltava **Lapsi**, **Puoliso**, **DomesticPartner**, **Sisarus**, **FamilyContact**, **OtherContact** tai **Vanhempi**. |
| **Työntekijä - Medicare** | Työntekijä > Työntekijä > Versiot > Työhistoria > Päivämäärän hallinta > Etutiedot | **Medicare-kelpoisuus**-kohdan arvona on **Kyllä**. **Medicare-kelpoisuuden päivämäärää** on muutettu. |
| **Syntymäpäivä** | Etujen hallinta > Elinkaaritapahtuman muutoksen käsittely | Nämä elinkaaritapahtumat luodaan **Elinkaaritapahtuman muutoksen käsittelystä**. Prosessi analysoi valitun kauden ja yrityksen sekä etsii niihin liittyviä työntekijöitä. Se laskee edellisen syntymäpäivän ja luo syntymäpäivän elinkaaritapahtuman, jos sitä ei ole jo luotu. |
| **Työntekijän kelpoisuusmuutos (ei koske vain Yhdysvaltoja)** |<br><ul><li>Työntekijä > Työsuhde</li><li>Työntekijä > Työntekijä > Versiot > Työhistoria</li></ul>| Luo elinkaaritapahtuman, kun:<br><ul><li>Luodaan uusi työsuhde ja myös edellinen työsuhde on olemassa ja työntekijätyyppi muuttuu.</li><li>Luodaan uudet työsuhdetiedot ja myös edelliset työsuhdetiedot ovat olemassa ja työsuhdetyyppi tai työsuhdeluokka muuttuu.</li><li>Työsuhdetietueen päivitys ja eri työntekijätyyppi on määritetty.</li><li>Työsuhdetietueen päivitys ja eri työsuhdetyyppi tai -luokka on määritetty.</li></ul> |
| **Uusi etukelpoisuuden ohitus (ei koske vain Yhdysvaltoja)** | Henkilöstöhallinnon kehittyneet > Edut > Suunnitelmat > Edut > Oikeutussäännön ohitus | Elinkaaritapahtuman käsittelyn käyttäminen<br>Uuden etusuunnitelman kelpoisuuden ohituksen luominen työntekijälle aiheuttaa tämän elinkaaritapahtuman.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Etukelpoisuussäännön ohituksen muutos (ei koske vain Yhdysvaltoja)** | Henkilöstöhallinnon kehittyneet > Edut > Suunnitelmat > Edut > Oikeutussäännön ohitus | **Voimassaolo alkaa**- tai **Voimassaolo päättyy** -arvojen päivittäminen etusuunnitelman kelpoisuuden ohituksessa käynnistää elinkaaritapahtuman. |
| **Etukelpoisuuden ohituksen päättyminen (ei koske vain Yhdysvaltoja)** | Etujen hallinta > Elinkaaritapahtuman muutoksen käsittely  | Nämä elinkaaritapahtumat luodaan **Elinkaaritapahtuman muutoksen käsittelystä**. Prosessi analysoi valitun kauden ja yrityksen sekä etsii niihin liittyviä etusuunnitelman kelpoisuuden ohituksia. Se luo elinkaaritapahtumia, jos ohitukset ovat vanhentuneet. |
| **Uusi etuussuunnitelma (ei koske vain Yhdysvaltoja)** | Henkilöstöhallinnon kehittyneet > Edut > Suunnitelmat > Uusi | Kelpoisuusvaihtoehdot lisätään nykyiseen suunnitelmaan. Uusi suunnitelma, johon on liitetty kelpoisuusehtoja, lisätään.</br></br>Henkilöstöhallinnon henkilökunnan tulisi suorittaa tässä tapauksessa elinkaaritapahtuman kelpoisuuden käsittely. |
| **Etukelpoisuussäännön muutos (ei koske vain Yhdysvaltoja)** | Etujen hallinta > Kelpoisuussäännöt | Elinkaaritapahtuman kelpoisuuskäsittelyn käyttäminen. Lokiin kirjataan , kun **BenefitEligibilityRule**-tietueissa on muutettu seuraavat arvot: **UseEmplCategory**, **UseEmplStatus** tai **UseEmplType**. Päivittää vain ne elinkaaritapahtuman tapahtumat, jotka ovat jo muuttuneessa säännössä tai kelpoisuusehdoissa. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
