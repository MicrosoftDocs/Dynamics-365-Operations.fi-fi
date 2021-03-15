---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (14. toukokuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 14. toukokuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8d65236d316035722451a871afabedc6ab73f7a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127846"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (14. toukokuuta 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia. Muutokset koskevat koontiversion numeroa 8.1.3244. Joissakin otsikoissa suluissa olevat luvut viittaavat Lifecycle Services (LCS) -palveluiden tukinumeroihin.

## <a name="platform-changes"></a>Alustan muutokset

Ympäristömuutokset sisältyvät tämän viikon julkaisuun. Lisätietoja on kohdassa [Finance and Operations -sovellusten version 10.0.10 ympäristöpäivitykset (toukokuu 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34). Tämä versio sisältää ohjelmakorjauksia ja tallennettujen näkymien muutoksia.
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>Dataverse -valintaluetteloiden ja lomien valintaluetteloiden yhdenmukaisuuden varmistaminen (436343)

Dataverse -valintaluettelot ja lomien valintaluettelot ovat nyt yhdenmukaisia.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Käyttäjät saavat määrittää lomapyyntötyönkulun pyydetyn määrän perusteella (300044)

Käyttäjät voivat määrittää lomapyyntötyönkulkuja pyydettyjen määrien perusteella.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Uuden työntekijän lomakkeessa tiedot tulevat näkyviin Näytä-valikossa, kun suojauksen lisäasetukset on otettu käyttöön (403185)

Tämä versio korjaa tavan, jolla työntekijöitä tarkastellaan yritysten toiminnoissa, kun lisäkäyttöoikeudet on otettu käyttöön ja muiden yritysten työntekijät ovat käytettävissä.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Yhden suunnitelman tai yhden yrityksen loman jaksotuksen salliminen (318844)

Tämän muutoksen myötä jaksotuksen voi suorittaa yrityksen tai suunnitelman kohdalla.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Toimen kokoaikaisuuden vastaavuuden näyttäminen (FTE) Rekisteröityneet työntekijät -lomakkeessa (414658)

Työntekijän toimen FTE-arvo määrittää työntekijän jaksotusarvon, kun FTE-vaihtoehto on otettu käyttöön lomatyypissä. Tämä kenttää sisältyy nyt **Rekisteröityneet työntekijät** -lomakkeeseen ja **Joukkorekisteröinti**-valintaikkuna.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Lomasaldon vanhentumisen erätyön lisääminen (431266)

Päivittäin suoritettava uusi erätyö on nyt saatavana. Se vähentää jäljellä olevaa lomasaldoa, kun vanhentumispäivät tulevat ajankohtaisiksi.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Työntekijöiden omien yhteyshenkilöiden vienti työntekijän oman yhteyshenkilöentiteetin avulla ei vie omia yhteyshenkilöitä, joissa on ylätason suhdetyyppi (345893)

**Työntekijän oma yhteyshenkilö** -tietoyksikkö (**HcmPersonalContactPersonEntity** DMF:ssä ja **PersonalContactPerson** ODatassa) ei voinut vielä omia yhteystietoja, joiden suhdetyyppi on **Ylätaso**. Tämä ongelma on korjattu omissa yhteystiedoissa, jotka on luotu tämän muutoksen jälkeen. Aiemmin luodut **Ylätaso**-tyypin omat yhteystiedot korjataan myöhemmässä versiossa.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Syykoodit näkyvät eri skenaarioissa, kun ne on merkitty lomaksi ja poissaoloksi ja yksinkertaistettu työtekijälomake on otettu käyttöön (434163)

Tämä muutos rajoittaa syykoodit vain loma- ja poissaolokoodeihin, kun yksinkertaistettu työntekijämerkintä otetaan käyttöön.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Esiversiotoiminto Määritä lomasuunnitelma työntekijöille tulevaisuudessa näyttää virheen (433555)

Tämä muutos korjaa virheen, kun lomasuunnitelmassa on määritetty kaksi lomatyyppiä ja yrität määrittää työntekijän.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Aloituspalkki näytetään kaikille käyttäjille (441731)

Tämän muutoksen myötä Aloituspalkki piilotetaan käyttäjiltä, jotka eivät ole järjestelmänvalvojia tai tiedonhallinnan järjestelmänvalvojia. 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Dataversen työntekijän osoite-entiteetti toimii eri tavalla kuin Human Resourcesin päivämäärän ja ajan voimassaolopäivät (425071)

Tämä muutos säilyttää osoitetietojen kohdistuksen tietyissä skenaarioissa osoitteen päivämäärien perusteella.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Liitettä ei voi lisätä hyväksyttyyn lomapyyntöön (425407)

Tämän viikon julkaisun myötä voi liittää liitteitä hyväksyttyihin lomapyyntöihin lomapyyntöä muuttamatta.

## <a name="in-preview"></a>Esiversiossa

## <a name="leave-suspension"></a>Loman keskeytys

Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa. Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset. Jos keskeytys tapahtuu jaksotuksen käsittelyn jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon. Lisätietoja on kohdassa [Loman keskeytys](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Päivitä käyttäjäkokemus osoittamaan, että jaksotus on keskeytetty (429550)

Käyttökokemus ilmaisee nyt, että jaksotus on keskeytetty suunnitelmaa varten.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Valitun lomatyypin kertymän keskeyttäminen (272447)

Tässä julkaisussa HR voi luoda säännön, joka keskeyttää työntekijöiden loma- ja palkatonta lomaa varten syötettyjen lomapyyntöjen maksamisen. Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla. Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten (429549)

DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Lisää syykoodi jaksotuskeskeytyksiin (429547)

Syykoodit on lisätty kertymän keskeyttämiseen.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Aloita siirryttäessä henkilöstöhallinnon parametreista loma- ja poissaoloparametreihin

Tämä julkaisu alkaa yhdistää henkilöstöhallinnon parametreja loma- ja poissaoloparametreihin.

## <a name="carry-forward-rules"></a>Siirtokirjauksen suorituksen säännöt

Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään. Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi. Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]