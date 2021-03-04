---
title: Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (1. lokakuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 69c0a805027f215b2a2a42d826ee7a346cfdd511
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529657"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-1-2019"></a>Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (1. lokakuuta 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2509. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="streamlined-employee-entry-and-navigation"></a>Yksinkertaistettu työntekijöiden lisääminen ja navigointi

Tämä toiminto on nyt käytettävissä kaikissa ympäristöissä. Ota tämä toiminto käyttöön valitsemalla **Järjestelmän hallinta > Linkit > Asetukset > Järjestelmän parametrit > Esiversio-ominaisuudet**. Valitse **Laajennettu työntekijälomake ja siirtyminen**. Nämä muutokset otetaan nyt käyttöön kaikille käyttäjille. Voit poistaa tämän asetuksen käytöstä milloin tahansa.

Lisätietoja on kohdassa [Yksinkertaistettu työntekijöiden lisääminen ja navigointi](./streamlined-employee-entry.md). Jos haluat katsoa videon näistä muutoksista, katso [Dynamics 365 for Talent 2019 -julkaisuaallon 2 yleiskatsaus](https://aka.ms/ROGT19RW2ROV).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Voit ottaa esikatselutoiminnot käyttöön eristys- ja kokeiluympäristöissä

Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi Tuotanto vai Eristys. Eristys-tyypin esiintymät sallivat uusien toimintojen kokeilemisen varhaisessa vaiheessa. Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään Eristys-esiintymätyypiksi, ota yhteyttä tukeen ja tee muutospyyntö.

Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](./provisioning-talent.md).

### <a name="compensation-date-defaults-to-a-different-date-than-the-position-assignment-337694"></a>Kompensaatiopäivämäärä on oletusarvoisesti eri päivämäärä kuin toimen toimeksianto (337694).

Tämän muutoksen myötä kompensaation alkamispäivä on oletusarvoisesti toimen toimeksiannon alkamispäivä.

### <a name="not-able-to-end-compensation-along-with-its-position-assignment-328993"></a>Kompensaatiota ei voi lopettaa yhdessä sen toimen toimeksiannon kanssa (328993)

Tämän muutoksen myötä voit lopettaa kompensaation, kun lopetat toimen toimeksiannon **Lopeta määritys** -vaihtoehdolla **Työntekijöiden toimimääritykset** -sivulta, kun henkilöstötoiminnot ovat käytössä.

### <a name="bank-account-validation-requires-routing-and-account-numbers-in-all-locations-340403"></a>Pankkitilin vahvistus edellyttää reititys- ja tilinumeroita kaikissa sijainneissa (340403)

Tämän viikon muutosten myötä on lisätty uusi määritysvaihtoehto, joka poistaa käytöstä **Reititysnumero**- ja **Pankkitili**-arvojen pakollisuuden vahvistuksesta. 

### <a name="attachments-are-not-enabled-in-mss-performance-journals-for-performance-feedback-341794"></a>Liitteet eivät ole käytössä esimiehen itsepalvelun suoritustason kirjauskansioissa suorituskyvyn palautteelle (341794)

Tämän viikon julkaisun myötä liitteet otetaan käyttöön palautenimikkeille Suoritustason kirjauskansio -sivulla.

### <a name="leave-request-details-dont-sync-from-common-data-service-to-talent-369608"></a>Lomapyyntöjen tietoja ei synkronoida Common Data Servicesta Talentiin (369608)

Näiden muutosten myötä Common Data Servicessa päivitettyjen lomapyyntöjen tiedot synkronoidaan takaisin Talentiin.

### <a name="job-description-doesnt-display-for-the-job-in-the-skill-gap-analysis-page-369398"></a>Työn kuvausta ei näytetä Osaamiseroanalyysi-sivulla (369398)

Tämän viikon koontiversiossa kuvaus näytetään, kun työ valitaan **Osaamiseroanalyysi**-sivulla.

## <a name="coming-soon"></a>Tulossa pian

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Työntekijät, esimiehet ja HR-ammattilaiset voivat tulostaa työntekijän kehityskeskustelun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]