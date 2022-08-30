---
title: Verolaskentamäärityksen päätietojen haun ottaminen käyttöön
description: Tässä artikkelissa käsitellään verolaskennan päätietojen hakutoiminnon määrittämistä ja käyttöönottamista.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f9d882340171173e5e503f8b5e3aa856e8544b0
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306200"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Verolaskentamäärityksen päätietojen haun ottaminen käyttöön 

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään verolaskennan päätietojen hakutoiminnon määrittämistä ja käyttöönottamista. Käytössä on avattava luettelo, jossa voi valita verolaskentamäärityksen arvoja esimerkiksi **Yritys**, **Toimittajan tili**-, **Nimikekoodi**- ja **Toimitusehto**-kenttiin. Nämä arvot saadaan Microsoft Dataverse -tietolähdettä käyttävästä yhdistetystä Microsoft Dynamics 365 Finance -ympäristöstä.

> [!NOTE] 
> Verolaskennan perustietojen hakutoiminto on valinnainen toiminto. Seuraavat vaiheet voidaan ohittaa, jos **Veropalvelun Dataverse-tietolähteiden tuki** -ominaisuus poistetaan käytöstä RCS (Regulatory Configuration Service) -palvelussa. Tällöin avattava luettelo ei kuitenkaan ole käytettävissä verolaskelman konfiguraatiossa.

Avattava luettelo voidaan ottaa käyttöön verolaskennan ominaisuusversion määrityksissä seuraavien ohjeiden avulla.

1. [Microsoft Power Platform -integroinnin ottaminen käyttöön ja Dataverse-ympäristön avaaminen](#enable)
2. [Talous- ja toimintosovellusten virtuaaliyksiköiden asentaminen](#install)
3. [Azure Active Directory (Azure AD) -sovelluksen rekisteröiminen](#register)
4. [Sovelluksen käyttöoikeuksien myöntäminen talous- ja toimintosovelluksissa](#grant)
5. [Virtuaaliyksikön tietolähteen määrittäminen](#configure)
6. [Dataverse-virtuaaliyksikön ottaminen käyttöön](#virtual)
7. [Verolaskennan yhdistetyn sovelluksen määrittäminen](#set-up)
8. [Dataverse-mallin yhdistämismääritysten tuominen ja määrittäminen](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>Microsoft Power Platform -integroinnin ottaminen käyttöön ja Dataverse-ympäristön avaaminen

Talous- ja toimintosovellusten sekä Microsoft Power Platformin integrointi voidaan ottaa käyttöön, kun uusi talous- ja toimintosovellusympäristö luodaan Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja on kohdassa [Microsoft Power Platform -apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Kun olet valmis, Microsoft Power Platform -ympäristön nimi näkyy **Power Platform -integrointi** -osassa.

1. Etsi LCS:n talous- ja toimintosovellusympäristön **Power Platform -integrointi** -osassa linkitetyn ympäristön **Ympäristön nimi** -arvo ja kirjoita se muistiin.

    [![Ympäristön nimi -arvo](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. Valitse [Power Platform -hallintakeskuksen](https://admin.powerplatform.microsoft.com/environments) **Ympäristöt**-välilehdessä se ympäristö, joka vastaa muistiin kirjoitettua **Ympäristön nimi** -arvoa.
3. Etsi **Tiedot**-sivulla Dataverse-ympäristön **Ympäristön URL-osoite** -arvo. Kirjoita tämä arvo muistiin, sillä tarvitset sitä [vaiheessa 7. Verolaskennan yhdistetyn sovelluksen määrittäminen](#set-up).
4. Varmista, että voit avata Dataverse-ympäristön selaimessa valitsemalla **Ympäristön URL-osoite** -arvon.

    [![Dataverse-ympäristön sivu](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Pidä Dataverse-ympäristö auki selaimessa. Sitä tarvitaan [vaiheessa 5. Virtuaaliyksikön tietolähteen määrittäminen](#configure).

Lisätietoja on kohdassa [Microsoft Power Platform -integroinnin ottaminen käyttöön](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>Talous- ja toimintosovellusten virtuaaliyksikön asentaminen

Talous- ja toimintosovellusten virtuaaliyksikköjen Dataverse-ratkaisu on asennettava Microsoft AppSource -virtuaaliyksikköratkaisusta.

1. Etsi AppSourcessa [talous- ja toimintosovellusten virtuaaliyksikkö](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Valitse **Hanki se nyt**.
3. Anna **Valitse ympäristö** -kentässä se **Ympäristön nimi** -arvo, joka kirjoitettiin aiemmin muistiin.
4. Valitse valintaruudut ja valitse sitten **Asenna**.

Kun asennus on valmis, **Talous- ja toimintosovellusten virtuaaliyksikkö** -sovelluksen voi etsiä [Power Platform -hallintakeskuksessa](https://admin.powerplatform.microsoft.com/) valitsemalla **Resurssit** \> **Dynamics 365 -sovellukset**.

Lisätietoja on kohdassa [Virtuaaliyksikköratkaisun hakeminen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Azure AD -sovelluksen rekisteröiminen

Azure AD -sovellus on rekisteröitävä samaan vuokraajaan kuin talous- ja toimintosovellukset, jotta Dataverse voi kutsua niitä.

1. Valitse [Azure-portaalissa](https://portal.azure.com) **Azure Active Directory \> Sovelluksen rekisteröinnit**.
2. Valitse **Uusi rekisteröinti** ja anna seuraavat tiedot:

    - **Nimi** – anna yksilöivä nimi.
    - **Tilityyppi** – anna **Mikä tahansa Azure AD -hakemisto** (yksi vuokraaja tai useita vuokraajia).
    - **Uudelleenohjauksen URI** – jätä tämä kenttä tyhjäksi.

3. Valitse **Rekisteröi**.
4. Kirjoita **Sovelluksen (asiakasohjelman) tunnus** -kohdan arvo muistiin, sillä tarvitset sitä myöhemmin.

    [![Azure AD -sovelluksen (asiakasohjelman) tunnuksen arvo](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Luo sovellukselle symmetrinen avain.
6. Valitse uudessa sovelluksessa **Varmenteet ja salaiset koodit**.
7. Valitse **Uusi asiakkaan salainen koodi**.
8. Kirjoita kuvaus, valitse vanhentumispäivä ja valitse sitten **Tallenna**. Avain luodaan ja näytetään. Kopioi arvo myöhempää käyttöä varten.

Lisätietoja on kohdassa [Azure AD -sovelluksen rekisteröiminen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>Sovelluksen käyttöoikeuksien myöntäminen talous- ja toimintosovelluksissa

Dataverse kutsuu talous- ja toimintosovelluksia juuri luodun Azure AD -sovelluksen avulla. Tämän vuoksi talous- ja toimintosovellusten on luotettava sovellukseen ja sen on oltava liitetty käyttäjätiliin, jossa on soveltuvat oikeudet. Talous- ja toimintosovelluksissa on luota erityinen palvelukäyttäjä, jolla on **vain** virtuaaliyksikkötoiminnon käyttöoikeudet. Tällä palvelukäyttäjällä ei saa olla muita oikeuksia. Kun tämä vaihe on suoritettu, mikä tahansa sovellus, jolla on luodun Azure AD -sovelluksen salainen koodi, voi kutsua talous- ja toimintosovellusympäristöä sekä käyttää virtuaaliyksikkötoimintoa.

1. Valitse ympäristössä **Järjestelmän hallinta** \> **Käyttäjät** \> **Käyttäjät**.
2. Lisää uusi käyttäjä valitsemalla **Uusi** ja anna seuraavat tiedot:

    - **Käyttäjätunnus** – anna **dataverseintegration** tai jokin muu arvo.
    - **Käyttäjänimi** – anna **dataverse-integrointi** tai jokin muu arvo.
    - **Palvelu** – määritä tämän kentän arvoksi **NonAAD**.
    - **Sähköposti** – Anna **dataverseintegration** tai jokin muu arvo. (Arvon ei tarvitse olla kelvollinen sähköpostitili.)

3. Delegoi käyttäjälle **Dataverse-virtuaalientiteettien integrointisovellus** -käyttöoikeusrooli.
4. Poista kaikki muut roolit, myös **Järjestelmän käyttäjä**.
5. Rekisteröi Dataverse valitsemalla **Järjestelmän hallinta** \> **Määritys** \> **Azure Active Directory -sovellukset**. 
6. Lisää rivi ja anna sitten **Asiakasohjelman tunnus** -kentässä aiemmin muistiin kirjoitettu **Sovelluksen (asiakasohjelman) tunnus** -arvo.
7. Anna nimi **Nimi**-kenttään. Kirjoita esimerkiksi **Dataverse-integrointi**.
8. Anna **Käyttäjätunnus**-kenttään aiemmin luotu käyttäjätunnus.

Lisätietoja on kohdassa [Sovelluksen käyttöoikeuksien myöntäminen talous- ja toimintosovelluksissa](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Virtuaaliyksikön tietolähteen määrittäminen

Anna Dataverse sekä talous- ja toimintosovellusesiintymä, johon yhteys muodostetaan.

1. Dataverse-ympäristön pitäisi olla edelleen avoimena selaimessa [vaiheen 1. Microsoft Power Platform -integroinnin ottaminen käyttöön ja Dataverse-ympäristön avaaminen](#enable) jäljiltä. Valitse ensin asetuspainike (rataskuvake) oikeassa yläkulmassa ja sitten **Lisäasetukset**.

    [![Lisäasetusten avaaminen Dataverse-ympäristössä](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. Valitse avattavassa **Asetukset**-valikossa **Hallinto**.

    [![Hallinto](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Valitse **Virtuaaliyksikön tietolähteet**.

    [![Virtuaaliyksikön tietolähteet](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Valitse **Talous- ja toimintosovellukset** -niminen tietolähde.

    [![Talous- ja toimintosovellusten tietolähde](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Anna seuraavat aiemmista vaiheista saadut tiedot:

    - **Kohde-URL-osoite** – anna URL-osoite, jossa talous- ja toimintosovelluksia voidaan käyttää.
    - **OAuth-URL-osoite** – anna `https://login.windows.net/`.
    - **Vuokraajan tunnus** – Määritä vuokraaja. Tämä arvo voi olla yrityksen sähköpostin toimialuenimi (kuten contoso.com).
    - **AAD-sovelluksen tunnus** – anna aiemmin luotu **Sovelluksen (asiakasohjelman) tunnus** -arvo.
    - **AAD-sovelluksen salainen koodi** – anna aiemmin luotu salainen koodi.
    - **AAD-resurssi** – Anna **00000015-0000-0000-c000-000000000000**. Tämä on Azure AD -sovellus, joka ilmaisee talous- ja toimintosovellukset. Sen on oltava aina sama arvo.

6. Tallenna muutokset.
7. Sulje sivu ja palaa **Hallinto**-sivulle, josta voidaan aloittaa [vaihe 6. Dataverse-virtuaaliyksikön ottaminen käyttöön](#virtual).

    [![Entiteetin sulkeminen muokkausta varten](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Lisätietoja on kohdassa [Virtuaaliyksikön tietolähteen määrittäminen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>Dataverse-virtuaaliyksiköiden ottaminen käyttöön

Talous- ja toimintosovellusten virtuaaliyksiköiden näkyvyydeksi on määritettävä **Kyllä**, ennen kuin verolaskentamääritykset voivat käyttää niitä.

> [!NOTE]
> Tämä vaihe voidaan ohittaa ottamalla verolaskentaan liittyvät virtuaaliyksiköt käyttöön yhdellä napsautuksella [vaiheessa 8. Verolaskennan yhdistetyn sovelluksen määrittäminen](#import). On kuitenkin suositeltavaa, että ainakin yksi virtuaaliyksikkö otetaan käyttöön manuaalisesti ilmaisemaan, että talous- ja toimintosovellusten sekä Dataversen välinen yhteys on muodostettu hyvin.

1. Valitse Dataverse-ympäristön **Hallinta**-sivulla suodatuspainike (suppilokuvake) oikeassa yläkulmassa.

    [![Suodatuspainike](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. Valitse **Erikoishaku**-ikkunan **Etsi:**-kentässä **Käytettävissä olevat talous- ja toimintosovellusyksiköt**.
3. Lisää seuraava sääntö: **Nimi** – **Sisältää** – **CompanyInfoEntity**. Valitse sitten **Tulokset**.

    [![Erikoishakuikkuna](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Valitse hakutuloksissa **CompanyInfoEntity**, valitse sitten **Näkyvät**-valintaruutu ja valitse lopuksi **Tallenna**.

    [![Yksikön näkyvyyden määrittäminen](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Toista edellä olevat vaiheet seuraavissa yksiköissä, joihin viitataan verolaskentamäärityksissä:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Dataverse voi noutaa vain 5 000 yksikön ensimmäistä tietuetta, ja sama määrä tietueita voi olla valittavissa verolaskentamääritysten avattavassa luettelossa.

Lisätietoja: [Microsoft Dataversen virtuaaliyksikköjen käyttöönotto](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>Verolaskennan yhdistetyn sovelluksen määrittäminen

1. Valitse **Sähköinen raportointi** ja valitse sitten **Liittyvät linkit** -osassa **Yhdistetyt sovellukset**.

    [![Yhdistetyt sovellukset](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

2. Lisää tietue valitsemalla **Uusi** ja anna seuraavat tiedot.

    - **Nimi** – Syötä nimi.
    - **Tyyppi** – valitse **Dataverse**.
    - **Sovellus** – anna Dataverse-ympäristön **Ympäristön URL-osoite** -arvo, joka kirjoitettiin muistiin [vaiheessa 1. Microsoft Power Platform -integroinnin ottaminen käyttöön ja Dataverse-ympäristön avaaminen](#enable).
    - **Vuokraaja** – anna vuokraaja.
    - **Mukautettu URL-osoite** – anna Dataversen URL-osoite ja liitä **/api/data/v9.1** siihen.

3. Valitse **Tarkista yhteys** ja valitse sitten valintaikkunassa **Yhdistä valittuun etäsovellukseen napsauttamalla tätä**.

    [![Yhteyden tarkistaminen](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
4. Varmista, että saat onnistumisesta ilmoittavan sanoman, joka ilmaisee, että yhteyden muodostaminen on onnistunut.

    [![Onnistumissanoma](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)
    
5. Avaa **Ominaisuuksien hallinta** -työtila RCS:ssä ja ota käyttöön seuraavat ominaisuudet:

    - Globalisaatio-ominaisuudet
    - Sähköisen raportoinnin Dataverse-tietolähteiden tuki
    - Veropalvelun Dataverse-tietolähteiden tuki

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>Dataverse-mallin yhdistämismääritysten tuominen ja määrittäminen

Microsoft toimittaa yksikön oletusarvoiset mallin yhdistämismääritykset talous- ja toimintosovelluksista verolaskentaan.

1. Valitse RCS:ssä **Sähköinen raportointi**.
2. Valitse **Määrityspalvelut**-osan **Microsoft**-palvelun ruudussa **Säilöt**.

    [![Säilöt](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Valitse **Yleinen määrityssäilö** -tietue ja valitse sitten **Avaa**.
4. Valitse ensin **Verotietomalli** \> **Verolaskennan tietomalli** ja sitten **Dataverse-mallin yhdistämismääritys** -määritykset.
5. Valitse **Versiot**-pikavälilehdessä talous- ja toimintosovellusten versiota vastaava versio ja valitse sitten **Tuo**.

    [![Dataverse-mallin yhdistämismääritys -määritysten tuonti](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > **Dataverse-mallin yhdistämismääritys** -määritykset toimivat vain suurimmassa tuodussa versiossa. Niinpä sellaista **Dataverse-mallin yhdistämismääritys** -määritysten versiota ei kannata tuoda, joka on suurempi kuin toteutettavan verolaskentamäärityksen versio. Jos tarkoitus on esimerkiksi toteuttaa verolaskentamäärityksen versio 40.50.225, kannattaa tuoda vain **Dataverse-mallin yhdistämismääritys** -määritysten versio 40.50.13. Älä tuo versiota 40.54.14. Se aiheuttaa tietomallin ristiriidan määrityksissä.

6. Palaa **Sähköinen raportointi** -kohtaan ja valitse **Veromääritykset**-ruutu.
7. Valitse tuodut **Dataverse-mallin yhdistämismääritys** -määritykset ja valitse sitten **Muokkaa**.
8. Määritä **Mallin yhdistämisasetuksen** oletusarvoksi **Kyllä**.
9. Valitse **Yhdistetty sovellus** -kentässä yhdistetty sovellus, joka määritettiin [vaiheessa 7. Verolaskennan yhdistetyn sovelluksen määrittäminen](#set-up).
10. Määritä kaikki verolaskentaan liittyvät virtuaaliyksiköt näkyviksi valitsemalla **Määritä virtuaalitaulun näkyvyys** -vaihtoehdossa **Kyllä**.

Päätietojen hakutoiminto on nyt määritetty. Dynamics 365 Financen kenttien, kuten **Yritys**, **Toimittajan tili**, **Nimikekoodi** ja **Toimitusehto**, avattava luettelo on nyt otettu käyttöön **Verolaskentaominaisuuden versio** -määrityksessä.

[![Avattava yritysluettelo](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
