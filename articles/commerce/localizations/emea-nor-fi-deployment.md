---
title: Käyttöönotto-ohjeet Norjan kassakoneille
description: Tässä artikkelissa on ohjeita kassan käyttötoimintojen käyttöönottamisesta Norjan Microsoft Dynamics 365 Commerce -lokalisointia varten.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 0e66ef93e65fecaca23f0434c386507a0672d251
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631312"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Käyttöönotto-ohjeet Norjan kassakoneille

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Ota tässä artikkelissa kuvatut vaiheet käyttöön vain, jos käytössä on Microsoft Dynamics 365 Commercen versio 10.0.29 tai uudempi versio. Commercen versiossa 10.0.28 ja aiemmissa versioissa on käytettävä Retail SDK:n edellistä versiota kehittäjän virtuaalikoneessa Microsoft Dynamics Lifecycle Servicesissa (LCS). Lisätietoja: [Kassakoneiden käyttöönotto-ohjeet (Norja) (vanha)](./emea-nor-loc-deployment-guidelines.md). Jos käytössä on Commercen versio 10.0.28 tai aiempi versio ja olet siirtymässä Commercen versioon 10.0.29 tai uudempaan versioon, noudata [Siirtyminen Norjan vanhoista Commerce-toiminnoista](./emea-nor-fi-migration.md) -kohdan ohjeita.

Tässä artikkelissa on ohjeita kassan käyttötoimintojen käyttöönottamisesta Norjan Commerce-lokalisointia varten. Lokalisointi sisältää useita osalaajennuksia, joiden avulla voit esimerkiksi tulostaa mukautettuja kenttiä kuitteihin, rekisteröidä muita kirjaustapahtumia, myyntitapahtumia ja maksutapahtumia myyntipisteessä (POS), allekirjoittaa myyntitapahtumia digitaalisesti sekä tulostaa raportteja paikallisissa muodoissa. Lisätietoja Norjan lokalisoinnista on kohdassa [Kassakoneen toiminnot, Norja](./emea-nor-cash-registers.md). Lisätietoja Commercen määrittämisestä Norjassa on kohdassa [Commercen määrittäminen (Norja)](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

## <a name="set-up-fiscal-registration-for-norway"></a>Kirjanpidon rekisteröinnin määrittäminen (Norja)

Norjan verorekisteröinnin esimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Commerce SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\SequentialSignatureNorway** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. [Esimerkki](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) koostuu veroasiakirjan tarjoajasta ja veroliittimestä, jotka ovat Commerce Runtimen (CRT) laajennuksia. Lisätietoja Commerce SDK:n käyttämisestä on kohdissa [Commerce SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja  NuGetista](../dev-itpro/retail-sdk/sdk-github.md) ja [Koontijakson asetusten määrittäminen riippumattoman pakkauksen SDK:ta varten](../dev-itpro/build-pipeline.md).

Suorita verorekisteröinnin määritysvaiheet [Commerce-kanavien kirjanpidon integroinnin määrittäminen](./setting-up-fiscal-integration-for-retail-channel.md) -kohdassa kuvatulla tavalla:

1. [Kirjanpidon rekisteröintiprosessin määrittäminen](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Muista ottaa huomioon [Norjan maakohtaisen](#configure-the-fiscal-registration-process) verorekisteröintiprosessin asetukset.
1. [Virheen käsittelyasetusten määrittäminen](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Lykätyn kirjanpidon rekisteröinnin manuaalisen suorituksen käyttöönotto](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Määritä kanavakomponentit](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Verorekisteröintiprosessin konfiguroiminen

Voit ottaa Norjan verorekisteröintiprosessin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.

1. Lataa kirjanpidon yhdistimien ja kirjanpitoasiakirjan toimittajien määritystiedostot Commerce SDK:sta:

    1. Avaa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilö.
    1. Avaa viimeinen käytettävissä oleva julkaisuhaara.
    1. Avaa **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Lataa veroasiakirjan tarjoajan määritystiedosto kohdassa **DocumentProvider.SequentialSignNorway \> Määritys \> DocumentProviderSequentialSignatureNorwaySample.xml**.
    1. Lataa veroliittimen määritysasiakirja kohdassa **Connector.SequentialSignNorway \> Määritys \> ConnectorSequentialSignatureNorwaySample.xml**.

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

#### <a name="development-environment"></a>Kehitysympäristö

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa näytettä.

1. Kloonaa tai lataa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilö. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan. Lisätietoja: [Commerce SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja NuGetista](../dev-itpro/retail-sdk/sdk-github.md).
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

#### <a name="production-environment"></a>Tuotantoympäristö

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
