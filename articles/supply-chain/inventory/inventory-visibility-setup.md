---
title: Varaston näkyvyyden apuohjelman määrittäminen
description: Tässä aiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8573fe01abb1c6092012baf85e8b7df40b74a31f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343581"
---
# <a name="set-up-inventory-visibility"></a>Varaston näkyvyyden apuohjelman määrittäminen

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Tässä aiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista.

Varaston näkyvyyden apuohjelman asentamiseen on käytettävä Microsoft Dynamics Lifecycle Servicesiä (LCS). LCS on yhteistyöportaali, jonka muodostamassa ympäristössä ja jonka säännöllisesti päivitetyillä palveluilla voi hallita Finance and Operations -sovellusten elinkaarta.

Lisätietoja on kohdassa [Lifecycle Services -resurssit](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Varaston näkyvyyden apuohjelman edellytykset

Seuraavat tehtävät on tehtävä ennen varaston näkyvyyden apuohjelman asentamista:

- Sellaisen LCS-toteutusprojektin hankkiminen, jossa on otettu käyttöön vähintään yksi ympäristö.
- Varmistetaan, että apuohjelmien asennusedellytykset toteutuvat. Lisätietoja näistä edellytyksistä on kohdassa [Apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Varaston näkyvyys ei edellytä kaksoiskirjoituslinkitystä.
- Seuraavat tarvittavat tiedostot saadaan ottamalla yhteyttä varaston näkyvyyden tuotetiimiin osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com):

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (jos käynnissä ollut Supply Chain Managementin versio on aiempi kuin 10.0.18)

> [!NOTE]
> Tällä hetkellä tuettuja maita ja alueita ovat esimerkiksi Kanada (CCA, ECA), Yhdysvallat (WUS, EUS), Euroopan unioni (NEU, WEU), Yhdistyneet kuningaskunnat (SUK, WUK) ja Australia (EAU, SEAU).

Näitä edellytyksiä koskevia kysymyksiä voi esittää varaston näkyvyyden tuotetiimille.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Määritys Dataverse

Varaston näkyvyyden kanssa käytettävä Dataverse asennetaan ottamalla varaston näkyvyyspaketti käyttöön Package Deployer -työkalulla. Seuraavissa aliosissa käsitellään kunkin tehtävän suorittamista.

> [!NOTE]
> Tällä hetkellä vain LCS:n avulla luotuja Dataverse-ympäristöjä tuetaan. Jos Dataverse-ympäristö luotiin jollain muulla tavalla (esimerkiksi Power Apps -hallintakeskuksessa) ja jos se on linkitetty Supply Chain Management -ympäristöön, yhdistämismäärityksen ongelma voidaan korjata ottamalla ensin yhteys varaston näkyvyyden tuotetiimiin. Varaston näkyvyyden apuohjelma voidaan asentaa sen jälkeen.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Siirtyminen Dataverse-ratkaisun vanhasta versiosta

Jos varaston näkyvyyden Dataverse-ratkaisun vanha versio on asennettu, päivitä versio seuraavien ohjeiden avulla. Tapausvaihtoehtoja on kaksi:

- **Tapaus 1:** Jos Dataverse asennetaan manuaalisesti tuomalla `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip` -ratkaisu, toimi seuraavasti:

    1. Lataa seuraavat kolme tiedostoa:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Tuo `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` ja `InventoryServiceBase_managed.cab` manuaalisesti Dataverseen toimimalla seuraavasti:

        1. Avaa Dataverse-ympäristön URL-osoite.
        1. Avaa **Ratkaisut**-sivu.
        1. Valitse **Tuo**.

    1. Ota `InventoryServiceApplication.PackageDeployer.zip`-paketti käyttöön käyttämällä Package Deployer -työkalua. Lisätietoja on jäljempänä tämän aiheen kohdassa [Paketin ottaminen käyttöön Package Deployer -työkalun avulla](#deploy-package).

- **Tapaus 2:** Jos Dataverse asennetaan Package Deployer -työkalulla ennen vanhan `.*PackageDeployer.zip`-paketin asentamista, lataa `InventoryServiceApplication.PackageDeployer.zip` ja tee päivitys. Lisätietoja on kohdassa [Paketin ottaminen käyttöön Package Deployer -työkalun avulla](#deploy-package).

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Paketin ottaminen käyttöön Package Deployer -työkalun avulla

1. Asenna kehittäjien työkalut kohdassa [Työkalujen lataaminen NuGetistä](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget) kuvatulla tavalla.
1. Poista Teams-ryhmästä ladatun `InventoryServiceApplication.PackageDeployer.zip`-tiedoston esto seuraavasti:

    1. Pidä tietuetta valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse **Ominaisuudet**.
    1. Etsi **Ominaisuudet**-valintaikkunan **Yleiset**-välilehden **Suojaus**-osa, valitse **Poista esto** ja käytä muutosta. Jos **Yleiset**-välilehdessä ei ole **Suojaus**-osaa, tiedostoa ei ole estetty. Siirry siinä tapauksessa seuraavaan vaiheeseen.

    ![Ladatun tiedoston eston poistaminen](media/unblock-file.png "Ladatun tiedoston eston poistaminen")

1. Pura `InventoryServiceApplication.PackageDeployer.zip`-tiedosto ja etsi seuraavat:

    - `InventoryServiceApplication`-kansio
    - `[Content_Types].xml`-tiedosto
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`-tiedosto

1. Kopio edellä mainitut kohteet `.\Tools\PackageDeployment`-hakemistoon. (Tämä hakemisto luotiin, kun kehittäjien työkalut asennettiin.)
1. Suorita `.\Tools\PackageDeployment\PackageDeployer.exe` ja tuo ratkaisut näytön ohjeiden mukaisesti.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Varaston näkyvyyden lisäapuohjelman asentaminen

Rekisteröi sovellus ennen apuohjelman asentamista ja lisää asiakasohjelman salasana Azure Active Directoryyn (Azure AD) Azure-tilauksessa. Lisätietoja on kohdassa [Sovelluksen rekisteröinti](/azure/active-directory/develop/quickstart-register-app) ja [Asiakasohjelman salasanan lisääminen](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Muista kirjoittaa **Sovelluksen (asiakasohjelman) tunnus**-, **Asiakasohjelman salasana**- ja **Vuokraajan tunnus** -arvot muistiin, sillä niitä tarvitaan myöhemmin.

Kun sovellus rekisteröidään ja asiakasohjelman salasana lisätään Azure AD:hen, asenna varaston näkyvyyden apuohjelma seuraavasti:

1. Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com/Logon/Index).
1. Valitse aloitussivulla projekti, jossa ympäristö on otettu käyttöön.
1. Valitse projektisivulla ympäristö, johon haluat asentaa apuohjelman.
1. Siirry ympäristösivulla alaspäin **Power Platform -integrointi** -osan **Ympäristön lisäosat** -osaan. Dataverse-ympäristön nimi löytyy sieltä.
1. Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.

    ![Ympäristösivu LCS:ssä](media/inventory-visibility-environment.png "Ympäristösivu LCS:ssä")

1. Valitse **Asenna uusi apuohjelma** -linkki. Käytettävissä olevien apuohjelmien luettelo avautuu.
1. Valitse luettelossa **Varaston näkyvyys**.
1. Määritä seuraavat ympäristön kentät:

    - **AAD-sovelluksen (asiakasohjelman) tunnus** – anna aiemmin muistiin kirjoitettu Azure AD -sovelluksen tunnus.
    - **AAD-vuokraajan tunnus** – anna aiemmin muistiin kirjoitettu vuokraajan tunnus.

    ![Apuohjelman määrityssivu](media/inventory-visibility-setup.png "Apuohjelman määrityssivu")

1. Hyväksy käyttöehdot valitsemalla **Käyttöehdot**-valintaruutu.
1. Valitse **Asenna**. Apuohjelman tilana näkyy nyt **Asennetaan**. Kun asennus on valmis, päivitä sivu. Tilan pitäisi olla nyt **Asennettu**.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Varaston näkyvyyden apuohjelman asennuksen poistaminen

Varaston näkyvyyden apuohjelma poistetaan valitsemalla **Poista asennus** LCS-sivulla. Asennuksen poistoprosessi lopettaa varaston näkyvyyden apuohjelman, poistaa apuohjelman rekisteröinnin LCS:stä ja poista mahdolliset varaston näkyvyyden apuohjelman tietojen välimuistiin tallennetut tilapäiset tiedot. Dataverse-tilaukseen tallennettuja ensisijaisia varastotietoja ei kuitenkaan poisteta.

Dataverse-tilaukseen tallennettujen varastotietojen asennus poistetaan avaamalla [Power Apps](https://make.powerapps.com), valitsemalla siirtymispalkissa **Ympäristö** ja valitsemalla sitten Dataverse-ympäristö, joka on sidottu LCS-ympäristöön. Valitse sitten **Ratkaisut** ja poista seuraavat viisi ratkaisua:

- Varaston näkyvyyssovelluksen ankkurisovellus Dynamics 365 -ratkaisuissa
- Dynamics 365 FNO SCM:n varaston näkyvyyden sovellusratkaisu
- Varastopalvelumääritykset
- Erillinen varaston näkyvyys
- Dynamics 365 FNO SCM:n varaston näkyvyyden perusratkaisu

Kun nämä ratkaisut on poistettu, myös taulukoihin tallennetut tiedot poistetaan.

## <a name="set-up-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Supply Chain Managementin määritys

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Varaston näkyvyyden integrointipaketin käyttöönotto

Jos käytössäsi on Supply Chain Management -versio 10.0.17 tai aiempi, ota yhteyttä varaston näkyvyyden tukihenkilöstöön osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) saadaksesi pakettitiedoston. Ota sitten paketti käyttöön LCS:ssä.

> [!NOTE]
> Jos käyttöönoton aikana ilmenee version vastaavuusvirhe, X++-projekti on tuotava manuaalisesti kehitysympäristöön. Luo sitten käyttöön otettava paketti kehitysympäristössä ja ota se käyttöön tuotantoympäristössä.
>
> Koodi sisältyy Supply Chain Management -versioon 10.0.18. Jos käytössä on tämä versio tai myöhempi versio, käyttöönottoa ei tarvita.

Varmista, että seuraavat ominaisuudet on otettu käyttöön Supply Chain Management -ympäristössä. (Oletusarvon mukaan ne ovat käytössä.)

| Toiminnon kuvaus | Koodiversio | Vaihda luokka |
|---|---|---|
| Varastodimensioiden ottaminen käyttöön InventSum-taulussa tai poistaminen käytöstä      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Varastodimensioiden ottaminen käyttöön InventSumDelta-taulussa tai poistaminen käytöstä | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Määritä Varaston näkyvyyden integrointi

1. Avaa Supply Chain Managementissa **[Ominaisuuden hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** -työtila ja ota käyttöön *Varaston näkyvyyden integraatio* -ominaisuus.
1. Siirry kohtaan **Varastonhallinta \> Määritys \> Varaston näkyvyyden integraation parametrit** ja kirjoita sen ympäristön URL-osoite, jossa varaston näkyvyys on käytössä. Lisätietoja on kohdassa [Palvelun päätepisteen etsiminen](inventory-visibility-power-platform.md#get-service-endpoint).
1. Valitse **Varastonhallinta \> Kausittainen \> Varaston näkyvyyden integraatio** ja ota työ käyttöön. Kaikki Supply Chain Managementin varastomuutostapahtumat kirjataan nyt varaston näkyvyyteen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
