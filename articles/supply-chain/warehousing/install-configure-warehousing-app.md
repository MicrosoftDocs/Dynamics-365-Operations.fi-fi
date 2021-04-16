---
title: Varastosovelluksen asentaminen ja yhdistäminen
description: Tässä ohjeaiheessa käsitellään varastosovelluksen asentamista mobiililaitteisiin ja niiden määrittämistä muodostamaan yhteys Microsoft Dynamics 365 Supply Chain Management -ympäristöön. Voit määrittää kunkin laitteen manuaalisesti tai voit tuoda yhteysasetukset käyttämällä tiedostoa tai lukemalla QR-koodin.
author: MarkusFogelberg
ms.date: 05/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c92fe991c8651d7665de2e850d8649b72f525f4c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835561"
---
# <a name="install-and-connect-the-warehouse-app"></a>Varastosovelluksen asentaminen ja yhdistäminen

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tässä ohjeaiheessa kuvataan, miten vanha varastosovellus (joka on nyt vanhentunut) määritetään. Lisätietoja uuden varaston hallinnan mobiilisovelluksen määrittämisestä on kohdassa [Varastonhallinnan mobiilisovelluksen asentaminen ja yhdistäminen](install-configure-warehouse-management-app.md).

> [!NOTE]
> Tässä aiheessa käsitellään pilvikäyttöönottojen varastointisovellusta. Lisätietoja varastointisovelluksen määrittämisestä paikallisissa käyttöönotoissa on kohdassa [Varastointi paikallisissa käyttöönotoissa](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).

Varastosovellus on saatavilla Google Play Storesta ja Microsoft Storesta. Se toimitetaan erillisenä osana. Niinpä se onkin ladattava kuhunkin laitteeseen ja määritettävä muodostamaan yhteys Microsoft Dynamics 365 Supply Chain Management -ympäristöön.

Tässä ohjeaiheessa käsitellään varastosovelluksen asentamista mobiililaitteisiin ja niiden määrittämistä muodostamaan yhteys Supply Chain Management -ympäristöön. Voit määrittää kunkin laitteen manuaalisesti tai voit tuoda yhteysasetukset käyttämällä tiedostoa tai lukemalla QR-koodin.

## <a name="system-requirements"></a>Järjestelmävaatimukset

Varastosovellus on saatavana sekä Windows- että Android-käyttöjärjestelmiin. Sovelluksen uusimman version käyttäminen edellyttää, että mobiililaitteisiin on asennettu jokin seuraavista käyttöjärjestelmistä:

- Windows 10 (universaali Windows-ympäristö \[UWP\]) Fall Creators -päivitys 1709 (koontiversio 10.0.16299) tai uudempi
- Android 4.4 tai uudempi

> [!NOTE]
> Jos ohjelman on tuettava vanhoja Windows-laitteita, joissa ei voi käyttää Windowsin uusinta versiota, voit silti ladata varastosovelluksen version 1.6.3.0 Microsoft Storesta. Tätä versiota käytetään Windows 10:n (UWP) marraskuun päivityksessä 1511 (koontiversio 10.0.10586) tai sitä uudemmassa versiossa. Tämä varastosovelluksen versio ei kuitenkaan tue yhteysasetusten joukkokäyttöönottoa. Tämän vuoksi [yhteys on määritettävä manuaalisesti](#config-manually) jokaisessa sovelluksen tätä versiota käyttävässä laitteessa.

## <a name="get-the-warehouse-app"></a>Varastosovelluksen hankkiminen

Lataa sovellus valitsemalla jompikumpi seuraavista linkeistä:

- **Windows (UWP):** [Dynamics 365 for Finance and Operations – Warehousing Microsoft Storessa](https://www.microsoft.com/store/apps/9p1bffd5tstm)
- **Android:** [Warehousing – Dynamics 365 Google Play Storessa](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

Pienissä käyttöönotoissa sovellus kannattaa asentaa valitusta kaupasta kuhunkin laitteeseen, jonka jälkeen yhteys käytettyyn ympäristöön voidaan määrittää manuaalisesti. Varastosovelluksen versiosta 1.7.0.0 alkaen sovelluksen käyttöönoton ja/tai määrityksen voi myös automatisoida. Tämä voi olla kätevää, jos hallittavia laitteita on useita ja käytössä on mobiililaitteiden ja -sovellusten hallintaratkaisu, kuten [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune). Lisätietoja sovellusten lisäämisestä Intunen avulla on kohdassa [Sovellusten lisääminen Microsoft Intuneen](https://docs.microsoft.com/mem/intune/apps/apps-add).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Verkkopalvelusovelluksen luominen Azure Active Directoryssa

Varastosovelluksen käyttö tietyn Supply Chain Management -palvelimen kanssa edellyttää, että verkkopalvelusovellus rekisteröidään Supply Chain Managementin vuokraajassa Azure Active Directoryssa (Azure AD). Seuraavaksi näytetään yksi tapa, jolla sen voi tehdä. Lisätietoja ja muita tapoja on jäljempänä.

1. Siirry selaimessa osoitteeseen [https://portal.azure.com](https://portal.azure.com/).
1. Anna sen käyttäjän nimi ja salasana, jolla on Azure‑tilauksen käyttöoikeus.
1. Valitse Azure-portaalin vasemmassa siirtymisruudussa **Azure Active Directory**.

    ![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")

1. Varmista, että käytössä on Supply Chain Managementin käyttämä Azure AD -esiintymä.
1. Valitse **Hallinta**-luettelossa **Sovelluksen rekisteröinnit**.

    ![Sovelluksen rekisteröinnit](media/app-connect-azure-register.png "Sovelluksen rekisteröinnit")

1. Avaa ohjattu **Sovelluksen rekisteröinti** -toiminto valitsemalla työkalurivillä **Uusi rekisteröinti**.
1. Anna sovelluksen nimi, valitse **Vain tämän organisaatiohakemiston tilit** -vaihtoehto ja valitse sitten **Rekisteröi**.

    ![Ohjattu sovelluksen rekisteröintitoiminto](media/app-connect-azure-register-wizard.png "Ohjattu sovelluksen rekisteröintitoiminto")

1. Uusi sovelluksen rekisteröinti avautuu. Kirjoita **Sovelluksen (asiakasohjelman) tunnus** -kohdan arvo muistiin, sillä tarvitset sitä myöhemmin. Tätä tunnusta kutsutaan myöhemmin tässä ohjeaiheessa *asiakasohjelman tunnukseksi*.

    ![Sovelluksen (asiakasohjelman) tunnus](media/app-connect-azure-app-id.png "Sovelluksen (asiakasohjelman) tunnus")

1. Valitse **Hallinta**-luettelossa **Varmenne ja salaisuudet**. Valitse sitten jokin seuraavista painikkeista sen mukaan, miten haluat määrittää todennuksen sovelluksessa. (Lisätietoja on jäljempänä tässä ohjeaiheessa kohdassa [Todennus käyttämällä varmennetta tai asiakasohjelman salaisuutta](#authenticate).)

    - **Lataa varmenne** – Lataa salaisuutena käytettävä varmenne. Tätä menetelmää kannattaa käyttää, sillä se on turvallinen ja se on laajemmin automatisoitavissa. Jos varastosovellusta käytetään Windows-laitteissa, kirjoita muistiin varmenteen lataamisen jälkeen näkyvän **allekirjoituksen** arvo. Tätä arvoa tarvitaan varmenteen määrittämiseen Windows-laitteissa.
    - **Uusi asiakasohjelman salasana** – Luo avain antamalla avaimen kuvaus ja sen kesto **Salasanat**-osassa ja valitse sitten **Lisää**. Kopioi avain ja tallenna se turvalliseen paikaan.

    ![Varmenne ja salaisuudet](media/app-connect-azure-authentication.png "Varmenne ja salaisuudet")

Lisätietoja verkkopalvelusovellusten määrittämisestä Azure AD:ssä on seuraavissa resursseissa:

- Lisätietoja verkkopalvelusovellusten määrittämisestä Azure AD:ssä Windows PowerShellin avulla on kohdassa [Ohje: Varmennetta käyttävän palvelun päänimen luominen Azure PowerShellin avulla](https://docs.microsoft.com/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Lisätietoja verkkopalvelusovelluksen luomisesta Azure AD:ssä on seuraavissa ohjeaiheissa:

    - [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)
    - [Toimintaohje: Azure AD -sovelluksen ja resursseja käyttävän palvelun päänimen luonti portaalin avulla](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Supply Chain Managementin käyttäjätilin luominen ja määrittäminen

Supply Chain Management voi käyttää Azure AD -sovellusta seuraavien ohjeiden mukaisesti:

1. Varastosovelluksen käyttäjän tunnistetietoja vastaavan käyttäjän luonti:

    1. Valitse Supply Chain Managementissa **Järjestelmän hallinta \> Käyttäjät \> Käyttäjät**.
    1. Luo käyttäjä.
    1. Määritä varastoinnin mobiililaitteen käyttäjä.

    ![Varastoinnin mobiililaitteen käyttäjän määrittäminen](media/app-connect-app-users.png "Varastoinnin mobiililaitteen käyttäjän määrittäminen")

1. Azure AD -sovelluksen liittäminen varastosovelluksen käyttäjään:

    1. Valitse **Järjestelmän hallinta \> Asetukset \> Azure Active Directory -sovellukset**.
    1. Luo rivi.
    1. Anna edellisessä osassa muistiin kirjoitettu asiakasohjelman tunnus, nimeä se ja valitse juuri luotu käyttäjä. Kaikille laitteille kannattaa antaa tunniste. Tällä tavoin kadotetun laitteen Supply Chain Managementin käyttöoikeus on helppo poistaa tällä sivulla.

    ![Azure Active Directory -sovellukset](media/app-connect-aad-apps.png "Azure Active Directory -sovellukset")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Todennus käyttämällä varmenteen tai asiakasohjelman salauskoodia

Azure AD:n todennuksen avulla mobiililaite voidaan yhdistää turvallisesti Supply Chain Managementiin. Todennuksen voi tehdä joko asiakasohjelman salauskoodilla tai varmenteella. Jos yhteysasetukset tuodaan, asiakasohjelman salauskoodin sijaan kannattaa käyttää varmennetta. Koska asiakasohjelman salauskoodi on aina tallennettava turvallisesti, sitä ei voi tuoda yhteysasetustiedostosta tai QR-koodista jäljempänä käsiteltävällä tavalla.

Varmenteita voidaan käyttää salauskoodeina, joilla voidaan todistaa sovelluksen käyttäjätiedot tunnusta pyydettäessä. Siinä missä varmenteen julkinen osa ladataan sovelluksen rekisteröintiin Azure-portaalissa, koko varmenne on otettava käyttöön jokaisessa laitteessa, johon varastosovellus on asennettu. Organisaatio vastaa varmenteen hallinnassa esimerkiksi kierron osalta. Itseallekirjoitettujen varmenteiden käyttö on mahdollista, mutta käyttävien varmenteiden on aina oltava ei-vietäviä.

Jokaisessa laitteessa, jossa varastosovellusta käytetään, on varmistettava, että varmenne on käytettävissä paikallisesti. Lisätietoja varmenteiden hallinnasta Intune-ohjatuissa laitteissa Intunea käytettäessä on kohdassa [Varmenteiden käyttö todennukseen Microsoft Intunessa](https://docs.microsoft.com/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Sovelluksen määrittäminen tuomalla yhteysasetukset

Sovellusten ylläpitoa ja käyttöönottoa useissa mobiililaitteissa helpottaa mahdollisuus tuoda yhteysasetuksen sen sijaan, että ne annettaisiin manuaalisesti jokaisessa laitteessa. Tässä osassa käsitellään asetusten luontia ja tuontia.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Yhteysasetustiedoston tai QR-koodin luominen

Yhteysasetukset voidaan tuoda joko tiedostona tai QR-koodina. Kummassakin tapauksessa on luotava ensin JSON (JavaScript Object Notation) -muotoa ja -syntaksia noudattava asetustiedosto. Tiedostossa on oltava yhteysluettelo, joka sisältää yksittäiset lisättävät yhteydet. Seuraavassa taulukossa on yhteenveto parametreista, jotka on määritettävä yhteysasetustiedostossa.

| Parametri | kuvaus |
| --- | --- |
| ConnectionName | Määritä yhteysasetuksen nimi. Enimmäispituus on 20 merkkiä. Koska tämä arvo on yhteysasetuksen yksilöivä tunniste, varmista, että se on ainoa kyseinen tunniste luettelossa. Jos laitteessa on jo saman niminen yhteys, tuodun tiedoston asetukset korvaavat sen. |
| ActiveDirectoryClientAppId | Määritä se asiakasohjelman tunnus, jonka kirjoitit muistiin määritettäessä Azure AD:tä kohdassa [Verkkopalvelusovelluksen luominen Azure Active Directoryssa](#create-service). |
| ActiveDirectoryResource | Määritä Supply Chain Managementin URL-pääosoite. |
| ActiveDirectoryTenant | Määritä Supply Chain Management -palvelimen kanssa käytettävä Azure AD -vuokraaja. Tämän arvon muoto on `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Esimerkki: `https://login.windows.net/contosooperations.onmicrosoft.com`. |
| Yritys  | Määritä Supply Chain Managementin yritys, johon sovellus halutaan yhdistää. |
| ConnectionType | (Valinnainen) Määritä, muodostaako yhteysasetus yhteyden ympäristöön varmenteen vai asiakasohjelman salauskoodin avulla. Kelvollisia arvoja ovat *"certificate"* ja *"clientsecret"*. Oletusarvo on *"certificate"*.<p>**Huomautus:** asiakasohjelman salauskoodeja ei voi tuoda.</p> |
| IsEditable | (Valinnainen) Määritä, saako sovelluksen käyttäjä muokata yhteysasetusta. Kelvolliset arvot ovat *true* ja *false*. Oletusarvo on *true*. |
| IsDefault | (Valinnainen) Määritä, onko yhteys oletusyhteys. Oletusyhteydeksi määritetty yhteys valitaan automaattisesti, kun sovellus avataan. Vain yksi yhteys voidaan määrittää oletusyhteydeksi. Kelvolliset arvot ovat *true* ja *false*. Oletusarvo on *false*. |
| CertificateThumbprint | (Valinnainen) Windows-laitteissa yhteydelle voi määrittää varmenteen allekirjoituksen. Android-laitteissa sovelluksen käyttäjän on valittava varmenne, kun yhteyttä käytetään ensimmäisen kerran. |

Seuraavassa esimerkissä on kaksi yhteyttä sisältävä kelvollinen yhteysasetustiedosto. Yhteysluettelo (jonka nimi tiedostossa on *"ConnectionList"*) on objekti, jonka taulukkoon kukin yhteys tallennetaan objektina. Kunkin objektin ympärillä on oltava aaltosulkeet ({}) ja ne on eroteltava pilkuilla. Lisäksi taulukko ympärillä on oltava hakasulkeet (\[\]).

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Voit tallentaa tiedot joko JSON-tiedostona tai luoda saman sisällön sisältävän QR-koodin. Jos tallennat tiedot tiedostona, se kannattaa tallentaa oletusnimellä *connections.json* etenkin siinä tapauksessa, että se tallennetaan oletussijaintiin kussakin mobiililaitteessa.

### <a name="save-the-connection-settings-file-on-each-device"></a>Yhteysasetustiedoston tallentaminen kuhunkin laitteeseen

Yleensä yhteysasetustiedostot jaetaan kuhunkin hallittavaan laitteeseen laitehallintatyökalun tai komentosarjan avulla. Jos oletusnimeä käyttävä yhteysasetustiedosto on tallennettu kussakin laitteessa oletussijaintiin, varastosovellus tuo sen automaattisesti myös silloin, kun sovellusta käytetään ensimmäisen kerran asennuksen jälkeen. Jos tiedostolla on mukautettu nimi tai se on tallennettu jonnekin muualle, sovelluksen käyttäjän on määritettävä nämä arvot ensimmäisellä käyttökerralla. Tämän jälkeen sovellus kuitenkin käyttää määritettyä nimeä ja sijaintia.

Sovellus tuo yhteysasetukset aiemmasta sijainnista aina, kun sovellus käynnistetään ja määrittää, onko tiedostoon tehty muutoksia. Sovellus päivittää vain yhteydet, joilla on sama nimi kuin yhteysasetustiedostossa olevilla yhteyksillä. Muita nimiä käyttäviä käyttäjän luomia yhteyksiä ei päivitetä.

Yhteyttä ei voi poistaa yhteysasetustiedoston avulla.

Kuten aiemmin mainittiin, yhteystiedoston nimi on *connections.json*. Tiedoston oletussijainti määräytyy sen perusteella, onko käytössä Windows- vai Android-laite:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`

Polut luodaan yleensä automaattisesti sovelluksen ensimmäisen käyttökerran jälkeen. Ne voidaan kuitenkin luoda manuaalisesti, jos yhteysasetustiedosto on siirrettävä laitteeseen ennen asennusta.

> [!NOTE]
> Jos sovelluksen asennut poistetaan, oletuspolku sisältöineen poistetaan.

### <a name="import-the-connection-settings"></a>Yhteysasetusten tuominen

Yhteysasetukset voidaan tuoda seuraavien ohjeiden mukaisesti tiedostosta tai QR-koodista.

1. Avaa varastosovellus mobiililaitteessa.
1. Valitse **Yhteysasetukset**.
1. Valitse **Käytä demotilaa** -vaihtoehdossa _Ei_.

    ![Käytä demotilaa -vaihtoehto](media/app-connect-app-demo-mode.png "Käytä demotilaa -vaihtoehto")

1. Valitse asetusten tuontitavan mukaan **Valitse tiedosto** tai **Lue QR-koodi**.

    - Jos yhteysasetukset tuodaan tiedostosta, sovellus on voinut jo löytää tiedoston, joka tiedostolla on oletusnimi ja se tallennettiin oletussijaintiin. Valitse muussa tapauksessa **Valitse tiedosto**, etsi tiedosto paikallisessa laitteessa ja valitse. Jos valitse mukautetun sijainnin, sovellus tallentaa sen ja käyttää sitä automaattisesti seuraavalla kerralla.
    - Jos yhteysasetukset tuodaan lukemalla QR-koodi, valitse **Lue QR-koodi**. Sovellus pyytää laitteen kameran käyttöoikeutta. Kun käyttöoikeus on myönnetty, kamera käynnistyy ja voit käyttää sitä lukemiseen. Laitteen kameran laadun ja QR-koodin monimutkaisuuden mukaan koodin lukeminen voi olla hankalaa. Vähennä siinä tapauksessa QR-koodin monimutkaisuutta luomalla kullekin QR-koodille vain yksi yhteys. (Tällä hetkellä QR-koodin voi lukea vain laitteen kameralla.)

    ![Yhteysasetusten tuominen](media/app-connect-app-select-file.png "Yhteysasetusten tuominen")

1. Kun yhteysasetukset on ladattu, valitse sivun vasemmassa yläkulmassa **Takaisin**-painike (nuoli vasemmalle).

    ![Ladatut yhteysasetukset](media/app-connect-app-settings-loaded.png "Ladatut yhteysasetukset")

1. Jos käytössä on Android-laite ja todennukseen käytetään varmennetta, laite pyytää valitsemaan varmenteen.

    ![Varmenteen valintakehote Android-laitteessa](media/app-connect-app-choose-cert.png "Varmenteen valintakehote Android-laitteessa")

1. Sovellus muodostaa yhteyden Supply Chain Management -palvelimeen ja avaa kirjautumissivun.

    ![Kirjautumissivu](media/app-connect-sign-in.png "Kirjautumissivu")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Sovelluksen määrittäminen manuaalisesti

Sovelluksen voi määrittää laitteessa manuaalisesti muodostamaan yhteyden Supply Chain Management -palvelimeen Azure AD -sovelluksen avulla.

1. Avaa varastosovellus mobiililaitteessa.
1. Valitse **Yhteysasetukset**.
1. Valitse **Käytä demotilaa** -vaihtoehdossa _Ei_.

    ![Käytöstä poistettu demotila](media/app-connect-app-select-file.png "Käytöstä poistettu demotila")

1. Laajenna **Valitse yhteys** -kenttää napauttamalla asetukset, jotka tarvitaan yhteyden tietojen antamiseen manuaalisesti.

    ![Manuaaliset yhteyskentät](media/app-connect-manual-connect.png "Manuaaliset yhteyskentät")

1. Kirjoita seuraavat tiedot:

    - **Käytä asiakasohjelman salauskoodi** – Valitse asetukseksi _Kyllä_, jos todennukseen Supply Chain Managementissa käytetään asiakasohjelman salauskoodia. Valitse _Ei_, jos todennukseen käytetään varmennetta. (Lisätietoja on kohdassa [Verkkosovelluksen luominen Azure Active Directoryssa](#create-service).)
    - **Yhteyden nimi** – Anna uudelleen yhteydelle nimi. Tämä nimi näkyy **Valitse yhteys** -kentässä, kun avaat yhteysasetukset seuraavan kerran. Annettavan nimen on oltava yksilöivä. (Se ei siis saa olla sama kuin jokin muu laitteeseen mahdollisesti tallennettu yhteyden nimi.)
    - **Active Directoryn asiakasohjelman tunnus** – anna se asiakasohjelman tunnus, jonka kirjoitit muistiin määritettäessä Azure AD:ä kohdassa [Verkkopalvelusovelluksen luominen Azure Active Directoryssa](#create-service).
    - **Active Directoryn asiakasohjelman salauskoodi** – Tämä kenttä on käytettävissä vain silloin, kun **Käytä asiakasohjelman tunnusta** -asetukseksi on valittu _Kyllä_. Anna se asiakasohjelman salauskoodi, jonka kirjoitit muistiin määritettäessä Azure AD:tä kohdassa [Verkkopalvelusovelluksen luominen Azure Active Directoryssa](#create-service).
    - **Active Directoryn varmenteen allekirjoitus** – Tämä kenttä on käytettävissä Windows-laitteissa vain silloin, kun **Käytä asiakasohjelman tunnusta** -asetukseksi on valittu _Ei_. Anna se varmenteen allekirjoitus, jonka kirjoitit muistiin määritettäessä Azure AD:tä kohdassa [Verkkopalvelusovelluksen luominen Azure Active Directoryssa](#create-service).
    - **Active Directoryn resurssi** – määritä Supply Chain Managementin URL-pääosoite.

        > [!NOTE]
        > Kauttaviiva (/) ei voi olla tämän arvon viimeinen merkki.

    - **Active Directory -vuokraaja** – Anna Azure AD -vuokraajaa, jota käytetään Supply Chain Management -palvelimen kanssa. Tämän arvon muoto on `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Esimerkki: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!NOTE]
        > Kauttaviiva (/) ei voi olla tämän arvon viimeinen merkki.

    - **Yritys** – Anna Supply Chain Managementin yritys, johon haluat muodostaa sovelluksella yhteyden.

1. Valitse sivun oikeassa yläkulmassa **Tallenna**-painike.
1. Jos käytössä on Android-laite ja todennukseen käytetään varmennetta, laite pyytää valitsemaan varmenteen.
1. Sovellus muodostaa yhteyden Supply Chain Management -palvelimeen ja avaa kirjautumissivun.

## <a name="remove-access-for-a-device"></a>Poista laitteen käyttöoikeudet

Jos laite katoaa tai vaarantuu, laitteen Supply Chain Managementin käyttöoikeus on poistettava. Käyttöoikeus kannattaa poistaa seuraavien ohjeiden mukaan:

1. Valitse **Järjestelmän hallinta \> Asetukset \> Azure Active Directory -sovellukset**.
1. Poista rivi, joka vastaa laitetta, jonka käyttöoikeuden haluat poistaa. Kirjoita muistiin poistettavan laitteen asiakasohjelman tunnus, sillä tätä tietoa tarvitaan myöhemmin.

    Jos rekisteröityjä asiakasohjelman tunnuksia on vain yksi ja useat laitteet käyttävät samaa tunnusta, kyseisille laitteille on lähetettävä uudet yhteysasetukset. Muussa tapauksessa ne menettävät käyttöoikeuden.

1. Kirjaudu Azure-portaalin osoitteessa [https://portal.azure.com](https://portal.azure.com/).
1. Valitse vasemmassa siirtymisruudussa **Active Directory** ja varmista, että olet oikeassa hakemistossa.
1. Valitse **Hallinta**-luettelossa ensin **Sovelluksen rekisteröinnit** ja sitten määritettävä sovellus. Määritystiedot sisältävä **Asetukset**-sivu avautuu.
1. Varmista, että sovelluksen asiakasohjelman tunnus vastaa vaiheessa 2 muistiin kirjoitettua asiakasohjelman tunnusta.
1. Valitse työkalurivillä **Poista**.
1. Valitse avautuvassa vahvistussanomassa **Kyllä**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]