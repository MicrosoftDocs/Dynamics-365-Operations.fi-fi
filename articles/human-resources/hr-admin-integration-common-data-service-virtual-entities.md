---
title: Määritä Dataverse-virtuaalitaulukot
description: Tässä artikkelissa käsitellään virtuaalitaulukoiden määrittämistä, luontia ja päivittämistä sekä Dynamics 365 Human Resourcesissa luotujen ja käytettävissä olevien taulukoiden analysointia.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 45155dba5063981eb3aeeed4dda1d79a57b7c8af
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067095"
---
# <a name="configure-dataverse-virtual-tables"></a>Määritä Dataverse-virtuaalitaulukot


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dynamics 365 Human Resources on Microsoft Dataversen virtuaalinen tietolähde. Se sisältää Dataversen ja Microsoft Power Platformin täydet CRUD (luonti, luku, päivitys ja poisto) -toiminnot. Virtuaalitaulukoiden tietoja ei tallenneta Dataverseen vaan sovelluksen tietokantaan.

Jos haluat ottaa Dataversen Human Resources -yksiköiden CRUD-toiminnot käyttää, yksiköiden on oltava käytettävissä virtuaalitaulukkoina Dataversessa. Voit suorittaa tällä tavoin Dataversen ja Microsoft Power Platformin CRUD-toimintoja Human Resourcesin tiedoissa. Toiminnot tukevat myös Human Resourcesin liiketoimintalogiikan tarkistuksia, joilla varmistetaan tietojen eheys kirjoitettaessa tietoja yksiköihin.

> [!NOTE]
> Human Resources -yksiköt vastaavat Dataverse-tauluja. Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Human Resourcesin käytettävissä olevat virtuaalitaulukot

Kaikki Human Resourcesin OData (Open Data Protocol) -yksiköt ovat käytettävissä virtuaalitaulukkoina Dataversessa. Ne ovat käytettävissä myös Power Platformissa. Voit nyt muodostaa sovelluksia ja kokemuksia käyttämällä tietoja suoraan Human Resourcesissa CRUD-ominaisuuksien avulla ilman, että tiedot kopioitava ja synkronoitava Dataverseen. Voit muodostaa Power Apps -portaalien avulla ulkoisia sivustoja, joiden avulla voidaan toteuttaa liiketoimintaprosessien yhteistyöskenaarioita Human Resourcesissa.

Voit tarkastella ympäristössä käyttöönotettujen virtuaalitaulukoiden luetteloa ja aloittaa [Power Appsin](https://make.powerapps.com) taulukoiden käyttämisen **Dynamics 365 HR -virtuaalitaulukoiden** ratkaisussa.

![Dynamics 365 HR -virtuaalitaulukot Power Appsissa.](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Virtuaalitaulut ja alkuperäiset taulut

Human Resourcesin virtuaalitaulukot eivät ole samoja kuin Human Resourcesille luodut alkuperäiset Dataversen taulukot. 

Human Resourcesin alkuperäiset taulukot luodaan erikseen ja niitä ylläpidetään HCM Common -ratkaisussa Dataversessa. Aluperäisissä taulukoissa tiedot tallennetaan Dataversessa, ja ne on synkronoitava Human Resourcesin sovellustietokannassa.

> [!NOTE]
> Alkuperäisten Human Resourcesin Dataverse -taulukoiden luettelo on kohdassa [Dataverse-taulukot](./hr-developer-entities.md).

## <a name="setup"></a>Luo perustiedot

Ota virtuaalitaulukot käyttöön ympäristössä tekemällä seuraavat määritykset.

### <a name="enable-virtual-tables-in-human-resources"></a>Human Resourcesin virtuaalitaulukoiden käyttöönotto

Ensin on otettava käyttöön virtuaalitaulukot **Ominaisuuksien hallinta** -työtilassa.

1. Valitse Human Resourcesissa **Järjestelmän hallinta**.

2. Valitse **Ominaisuuksien hallinta** -ruutu.

3. Valitse **Dataversen virtuaalitaulukon tuki HR:lle** ja valitse sitten **Ota käyttöön**.

Lisätietoja ominaisuuksien ottamisesta käyttöön ja poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Sovelluksen rekisteröinti Microsoft Azuressa

Human Resources -esiintymä on rekisteröitävä Azure-portaalissa, jotta Microsoftin käyttäjätietoympäristö voi toimittaa todennus- ja valtuutuspalvelut sovellukselle ja käyttäjille. Lisätietoja sovellusten rekisteröinnistä Azuressa on kohdassa [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](/azure/active-directory/develop/quickstart-register-app).

1. Avaa [Microsoft Azure -portaali](https://portal.azure.com).

2. Valitse Azure-palveluluettelossa **Sovelluksen rekisteröinnit**.

3. Valitse **Uusi rekisteröinti**.

4. Kirjoita **Nimi**-kenttään sovellusta kuvaava nimi. Esimerkki: **Dynamics 365 Human Resourcesin virtuaalitaulukot**.

5. Anna **Uudelleenohjauksen URI** -kenttään Human Resources -esiintymän nimitilan URL-osoite.

6. Valitse **Rekisteröi**.

7. Kun rekisteröinti valmistuu, Azure-portaali näyttää sovelluksen rekisteröinnin **Yleiskatsaus**-ruudussa, joka sisältää myös sen **sovelluksen (asiakasohjelman) tunnuksen**. Kirjoita muistiin tämä **sovelluksen (asiakasohjelman) tunnus**. Nämä tiedot annetaan, kun [määrität virtuaalitaulukon tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. Valitse vasemmassa siirtymisruudussa **Varmenteet ja salaiset koodit**.

9. Valitse sivun **Asiakasohjelman salasana** -osassa **Uusi asiakasohjelman salasana**.

10. Anna kuvaus, valitse kesto ja valitse **Lisää**.

11. Kirjaa sen arvo taulun **Arvo**-ominaisuudesta. Nämä tiedot annetaan, kun [määrität virtuaalitaulukon tietolähteen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > Muista kirjoittaa salaisen koodin arvo muistiin tässä vaiheessa. Salaista koodi ei näytetä sen jälkeen, kun poistut sivulta.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Dynamics 365 HR Virtual Table -sovelluksen asentaminen

Asenna Dynamics 365 HR Virtual Table -sovellus Power Apps -ympäristöön ottamaan virtuaalitaulukon ratkaisupaketti käyttöön Dataversessa.

1. Avaa Human Resourcesissa **Microsoft Dataverse-integraatio** -sivu.

2. Valitse **Virtuaalitaulukot**-välilehti.

3. Valitse **Asenna virtuaalitaulusovellus**.

### <a name="configure-the-virtual-table-data-source"></a>Virtuaalitaulukon tietolähteen määrittäminen

Seuraavaksi määritetään virtuaalitaulukon tietolähde Power Apps -ympäristössä.

1. Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).

2. Valitse **Ympäristöt**-luettelossa Human Resources -esiintymään liitetty Power Apps -ympäristö.

3. Valitse **Ympäristön URL-osoite** sivun **Tiedot**-osassa.

4. Valitse **Ratkaisun kunnon keskus** -kohdassa **Erikoishaku**-kuvake sovellussivun oikeassa yläkulmassa.

5. Valitse **Erikoishaku**-sivun avattavassa **Etsi**-luettelossa **Talous- ja toimintosovellusten virtuaalitietolähteen määritykset**.

   > [!NOTE]
   > Virtuaalitaulusovelluksen asentaminen edellisestä asennusvaiheesta voi kestää muutaman minuutin. Jos **Talous- ja toimintosovellusten virtuaalitietolähteen määritykset** eivät ole käytettävissä luettelossa, odota minuutti ja päivitä luettelo.

6. Valitse **Tulokset**.

7. Valitse **Microsoft HR -tietolähde** -tietue.

8. Anna tietolähteen määrityksessä seuraavat tarvittavat tiedot:

   - **Kohde-URL**: Human Resources -nimitilan URL-osoite. Kohde-URL-osoitteen muoto on seuraava:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Esimerkki:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Virheiden välttämiseksi varmista, että URL-osoittee lopussa on merkki **/**.

     >[!NOTE]
     >Kohde-URL määrittää Human Resources -ympäristön, jonka virtuaalitaulukot osoittavat tiedoille. Jos eristysympäristö luodaan luomalla tuotantoympäristön kopio, tähän arvoon on päivitettävä uuden eristysympäristön nimitilan URL-osoite. Näin varmistetaan, että virtuaalitaulukot on yhdistetty eritysympäristön tietoihin sen sijaan, että osoittaisivat edelleen tuotantoympäristöön.

   - **Vuokraajan tunnus**: Azure Active Directory (Azure AD) -vuokraajan tunnus.

   - **AAD-sovelluksen tunnus**: Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu sovelluksen (asiakaspalvelijan) tunnus. Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.

   - **AAD-sovelluksen salainen koodi**: Microsoft Azure -portaalissa rekisteröidylle sovellukselle luotu asiakasohjelman salasana. Saint nämä tiedot aiemman [Sovelluksen rekisteröinti Microsoft Azuressa](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) -vaiheen aikana.

   ![Microsoft HR -tietolähde.](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Valitse **Tallenna ja sulje**.

### <a name="grant-app-permissions-in-human-resources"></a>Sovelluksen oikeuksien myöntäminen Human Resourcesissa

Myönnä kahden Azure AD -sovelluksen oikeudet Human Resourcesissa:

- Vuokraajalle Microsoft Azure -portaalissa luotu sovellus
- Power Apps -ympäristössä asennettu Dynamics 365 HR Virtual Table -sovellus 

1. Avaa Human Resourcesissa **Azure Active Directory -sovellukset** -sivu.

2. Luo uusi sovellustietue valitsemalla **Uusi**.

    - Anna **Asiakastunnus**-kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen asiakastunnus.
    - Anna **Nimi**-kentässä Microsoft Azure -portaalissa rekisteröidyn sovelluksen nimi.
    - Valitse **Käyttäjätunnus**-kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.

3. Luo toinen sovellustietue valitsemalla **Uusi**.

    - **Asiakastunnus**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Nimi**: Dynamics 365 HR Virtual Table
    - Valitse **Käyttäjätunnus**-kentässä sellaisen käyttäjän käyttäjätunnus, jolla on Human Resources- ja Power Apps -ympäristön järjestelmänvalvojan käyttöoikeudet.

## <a name="generate-virtual-tables"></a>Virtuaalitaulukoiden luominen

Voit valita asennuksen valmistumisen jälkeen virtuaalitaulukot, jotka haluat luoda ja ottaa käyttöön Dataverse -esiintymässä.

1. Avaa Human Resourcesissa **Microsoft Dataverse-integraatio** -sivu.

2. Valitse **Virtuaalitaulukot**-välilehti.

> [!NOTE]
> **Ota virtuaalitaulukot käyttöön** -tilanvaihtopainike on automaattisesti **Kyllä**-asennossa, kun kaikki tarvittavat määritykset on tehty. Jos tilanvaihtopainike on **Ei**-asennossa, tarkista tämä asiakirjan edellisten osien vaiheet ja varmista, että kaikki edellytettävät asetukset on määritetty.

3. Valitse Dataversessa luotava taulukko tai luotavat taulukot.

4. Valitse **Luo/päivitä**.

![Dataverse-integraatio.](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Taulukon luontitilan tarkistaminen

Virtuaalitaulukot luodaan Dataversessa asynkronisena taustaprosessina. Prosessin päivitykset näkyvät toimintokeskuksessa. Prosessin tiedot, kuten virhelokit, näkyvät **Prosessin automatisoinnit** -sivulla.

1. Avaa Human Resourcesissa **Prosessin automatisoinnit** -sivu.

2. Valitse **Taustaprosessit**-välilehti.

3. Valitse **Virtuaalitaulukon kyselyn asynkroninen toiminnon taustaprosessi**.

4. Valitse **Näytä viimeisimmät tulokset**.

Esiin tulevassa ruudussa näkyy prosessin viimeksi suoritetut tulokset. Voit tarkastella prosessin lokia, mukaan lukien mahdollisia Dataversen palauttamia virheitä.

## <a name="see-also"></a>Lisätietoja

[Mikä on Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Taulut Dataversessa](/powerapps/maker/common-data-service/entity-overview)<br>
[Taulukkosuhteiden yleiskatsaus](/powerapps/maker/common-data-service/relationships-overview)<br>
[Ulkoisten tietolähteiden tietoja sisältävien virtuaalitaulukoiden luominen ja muokkaaminen](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Mitä Power Apps -portaalit ovat?](/powerapps/maker/portals/overview)<br>
[Yleiskatsaus sovellusten luonnista Power Appsissa](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

