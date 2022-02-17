---
title: Käyttöönotto-ohjeet Norjan kassakoneille
description: Tässä aiheessa on ohjeita kassan käyttötoimintojen käyttöönottamisesta Norjan Microsoft Dynamics 365 Commerce -lokalisointia varten.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: f0744b18ed59c692ae336c92e488d339ae158368
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077137"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Käyttöönotto-ohjeet Norjan kassakoneille

[!include[banner](../includes/banner.md)]

Tässä aiheessa on ohjeita kassan käyttötoimintojen käyttöönottamisesta Norjan Microsoft Dynamics 365 Commerce -lokalisointia varten. Lokalisointiin kuuluu useita komponenttien laajennuksia. Näiden laajennusten avulla voit esimerkiksi tulostaa mukautettuja kenttiä kuitteihin, rekisteröidä muita kirjaustapahtumia, myyntitapahtumia ja maksutapahtumia myyntipisteessä (POS), allekirjoittaa myyntitapahtumia digitaalisesti sekä tulostaa raportteja paikallisissa muodoissa. Lisätietoja Norjan lokalisoinnista on kohdassa [Kassakoneen toiminnot, Norja](./emea-nor-cash-registers.md). Lisätietoja Commercen määrittämisestä Norjassa on kohdassa [Commercen määrittäminen (Norja)](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä lokalisointitoiminnallisuudessa. Sinun on käytettävä Norjan digitaalisten allekirjoitusten esimerkkiversiota Retail-ohjelmiston kehityssarjan (SDK) aiemmassa versiossa kehittäjän virtuaalikoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja: [Kassakoneiden käyttöönotto-ohjeet (Norja) (vanha)](./emea-nor-loc-deployment-guidelines.md).
>
> Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

## <a name="set-up-fiscal-registration-for-norway"></a>Kirjanpidon rekisteröinnin määrittäminen (Norja)

Norjan verorekisteröinnin esimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Retail SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\SequentialSignatureNorway** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä (esim. [julkaisun 9.34 esimerkki](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)). Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta ja veroliittimestä, jotka ovat Commerce Runtimen (CRT) laajennuksia. Lisätietoja Retail SDK:n käytöstä on kohdissa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Määritä itsenäisen pakkaus-SDK:n koontiversioputki](../dev-itpro/build-pipeline.md).

Suorita verorekisteröinnin määritysvaiheet [Commerce-kanavien kirjanpidon integroinnin määrittäminen](./setting-up-fiscal-integration-for-retail-channel.md) -kohdassa kuvatulla tavalla:

1. [Kirjanpidon rekisteröintiprosessin määrittäminen](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Muista ottaa huomioon [Norjan maakohtaisen](#configure-the-fiscal-registration-process) verorekisteröintiprosessin asetukset.
1. [Virheen käsittelyasetusten määrittäminen](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Ota käyttöön lykätyn tilikausirekisteröinnin manuaalinen käyttö](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Määritä kanavakomponentit](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Verorekisteröintiprosessin konfiguroiminen

Voit ottaa Norjan verorekisteröintiprosessin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.

1. Lataa kirjanpidon yhdistimien ja kirjanpitoasiakirjan toimittajien määritystiedostot Commerce SDK:sta:

    1. Avaa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilö.
    1. Avaa viimeinen käytettävissä oleva julkaisuhaara (esim. **[julkaisu 9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. Avaa **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Lataa veroasiakirjan tarjoajan konfigurointitiedosto kohdasta **DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSignatureNorwaySample.xml** (esim. [julkaisun 9.34 tiedosto](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)).
    1. Lataa veroliittimen konfiguraatiotiedosto kohdasta **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml** (esim. [julkaisun 9.34 tiedosto](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)).

1. Valitse **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Jaetut parametrit**. Määritä **Yleiset**-pikavälilehdessä **Ota kirjanpidon integrointi käyttöön**-asetukseksi **Kyllä**.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistimet**, ja lataa aiemmin lataamasi kirjanpidon yhdistimen konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpitoasiakirjan toimittajat**, ja lataa aiemmin lataamasi kirjanpitoasiakirjan toimittajan konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen toiminnalliset profiilit**. Luo uusi liittimen toiminnallinen profiili ja valitse aiemmin ladattu asiakirjan toimittaja ja veroliitin.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen tekniset profiilit**. Luo uusi liittimen tekninen profiili ja valitse aiemmin ladattu liitin. Määritä liittimen tyypiksi **Sisäinen**.
1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmät** ja luo uusi kirjanpidon yhdistinryhmä aiemmin luodulle yhdistimen toiminnalliselle profiilille.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**. Luo uusi kirjanpidon rekisteröintiprosessi ja verorekisteröintiprosessi vaihe ja valitse aiemmin luomasi kirjanpidon yhdistinryhmä.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**. Valitse siihen myymälään linkitetty toimintoprofiili, jossa rekisteröintiprosessi tulee aktivoida. Valitse **Kirjanpidon rekisteröintiprosessi** -pikavälilehdessä aiemmin luomasi kirjanpidon rekisteröintiprosessi. Valitse **Kirjanpidon palvelut** -pikavälilehdessä aiemmin luomasi liittimen tekninen profiili. 
1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**. Avaa jakeluaikataulu ja valitse työt **1070** ja **1090** siirtääksesi tiedot kanavatietokantaan.

### <a name="configure-the-digital-signature-parameters"></a>Digitaalisten allekirjoitusten parametrien konfiguroiminen

Ne sertifikaatit on määritettävä, joita käytetään myymälän myyntitapahtumien allekirjoittamiseen digitaalisesti. Allekirjoitusta varten käytetään Azure Key Vaultiin tallennettua digitaalista sertifikaattia. Modern POS -sovelluksen offline-tilaa varten allekirjoitus voidaan tehdä myös käyttäen digitaalista sertifikaattia, joka on tallennettu sen laitteen paikalliseen tallennustilaan, johon Modern POS on asennettu.

Seuraavat vaiheet on suoritettava, ennen kuin voit käyttää Key Vaultiin tallennettua digitaalista sertifikaattia.

1. Key Vault -tallennustila on luotava. On suositeltavaa käyttöönottaa tallennustila samalla maantieteellisellä alueella kuin Commerce Scale Unit.
1. Sertifikaatti on ladattava avaimen Key Vault -tallennustilaan base64-merkkijonomuotoisena salaisuutena.
1. Application Object Server (AOS) -sovelluksella on oltava valtuudet lukea salaisuuksia Key Vault -tallennustilasta.

Lisätietoja Key Vaultin käyttämisestä: [Azure Key Vaultin käytön aloittaminen](/azure/key-vault/key-vault-get-started).

Seuraavaksi **Key Vault -parametrit** -sivulla on määritettävä Key Vault -tallennustilan käytön parametrit:

- **Nimi** ja **Kuvaus** –Key Vault -tallennustilan nimi ja kuvaus.
- **Key Vault URL** – Key Vault -tallennustilan URL-osoite.
- **Key Vault -asiakasohjelma** - Key Vault -tallennustilaan liittyvän Azure Active Directory (Azure AD) -sovelluksen vuorovaikutteinen asiakastunnus todennusta varten. Asiakasohjelman tulisi pysytä lukea salaisuuksia tallennustilasta.
- **Key Vaultin salainen avain** – Azure AD -sovellukseen liittyvä salainen avain, jota käytetään Key Vault -tallennustilan todennusta varten.
- **Nimi**, **Kuvaus** ja **Salainen viite** – Sertifikaatin nimi, kuvaus ja salainen viittaus.

Seuraavaksi sinun on konfiguroitava niiden sertifikaattien liitin, jotka on tallennettu Key Vault -tallennustilaan tai paikalliseen sertifikaattivarastoon. Tätä liitintä käytetään kanavan puolella allekirjoitettaessa.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen tekniset profiilit**.
1. Määritä **Asetukset**-pikavälilehdessä seuraavat digitaalisten allekirjoitusten parametrit:

    - **Salainen nimi** – Voit valita aiemmin **Key Vault -parametrit** -sivulla konfiguroidun salaisen nimen.
    - **Paikallinen sertifikaatin allekirjoitus** – Anna sertifikaattia varten allekirjoitus, joka on tallennettu paikallisesti.
    - **Hash-algoritmi** – Määritä yksi Microsoft .NET:n tukemista kryptografisista hash-algoritmeista, kuten **SHA1**.
    - **Sertifikaattisäilön nimi** – Tämä kenttä on valinnainen. Määritä sen avulla oletusmyymälän nimi, jolla haetaan paikallisia varmenteita.
    - **Sertifikaattisäilön sijainti** – Tämä kenttä on valinnainen. Määritä sen avulla oletusmyymälän sijainti, jolla haetaan paikallisia varmenteita.
    - **Yritä ensin paikallista sertifikaattia** – Valitse tämä vaihtoehto, kun haluat oletusarvoisesti käyttää tietojen allekirjoittamiseen paikallisen myymälän sertifikaattia Key Vault -sertifikaatin asemesta.
    - **Aktivoi kuntotarkistus** – Saat lisätietoja kuntotarkastustoiminnosta kohdasta [Tilikausirekisteröinnin kuntotarkastus](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Vain kryptografinen hash-algoritmi **SHA1** on tällä hetkellä käytettävissä Norjassa.
> - Oletusmyymälän nimi ja sijainti lisätään yksinkertaistamaan paikallisten varmenteiden hakuprosessia CRT-palvelussa. X509StoreProvider sisältää kansioluettelon, johon varmenteen tallennetaan. Jos oletusmyymälän nimeä ja sijaintia ei ole määritetty, X509StoreProvider yrittää löytää varmenteen luettelon kaikista kansioista.

### <a name="configure-channel-components"></a>Määritä kanavakomponentit

### <a name="development-environment"></a>Kehitysympäristö

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa näytettä.

1. Kloonaa tai lataa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilö. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan. Lisätietoja: [Retail SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja NuGetista](../dev-itpro/retail-sdk/sdk-github.md).
1. Avaa **SequentialSignatureNorway.sln** -ratkaisu kohdassa **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway** ja muodosta se.
1. Asenna CRT-laajennukset:

    1. Etsi CRT-laajennuksen asennusohjelma:

        - **Commerce Scale Unit:** Etsi **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461** -kansiosta **ScaleUnit.SequentialSignNorway.Installer**-asennusohjelma.
        - **Paikallinen CRT Modern POS -sovelluksessa:** Etsi **SequentialSignatureNorway\\ModernPOS\\ModernPos.SequentialSignNorway.Installer\\bin\\Debug\\net461**-kansiosta **ModernPos.SequentialSignNorway.Installer**-asennusohjelma.

    1. Käynnistä CRT-laajennusten asennusohjelma komentoriviltä:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Paikallinen CRT Modern POS -sovelluksessa:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Tuotantoympäristö

Luo ja julkaise verointegraatioesimerkin Cloud Scale Unit ja itsepalveluna käyttöönotettavat paketit noudattamalla [Määritä koontijakso verointegraatioesimerkille](fiscal-integration-sample-build-pipeline.md) -ohjeen vaiheita. **SequentialSignatureNorway build-pipeline.yaml**-niminen YAML-mallitiedosto löytyy **Pipeline\\YAML_Files** -kansiosta[Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilöstä.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Ota digitaalinen allekirjoitus käyttöön offline-tilassa Modern POS -sovelluksessa

Jos haluat ottaa digitaalisten allekirjoituksen käyttöön offline-tilassa Modern POS -sovellusta varten, noudata näitä ohjeita, kun olet aktivoinut Modern POS:n uudella laitteella.

1. Kirjaudu sisään POS:ään.
1. Varmista **Tietokantayhteyden tila** -sivulla, että offline-tietokanta on täysin synkronoitu. Kun **Odottavat lataukset** kentän arvo on **0** (nolla), tietokanta on täysin synkronoitu.
1. Kirjaudu ulos myyntipisteestä.
1. Odota, kunnes offline-tietokanta synkronoidaan täysin.
1. Kirjaudu sisään POS:ään.
1. Varmista **Tietokantayhteyden tila** -sivulla, että offline-tietokanta on täysin synkronoitu. Kun **Offline-tietokannan odottavat tapahtumat** kentän arvo on **0** (nolla), tietokanta on täysin synkronoitu.
1. Avaa Modern POS uudelleen.
