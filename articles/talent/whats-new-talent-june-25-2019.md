---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (25.6.2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
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
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 98ac7df9fa33635814b390427fd3292bdc1175ed
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528642"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-25-2019"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (25.6.2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="coming-soon-in-attract"></a>Tulossa pian Attractiin

### <a name="job-approvals-appear-on-the-home-page"></a>Työn hyväksynnät näkyvät aloitussivulla

Hyväksynnät näkyvät koontinäytön **Hyväksynnät**-osassa. Hyväksyjät voivat tarkistaa **Vastuualueensa** hyväksynnät, jolloin työn tunnus, otsikko, muut hyväksyjät ja määritetty päivämäärä näkyvät. Käyttäjät, jotka lähettävät työn hyväksyttäväksi, voivat tarkastella töitään kohdassa **Mitä olet pyytänyt**, joka näyttää hyväksyjät, joiden on vielä hyväksyttävä lähetetty työ.

## <a name="changes-in-onboard"></a>Onboardin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2357.

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>Ensisijaisen sijainnin näkyvä arvo on virheellinen (314266)

Nämä muutokset näyttävät **Ensisijainen sijainti** -asetuksen yhdenmukaisesti kaikilla sivuilla.

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>Muokkaus ei ole mahdollinen sen jälkeen, kun työnkulku on peruutettu tarkistuksessa (318180)

Työnkulun kautta peruutettuja tarkistuksia voi nyt muokata.

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>Tarkistusten viimeisten kommenttien kenttää ei ole käännetty (325921)

**Viimeisten kommenttien** selite käännetään Talentissa.

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Vain eritysympäristöissä käyttöönotettavat esiversiotoiminnot

Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi **Tuotanto** vai **Eristys**. **Eristys**-esiintymätyyppi mahdollistaa uusien toimintojen testaamisen varhaisessa vaiheessa. Kaikki aiemmin luodut Talent-esiintymät päivitetään **Tuotanto**-esiintymän tyyppiin. Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään **Eristys**-esiintymätyypiksi, ota yhteyttä [tukeen](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) ja tee muutospyyntö.

Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

## <a name="in-preview"></a>Esiversiossa

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Poissaolopyyntöjen lomatyyppien rajoittaminen

Organisaatiot voivat tarjota työntekijöille useita lomatyyppejä. Työntekijät eivät kuitenkaan ehkä voi lähettää joidenkin lomatyyppien poissaolopyyntöjä. Kyseisiä lomatyyppejä hallitaan sen sijaan henkilöstöhallinnossa. Tässä versiossa voit määrittää, mitä lomatyyppejä varten työntekijät voivat lähettää pyyntöjä. 

## <a name="coming-soon-in-core-hr"></a>Tulossa pian Core HR:ään

### <a name="feature-management-area-in-talent"></a>Toimintojen hallinnan alue Talentissa

**Toimintojen hallinta** poistetaan **järjestelmän hallinnasta** toimintoon liittyvien ongelmien vuoksi. **Toimintojen hallinta** otetaan uudelleen käyttöön tulevassa julkaisussa. 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service mukautettujen kenttien yksikkötuki

Seuraavat yksiköt tukevat mukautettuja kenttiä: **Palkanlaskennan ansiokoodit**, **Kiinteä kompensaatiotapahtuma**, **Kompensaatioruudukko**, **Maksukausi** ja **Kompensaation viitepiste**. 

### <a name="new-common-data-service-entities"></a>Uudet Common Data Service -yksiköt

**Syykoodit** lisätään sitten Common Data Serviceeen.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Suorien ja epäsuorien alaisten suoritustietojen näyttäminen esimiehen itsepalvelutoiminnossa

Uuden vaihtoehdon avulla esimiehet voit tarkastella sekä suorien että epäsuorien alaisten suoriutumista. Tällä hetkellä linjapäälliköt voivat määrittää ja päivittää suorituskykytavoitteita ja antaa uusia arvioita. Lisäksi suorat esimiehet ja heidän alaisensa voivat ylläpitää ja päivittää suoritustason kirjauskansioita. Tämä auttaa varmistamaan, että kehityskeskusteluprosessi toimii sujuvasti. Kun tämä muutos otetaan käyttöön, esimiehet voivat tarkastella ja ylläpitää epäsuorien alaisten suoritustasotietoja suorien alaisten tietojen lisäksi.

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Työntekijät, esimiehet ja henkilöstöhallinto voi tulostaa työntekijän kehityskeskustelun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]