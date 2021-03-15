---
title: Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet (16. syyskuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 16. syyskuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 74a87ddb4ed14042dd4e716ad64bc844a800a0a0
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112433"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet (16. syyskuuta 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia. Muutokset koskevat koontiversion numeroa 8.1.3557. Joidenkin toimintojen vieressä suluissa olevat luvut viittaavat Lifecycle Services (LCS) -palveluiden tukinumeroihin.

## <a name="included-in-this-release"></a>Tässä julkaisussa mukana olevat ominaisuudet

-  [Tallennetut näkymät – yleinen saatavuus](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Lisätietoja: [Tallennetut näkymät](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views). 

- **Toimen toiminnot** -lomakkeessa on päivitetty dimensioruudukko ja uusi valintaikkuna (469495).

- Jos määrität kohdan **Rajoita työntekijätietojen käyttöoikeuksien** arvoksi kyllä **Jaetut henkilöstöhallinnon parametrit** -kohdan kohdassa **Lisäkäyttöoikeudet**, lomakkeissa näkyvät nyt vain sopivat työntekijät (393384).

- Uuden kalenterin luontivaihtoehdot **WorkCalendar**-yksikössä (477055):<br>- Oletusarvoinen päättymisaika<br>-    Oletusarvoinen alkamisaika<br>-  Perjantai työpäivä?<br>-  Maanantai työpäivä?<br>-  Lauantai työpäivä?<br>-  Sunnuntai työpäivä?<br>-  Torstai työpäivä?<br>-  Tiistai työpäivä?<br>-  Keskiviikko työpäivä?<br>- Työkalenterin lomatunnus

- **LeaveBankTransactionV1**-yksikkö sisältää nyt syykoodin (477823).

- Voit nyt tallentaa tehtävätallenteita (492923).

- Tietoja julkaistaan nyt onnistuneesti yksiköstä **HCMWorkerContactEntity** (427620).

- **Kompensaatio**-pikavälilehti näkyy nyt alihankkijan työntekijätyypin osalta **Työntekijätoiminnot**-lomakkeessa (482494).

- **Taso**- ja **Suunnitelma**-kentät ovat nyt pakollisia, kun määritetään **Kiinteä kompensaatio**. Jos jätät nämä kentät tyhjiksi, näkyviin tulee virhesanoma (482497).

- **Etuudet**-kohdan **Suunnitelma**-kenttä on nyt avattava luettelo (488768).

- Järjestelmänvalvojat saavat nyt ilmoituksen, jos mukautettu kenttä poistetaan henkilöstöresursseista (481408).

- Työntekijän työsuhteen päättymisen yhteydessä henkilöstöhallinto toimii odotetusti eikä muuta valittua yritystä lukitsemisen jälkeen (479877). 

- Esimiehet eivät voi enää lisätä numerosaraketta mukautuksen kautta (485317).

- Esimiehet eivät voi enää poistaa tietoalueen suodatinta vanhentuvista tunnusnumeroista (485321).

- Kun **Raportoi toimelle** -kenttä on tyhjä, aseman tiedot näkyvät edelleen, kun hiiren osoitin on aseman päällä (433328).

- Työntekijät voivat nyt tarkastella etuussuunnitelmien tietoja työntekijän itsepalvelussa (481676).

- Työntekijät voivat nyt nähdä kaikki rekisteröidyt kurssit (429048).

- Voit nyt rajoittaa **Ammattisertifikaatit**-sivun tarkastelumahdollisuuksia. Voit rajoittaa tarkasteluoikeudet nykyiseen yritykseen, työntekijän tilan perusteella sekä työntekijän tyypin perusteella (451501). 


## <a name="in-preview"></a>Esiversiossa

### <a name="human-resources-app-in-teams"></a>Teamsin Human Resources -sovellus

Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä. Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä. Lisätietoja:

- [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 1 -suunnitelmassa
- [Teamsin Human Resources -sovellus](https://go.microsoft.com/fwlink/?linkid=2127841) Human Resources -sovelluksen dokumentaatiossa

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources -sovellus Teamsin esiversiotoiminnoissa
 
-  **Ilmoitukset**: Poissaolopyyntöjen lähettäjät ja hyväksyjät saavat ilmoitukset Teamsin Human Resources -sovelluksessa. Hyväksyjät voivat hyväksyä tai hylätä poissaolopyyntöjä. Lähettäjille ilmoitetaan, jos pyyntö on hyväksytty tai hylätty. Lisätietoja:
   - [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 2 -suunnitelmassa
   - [Teamsin Human Resources -sovelluksen ilmoitusten käyttöönotto](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) Human Resources -sovelluksen dokumentaatiossa
   - [Teams-ilmoitusten käyttöönotto tai käytöstäpoisto yksittäisille käyttäjille](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) Human Resources -sovelluksen dokumentaatiossa
   - [Teams-ilmoitukset](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) Human Resources -sovelluksen dokumentaatiossa
   - [Ryhmän lomakalenterin tarkasteleminen](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) Human Resources -sovelluksen dokumentaatiossa
 
- **Esimiehen poissaolokalenteri**: Esimiehet voivat nähdä suorien alaisten hyväksytyt ja odottavat poissaolot kalenterinäkymässä. Tämän näkymän avulla on helppo hahmottaa, milloin ryhmä jäsenet ovat poissa töistä. Lisätietoja:
   - [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 2 -suunnitelmassa
   - [Ryhmän lomakalenterin tarkasteleminen](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) Human Resources -sovelluksen dokumentaatiossa

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus (477004)

Uusi asetus on nyt käytettävissä toimelle **Itselle määritetyt työnimikkeet** -luettelossa koontinäytön oikeanpuoleisessa sarakkeessa. Tämän muutoksen myötä kaikki työnimikkeet ja tehtäväluettelot näkyvät samalla alueella. Jos haluat tämän toiminnon käyttöön, ota käyttöön **Esikatselu - työnkulun käyttökokemuksen parannukset** -kohta ominaisuuksien hallinnassa. Lisätietoja esikatseluominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

Tämä toiminto edistää myös henkilöstön toimintojen lomakkeissa olevia työnkulkuasetuksia. Työnkulunasetukset näkyvät myös toiminnon nopean käytön pikavälilehdessä. Lisätietoja: 

- [Organisaation ja henkilöstön hallinnan työnkulun käyttökokemuksen parannukset](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) Dynamics 365:n vuoden 2020 julkaisuaallon 2 suunnitelmassa

![Minulle määritetyt työnimikkeet](./media/hr-workflow-work-items-assigned-to-me.png)

![Työnkulkunimikkeiden nopea käyttö](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Loma- ja poissaolokalenteri

Tämä julkaisu sisältää lisää kalenterivaihtoehtoja loma- ja poissaolokalentereja varten. Lisätietoja on kohdassa [Ryhmä- ja yrityskalenterien tarkasteleminen](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).

## <a name="coming-soon"></a>Tulossa pian

### <a name="checklist-entities-included-in-dataverse"></a>Dataverseen sisältyvät tarkistusluettelokohdat

Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.

### <a name="benefits-management-reason-codes"></a>Etujen hallinnan syykoodit

Etujen hallinnan syykoodit yhdistetään pian olemassa oleviin syykoodeihin Human Resources -sovelluksessa. Jos olet määrittänyt etujen hallinnassa syykoodeja, joiden pituus on yli 15 merkkiä, syykoodin nimeä on muutettava etujen hallinnan **Syykoodit**-lomakkeessa niin, että pituus on enintään 15 merkkiä. Kun olet päivittänyt nimen, syykoodi näkyy olemassa olevan syykoodilomakkeen henkilöstön hallinnassa. Tämä muutos on käytettävissä tulevaisuudessa. Se ei vaikuta olemassa oleviin toimintoihin.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]