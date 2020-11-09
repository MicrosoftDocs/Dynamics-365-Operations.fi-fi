---
title: Common Data Service -virtuaaliyksiköiden määrittäminen
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin virtuaaliyksiköiden määrittämistä. Virtuaaliyksiköiden luominen ja aiemmin luotujen päivittäminen sekä luotujen ja käytettävissä olevien yksiköiden analysoiminen.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058151"
---
# <a name="configure-common-data-service-virtual-entities"></a>Common Data Service -virtuaaliyksiköiden määrittäminen

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources on Common Data Servicen virtuaalinen tietolähde. Se sisältää Common Data Servicen ja Microsoft Power Platformin täydet CRUD (luonti, luku, päivitys ja poisto) -toiminnot. Virtuaaliyksiköiden tietoja ei tallenneta Common Data Serviceen vaan sovelluksen tietokantaan. 

Jos haluat ottaa Common Data Servicen Human Resources -yksiköiden CRUD-toiminnot käyttää, yksiköiden on oltava käytettävissä virtuaaliyksikköinä Common Data Servicessa. Voit suorittaa tällä tavoin Common Data Servicen ja Microsoft Power Platformin CRUD-toimintoja Human Resourcesin tiedoissa. Toiminnot tukevat myös Human Resourcesin liiketoimintalogiikan tarkistuksia, joilla varmistetaan tietojen eheys kirjoitettaessa tietoja yksiköihin.

## <a name="available-virtual-entities-for-human-resources"></a>Human Resourcesin käytettävissä olevat virtuaaliyksiköt

Kaikki Human Resourcesin OData (Open Data Protocol) -yksiköt ovat käytettävissä virtuaaliyksikköinä Common Data Servicessa. Ne ovat käytettävissä myös Power Platformissa. Voit nyt muodostaa sovelluksia ja kokemuksia käyttämällä tietoja suoraan Human Resourcesissa CRUD-ominaisuuksien avulla ilman, että tiedot kopioitava ja synkronoitava Common Data Serviceen. Voit muodostaa Power Apps -portaalien avulla ulkoisia sivustoja, joiden avulla voidaan toteuttaa liiketoimintaprosessien yhteistyöskenaarioita Human Resourcesissa.

Voit tarkastella ympäristössä käyttöönotettujen virtuaaliyksiköiden luetteloa ja aloittaa [Power Appsin](https://make.powerapps.com) yksiköiden käyttämisen **Dynamics 365 HR -virtuaaliyksiköiden** ratkaisussa.

![Dynamics 365 HR -virtuaaliyksiköt Power Appsissa](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Virtuaaliyksiköiden ja tavallisten yksiköiden vertailu

Human Resourcesin virtuaaliyksiköt eivät ole samoja kuin Human Resourcesin luodut Common Data Servicen yksiköt. Human Resourcesin tavalliset yksiköt luodaan erikseen ja niitä ylläpidetään HCM Common -ratkaisussa Common Data Servicessa. Tavallisissa yksiköissä tiedot tallennetaan Common Data Servicessa, ja ne on synkronoitava Human Resourcesin sovellustietokannassa.

> [!NOTE]
> Tavallisten Human Resourcesin Common Data Service -yksiköiden luettelo on kohdassa [Common Data Service -yksiköt](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Luo perustiedot

Ota virtuaaliyksiköt käyttöön ympäristössä tekemällä seuraavat määritykset. 

### <a name="register-the-app-in-microsoft-azure"></a>Sovelluksen rekisteröinti Microsoft Azuressa

Sovellus on rekisteröitävä ensin Azure-portaalissa, jotta Microsoftin käyttäjätietoympäristö voi toimittaa todennus- ja valtuutuspalvelut sovellukselle ja käyttäjille. Lisätietoja sovellusten rekisteröinnistä Azuressa on kohdassa [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Avaa [Microsoft Azure -portaali](https://portal.azure.com).

2. Valitse Azure-palveluluettelossa **Sovelluksen rekisteröinnit**.

3. Valitse **Uusi rekisteröinti**.

4. Kirjoita **Nimi** -kenttään sovellusta kuvaava nimi. Esimerkki: **Dynamics 365 Human Resourcesin virtuaaliyksiköt**.

5. Anna **Uudelleenohjauksen URI** -kenttään Human Resources -esiintymän nimitilan URL-osoite.

6. Valitse **Rekisteröi**.

7. Kun rekisteröinti valmistuu, Azure-portaali näyttää sovelluksen rekisteröinnin **Yleiskatsaus** -ruudussa, joka sisältää myös sen **sovelluksen (asiakasohjelman) tunnuksen**. Kirjoita muistiin tämä **sovelluksen (asiakasohjelman) tunnus**. Nämä tiedot annetaan, kun [määrität virtuaaliyksikön tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. Valitse vasemmassa siirtymisruudussa **Varmenteet ja salaiset koodit**.

9. Valitse sivun **Asiakasohjelman salasana** -osassa **Uusi asiakasohjelman salasana**.

10. Anna kuvaus, valitse kesto ja valitse **Lisää**.

11. Kirjaa salaisen koodin arvo muistiin. Nämä tiedot annetaan, kun [määrität virtuaaliyksikön tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > Muista kirjoittaa salaisen koodin arvo muistiin tässä vaiheessa. Salaista koodi ei näytetä sen jälkeen, kun poistut sivulta.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Dynamics 365 HR Virtual Entity -sovelluksen asentaminen

Asenna Dynamics 365 HR Virtual Entity -sovellus Power Apps -ympäristöön ottamaan virtuaaliyksikön ratkaisupaketti käyttöön Common Data Servicessa.

1. Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).

2. Valitse **Ympäristöt** -luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.

3. Valitse sivun **Resurssit** -osassa **Dynamics 365 -sovellukset**.

4. Valitse **Asenna sovellus** -toiminto.

5. Valitse ensin **Dynamics 365 HR Virtual Entity** ja valitse **Seuraava**.

6. Tutustu palvelun käyttöehtoihin ja merkitse ne hyväksytyiksi.

7. Valitse **Asenna**.

Asennus kestää muutaman minuutin. Kun asennus valmistuu, jatka seuraaviin vaiheisiin.

![Dynamics 365 HR Virtual Entity -sovelluksen asentaminen Power Platform -hallintakeskuksessa](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Virtuaaliyksikön tietolähteen määrittäminen 

Seuraavaksi määritetään virtuaaliyksikön tietolähde Power Apps -ympäristössä. 

1. Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).

2. Valitse **Ympäristöt** -luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.

3. Valitse **Ympäristön URL-osoite** sivun **Tiedot** -osassa.

4. Valitse **Ratkaisun kunnon keskus** -kohdassa **Erikoishaku** -kuvake sovellussivun oikeassa yläkulmassa.

5. Valitse **Erikoishaku** -sivun avattavassa **Etsi** -luettelossa **Finance and Operations -virtuaalitietolähteen määritykset**.

6. Valitse **Tulokset**.

7. Valitse **Microsoft HR -tietolähde** -tietue.

8. Anna tietolähteen määrityksessä tarvittavat tiedot.

   - **Kohde-URL** : Human Resources -nimitilan URL-osoite.
   - **Vuokraajan tunnus** : Azure Active Directory (Azure AD) -vuokraajan tunnus.
   - **AAD-sovelluksen tunnus** : Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu sovelluksen (asiakaspalvelijan) tunnus. Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.
   - **AAD-sovelluksen salainen koodi** : Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu asiakasohjelman salasana. Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.

9. Valitse **Tallenna ja sulje**.

   ![Microsoft HR -tietolähde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>Sovelluksen oikeuksien myöntäminen Human Resourcesissa

Myönnä kahden Azure AD -sovelluksen oikeudet Human Resourcesissa:

- Vuokraajalle Microsoft Azure -portaalissa luotu sovellus
- Power Apps -ympäristössä asennettu Dynamics 365 HR Virtual Entity -sovellus 

1. Avaa Human Resourcesissa **Azure Active Directory -sovellukset** -sivu.

2. Luo uusi sovellustietue valitsemalla **Uusi**.

    - Anna **Asiakastunnus** -kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen asiakastunnus.
    - Anna **Nimi** -kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen nimi.
    - Valitse **Käyttäjätunnus** -kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.

3. Luo toinen sovellustietue valitsemalla **Uusi**.

    - **Asiakastunnus** : f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Nimi** : Dynamics 365 HR Virtual Entity
    - Valitse **Käyttäjätunnus** -kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.

## <a name="generate-virtual-entities"></a>Virtuaaliyksiköiden luominen

Voit valita asennuksen valmistumisen jälkeen virtuaaliyksiköt, jotka haluat luoda ja ottaa käyttöön Common Data Service -esiintymässä.

1. Avaa Human Resourcesissa **Common Data Service (CDS) -integraatio** -sivu.

2. Valitse **Virtuaaliyksiköt** -välilehti.

> [!NOTE]
> **Ota virtuaaliyksikkö käyttöön** -tilanvaihtopainike on automaattisesti **Kyllä** -asennossa, kun kaikki tarvittavat määritykset on tehty. Jos tilanvaihtopainike on **Ei** -asennossa, tarkista tämä asiakirjan edellisten osien vaiheet ja varmista, että kaikki edellytettävät asetukset on määritetty.

3. Valitse Common Data Servicessa luotavat yksiköt.

4. Valitse **Luo/päivitä**.

![Common Data Service -integraatio](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>Yksikön luontitilan tarkistaminen

Virtuaaliyksiköt luodaan Common Data Servicessa asynkronisena taustaprosessina. Prosessin päivitykset näkyvät toimintokeskuksessa. Prosessin tiedot, kuten virhelokit, näkyvät **Prosessin automatisoinnit** -sivulla.

1. Avaa Human Resourcesissa **Prosessin automatisoinnit** -sivu.

2. Valitse **Taustaprosessit** -välilehti.

3. Valitse **Virtuaaliyksikön kyselyn asynkroninen toiminnon taustaprosessi**.

4. Valitse **Näytä viimeisimmät tulokset**.

Esiin tulevassa ruudussa näkyy prosessin viimeksi suoritetut tulokset. Voit tarkastella prosessin lokia, mukaan lukien mahdollisia Common Data Servicen palauttamia virheitä.

## <a name="see-also"></a>Lisätietoja

[Mikä on Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Yksikön yleiskatsaus](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Yksikkösuhteiden yleiskatsaus](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Ulkoisten tietolähteiden tietoja sisältävien virtuaaliyksiköiden luominen ja muokkaaminen](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Mitä Power Apps -portaalit ovat?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Yleiskatsaus sovellusten luonnista Power Appsissa](https://docs.microsoft.com/powerapps/maker/)
