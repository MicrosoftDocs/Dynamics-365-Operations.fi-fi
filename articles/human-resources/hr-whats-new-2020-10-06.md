---
title: Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet (6. lokakuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 6. lokakuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: jcart1106
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 090533a4391488f4ec0929dd4866e55a478ee6e639563ad37a6819592e91b23c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739200"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet (6. lokakuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia. Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2020 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.3636.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraava ominaisuus on yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Lisää merkityksellisiä tietoja lomakalentereissa | [Merkityksellisten lomakalentereita koskevien lisätietojen antaminen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Ryhmä- ja yrityskalenterin tarkasteleminen](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

>[!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitykset saattavat sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Varasto-otto | kuvaus |
| --- | --- | --- |
| 448806 | **Oletustunnuksen tyyppi** viedään muodossa **RecID** HCM-parametreissa | Tämä Human Resourcesin parametriyksikön muutos lisää lisäsarakkeen, jossa näkyy **Oletustunnuksen tyyppi**. |
| 492923 | Tehtävätallenteet eivät tallennu Lifecycle Servicesissa (LCS) | Tehtävätallenteet voidaan nyt tallentaa LCS:ssa. |
| 429950 | Kiinteä kompensaatio ei pääty oikein työtehtävää vaihdettaessa | Kun työntekijän työtehtävää vaihdetaan **Siirrä työntekijä** -sivulla, kompensaation päättymispäiväksi oli määritetty yksi päivä työtehtävän päättymisen jälkeen. Kompensaation päättymispäivä on nyt sama kuin työtehtävän päättymispäivä. |
| 467214 | **Kuukausipalkka-analyysi** näkyy vain, jos **Palkkion muunnoksen nimi** -asetuksena on **Vuosittainen** | .Jos kuukausipalkan nimi on jokin muu kuin **Vuosittainen**, se ei näkynyt kompensaatioanalyysissa. Tämän päivityksen myötä kompensaatioanalyysi käyttää nyt kaikkia palkkion muunnoksia. Jos raportin suoritusperusteena on **Tunti** tai **Palkka**, kaikki jotakin muuta kuin tuntia jaksona käyttävä palkkion muunnos sisältyy **Palkka**-suodattimeen. **Tunneittain**-suodatin sisältää vain **Tunti**-jakson palkkiot. |
| 482464 | Kun **arvosteluja** tarkastellaan, **Tiedot**-näkymä ei vaihdu ruudukkonäkymäksi suodattimen käytön jälkeen. | Kun suodatinta on käytetty, arvosteluruudukko näkyy odotetusti. |
| 483184 | Human Resources ei luo lomakertymiä, kun **Tasoperuste** valitaan **Muutettu aloituspäivämäärä** -asetuksena **Loman rekisteröinti** -tietueessa |**Muutettu aloituspäivämäärä** täytetään ja sitä käytetään lomakertymiä luotaessa.  |
| 509731 | Sellaisen työntekijän poissaolopyyntö, jonka työsuhde päättyy tulevaisuudessa, jos työntekijä teki poissaolopyynnön ajankohta on työsuhteen päättymispäivän jälkeen | Poissaolopyyntöjä voidaan nyt lähettää työtekijöille, joiden työsuhde päättyy tulevaisuudessa, kunhan pyyntö koskee aikaa ennen työsuhteen päättymispäivää. |
| 510716 | Kompensaatioanalyysi sisältää sekä mies- että naistyöntekijät **Miesten keskituntipalkka** -kohdassa | Kompensaatioanalyysin **Kompensaation demografiatietojen analyysi** -kohdan **Miesten keskituntipalkka** sisälsi naisten keskipalkan. Se sisältää nyt vain miesten tiedot. |
| 511348 | Etujen itsepalvelussa pitäisi näkyvä vain kuluvasta päivästä etujakson loppuun voimassa olevat etuussuunnitelmat | Työntekijät näkivät vanhentuneet etuussuunnitelmat **Eturekisteröinti**-sivulla. Tämä korjaus poistaa kyseiset suunnitelmat. |
| 512706 | Seuraavat kentät määritetään vain luku -muotoisiksi:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Dimensiotietojen **Lisää**- ja **Poista**-painikkeet otettiin virheellisesti käyttöön toiminnon valmistumisen jälkeen. Tämän **Toimen toimintojen tiedot** -sivun päivitysten jälkeen, kenttiä ei voi muokata toiminnon valmistumisen jälkeen. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Microsoft Teamsin Human Resources -sovellus | [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teamsin Human Resources -sovellus](./hr-admin-teams-leave-app.md)<br>[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md) |
| Työnkulun parannetut pyynnöt ja hyväksynnät | [Organisaation ja henkilöstöhallinnon työnkulkukokemuksen parannukset](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Human Resourcesin Dataversen virtuaaliyksiköt | [Dynamics 365 Human Resources -perustietojen laajentaminen Dataversessa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Dataverse -virtuaaliyksiköiden määrittäminen](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Tulossa pian

Seuraavat uudet ominaisuudet on aikataulutettu tukeviin julkaisuihin:

- **Dataverseen sisällytetty tarkistusluetteloyksiköt**: käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluetteloyksiköt ovat pian saatavilla Dataversessa.

- **Etujen hallinnan syykoodit**: Etujen hallinnan syykoodit yhdistetään pian olemassa oleviin syykoodeihin Human Resourcesissa. Jos olet määrittänyt etujen hallinnassa syykoodeja, joiden pituus on yli 15 merkkiä, syykoodin nimeä on muutettava etujen hallinnan **Syykoodit**-lomakkeessa niin, että pituus on enintään 15 merkkiä. Kun olet päivittänyt nimen, syykoodi näkyy olemassa olevan syykoodilomakkeen henkilöstön hallinnassa. Tämä muutos on käytettävissä tulevaisuudessa. Se ei vaikuta olemassa oleviin toimintoihin.

- **Esimiehen itsepalvelun mukautetut linkit**: Esimiehen itsepalvelun ominaisuuksia laajennetaan esimiesten tueksi. Lisättävän on ominaisuus, jolla lisätään mukautettuja linkkejä **Oma ryhmä** -välilehdessä. Tämä ominaisuus muistuttaa mukautettuja linkkejä työntekijän itsepalvelun **Omat tiedot -välilehdessä**. Lisätietoja on kohdassa [Esimiehen itsepalvelun linkkien mukauttaminen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2019 2. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Lisäresurssit

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2020 julkaisuaallosta 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]