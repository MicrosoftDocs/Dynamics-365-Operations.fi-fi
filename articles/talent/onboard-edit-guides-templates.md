---
title: 'Perehdytysoppaiden ja mallien muokkaaminen Dynamics 365 Talent: Onboardissa'
description: 'Tässä ohjeaiheessa käsitellään tehtävien ja muiden tietojen lisäämistä Microsoft Dynamics 365 Talent: Onboardin perehdytysoppaisiin ja malleihin.'
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897117"
---
# <a name="edit-onboarding-guides-and-templates"></a>Perehdytysoppaiden ja mallien muokkaaminen

[!include [banner](includes/banner.md)]

Kun olet luonut perehdytysoppaan tai mallin Microsoft Dynamics 365 Talent: Onboard, sinun on lisättävä johdanto, tehtävät, yhteyshenkilöt ja resurssit. Voit lisätä Onboardin perehdytysoppaisiin monipuolista sisältöä, kuten seuraavat:

- YouTube-videot
- Microsoft Sway -esitykset
- Microsoft PowerApps -sovellukset
- Microsoft Stream -videot
- Microsoft Forms -lomakkeet
- Verkkosisältöä sisältävät iFrame-kehykset

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Mallista tuotujen johdantojen tai tehtävien muokkaaminen

Jos luot perehdytysoppaan mallista tai tuot tehtäviä mallista toiseen malliin, tuoduissa tehtävissä on **Lukitus**-painike. Näitä tehtäviä kutsutaan *hallituiksi tehtäviksi*.

[![Hallitut tehtävät](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Kun valitset hallitun tehtävän, lähdemalli näkyy tehtävän yläosassa.

[![Hallitun tehtävän lähde](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Jos muokkaat tehtävää mallissa, Onboard siirtää muutokset kaikkiin malleihin ja kyseiseen malliin perustuviin lähettämättömiin oppaisiin. Jos valitset lähettämättömän oppaan muokkaamasi mallin perusteella ja valitset sitten oppaassa **Tehtävät**-välilehden, huomaat, että opas on muuttunut. Voit hylätä ilmoituksen valitsemalla **OK**. 

[![Muutosilmoitus](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Päivitettyjen tehtävien vieressä on musta piste.

[![Muutettu tehtävä](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Hallittuja tehtäviä ei voi muokata alkuperäisen mallin ulkopuolella lukuun ottamatta vastuunhenkilön, määräpäivän tai muiden tehtävän oikeanpuolisessa olevien tietojen lisäämistä.

Jos haluat muokata hallittua tehtävää tai jos et halua, että tehtävä saa päivityksiä alkuperäisestä mallista, valitse kyseisen tehtävän **Lukitus**-painike. **Lukitus**-painike häviää. Alkuperäinen malli ei enää hallitse tehtävää eikä se enää vastaanota päivityksiä kyseisestä mallista. Tehtävään tehdyt päivitykset eivät vaikuta alkuperäiseen malliin.

Jos poistat tehtävän oppaasta ja siirrät kyseisen oppaan mallin muutokset, tehtävät jää poistetuksi oppaassa.

> [!NOTE]
> Mallit eivät hallitse yhteyshenkilöitä ja resursseja. Myöskään osat eivät ole hallittuja, joten jos lisäät osan tai muokkaat sitä mallissa, muutoksia ei siirretä muihin kyseistä mallia käyttäviin oppaisiin tai malleihin.
> 
> Jos lisäät uusia tehtäviä malliin, uudet tehtävät siirretään kyseiseen malliin perustuviin oppaisiin ja malleihin. Nämä uudet tehtävät näkyvät kyseisen mallin yläosassa.

## <a name="import-activities-from-another-template"></a>Tehtävien tuominen toisesta mallista

Voit tuoda tehtäviä oppaaseen tai malliin yhdestä tai useasta mallista.

1. Valitse muokattava opas tai malli.

2. Valitse **Tehtävät**-välilehti.

3. Valitse oikealla **Tuo**-välilehti.

   [![Tehtävien tuominen](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Voit esikatsella tehtäviä uudessa selaimen välilehdessä valitsemalla mallissa **Avaa uudessa välilehdessä** -painike.

   [![Tehtävien tuominen](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Vedä ja pudota sopiva malli siihen ohjemallin kohtaan, jossa haluat tehtävien näkyvän. Jatka oppaan tai mallin muokkaamista.

Tuoduissa tehtävissä on **Lukitus**-painike, joka ilmaisee, että se malli hallitsee kyseisiä tehtäviä, josta ne tuotiin. Kun teet muutoksia tuotuun malliin, nämä tehtävät päivitetään mallissa, johon ne tuotiin. Muutoksia ei kuitenkaan voi siirretä automaattisesti kaikkiin siitä mallista luotuihin oppaisiin, joihin tuonti tapahtui.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Muutosten siirtäminen mallista toiseen malliin tai oppaaseen.

Jos muokkaat muissa malleissa tai oppaissa käytettyjä tehtäviä, muutokset on siirrettävä, jos haluat niiden näkyvän muissa malleissa tai oppaissa.

Jos et ole varma, käytetäänkö mallin tehtäviä muissa malleissa tai oppaissa, valitse **Käytössä**-välilehti ja tarkista, missä kyseiset tehtävät näkyvät.

   [![Niiden oppaiden ja mallien näyttäminen, joissa tehtäviä käytetään](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Muutosten siirtäminen:

1. Tallenna muutokset valitsemalla **Tallenna**-painike. Jos et toimi näin, sinua pyydetään tallentamaan muutokset seuraavassa vaiheessa.

2. Valitse **Siirrä nämä muutokset**.

   
## <a name="add-or-edit-an-introduction"></a>Johdannon lisääminen tai muokkaaminen

1. Kirjoita oppaalle otsikko ja avausviesti **Johdanto**-välilehti. Voit käyttää näytetekstiä valitsemalla **Käytä tätä viestiä**.

    [![Onboard-mallin Johdanto-välilehti](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Käytä muotoilupainikkeita tarpeen mukaan tekstin hakemiseen tai kuvien tai linkkien lisäämiseen.
3. Tallenna työsi valitsemalla **Tallenna**.

## <a name="add-or-edit-activities"></a>Tehtävien lisääminen tai muokkaaminen

1. Vedä kohteita **Tehtävät**-välilehdessä oikealta muokkausalueelle.
2. Järjestä opas osiin vetämällä **Uusi osa** -kohde muokkausalueelle ja anna osalle nimi ja valinnainen kuvaus.

    ![[Uuden osan lisääminen onboarding-oppaaseen tai malliin](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Lisää tehtäviä uudelle työntekijälle tehtäväksi vetämällä **Uusi tehtävä** -kohde muokkausalueelle ja anna tehtävälle nimi ja kuvaus.

    ![[Uuden tehtävän lisääminen onboarding-oppaaseen tai malliin](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Monipuolisen sisällön lisääminen perehdytysoppaaseen:

    - Lisää YouTube-video vetämällä **YouTube**-kohde muokkausalueelle, anna tehtävälle nimi ja kuvaus ja anna YouTube-videon URL-osoite.
    - Lisää Sway-esitys tai -uutiskirje vetämällä **Sway**-kohde muokkausalueelle, anna tehtävälle nimi ja kuvaus ja anna Sway-esityksen tai -uutiskirjeen upotettu URL-osoite.
    - Lisää Microsoft Power Apps-sovellus vetämällä **Power Apps**-kohde muokkausalueelle, anna tehtävän nimi ja kuvaus ja joko valitse Power Apps-sovellus tai anna Power Apps-sovelluksen tunnus.
    - Lisää Microsoft Stream -video vetämällä **Microsoft Stream** -kohde muokkausalueelle, anna tehtävälle nimi ja kuvaus ja anna Microsoft Stream -videon URL-osoite.
    - Lisää Microsoft Forms -lomake vetämällä **Microsoft Forms** -kohde muokkausalueelle, anna tehtävän nimi ja kuvaus, anna Microsoft Forms -lomakkeen URL-osoite ja määritä näyttöalueen koko.
    - Lisää verkkosisältöä sisältävä iframe vetämällä **Internet-sisältö (iframe)** -kohde muokkausalueelle, anna tehtävän nimi ja kuvaus, anna verkkosisällön URL-osoite ja määritä näyttöalueen koko.

    ![[RTF-muotoisen sisällön lisääminen onboarding-oppaaseen tai malliin](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Valinnainen: määritä kunkin tehtävän oikealla puolella olevalla alueella tehtävä tietylle henkilölle tai tiettyyn rooliin, lisää määräpäivä ja yhteyshenkilö ja määritä luokan väri. Kun määrität tehtävän henkilölle tai rooliin, tehtävä luodaan kullekin henkilölle. Tämä tehtävä näkyy Onboardin **tehtävät**-valikossa.

    [![Tehtävän määrittäminen perehdytysoppaassa tai mallissa](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Tallenna työsi valitsemalla **Tallenna**.

Poista tehtävä tai osa valitsemalla **Poista**-painike (roskakorisymboli) tehtävän tai osan oikeassa yläkulmassa.

Muuta tehtävien tai osien järjestystä vetämällä ne uuteen sijaintiin.

## <a name="add-or-edit-contacts"></a>Yhteyshenkilöiden lisääminen tai muokkaaminen

Voit lisätä yhteyshenkilöitä, jotka voivat auttaa uutta työntekijää menestymään ensimmäistä työpäivästä alkaen. Nämä yhteyshenkilöt voivat olla työhönottajia, ryhmän jäseniä, perehdyttäjiä, mentoreita, järjestelmänvalvojia ja IT-tuen henkilöitä.

1. Valitse **Yhteyshenkilöt**-välilehdessä **Uusi yhteyshenkilö**.
2. Anna **Lisää ryhmän jäsen** -valintaikkunassa yhteyshenkilön nimi tai sähköpostiosoite, lisää sitten lyhyt kuvaus, joka selittää, miten yhteyshenkilö voi auttaa uutta työntekijää, ja valitse lopuksi **Lisää**. 

    ![[Yhteyshenkilöiden lisääminen onboarding-oppaaseen tai malliin](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Vaihtoehtoisesti voit valita vähintään yhden yhteyshenkilön **Ehdotukset**-kohdassa.

3. Tallenna työsi valitsemalla **Tallenna**.

Poista yhteyshenkilö valitsemalla **Poista**-painike (roskakorisymboli) yhteyshenkilön oikealla puolella.

Muokkaa yhteyshenkilöä valitsemalla **Muokkaa**-painike (kynäsymboli) yhteyshenkilön oikealla puolella.

## <a name="add-or-edit-resources"></a>Resurssien lisääminen tai muokkaaminen

Voit lisätä hyödyllisiä tiedostoja, karttoja ja linkkejä perehdytysoppaan **Resurssit**-osaan.

1. Valitse **Resurssit**-välilehdessä **Uusi resurssi**.
2. Noudata seuraavia ohjeita:

    - Lisää tiedosto valitsemalla **Tiedosto**-välilehti ja vetämällä tiedosto määritetylle alueelle. (Vaihtoehtoisesti voit napsauttaa kyseistä aluetta ja siirtymällä tiedostoon tietokoneessa tai valitse **Selaa OneDrive**.) Anna tiedostolle nimi ja valitse sitten **Lisää**.
    - Lisää linkki valitsemalla **Linkki**-välilehti, anna linkille nimi ja osoite ja valitse sitten **Lisää**.
    - Lisää kartta valitsemalla **Kartta**-välilehti, anna kartta nimi ja osoite ja valitse sitten **Lisää**. Onboard sisällyttää määritetyn osoitteen kartan.

    ![[Resurssin lisääminen onboarding-oppaaseen tai malliin](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Tallenna työsi valitsemalla **Tallenna**.

Poista resurssi valitsemalla **Poista**-painike (roskakorisymboli) resurssin oikealla puolella.

Muokkaa yhteyshenkilöä valitsemalla **Muokkaa**-painike (kynäsymboli) resurssin oikealla puolella.

## <a name="next-steps"></a>Seuraavat vaiheet

- [Sisällön jakaminen muiden osallisten kanssa](./onboard-share-template.md)
- [Työntekijöiden tehtävien ja perehdyttämisen tilan näyttäminen](./onboard-view-status.md)
- [Työhönottoryhmien luominen Onboardissa](./onboard-create-team.md)

### <a name="see-also"></a>Lisätietoja

- [Onboard-sovelluksen kokeileminen tai ostaminen](https://dynamics.microsoft.com/talent/onboard/)
- [Dynamics 365 Talentin uudet ja muuttuneet ominaisuudet](./whats-new.md)
- [Julkaisusuunnitelmat](https://docs.microsoft.com/business-applications-release-notes/index)
- [Microsoft iDynamics 365 Talentin tuki](./talent-support.md)
