---
title: Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 22. lokakuuta 2020
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 22. lokakuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: jcart1106
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 69534ce0024986e0b78932b3957023fcb9b8a584
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055601"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet 22. lokakuuta 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia. Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.3680.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Platform update 10.0.14(38) | -- | [Finance and Operations -sovellusten version 10.0.14 Platform update -päivitykset (marraskuu 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md) |
| Organisaation ja henkilöstöhallinnon työnkulkukokemuksen parannukset | [Organisaation ja henkilöstöhallinnon työnkulkukokemuksen parannukset](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero| Varasto-otto  | kuvaus|
| --- | --- | --- |
| 437922 | FMLA-tuntien tuominen DMF-entiteetin tulosten avulla vain luku -virheessä. | FMLA-tuntientiteetin käyttäminen tuomaan FMLA-palvelupyyntöön liitettyjä tunteja epäonnistui. Lisätty logiikka varmistaa, että tuodut tunnit eivät ylitä palvelupyynnössä jäljellä olevia tunteja. |
| 512019 | Virheellinen **Viimeisin siirtokirjaus** -summa. | **Tilannepäivämäärä**-asetuksen muuttaminen **Poissaolo**-sivulla seuraavan tilikauden ensimmäiseen päivään näytti virheellisen **Viimeisin siirtokirjaus** -summan **Vuosiloma**-tyypille. Nyt näkyvissä on oikea summa. |
| 458639 | **Työntekijän yhteyshenkilöt** -entiteetti ei tue muutosten seurantatilaa. | **Työntekijän yhteyshenkilöt** -entiteetti päivitettiin sitten, että sitä voidaan käyttää BYOD-skenaarioissa.|
| 505347 | Koulutusesimiehet voivat lähettää työntekijän poissaolopyynnön, kun virtaviivaistettu työntekijäominaisuus on otettu käyttöön. | Henkilöstöavustajan ja henkilöstöpäällikön rooleja lukuun ottamatta roolit eivät saa lähettää työntekijöiden lomapyyntöjä. |
| 513490 | Etujen hallinnan lokikirjaus: lokikirjauksen lisääminen suunnitelmiin, joissa ei ole kattavuusasetuksia. | Lokikirjaustulokset otettiin käyttöön **suunnitelmissa, joissa ei ole kattavuusasetuksia**. Ne näytetään nyt **Prosessin tulokset** -taulukossa ja ne lajitellaan näkymään oikein yläosassa. |
| 517021 | Useita suunnitelmia ei voi valita samalla **suunnitelman tyypin** koodilla, jos **suunnitelman tyypissä** on yksi tyyppikohtainen rekisteröityminen. | Rajoituksia muutettiin tilanteessa, jossa suunnitelmia valittaessa vain yksi rekisteröityminen sallitaan. Rajoitukset ovat nyt **suunnitelman tyyppikoodin** tasolla eikä **suunnitelman tyypin** tasolla. Tämän muutoksen ansiosta sallitaan suunnitelmat, kuten HSA ja FSA, joiden tyyppi on sama, mutta niille voidaan antaa eri **suunnitelman tyypin koodi**. Tällä tavoin voidaan valita molemmat samalla rekisteröitymisjaksolle. |
| 444791 | Kompensaatiota ei voi tarkastella työntekijän itsepalvelussa, kun **Rajoita käyttöä** on otettu käyttöön kompensaatiosuunnitelmassa. | Työntekijän itsepalvelun **Kompensaatio**-kortissa kompensaation tämän hetkisenä summana ja kasvuprosenttina näkyi 0, jos työntekijä oli rekisteröitynyt suunnitelmaan, kun **Rajoita käyttöä** oli käytössä ja määritetty tietyille rooleille. Tämä ongelma ratkaistiin siten, että työntekijä ja esimies voivat aina nähdä oman ja suorien alaisten kompensaatiotiedot. |
| 457542 | Kurssitietojen päivittäminen kurssin sulkemisen jälkeen ei päivitä samoja kurssiin osallistuneen työntekijän tietoja. | Työntekijän tiedot päivittyvät nyt oikein, kun kurssin tietoja muutetaan sen jälkeen, kun kurssi on suljettu ja sitten avattu uudelleen. |
| 515342 | Tietoja ei voi käyttää **CDSLeaveRequestDetailEntity**-arvon avulla. Yritystä ei löytynyt tai sitä ei ole. | Tietoja voi nyt lisätä käyttämällä **CDSLeaveRequestDetailEntity**-arvoa. |
| 514743 | Virhe **Sähköpostiparametri**-lomakkeessa, kun käytössä on Microsoft Exchange. | Sanoma Tiedostoja tai kokoonpanoa ei voitu ladata... näytettiin **Sähköpostiparametrit**-sivulla, kun sähköpostipalveluksi oli määritetty **Exchange**. Tämän korjauksen ansiosta **Sähköpostiparametrit**-sivu myös latautuu ja tallentuu odotetusti. |


## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Microsoft Teamsin Human Resources -sovellus | [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teamsin Human Resources -sovellus](./hr-admin-teams-leave-app.md)<br>[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md) |
| Työnkulun parannetut pyynnöt ja hyväksynnät | [Organisaation ja henkilöstöhallinnon työnkulkukokemuksen parannukset](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Human Resourcesin Dataversen virtuaaliyksiköt | [Dynamics 365 Human Resources -perustietojen laajentaminen Dataversessa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Dataverse -virtuaaliyksiköiden määrittäminen](hr-admin-integration-common-data-service-virtual-entities.md) |
| LinkedIn Talent Hub -integrointi | [LinkedIn Talent Hub -integrointi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub -integrointi](./hr-admin-integration-linkedin.md) |
| Mukautetut linkit esimiehen itsepalvelussa | [Mukautetut linkit esimiehen itsepalvelussa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Mukautetut linkit esimiehen itsepalvelussa](./hr-employee-manager-self-service-custom-links.md) |

## <a name="coming-soon"></a>Tulossa pian

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2020 julkaisuaallosta 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]