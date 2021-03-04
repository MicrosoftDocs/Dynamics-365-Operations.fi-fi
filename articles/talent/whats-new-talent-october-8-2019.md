---
title: Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (8. lokakuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40898ca7f54089337180def964b8942e8653663b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529477"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (8. lokakuuta 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2542. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Etuuksien avoimen haun poistaminen julkisesta esiversiosta

Blogiviestissä [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) annetun ilmoituksen myötä Microsoft poistaa etuuksien avoimen haun ominaisuuden julkisesta esiversiosta 18.10.2019. Sen korvaava toiminto julkaistaan myöhemmin. Julkisessa esiversiossa olevaa etuuksien avoimen haun toimintoa ei tueta tuotantokäytössä. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Common Data Service -integrointi on nyt oletusarvoisesti pois käytöstä uusissa provisioinneissa (343675)
 
Kun uusia ympäristöjä provisioidaan, Common Data Service -integrointi ei nyt ole käytössä. Lisätietoja on kohdassa [Common Data Service -integroinnin määritys](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Yksinkertaistettu työntekijöiden lisääminen ja navigointi

Työntekijöiden lisäämisen ja navigoinnin toiminto on nyt käytettävissä kaikissa ympäristöissä. Voit ottaa tämän toiminnon käyttöön siirtymällä kohtaan **Järjestelmän hallinta \> Linkit \> Asetukset \> Järjestelmän parametrit \> Esiversioton toiminnot** ja valitsemalla **Laajennettu työntekijälomake ja siirtyminen**. Tällöin toiminto ei ole käytössä kellään käyttäjällä. Voit poistaa tämän asetuksen käytöstä milloin tahansa.

Katso lisätietoja Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelman kohdasta [Yksinkertaistettu työntekijöiden lisääminen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry).

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Attract ja Onboard luovat ei-aktiivisia työntekijöitä Core HR:ssä (380517)

Tämän viikon julkaisu korjaa ongelman, jossa Houkuttele ja Tutustuta luovat ei-aktiivisia työntekijöitä Core HR:ssä

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Työnkulku epäonnistuu, kun esimies on kirjautuneena toiseen yritykseen päättäessään työntekijän työsuhteen (346852)

Työnkulku ei enää epäonnistu sen yrityksen perusteella, johon esimies on kirjautunut.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Puuttuvia tietoja kohteessa HcmOnboardingWorkerChecklistTaskEntity (349591)

Tämä julkaisu sisältää lisätietoja kohteesta **HcmOnboardingWorkerChecklistTaskEntity**. Seuraavassa on muutamia esimerkkejä:

- **Ryhmän nimi**, kun osoitettu tyyppi on **Ryhmä**
- **Työntekijän nimi**, kun osoitettu tyyppi on **Työntekijä**
- **Esimiehen nimi**, kun osoitettu tyyppi on **Esimies**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Entiteetit eivät näy aakkosjärjestyksessä Common Data Servicen hallinnassa (377414)

Entiteetit ovat nyt aakkosjärjestyksessä **CDS-hallinto**-sivulla.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Työsuhdetyypin muuttaminen tulevalla päivämäärällä ei salli toimen määritystä (339958)

Tämä muutos sallii toimen määritykset, kun työntekijätyyppejä muutetaan (esimerkiksi työntekijästä alihankkijaksi).

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Common Data Servicen lomapankin tapahtumayksikkö luo uuden tietueen kohteeseen Talentissa (352938)

Lomatapahtuma päivitetään nyt, kun Common Data Service päivitetään lomapankkitapahtumia varten.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Palautenimikkeiden liitteiden otsikossa näkyy palautteen kuvaus (343765)

Palautteen kuvaus ei enää näy liitteen otsikossa.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Kompensaatiotyönkulun Kommentit-kentässä näkyy virheellistä sisältöä (339297)

Tämä muutos näyttää kentän **%HcmActionState.HcmWorkerActionComment.Comments%** sisällön.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity ja WorkCalendarDayEntity eivät näy ODatan kautta (376329)

Tässä julkaisussa **WorkCalendarEntity** ja **WorkCalendarDayEntity** ovat nyt käytettävissä ODatan (Open Data Protocol) kautta.

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity on hidas, kun OData on käytössä (375221)

Muutoksia kohteen **HCMWorkerEntity** suorituskyvyn parantamiseksi, kun käytetään Microsoft Excelin työkirjan suunnittelua.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Esimiehen suorituskirjauskansiovienti näyttää virheen, kun suorituskirjauskansio on poistettu ja uusi luotu (336061)

Tämä julkaisu korjaa ongelman, joka ilmenee, kun yksi suorituskirjauskansio poistetaan ja toinen luodaan välittömästi sen jälkeen. Tämä korjaus muuttaa esimiehen itsepalvelun toimintaa.

## <a name="coming-soon"></a>Tulossa pian

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Katso lisätietoja Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelman kohdasta [Kehityskeskustelujen tulostaminen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews).


[!INCLUDE[footer-include](../includes/footer-banner.md)]