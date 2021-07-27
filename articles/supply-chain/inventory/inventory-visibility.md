---
title: Varaston näkyvyyden apuohjelma
description: Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8709b91b354fa4e1319b406c009bfdadeef48a41
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358095"
---
# <a name="inventory-visibility-add-in"></a>Varaston näkyvyyden apuohjelma

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Varaston näkyvyyden apuohjelma on itsenäinen ja erittäin skaalautuva mikropalvelu, joka mahdollistaa reaaliaikaisen käytettävissä olevan varaston seurannan ja antaa tällä tavoin yleisen näkymän varaston näkyvyyteen.

Kaikki käytettävissä olevaan varastoon liittyvät tiedot viedään palveluun lähes reaaliaikaisesti käyttämällä matala-asteista SQL-integraatiota. Ulkoiset palvelut käyttävät palvelut tekevät RESTful API -ohjelmointirajapinnoilla käytettävissä olevien tietojen kyselyjä annetuissa dimensioissa ja saavat tällä tavoin luettelon käytettävissä olevista paikoista.

Varaston näkyvyys on Microsoft Dataverseen perustuva mikropalvelu, joten sitä voi laajentaa muodostamalla Power Apps -sovelluksia ja käyttämällä Power BI:ta tuottamaan liiketoiminnan tarpeita vastaavia mukautettuja toimintoja. Indeksi voidaan lisäksi päivittää tekemään varastokyselyjä.

Varaston näkyvyydessä on määritysvaihtoehtoja, joiden avulla sen voi integroida useiden kolmannen osapuolen järjestelmien kanssa. Se tukee standardoitua varastodimensiota, mukautettua laajennettavuutta ja standardoituja, määritettäviä laskettuja määriä.

Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä sekä sen ohjelmointirajapinnan käyttöä.

## <a name="install-the-inventory-visibility-add-in"></a>Varaston näkyvyyden lisäapuohjelman asentaminen

Varaston näkyvyyden lisäapuohjelman asentamiseen on käytettävä Microsoft Dynamics Lifecycle Servicesiä (LCS). LCS on yhteistyöportaali, jonka muodostamassa ympäristössä ja jonka säännöllisesti päivitetyillä palveluilla voi hallita Dynamics 365 Finance and Operations -sovellusten elinkaarta.

Lisätietoja on kohdassa [Lifecycle Services -resurssit](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="inventory-visibility-add-in-prerequisites"></a>Varaston näkyvyyden apuohjelman edellytykset

Ennen varaston näkyvyyden apuohjelman asentamista:

- Hanki LCS-toteutusprojekti, jossa on otettu käyttöön vähintään yksi ympäristö.
- Varmista, että kohdassa [Lisäosien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) annetut edellytykset lisäosien määrittämiselle on täytetty. Varaston näkyvyys ei edellytä kaksoiskirjoituslinkitystä.
- Ota yhteyttä varaston näkyvyyden tiimiin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), jotta saat seuraavat kolme vaadittua tiedostoa:
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - `Inventory Visibility Integration.zip` (jos käynnissä ollut Supply Chain Managementin versio on aiempi kuin 10.0.18)
- Vaihtoehtoisesti ota yhteyttä varaston näkyvyyden tiimiin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), jotta saat Package Deployer -paketit. Virallinen Package Deployer -työkalu voi käyttää näitä pakkauksia.
  - `InventoryServiceBase.PackageDeployer.zip`
  - `InventoryServiceApplication.PackageDeployer.zip` (tämä paketti sisältää kaikki `InventoryServiceBase`-paketin muutokset sekä muut käyttöliittymäsovelluksen komponentit)
- Noudata seuraavassa annettuja ohjeita: [Pikaopas: Rekisteröi hakemus Microsoft identity Platformiin](/azure/active-directory/develop/quickstart-register-app) sovelluksen rekisteröimiseksi ja asiakkaan lisäämiseksi AAD:lle ylläpitosopimuksen mukaan.
  - [Sovelluksen rekisteröinti](/azure/active-directory/develop/quickstart-register-app)
  - [Lisää asiakasohjelman salasana](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - **Sovelluksen (asiakas) tunnuksen**, **asiakasohjelman salasanan** ja **vuokraajan tunnuksen** avulla voidaan tehdä seuraavat vaiheet.

> [!NOTE]
> Tällä hetkellä tuettuja maita ja alueita ovat Kanada, Yhdysvallat ja Euroopan unioni (EU).

Jos sinulla on näitä edellytyksiä koskevia kysymyksiä, ota yhteys varaston näkyvyyden tuotetiimiin.

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Määritys Dataverse

Jotta voit määrittää Dataversen käytön varaston näkyvyyden avulla, sinun on ensin valmisteltava edellytykset ja päätettävä, määritetäänkö Dataverse joko Package Deployer -työkalun avulla vai tuomalla ratkaisut manuaalisesti (molempia ei tarvitse tehdä). Asenna sitten Varaston näkyvyyden lisäapuohjelma. Seuraavissa aliosissa kuvataan, kuinka kukin tehtävä viimeistellään.

#### <a name="prepare-dataverse-prerequisites"></a>Dataverse-edellytysten valmisteleminen

Ennen kuin aloitat Dataversen määrittämisen, lisää vuokraajaan huoltoperiaate seuraavasti:

1. Asenna Azure AD PowerShell Module v2, kuten kuvattu kohdassa [Asenna Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).

1. Suorita seuraava PowerShell-komento:

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a>Dataversen määrittäminen Package Deployer -työkalun avulla

Kun olet määrittänyt tarvittavat edellytykset, käytä seuraavaa menettelyä, jos haluat määrittää Dataversen Package Deployer -työkalun avulla. Seuraavassa osassa on tietoja ratkaisujen tuonnista manuaalisesti (älä tee molempia).

1. Asenna kehittäjien työkalut kohdassa [Lataa työkalut kohteesta NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget) kuvatulla tavalla.

1. Liiketoimintavaatimustesi mukaan valitse `InventoryServiceBase`- tai `InventoryServiceApplication`-paketti.

1. Tuo ratkaisut:
    1. `InventoryServiceBase`-paketille:
        - Pura `InventoryServiceBase.PackageDeployer.zip`
        - Etsi kansio `InventoryServiceBase`, tiedosto `[Content_Types].xml`, tiedosto `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, tiedosto `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` ja tiedosto `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`. 
        - Kopioi nämä kansiot ja tiedostot `.\Tools\PackageDeployment`-hakemistoon, joka luotiin kehittäjien työkalujen asennuksen yhteydessä.
    1. `InventoryServiceApplication`-paketille:
        - Pura `InventoryServiceApplication.PackageDeployer.zip`
        - Etsi kansio `InventoryServiceApplication`, tiedosto `[Content_Types].xml`, tiedosto `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, tiedosto `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` ja tiedosto `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.
        - Kopioi nämä kansiot ja tiedostot `.\Tools\PackageDeployment`-hakemistoon, joka luotiin kehittäjien työkalujen asennuksen yhteydessä.
    1. Suorita `.\Tools\PackageDeployment\PackageDeployer.exe`. Voit tuoda ratkaisut noudattamalla näytön ohjeita.

1. Määritä käyttöoikeusroolit sovelluksen käyttäjälle.
    1. Avaa Dataverse-ympäristön URL-osoite.
    1. Valitse **Lisäasetukset \> Järjestelmä \> Suojaus \> Käyttäjät** ja etsi käyttäjä nimeltä **# InventoryVisibility**.
    1. Valitse **Määritä rooli** ja valitse sitten **Järjestelmänvalvoja**. Jos saatavana on rooli nimeltä **Common Data Service -käyttäjä**, valitse myös se.

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a>Määritä Dataverse manuaalisesti tuomalla ratkaisuja

Kun olet määrittänyt tarvittavat edellytykset, käytä seuraavaa menettelyä, jos haluat määrittää Dataversen tuomalla ratkaisuja manuaalisesti. Edellisessä osassa on lisätietoja Package Deployer -työkalun käytöstä sen sijaan (älä tee molempia).

1. Luo sovelluskäyttäjä varaston näkyvyydelle Dataversessä:

    1. Avaa Dataverse-ympäristön URL-osoite.
    1. Valitse **Lisäasetukset \> Järjestelmä \> Suojaus \> Käyttäjät** ja luo sovelluskäyttäjä. Vaihda sivunäkymäksi **Sovelluskäyttäjät** näkymävalikossa.
    1. Valitse **Uusi**. Aseta sovellustunnukseksi *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*. (Objektin tunnus ladataan automaattisesti, kun tallennat muutokset.) Voit mukauttaa nimeä. Voit muuttaa sen esimerkiksi nimeksi *Varaston näkyvyys*. Kun olet valmis, valitse **Tallenna**.
    1. Valitse **Määritä rooli** ja valitse sitten **Järjestelmänvalvoja**. Jos saatavana on rooli nimeltä **Common Data Service -käyttäjä**, valitse myös se.

    Lisätietoja on kohdassa [Sovelluskäyttäjän luominen](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. Jos oletuskieli ei Dataversessäsi ole **englanti**:

    1. Siirry kohtaan **Lisäasetukset \> Hallinta \> Kielet**,
    1. Valitse **englanti (LanguageCode=1033)** ja valitse **Ota käyttöön**.

1. Tuo `Inventory Visibility Dataverse Solution.zip` -tiedosto, joka sisältää Dataverse-konfiguraatioon liittyvät entiteetit ja Power Apps -sovellukset:

    1. Siirry **Ratkaisut**-sivulle.
    1. Valitse **Tuo**.

1. Tuo konfiguraation päivityksen käynnistimen työnkulku:

    1. Siirry Microsoft Flow -sivulle.
    1. Varmista, että yhteys nimeltä *Dataverse (vanha)* on olemassa. (Jos sitä ei ole olemassa, luo se.)
    1. Tuo `Inventory Visibility Configuration Trigger.zip` -tiedosto. Kun käynnistys on tuotu, se näkyy **Omat työnkulut** -kohdassa.
    1. Alusta seuraavat neljä muuttujaa ympäristön tietojen perusteella:

        - Azure-vuokraajan tunnus
        - Azure-sovelluksen asiakastunnus
        - Azure-sovelluksen asiakasohjelman salasana
        - Varaston näkyvyyden päätepiste

            Lisätietoja tästä muuttujasta on jäljempänä tässä ohjeaiheessa kohdassa [Varaston näkyvyyden integraation määrittäminen](#setup-inventory-visibility-integration).

        ![Määrityksen käynnistin.](media/configuration-trigger.png "Määrityksen käynnistin")

    1. Valitse **Ota käyttöön**.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Lisäosan asentaminen

Varaston näkyvyyden apuohjelman asentaminen:

1. Kirjaudu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) -portaaliin.
1. Valitse aloitussivulla projekti, jossa ympäristö on otettu käyttöön.
1. Valitse projektisivulla ympäristö, johon haluat asentaa apuohjelman.
1. Siirry ympäristösivulla alaspäin, kunnes näet **Ympäristön lisäosat** -kohdan **Power Platform -integraatio** -kohdassa, josta löytyy Dataverse-ympäristön nimi.
1. Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.

    ![Ympäristösivu LCS:ssä.](media/inventory-visibility-environment.png "Ympäristösivu LCS:ssa")

1. Valitse **Asenna uusi apuohjelma** -linkki. Käytettävissä olevien apuohjelmien luettelo avautuu.
1. Valitse luettelosta **Vataston näkyvyys**.
1. Anna arvot seuraavissa ympäristön kentissä:

    - **AAD-sovelluksen (asiakasohjelman) tunnus**
    - **AAD-vuokraajan tunnus**

    ![Apuohjelman määrityssivu.](media/inventory-visibility-setup.png "Apuohjelman määrityssivu")

1. Hyväksy käyttöehdot valitsemalla **Käyttöehdot**-valintaruutu.
1. Valitse **Asenna**. Apuohjelman tilana näkyy nyt **Asennetaan**. Se on valmis, päivitä sivu, jonka jälkeen tilana on **Asennettu**.

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>Lisäosan asennuksen poistaminen

Poista apuohjelman asennus valitsemalla **Poista asennus**. Kun päivität LCS:n, varaston näkyvyyden apuohjelma poistetaan. Asennuksen poistoprosessi poistaa apuohjelman rekisteröinnin sekä käynnistää kaikkien palveluun tallennettujen liiketoimintatietojen puhdistustyön.

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>Käytettävissä olevan varaston tietojen käyttäminen Supply Chain Managementista

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Varaston näkyvyyden integrointipaketin käyttöönotto

Jos käytössäsi on Supply Chain Management -versio 10.0.17 tai aiempi, ota yhteyttä varaston näkyvyyden tukihenkilöstöön osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) saadaksesi pakettitiedoston. Ota sitten paketti käyttöön LCS:ssä.

> [!NOTE]
> Jos käyttöönoton aikana ilmenee version vastaavuusvirhe, X++-projekti on tuotava manuaalisesti kehitysympäristöön. Luo sitten käyttöön otettava paketti kehitysympäristössä ja ota se käyttöön tuotantoympäristössä.
> 
> Koodi sisältyy Supply Chain Management -versioon 10.0.18. Jos käytössä on tämä versio tai myöhempi versio, käyttöönottoa ei tarvita.

Varmista, että seuraavat ominaisuudet on otettu käyttöön Supply Chain Management -ympäristössä. (Oletusarvon mukaan ne ovat käytössä.)

| Toiminnon kuvaus | Koodiversio | Vaihda luokka |
|---|---|---|
| Varastodimensioiden ottaminen käyttöön InventSum-taulussa tai poistaminen käytöstä | 10.0.11 | InventUseDimOfInventSumToggle |
| Varastodimensioiden ottaminen käyttöön InventSumDelta-taulussa tai poistaminen käytöstä | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Määritä Varaston näkyvyyden integrointi

1. Avaa Supply Chain Managementissa **[Ominaisuuden hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** -työtila ja ota käyttöön **Varaston näkyvyyden integraatio** -ominaisuus.
1. Siirry kohtaan **Varastonhallinta \> Määritys \> Varaston näkyvyyden integraation parametrit** ja kirjoita sen ympäristön URL-osoite, jossa varaston näkyvyys on käytössä.

    Etsi LCS-ympäristösi Azure-alue ja kirjoita sitten URL-osoite. URL-osoitteessa on seuraava muoto:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    Esimerkiksi Euroopassa ympäristössäsi on jokin seuraavista URL-osoitteista:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    Seuraavat alueet ovat käytettävissä tällä hetkellä.

    | Azure-alue | Alueen lyhyt nimi |
    |---|---|
    | Itä-Australia | eau |
    | Kaakkois-Australia | seau |
    | Kanada, keskinen | cca |
    | Kanada, itäinen | eca |
    | Pohjois-Eurooppa | neu |
    | Länsi-Eurooppa | weu |
    | Itä-Yhdysvallat | eus |
    | Länsi-Yhdysvallat | wus |

1. Valitse **Varastonhallinta \> Kausittainen \> Varaston näkyvyyden integraatio** ja ota työ käyttöön. Kaikki Supply Chain Managementin varastomuutostapahtumat kirjataan nyt varaston näkyvyyteen.

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>Varaston näkyvyyden apuohjelman julkinen ohjelmointirajapinta

Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä. Se tukee kolmea pääasiallista vuorovaikutustyyppiä:

- Varastosaldon määrän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä
- Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä
- Automaattinen synkronointi Supply Chain Managementin käytettävissä olevan varaston kanssa

Automaattinen synkronointi ei kuulu julkiseen ohjelmointirajapintaan. Sen sijaan sitä käsitellään niiden ympäristöjen taustalla, joissa varaston näkyvyyden apuohjelma on otettu käyttöön.

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Todennus

Ympäristön suojaustunnuksen avulla kutsutaan varaston näkyvyyden apuohjelmaa. Siksi sinun on luotava *Azure Active Directory (Azure AD) -tunnus* Azure AD -sovelluksen avulla. Tämän jälkeen Azure AD -tunnuksen avulla saat *käyttöoikeustunnuksen* suojauspalvelusta.

Palvelun suojaustunnus haetaan seuraavasti:

1. Kirjaudu Azure-portaaliin ja etsi sen avulla Supply Chain Management -sovelluksen `clientId` ja `clientSecret`.
1. Nouda Azure Active Directory -tunnus (`aadToken`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Tapa** - `GET`
    - **Tekstisisältö (lomaketiedot)**:

        | avain | arvo |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | resurssi | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. Vastauksena pitäisi olla `aadToken` , joka muistuttaa seuraavaa esimerkkiä.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Muodosta seuraavankaltainen JSON-pyyntö:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Jossa:
    - `client_assertion`-arvon on oltava edellisessä vaiheessa vastaanotettu `aadToken`.
    - `context`-arvon on oltava ympäristötunnus, jossa apuohjelma halutaan ottaa käyttöön.
    - Kaikki muut arvot määritetään samoiksi kuin esimerkissä.

1. Lähetä HTTP-pyyntö, jossa on seuraavat ominaisuudet:
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **Tapa** - `POST`
    - **HTTP-otsikko** - sisällytä ohjelmointirajapinnan versio (avain on `Api-Version` ja arvo `1.0`)
    - **Tekstisisältö** - sisällytä edellisessä vaiheessa luotu JSON-pyyntö.

1. `access_token` saadaan vastauksessa. Sitä tarvitaan haltijatunnuksena, jolla varastoin näkyvyyden ohjelmointirajapintaa kutsutaan. Esimerkki:

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a>Mallipyyntö

Tässä on esimerkki http-pyynnöstä. Voit käyttää mitä tahansa työkaluja tai koodauskieltä lähettääksesi pyynnön, esimerkiksi ``Postman``.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>Varaston näkyvyyden ohjelmointirajapinnan määrittäminen

Ennen palvelun käyttöä on tehtävä valmiiksi seuraavissa aliosissa käsiteltävät määritykset. Määritykset voivat vaihdella ympäristön tietojen mukaan. Siinä pääasiallisesti neljä osaa:

- [Osiointi](#partitioning)
- [Dimensiomääritykset](#dimension-configurations)
- [Indeksointi](#indexing)
- [Mukautettu mitta](#custom-measurement)

#### <a name="partitioning"></a>Osiointi

Osiointi voi vaikuttaa merkittävästi varaston näkyvyyden ohjelmointirajapinnan toimintaan. Niinpä kannattaakin määrittää rakenne, jossa voidaan ryhmitellä tietoja pienissä osissa siten, että merkitykselliset tietokyselyt ovat mahdollisia.

`organizationId` (Supply Chain Managementissa `dataAreaId`) sisältyy aina osiointiin, ja varaston näkyvyys osioidaan oletusarvoisesti dimensioiden perusteella, kuten *Toimipaikka + sijainti*. Tämän vuoksi palveluissa tehtävissä kyselyissä on aina käytettävä suodattimissa määritettyjä dimensioita.

> [!NOTE]
> *Toimipaikka* ja *sijainti* ovat kaksi varaston näkyvyyden yleistä oletusdimensiota. Supply Chain Managementin näiden dimensioiden nimet ovat *toimipaikka* (`InventSiteId`) ja *varasto* (`InventLocationId`)

### <a name="dimension-configurations"></a>Dimensiomääritykset

Varaston näkyvyyden yleisten oletusdimensioiden luettelon ansiosta usein lähdejärjestelmien integrointi on mahdollista.

Seuraavassa taulukossa on varastodimensiot, jotka tulevat varaston näkyvyyden oletusdimensionimiksi.

| Dimensiotyyppi | Dimension nimi |
|---|---|
| Tuote | `ColorId` |
| Tuote | `SizeId` |
| Tuote | `StyleId` |
| Tuote | `ConfigId` |
| Seuranta | `BatchId` |
| Seuranta | `SerialId` |
| Toimipaikka | `LocationId` |
| Toimipaikka | `SiteId` |
| Varaston tila | `StatusId` |
| Varastokohtainen | `WMSLocationId` |
| Varastokohtainen | `WMSPalletId` |
| Varastokohtainen | `LicensePlateId` |

> [!NOTE]
> Edellisessä taulukossa mainittu dimensiotyyppi on tarkoitettu vain tiedoksi. Dimensiotyyppiä ei tarvitse määrittää varaston näkyvyydessä.

Jos mukautettu dimensio on luotu ja sen on siirryttävä oletusarvoon, kun varaston näkyvyys käyttää sitä, **mukautetun dimension** nimi voidaan määrittää varaston näkyvyydessä.

Ulkoiset järjestelmät käyttävät varaston näkyvyyttä RESTful API -ohjelmointirajapinnoilla, jotka ottavat käytettävissä olevat tiedot käyttöön annetuissa dimensiojoukoissa, joissa kyselyt tehdään. Integroinnin osalta varaston näkyvyydessä voidaan määrittää *ulkoinen kanavan tietolähde* ja *kohdedimensioiden* lähdedimensio varaston näkyvyydessä.

Kohdedimensioiden on oltava jokin seuraavista:

- Varaston näkyvyyden oletusdimensiot
- Mukautetut dimensiot

Dimensiomääritysten tarkoitus on standardoida monen järjestelmän integrointi dimensiokyselyitä ja tapahtuman dimensioihin kirjaamista varten.

#### <a name="indexing"></a>Indeksointi

Käytettävissä olevan varaston kysely ei ole useimmiten korkeimmalla kokonaistasolla, vaan tulokset halutaan ehkä nähdä varastodimensioiden mukaan koostettuina.

Varaston näkyvyys on joustava, sillä siinä voidaan määrittää dimensioon tai dimensioyhdistelmiin perustuvia indeksejä.

> [!NOTE]
> Tällä hetkellä indeksejä voi määrittään enintään viisi. Käytettävää dimensiota tai dimensioyhdistelmää on harkittava huolellisesti ennen toteutusta, sillä näin voidaan varmistaa, että se todella vastaa liiketoiminnan tarpeita. Tuotekysely voidaan haluta tehdä esimerkiksi seuraavasti:

- Kyselynä käytettävissä oleva koostetuote *väri*- ja *koko*-dimension mukaan.
- Joissakin tapauksissa kyselyn kohteena voi olla tuote kokonaisuudessaan.

Kaksi indeksiä määritetään seuraavasti:

- `["ColorId", "SizeId"]`
- `[]`

Tyhjä hakasulje tekee koosteen osiossa olevan tuotetunnuksen perusteella.

Indeksointi määrittää, miten tulokset ryhmitellään `groupBy`-kyselyasetuksen perusteella. Jos tässä tapauksessa ei määritetä `groupBy`-arvoja, tuloksena on `productid`-kohtainen kokonaismäärä. Jos `groupBy`-määrityksenä on sen sijaan `groupBy=ColorId&groupBy=SizeId`, tuloksena on useita rivejä, jotka perustuvat järjestelmässä oleviin väri- ja kokoyhdistelmiin.

Kyselyehdot voidaan asettaa pyynnön tekstiosaan.

Seuraavassa esimerkissä on väri- ja kokoyhdistelmää käyttävä tuotekysely.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

`filters`-kenttää varten vain `ProductId` tukee tällä hetkellä useita arvoja. Jos `ProductId` on tyhjä matriisi, kaikkia tuotteita kysellään.

#### <a name="custom-measurement"></a>Mukautettu mitta

Oletusmittamäärät linkitetään Supply Chain Managementiin. Haluat ehkä kuitenkin määrän, joka koostuu oletusmitoista. Sitä varten on määritettävä mukautettuja määritä, jotka lisätään käytettävissä olevan määrän tulosteisiin.

Toiminnon antaa yksinkertaisesti mahdollisuuden määrittää lisättävän ja/tai vähennettävän mittajoukon, joiden avulla voidaan muodostaa mukautettu mitta.

Esimerkiksi seuraavalla kyselyehdolla määritetään mukautetun mitan määräksi `MyCustomAvailableforReservation`, jonka kulutusjärjestelmä käyttää.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Kulutusjärjestelmä | Lasketut mitat | Tietolähde | Määre | Määreen laskentatyyppi |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Vähennyslasku |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Vähennyslasku |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Vähennyslasku |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Vähennyslasku |

Mukautetun mittamäärän kysely palauttaa sitten seuraavan tuloksen.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

`MyCustomAvailableforReservation`-tulos perustuu seuraavaan mukautettujen mittojen laskenta-asetukseen:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Varastosaldon muutosten kirjaaminen

Tarkka URL-osoite, johon tapahtuma kirjataan, määräytyy maantieteellisen alueen mukaan. Sen muoto on seuraava:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Tätä URL-osoitetta käytetään todennuksessa HTTP `POST` -menetelmän ohella lähettämään varastosaldon muutostapahtumat palveluun.

Dynamics 365 -palvelun kanssa HTTP-pyyntöjen avulla tapahtuvassa viestinnässä käytetään erityisotsikko, joka ilmaisee sen Supply Chain Management -esiintymän ympäristötunnuksen, johon tiedot on linkitetty. Esimerkki:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Varastosaldon muutosten kirjaamisen kyselyesimerkki 1

Tässä esimerkissä on skenaario, jossa dimensiomääritys määritetään Power Appsissa.

Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä. Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Varastosaldon muutosten kirjaamisen kyselyesimerkki 2

Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita. Kaikkien dimensioiden on oltava perusdimensioita, kun `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON-tiedostokentän ominaisuudet

Aiemmin käsitellyissä JSON-kyselyesimerkkien kentissä oli seuraavassa taulukossa olevia ominaisuuksia.

| Kentän tunnus | kuvaus |
|---|---|
| `id` | Tietyn muutostapahtuman yksilöivä tunnus. Tämän tunnuksen avulla varmistetaan, että jos viestintä palveluun epäonnistuu kirjauksen aikana, tapahtuman lähettäminen uudelleen ei aiheuta saman tapahtuman laskemista kahdesti järjestelmässä. |
| `organizationId` | Tapahtumaan linkitetyn organisaation tunnus. Tämä yhdistetään Supply Chain Management -organisaatioihin tai tietoalueen tunnuksiin. |
| `productId` | Kyseisen tuotteen tunniste. |
| `quantity` | Määrä, jolla varastosaldoa on muutettava. Jos hyllylle esimerkiksi lisättiin 10 uutta sämpylää, tämä arvo 10. Jos 3 sämpylää sitten poistettiin hyllystä tai myyntiin, tämä arvo on -3. |
| `dimensionDataSource` | Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde. Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää. Dimensiomääritysten ansiosta varaston näkyvyys voi yhdistää mukautetut dimensiot yleisiin oletusdimensioihin. Jos `dimensionDataSource` ei ole määritetty, kyselyissä voi käyttää vain yleisiä oletusdimensioita.   |
| `dimensions` | Dynaaminen avain- ja arvoparisäilö. Ne yhdistetään joihinkin Supply Chain Managementin dimensioihin, minkä lisäksi voidaan lisätä mukautettuja dimensioita (kuten *Lähde*), jotka voivat ilmaista, saapuuko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä. |

### <a name="querying-current-on-hand"></a>Kyselyt nykyisessä varastosaldossa

Nykyisen varastosaldon kyselyjen päätepisteessä on samankaltainen URL-osoite:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Kysely siinä tehdään HTTP `POST` -menetelmällä.

#### <a name="current-on-hand-query-example-1"></a>Nykyisen varastosaldon kyselyesimerkki 1

Tässä esimerkissä on skenaario, jossa Power Appsissa on jo valmis dimensiomääritys.

Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä. Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi. `DimensionDataSource` voidaan määrittää `filters`-kohdassa ja mukautetut dimensiot vodaan määrittää sekä `filters`- että `groupByValues`-kohdissa. Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Nykyisen varastosaldon kyselyesimerkki 2

Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita. Kaikkien dimensioiden on oltava perusdimensioita, kun `filters`-kohdan `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Palautetun tuloksen esimerkki

Edellisten esimerkkien kyselyissä voitiin palauttaa seuraavankaltainen tulos.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Huomaa, että määräkentät on jäsennelty mittahakemistoksi ja niihin liittyviksi arvoiksi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
