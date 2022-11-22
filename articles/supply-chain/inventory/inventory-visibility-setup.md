---
title: Varaston näkyvyyden lisäapuohjelman asentaminen
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c08568b14d7f5c79a1d3609107a88f905498ce2b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762778"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibilityn asentaminen ja määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista.

Inventory Visibility -apuohjelman asentamisessa on käytettävä [Microsoft Dynamics Lifecycle Servicesia](https://lcs.dynamics.com/v2). Lifecycle Services on yhteistyöportaali, jonka muodostamassa ympäristössä ja jonka säännöllisesti päivitetyillä palveluilla voi hallita talous- ja toimintosovellusten elinkaarta. Lisätietoja on kohdassa [Lifecycle Services -resurssit](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> On suositeltavaa liittyä Varaston näkyvyyden lisäosa -käyttäjäryhmään, josta on käyttökelpoisia ohjeita, saada uusimpia päivityksiä ja kirjata varaston näkyvyyteen mahdollisesti liittyvät kysymykset. Jos haluat liittyä, lähetä sähköpostia varaston näkyvyyden tuotetiimille osoitteeseen [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) ja sisällytä Supply Chain Management -ympäristön tunnus.

## <a name="inventory-visibility-prerequisites"></a>Varaston näkyvyyden apuohjelman edellytykset

Seuraavat tehtävät on tehtävä ennen varaston näkyvyyden apuohjelman asentamista:

- Sellaisen Lifecycle Services -toteutusprojektin hankkiminen, jossa on otettu käyttöön vähintään yksi ympäristö.
- Varmistetaan, että apuohjelmien asennusedellytykset toteutuvat. Lisätietoja näistä edellytyksistä on kohdassa [Apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Varaston näkyvyys ei edellytä kaksoiskirjoituslinkitystä.

> [!NOTE]
> Tällä hetkellä tuettuja maita ja alueita ovat esimerkiksi Kanada (CCA, ECA), Yhdysvallat (WUS, EUS), Euroopan unioni (NEU, WEU), Yhdistyneet kuningaskunnat (SUK, WUK), Australia (EAU, SEAU), Japani (EJP, WJP) ja Brasilia (SBR, SCUS).

Jos sinulla on näitä edellytyksiä koskevia kysymyksiä, ota yhteys varaston näkyvyyden tuotetiimiin osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Varaston näkyvyyden lisäapuohjelman asentaminen

Rekisteröi sovellus ennen apuohjelman asentamista ja lisää asiakasohjelman salasana Azure Active Directoryyn (Azure AD) Azure-tilauksessa. Lisätietoja on kohdassa [Sovelluksen rekisteröinti](/azure/active-directory/develop/quickstart-register-app) ja [Asiakasohjelman salasanan lisääminen](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Muista kirjoittaa **Sovelluksen (asiakasohjelman) tunnus**-, **Asiakasohjelman salasana**- ja **Vuokraajan tunnus** -arvot muistiin, sillä niitä tarvitaan myöhemmin.

> [!IMPORTANT]
> Jos sinulla on useita Lifecycle Services -ympäristöjä, luo kullekin ympäristölle erilainen Azure AD -sovellus. Jos käytät samaa sovellustunnusta ja vuokraajatunnusta Inventory Visibility -apuohjelman asentamisessa eri ympäristöihin, vanhemmissa ympäristöissä ilmenee tunnusongelma. Tuloksena vain viimeinen asennus on kelvollinen.

Kun sovellus rekisteröidään ja asiakasohjelman salasana lisätään Azure AD:hen, asenna varaston näkyvyyden apuohjelma seuraavasti:

1. Kirjaudu [Lifecycle Servicesiin](https://lcs.dynamics.com/Logon/Index).
1. Valitse aloitussivulla projekti, jossa ympäristö on otettu käyttöön.
1. Valitse projektisivulla ympäristö, johon haluat asentaa apuohjelman.
1. Siirry ympäristösivulla alaspäin **Power Platform -integrointi** -osan **Ympäristön lisäosat** -osaan. Dataverse-ympäristön nimi löytyy sieltä. Varmista, että Dataverse-ympäristön nimi on se, jota halutaan käyttää varaston näkyvyydessä.

    > [!NOTE]
    > Tällä hetkellä vain Lifecycle Servicesin avulla luotuja Dataverse-ympäristöjä tuetaan. Jos Dataverse-ympäristö luotiin jollain muulla tavalla (esimerkiksi PowerApps -hallintakeskuksessa) ja jos se on linkitetty Supply Chain Management -ympäristöön, yhdistämismäärityksen ongelma on korjattava ennen varaston näkyvyyden apuohjelman asentamista.
    >
    > On mahdollista, että kaksoiskirjoitusympäristö on linkitetty Dataverse-esiintymään, kun taas Lifecycle Servicesiä ei ole määritetty Power Platform -integrointia varten. Linkittämisen vastaamattomuus voi aiheuttaa odottamattomia toimintoja. Lifecycle Services -ympäristön tietojen tulee vastata sen ympäristön tietoja, johon käyttäjällä on yhteys kaksoiskirjoituksessa, jotta liiketoimintatapahtumat, virtuaalitaulukot ja apuohjelmat voivat käyttää samaa yhteyttä. Lisätietoja yhdistämismäärityksen ongelman korjaamisesta on kohdassa [Linkitysristiriita](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch). Kun yhdistämismäärityksen ongelma on ratkaistu, voit jatkaa varaston näkyvyyden asentamista.

1. Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.

    ![Lifecycle Servicesin Ympäristö-sivu](media/inventory-visibility-environment.png "Lifecycle Servicesin Ympäristö-sivu")

1. Valitse **Asenna uusi apuohjelma** -linkki. Käytettävissä olevien apuohjelmien luettelo avautuu.
1. Valitse luettelossa **Varaston näkyvyys**.
1. Määritä seuraavat ympäristön kentät:

    - **AAD-sovelluksen (asiakasohjelman) tunnus** – anna aiemmin muistiin kirjoitettu Azure AD -sovelluksen tunnus.
    - **AAD-vuokraajan tunnus** – anna aiemmin muistiin kirjoitettu vuokraajan tunnus.

    ![Apuohjelman määrityssivu](media/inventory-visibility-setup.png "Apuohjelman määrityssivu")

1. Hyväksy käyttöehdot valitsemalla **Käyttöehdot**-valintaruutu.
1. Valitse **Asenna**. Apuohjelman tilana näkyy nyt **Asennetaan**. Kun asennus on valmis, päivitä sivu. Tilan pitäisi olla nyt **Asennettu**.
1. Valitse Dataversen vasemmassa siirtymisruudussa **Sovellukset**-osa ja varmista, että **Varaston näkyvyys** Power Apps -asennus onnistui. Jos **Sovellukset**-osaa ei ole, ota yhteys varaston näkyvyyden tuotetiimiin osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!NOTE]
> Jos järjestelmä varoittaa Inventory Visibilityn asentamisessa tarvittavan käyttöoikeuden puuttumisesta Lifecycle Servicesissa, ota yhteyttä järjestelmänvalvojaan oikeuksien muokkaamiseksi.
>
> Jos asennus Lifecycle Services -sivulta kestää yli tunnin, käyttäjätililtä ei ehkä ole käyttöoikeutta asentaa ratkaisuja Dataverse-ympäristöön. Korjaa ongelma seuraavien ohjeiden mukaisesti:
>
> 1. Inventory Visibility -apuohjelman asennus peruutetaan Lifecycle Services -sivulla.
> 1. Kirjaudu sisään [Microsoft 365-hallintakeskukseen](https://admin.microsoft.com) ja varmista, että lisäosan asennuksessa käytettävälle käyttäjätilille on määritetty "Dynamics 365 Unified Operations-suunnitelman" käyttöoikeus. Määritä käyttöoikeus tarvittaessa.
> 1. Kirjaudu [Power Platform-hallintakeskukseen](https://admin.powerplatform.microsoft.com) asiaankuuluvaa käyttäjätiliä käyttäen. Asenna sitten varaston näkyvyyden apuohjelma noudattamalla seuraavia vaiheita:
>     1. Valitse ympäristö, johon haluat asentaa apuohjelman.
>     1. Valitse **Dynamics 365 -sovellukset**.
>     1. Valitse **Asenna sovellus**.
>     1. Valitse **Varaston näkyvyys**
>
> 1. Kun asennus on valmis, siirry takaisin Lifecycle Services -sivulle ja yritä asentaa **Inventory Visibility** -apuohjelma uudelleen.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Varaston näkyvyyden määritys Supply Chain Managementissa

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Varaston näkyvyyden integrointipaketin käyttöönotto

Jos käytössäsi on Supply Chain Management -versio 10.0.17 tai aiempi, ota yhteyttä varaston näkyvyyden tukihenkilöstöön osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) saadaksesi pakettitiedoston. Ota sitten paketti käyttöön Lifecycle Servicesissä.

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

Kun olet asentanut lisäosan, valmistele Supply Chain Management -järjestelmäsi toimimaan sen kanssa noudattamalla seuraavia ohjeita.

1. Avaa Supply Chain Managementissa **[Ominaisuuden hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** -työtila ja ota seuraavat ominaisuudet käyttöön:
    - *Varaston näkyvyyden integrointi* – Vaaditaan.
    - *Varaston näkyvyyden integrointi varauksen vastakirjauksella* – Suositeltava mutta valinnainen. Vaatii version 10.0.22 tai sitä uudemman. Lisätietoja on kohdassa [Varaston näkyvyyden varaukset](inventory-visibility-reservations.md).

1. Valitse **Varastonhallinta \> Määritys \> Varaston näkyvyyden integroinnin parametrit**.
1. Avaa **Yleistä**-välilehti ja määritä seuraavat asetukset:
    - **Varaston näkyvyyden päätepiste** – Anna sen ympäristön URL-osoite, jossa suoritat varaston näkyvyyden. Lisätietoja on kohdassa [Palvelun päätepisteen etsiminen](inventory-visibility-configuration.md#get-service-endpoint).
    - **Yksittäisen pyynnön tietueiden enimmäismäärä** – Määritä yhteen pyyntöön sisällytettävien tietueiden enimmäismäärä. Sinun on annettava positiivinen kokonaisluku, joka on enintään 1 000. Oletusarvo on 512. On erittäin suositeltavaa pitää oletusarvo voimassa, ellei Microsoftin tuki ole muuta neuvonut tai ellet ole muuten varma, että sinun on muutettava sitä.

1. Jos olet ottanut valinnaisen *Varaston näkyvyyden integrointi varauksen vastakirjauksella* -ominaisuuden, avaa **Varauksen vastakirjaus** -välilehti ja määritä seuraavat asetukset:
    - **Ota varauksen vastakirjaus käyttöön** – Voit ottaa tämän toiminnon käyttöön asettamalla arvoksi *Kyllä*.
    - **Varauksen vastakirjauksen muuttuja** – Valitse varaston tapahtumatila, joka vastakirjaa varaston näkyvyydessä tehdyt varaukset. Tämä asetus määrittää tilauksen käsittelytilan, joka käynnistää vastakirjaukset. Vaihetta seurataan tilauksen varastotapahtuman tilan perusteella. Valitse jompikumpi seuraavista vaihtoehdoista:
        - *Tilauksessa* – kun tilana on *Tapahtumassa*, tilaus lähettää vastakirjauspyynnön, kun se luodaan. Vastakirjauksen määrä on luodun tilauksen määrä.
        - *Varaus* – Kun tilana on *Varaa tilattu tapahtuma*, tilaus lähettää vastakirjauspyynnön, kun tilaus varataan tai poimitaan, kun sen pakkausluettelo kirjataan tai kun se laskutetaan. Pyyntö käynnistetään vain kerran ensimmäisessä vaiheessa, kun mainittu prosessi tapahtuu. Vastakirjauksen määrä on määrä, jossa varastotapahtuman tila muuttui tilasta *Tilauksessa* tilaan *Tilaukseen varattu* (tai myöhempään tilaan) kulloisellakin tilausrivillä.

1. Valitse **Varastonhallinta \> Kausittainen \> Varaston näkyvyyden integraatio** ja ota työ käyttöön. Kaikki Supply Chain Managementin varastomuutostapahtumat kirjataan nyt varaston näkyvyyteen.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Varaston näkyvyyden apuohjelman asennuksen poistaminen

Seuraavien ohjeiden avulla voit poistaa varaston näkyvyyden apuohjelman asennuksen:

1. Kirjaudu Supply Chain Managementiin.
1. Valitse **Varastonhallinta \> Kausittainen \> Varaston näkyvyyden integraatio** ja poista työ käytöstä.
1. Siirry Lifecycle Servicesiin ja avaa sen ympäristön sivu, jossa haluat poistaa apuohjelman asennuksen (katso myös [Inventory Visibility -apuohjelman asentaminen](#install-add-in)).
1. Valitse **Poista asennus**.
1. Asennuksen poistoprosessi lopettaa nyt Inventory Visibility -apuohjelman, poistaa apuohjelman rekisteröinnin Lifecycle Servicesistä ja poista mahdolliset Inventory Visibility -apuohjelman tietojen välimuistiin tallennetut tilapäiset tiedot. Dataverse-tilaukseen synkronoidut ensisijaiset varastotiedot tallennetaan yhä sinne. Jos haluat poistaa nämä tiedot, tee nämä toiminnot loppuun.
1. Avaa [Power Apps](https://make.powerapps.com).
1. Valitse siirtymispalkissa **Ympäristö**.
1. Valitse Dataverse-ympäristö, joka on sidottu Lifecycle Services -ympäristöön.
1. Valitse **Ratkaisut** ja poista nämä viisi ratkaisua seuraavassa järjestyksessä:
    1. Dynamics 365 Inventory Visibility – ankkuri
    1. Dynamics 365 Inventory Visibility – laajennukset
    1. Dynamics 365 Inventory Visibility – sovellus
    1. Dynamics 365 Inventory Visibility – ohjausobjektit
    1. Dynamics 365 Inventory Visibility – perusmääritys 

    Kun nämä ratkaisut on poistettu, myös taulukoihin tallennetut tiedot poistetaan.

> [!NOTE]
> Jos palautat Supply Chain Management -tietokannan sen varaston näkyvyyden apuohjelman asennuksen poistamisen jälkeen ja haluat sitten asentaa sen uudelleen, varmista ennen lisäosan uudelleenasennusta, että olet poistanut Dataverse-tilaukseen (edellisissä ohjeissa kuvatulla tavalla) tallennetut varaston näkyvyyden vanhat tiedot. Näin estät muussa tapauksessa mahdollisesti esiintyvät ristiriidat tietojen välillä.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a>Varaston näkyvyyden tietojen tyhjentäminen Dataversesta ennen Supply Chain Management -tietokannan palauttamista

Jos käytössä on varaston näkyvyys ja palautat Supply Chain Management -tietokannan, palautettu tietokanta voi sisältää tietoja, jotka ovat ristiriidassa niiden tietojen kanssa, jotka varaston näkyvyys on synkronoinut aiemmin Dataverseen. Tämä ristiriita tiedoissa voi aiheuttaa järjestelmävirheitä ja muita ongelmia. Tämän vuoksi on tärkeää, että tyhjennät aina kaikki Inventory Visibility -tiedot Dataversesta ennen Supply Chain Management -tietokannan palautusta.

Jos haluat palauttaa Supply Chain Management -tietokannan, toimi seuraavasti:

1. Poista varaston näkyvyyden apuohjelman asennus ja poista kaikki liittyvät tiedot Dataversesta [Varaston näkyvyyden apuohjelman asennuksen poistaminen](#uninstall-add-in) -kohdan ohjeiden mukaan
1. Palauta Supply Chain Management -tietokanta esimerkiksi [Tietokannan tietyn ajankohdan palautus](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md)- tai [Tuotantotietokannan ajankohdan palautus eristysympäristöön](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md) -kohdan ohjeiden mukaan.
1. Jos haluat yhä käyttää sitä, poista asennus ja määritä varaston näkyvyyden apuohjelma [Varaston näkyvyyden lisäapuohjelman asentaminen](#install-add-in)- ja [Varaston näkyvyyden integraation määrittäminen](#setup-inventory-visibility-integration) -kohdan ohjeiden mukaan


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
