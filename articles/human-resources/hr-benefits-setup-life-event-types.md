---
title: Elämäntapahtumatyyppien määrittäminen
description: Microsoft Dynamics 365 Human Resources käyttää elinkaaritapahtumatyyppejä sellaisten tapahtumien määrittämiseen, joissa työntekijän etujen rekisteröiminen päivitetään.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5286bcd940f4068531bae624876c8a35e64db4c3
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741483"
---
# <a name="configure-life-event-types"></a>Elämäntapahtumatyyppien määrittäminen

Microsoft Dynamics 365 Human Resources käyttää elinkaaritapahtumatyyppejä sellaisten tapahtumien määrittämiseen, joissa työntekijän etujen rekisteröiminen päivitetään. Esimerkiksi avioliiton solmiminen tai lapsen saaminen. Kukin elinkaaritapahtumatyypin tunnus voidaan liittää vain yhteen elinkaaritapahtumatyyppiin. Jos esimerkiksi luot elinkaaritapahtuman tunnuksen nimeltä "osoitteenmuutos", joka liittyy elinkaaritapahtumatyyppiin työntekijän osoitteenmuutos, et voi luoda toista tunnusta, jonka nimi on työntekijän osoitteenmuutos ja liittää sitä elinkaaritapahtumatyyppiin työntekijän osoitteenmuutos. 

Kun olet luonut elinkaaritapahtumatyypit, sinun on liitettävä ne suunnitelmatyyppeihin. Lisätietoja on kohdassa [Suunnitelmatyyppien luominen](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Kun olet luonut elinkaaritapahtuman, sinun on liitettävä se suunnitelmatyyppiin. Lisätietoja on kohdassa [Suunnitelmatyyppien luominen](hr-benefits-setup-life-event-types.md).

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
| **Työllisyystilanteen muutos** | <ul><li>Työntekijä > Työsuhde</li><li>Työsuhdehistoriasivu</li></ul> | Työsuhteen tilan muutos |
| **Työntekijän osoitteen muutos** | <ul><li>Työntekijä > Profiili > Osoitteet </li><li>Työntekijä > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Osoite</li></ul> Lisätty, muokattu tai poistettu osoite |
| **Huollettavan muutos** | <ul><li>Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Lisää tai poista riippuvainen</li><li>Työntekijän itsepalvelu</li></ul> | Lisätty tai poistettu riippuvainen. Henkilökohtaisen yhteyshenkilön suhteen on oltava lapsi, puoliso, avopuoliso tai entinen puoliso. **Voimassaolon alkamispäivämäärän** päivittäminen käynnistää elinkaaritapahtuman. Jos et päivitä tätä päivämäärää, mitään elinkaaritapahtumaa ei laukaista. |
| **Syntymä tai adoptio (huollettava)** | <ul><li>Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot</li><li>Työntekijän itsepalvelu</li></ul> | **Adoptiopäivämäärä**-kenttä täytetään. Lapsen syntymäaika on pakollinen. |
| **Kattavuuden menetys (puoliso/asuinkumppani)** | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot > Kattavuuden menetys | Henkilökohtaista kontaktia varten valitun **Kattavuuden menetys** sekä **Voimaantulopäivämäärä** |
| Asuinkumppanin työsuhteen muutos | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot > Toimessa. | <ul><li>Huollettavan tietue luotu ja **Henkilökohtainen yhteyshenkilö** -ruutu = Kyllä</li><li>**Henkilökohtainen yhteyshenkilö** -ruutu muutettu (Kyllä tai Ei)</li></ul> |
| **Virkavapaa (puoliso/asuinkumppani)** | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot > Virkavapaa | <ul><li>Huollettavien tiedot -tietue on luotu ja **EhrLOAEffectiveDate** täytetty</li><li>**personPrivateDetails.EhrIsLOA** on muutettu (Kyllä tai Ei)</li><li>**personPrivateDetails.EhrLOAEffectiveDate** on muutettu</li></ul> |
| **Muutos kattavuudessa (toimi)** | <ul><li>Työntekijä > Toimimääritys > Työntekijöiden toimimääritykset</li><li>Toimet > Toimet</li></ul> | <ul><li>Muuta työntekijän toimen määritystietueissa olevaa paikkaa</li><li>Työntekijän toimen määrityksen muutos</li></ul> |
| **Medicare (työntekijä/huollettava)** | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot > Medicaren voimaantulopäivä | Ei käynnisty automaattisesti, kun henkilökohtainen yhteyshenkilö syöttää voimaantulopäivän. |
| **Tuomioistuimen määräämä tuki** | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettava > Tuomioistuimen määräämä tuki (QMSCO/QDRO) ja voimaantulopäivät | Ei aiheuta automaattisia päivityksiä. Se ei vaikuta tukikelpoisuuteen. Se tallentaa elinkaaritapahtuman. |
| **Kuollut** | Työntekijä > profiili > henkilökohtaiset tiedot > Kuolinpäivämäärä | Kuolinpäivämäärä syötetään |
| **Todiste vakuutuksesta** | <ul><li>Työntekijä > Työntekijä > Versiot > Työhistoria > Päivämäärän hallinta > Etutiedot</li><li> Työntekijä > Työsuhde > Etuustiedot > Vahvistuspäivämäärä</li></ul> | <ul><li>Työntekijä syöttää vahvistuspäivämäärän</li><li>Työntekijä määrittää EvidenceOfInsurability-kentän arvoksi **Kyllä**</li></ul> |
| **Edunsaaja** | Työntekijä > Profiili > Henkilökohtaiset yhteystiedot > Henkilökohtaiset yhteyshenkilöt | Henkilökohtainen yhteyshenkilö lisätään ja **Edunsaaja**-ruutu sekä **Voimaantulopäivämäärä** täytetään. Henkilökohtaisen yhteyshenkilön tyypin on oltava **Lapsi**, **Puoliso**, **DomesticPartner**, **Sisarus**, **FamilyContact**, **OtherContact**, **Vanhempi**, **BeneficiaryEstate**, **BeneficiaryOrg** tai **BeneficiaryTrust**. |
| **Työntekijä - Medicare** | Työntekijä > Työntekijä > Versiot > Työhistoria > Päivämäärän hallinta > Etutiedot | <ul><li>**EhrMedicareEligibilityDate** on muutettu</li><li>**MedicareEligibile**:n arvoksi on asetettu **Kyllä**</li></ul> |
| **Syntymäpäivä** | Työntekijä > Profiili > Henkilökohtaiset tiedot > Henkilökohtaiset yhteystiedot > Huollettavan tiedot > Syntymäpäivä | Syntymäaika lisätään tai päivitetään (ei elinkaaritapahtuman muutoksen käsittelyn jälkeen). Esimerkki: Jos lapsen **Henkilökohtaisen yhteyshenkilön kelpoisuusvaihtoehdot** -kohtaan on asetettu ikä: 26, kohdassa Määritys > Etuudet > Henkilökohtaisten yhteystietojen kelpoisuusasetukset ja jos HR-henkilöstö suorittaa elinkaaritapahtuman muutoksen käsittelyn joka päivä sen jälkeen, kun huollettava täyttää 26, näyttöön tulee sanoma, jossa kerrotaan, että huollettava ei ole enää oikeutettu kattavuuteen. |
| **Työntekijän kelpoisuusmuutos (ei koske vain Yhdysvaltoja)** | <ul><li>Työntekijä > Työsuhde</li><li>Työntekijä > Työntekijä > Versiot > Työhistoria</li></ul> | <ul><li>Työntekijän tyyppi, työsuhdeluokka tai viisi käyttäjän määriteltävissä olevaa kelpoisuuskenttää muuttuvat</li><li>**HcmEmploymentDetail.EhrEmploymentType** -muutokset ( käsitellään vain *muuttuneiden* työtietojen tietueissa, joita ei käsitellä *Uusissa* työtietueissa, kuten uudelleentyöhönotto ja irtisanominen)</li></ul> |
| **Uusi etukelpoisuuden ohitus (ei koske vain Yhdysvaltoja)** | Henkilöstöhallinnon kehittyneet > Edut > Suunnitelmat > Edut > Oikeutussäännön ohitus | Elinkaaritapahtuman käsittelyn käyttäminen | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Etukelpoisuussäännön ohituksen muutos (ei koske vain Yhdysvaltoja)** | Henkilöstöhallinnon kehittyneet > Edut > Suunnitelmat > Edut > Oikeutussäännön ohitus | Elinkaaritapahtuman käsittelyn käyttäminen (nappaa vain muutokset **ValidFrom**- ja **ValidTo** -kentille kelpoisuussäännön ohitustilassa) |
| **Etukelpoisuuden ohituksen päättyminen (ei koske vain Yhdysvaltoja)** | Henkilöstöhallinnon kehittyneet > Edut > Suunnitelmat > Edut > Oikeutussäännön ohitus | Elinkaaritapahtuman muutoksen käsittelyn käyttäminen. Jos esimerkiksi muokkaat suunnitelman oikeutussääntöä, jonka mukaan vanhentumispäivä on tänään klo 5:00 PM, milloin tahansa sen jälkeen, kun 5:00 PM tai seuraavat päivät on kulunut, ja suoritat sitten elinkaaritapahtuman muutoksen käsittelyn, näyttöön tulee sanoma, jonka mukaan oikeutussäännön ohitus on vanhentunut. |
| **Uusi etuussuunnitelma (ei koske vain Yhdysvaltoja)** | Henkilöstöhallinnon kehittyneet > Edut > Suunnitelmat > Uusi | <ul><li>Kelpoisuusvaihtoehdot lisätään nykyiseen suunnitelmaan</li><li>Uusi suunnitelma, johon on liitetty kelpoisuusehtoja, lisätään</li></ul></br></br>Henkilöstöhallinnon henkilökunnan tulisi suorittaa tässä tapauksessa elinkaaritapahtuman kelpoisuuden käsittely. |
| **Etukelpoisuussäännön muutos (ei koske vain Yhdysvaltoja)** | Henkilöstöhallinnon kehittyneet > Edut > Säännöt/vaihtoehdot > Kelpoisuussäännöt | Elinkaaritapahtuman kelpoisuuskäsittelyn käyttäminen. Lokiin kirjataan , kun **EhrBenefitEligibilityRule**-tietueissa on muutettu seuraavat arvot: **UseEmplCategory**, **UseEmplStatus** tai **UseEmplType**. Päivittää vain ne elinkaaritapahtuman tapahtumat, jotka ovat jo muuttuneessa säännössä tai kelpoisuusehdoissa. |
