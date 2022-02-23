---
title: LinkedIn Talent Hub -integrointi
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin ja LinkedIn Talent Hubin integroinnin määrittämistä.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6f70e3a6ccf9770c75334d355db5e9df9ee912dd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527882"
---
# <a name="integrate-with-linkedin-talent-hub"></a>LinkedIn Talent Hub -integrointi

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) on ATS (hakijoiden seurantajärjestelmä) -ympäristö. Sen avulla voit hakea, hallita ja palkata työntekijöitä samassa paikassa. Kun Microsoft Dynamics 365 Human Resources integroidaan LinkedIn Talent Hubiin, Human Resourcesissa on helppo luoda työntekijätietueita toimeen palkatuille hakijoille.

## <a name="setup"></a>Luo perustiedot

Järjestelmänvalvojan on tehtävä määritykset, joita tarvitaan LinkedIn Talent Hub -integrointia varten. Power Apps -ympäristössä on määritettävä ensin käyttäjä ja käyttöoikeusrooli, jolla LinkedIn Talent Hubille myönnetään tietojen kirjoitusoikeudet Human Resourcesiin.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Ympäristön linkittäminen LinkedIn Talent Hubiin

1. Avaa [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. Valitse käyttäjän avattavassa valikossa **Tuotteen asetukset**.

3. Valitse vasemman siirtymisruudun **Lisäasetukset**-osassa **Integroinnit**.

4. Valitse Microsoft Dynamics 365 Human Resources -integroinnin osalta **Valtuuta**.

5. Valitse **Dynamics 365 Human Resources** -sivulla ympäristö, johon LinkedIn Talent Hub linkitetään, ja valitse sitten **Linkitä**.

    ![LinkedIn Talent Hubin käyttöönotto](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Linkityksen voi tehdä vain sellaisiin ympäristöihin, joissa linkittäjän käyttäjätilillä on järjestelmänvalvojan oikeudet sekä Human Resources -ympäristössä että liitetyissä Power Apps -ympäristössä. Jos Human Resourcesin linkkisivulla ei ole yhtään ympäristöä, varmista, että vuokraajan Human Resources -ympäristöillä on käyttöoikeus ja että linkkisivulle kirjautumiseen käytetyllä käyttäjällään sekä Human Resources- että Power Apps -ympäristön järjestelmänvalvojan oikeudet.

### <a name="create-a-power-apps-security-role"></a>Power Apps -käyttöoikeusroolin luominen

1. Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).

2. Valitse **Ympäristöt**-luettelossa ympäristö, joka on liitetty siihen Human Resources -ympäristöön, johon haluat linkittää LinkedIn Talent Hub -esiintymän.

3. Valitse **Asetukset**.

4. Laajenna **Käyttäjät ja käyttöoikeudet** -solmu ja valitse **Käyttöoikeusroolit**.

5. Valitse **Käyttöoikeusroolit**-sivun työkalurivillä **Uusi rooli**.

6. Anna roolille nimi **Tiedot**-välilehdessä. Se voi olla vaikkapa **LinkedIn Talent Hub HRIS integraatio**.

7. Valitsee **Mukauttaminen**-välilehdessä organisaatiotason **Luku**-oikeudet seuraaville entiteeteille:

    - Kokonaisuus
    - Kenttä
    - Suhde

8. Tallenna ja sulje käyttöoikeusrooli.

### <a name="create-a-power-apps-application-user"></a>Power Apps -sovelluskäyttäjän luominen

LinkedIn Talent Hub -sovittimeen on luotava sovelluskäyttäjä, jotta sovittimelle voidaan myöntää oikeudet hakijatietueiden kirjoittamiseen Power Apps -ympäristöön.

1. Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).

2. Valitse **Ympäristöt**-luettelossa ympäristö, joka on liitetty siihen Human Resources -ympäristöön, johon haluat linkittää LinkedIn Talent Hub -esiintymän.

3. Valitse **Asetukset**.

4. Laajenna **Käyttäjät ja käyttöoikeudet** -solmu ja valitse **Käyttäjät**.

5. Valitse **Käyttäjien hallinta Dynamics 365:ssä**.

6. Voit vaihtaa luettelon yläpuolella olevassa avattavassa valikossa **Aktivoidut käyttäjät** -oletusnäkymän **Sovelluskäyttäjät**-näkymään.

    ![Sovelluskäyttäjät-näkymä](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Valitse työkalurivillä **Uusi**.

8. Toimi seuraavasti **Uusi käyttäjä** -sivulla:

    1. Vaihda **Käyttäjätyyppi**-kentän arvoksi **Sovelluskäyttäjä**.
    2. Määritä **Käyttäjänimi**-kentän arvoksi **Dynamics365 HR LinkedIn HRIS -integraatio**.
    3. Määritä **Sovellustunnus**-kentän arvoksi **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Anna **Etunimi**-, **Sukunimi**- ja **Ensisijainen sähköposti** -kenttiin jokin arvo.
    5. Valitse työkalurivillä **Tallenna ja sulje**.

### <a name="assign-a-security-role-to-the-new-user"></a>Käyttöoikeusroolin määrittäminen uudelle käyttäjälle

Kun uusi sovelluskäyttäjä on tallennettu ja suljettu edellisessä osassa, olet takaisin **Käyttäjäluettelo**-sivulla.

1. Vaihda **Käyttäjäluettelo**-sivulla **Sovelluskäyttäjät**-näkymään.

2. Valitse edellisessä osassa luotu sovelluskäyttäjä.

3. Valitse työkalurivillä **Roolien hallinta**.

4. Valitse aiemmin integraatiota varten luotu käyttöoikeusrooli.

5. Valitse **OK**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Azure Active Directory -sovelluksen lisääminen Human Resourcesiin

1. Avaa Dynamics 365 Human Resourcesissa **Azure Active Directory -sovellukset** -sivu.
2. Lisää uusi tietue luetteloon ja määritä seuraavat kentät:

    - **Asiakastunnus**: anna **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **Nimi**: anna aiemmin luodun Power Appsin käyttöoikeusroolin nimi, kuten **LinkedIn Talent Hub HRIS integraatio**.
    - **Käyttäjätunnus**: valitse käyttäjä, jolla on tietojen kirjoitusoikeudet henkilöstöhallinnossa.

### <a name="create-the-entity-in-common-data-service"></a>Yksikön luominen Common Data Servicessa

> [!IMPORTANT]
> LinkedIn Talent Hub -integraatio määräytyy Human Resourcesin Common Data Servicessa virtuaaliyksiköiden mukaan. Määritysten tätä vaihetta varten on määritettävä virtuaaliyksiköitä. Lisätietoja virtuaaliyksiköiden määrittämisestä on kohdassa [Common Data Servicen virtuaaliyksiköiden määrittäminen](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

1. Avaa Human Resourcesissa **Common Data Service (CDS) -integraatio** -sivu.

2. Valitse **Virtuaaliyksiköt**-välilehti.

3. Etsi **LinkedInin viety ehdokas** suodattamalla yksikköluetteloa yksikön otsikon perusteella.

4. Valitse ensin yksikkö ja sitten **Luo/päivitä**.

## <a name="exporting-candidate-records"></a>Hakijatietojen vieminen

Kun määritykset on tehty, työhönottaja ja henkilöstöhallinnon (HR) ammattilaiset voivat viedä palkattujen hakijoiden tietueet LinkedIn Talent Hubista Human Resourcesiin LinkedIn Talent Hubin **Vie HRIS-järjestelmään** -toiminnolla.

### <a name="export-records-from-linkedin-talent-hub"></a>Tietojen vieminen LinkedIn Talent Hubista

Kun hakija on siirtynyt työhönottoprosessin läpi ja hänet on palkattu, hakijan tietue voidaan viedä LinkedIn Talent Hubista Human Resourcesiin.

1. Avaa LinkedIn Talent Hubissa projekti, johon uusi työntekijä on palkattu.

2. Valitse hakijatietue.

3. Valitse **Muuta tilaa** ja valitse sitten **Otettu työhön**.

4. Valitse hakijan kolmen pisteen valikossa (**...**) **Vie HRIS-järjestelmään**.

5. Anna **Vie HRIS-järjestelmään** -ruudussa tiedot, jotka on vietävä:

    - Valitse **HRIS-palvelu**-kentässä **Microsoft Dynamics 365 Human Resources**.
    - Valitse **Alkamispäivä**-kentässä arvo uudelle työntekijälle.
    - Anna **Työnimike**-kentässä uuden työntekijän toimen työnimike.
    - Anna **Sijainti**-kentässä sijainti, joka on työntekijän ensisijainen työpaikka.
    - Anna tai tarkista työntekijän sähköpostiosoite.

![Vie HRIS-järjestelmään -ruutu LinkedIn Talent Hubissa](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Käyttöönoton päättäminen Human Resourcesissa

LinkedIn Talent Hubista Human Resourcesiin vietävät hakijatietueet näkyvät **Henkilöstöhallinto**-sivun **Työhönotettavat hakijat** -osassa.

1. Avaa Human Resourcesissa **Henkilöstöhallinto**-sivu.

2. Valitse **Työhön otettavat hakijat** -osassa **Työhönotto** valitun hakijan kohdalla.

3. Tarkista tietue **Ota palvelukseen uusi työntekijä** -valintaikkunassa ja lisää mahdolliset pakolliset tiedot. Voit myös valita sen toimen numeron, jota varten hakija on otettu töihin.

Kun pakolliset tiedot on annettu, voit jatkaa työntekijätietueiden luonnin ja työntekijöiden perehdyttämisen vakioprosesseja.

Seuraava tiedot tuodaan, ja ne sisältyvät työntekijätietueeseen:

- Etunimi
- Sukunimi
- Työsuhteen alkamispäivä
- Sähköpostiosoite
- Puhelinnumero

## <a name="see-also"></a>Lisätietoja

[Common Data Service -virtuaaliyksiköiden määrittäminen](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Mikä on Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
