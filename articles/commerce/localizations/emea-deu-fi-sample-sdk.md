---
title: Verorekisteröintipalvelun integroinnin esimerkkiä koskevat käyttöönoton ohjeet (Saksa) (vanha)
description: Tässä aiheessa on ohjeita Saksan verointegroinnin esimerkin käyttöönottamiseksi Microsoft Dynamics 365 Commerce Retail -ohjelmistokehityspaketista (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 51107731090b77e75a0e5a8c91b052d494b452e4
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944912"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Verorekisteröintipalvelun integroinnin esimerkkiä koskevat käyttöönoton ohjeet (Saksa) (vanha)

[!include [banner](../includes/banner.md)]

Tässä aiheessa on ohjeita, jotka koskevat Saksan verorekisteröintipalvelun integroinnin käyttöönottoa Microsoft Dynamics 365 Commerce Retail -ohjelmistokehityspaketista (SDK) kehittäjän virtuaalitietokoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja verointegroinnin esimerkistä on kohdassa [Verorekisteröintipalvelun integroinnin esimerkki (Saksa)](emea-deu-fi-sample.md). 

Saksan verointegraation esimerkki kuuluu Retail SDK -pakettiin. Lisätietoja SDK:n asentamisesta ja käytöstä on kohdassa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md). Tämä esimerkki koostuu Commerce runtime (CRT)- ja Hardware Station -laajennusosista. Voit suorittaa tämän näyteversion muokkaamalla ja rakentamalla CRT- ja Hardware Station -projektit. Suosittelemme, että teet tässä aiheessa kuvatut muutokset käyttämällä Retail SDK -pakettia, jota ei ole muutettu. On myös suositeltavaa käyttää lähteenhallintajärjestelmää, kuten Azure DevOpsia, jossa tiedostoja ei ole vielä muutettu.

## <a name="development-environment"></a>Kehitysympäristö

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa näytettä.

### <a name="enable-commerce-runtime-extensions"></a>Commerce Runtime -laajennusten käyttöönotto

CRT -laajennuskomponentit sisältyvät CRT-näytteisiin. Voit suorittaa seuraavat vaiheet avaamalla **CommerceRuntimeSamples.sln**-ratkaisun kohdassa **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample-komponentti

1. Etsi **Runtime.Extensions.DocumentProvider.EFRSample**-projekti ja luo se.
2. Etsi **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Commerce Scale Unit:** Kopioi tiedosto **\\bin\\ext**-kansioon Internet Information Services (IIS) Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi tiedosto **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Commerce Scale Unit:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR-komponentti

1. Etsi **Runtime.Extensions.DocumentProvider.DataModelEFR**-projekti ja luo se.
2. Etsi **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Commerce Scale Unit:** Kopioi tiedosto **\\bin\\ext**-kansioon Internet IIS Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi tiedosto **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Commerce Scale Unit:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Laajennuksen määritystiedosto

1. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Commerce Scale Unit:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

2. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-hardware-station-extensions"></a>Ota käyttöön Hardware station -laajennukset

Hardware station -laajennuskomponentit sisältyvät Hardware station -esimerkkeihin. Voit suorittaa seuraavat vaiheet avaamalla **HardwareStationSamples.sln**-ratkaisun kohdassa **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="efrsample-component"></a>EFRSample-komponentti

1. Etsi **HardwareStation.Extension.EFRSample**-projekti ja luo se.
2. Etsi **Extension.EFRSample\\bin\\Debug** -kansiosta seuraavat kokoonpanotiedostot:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopioi kokoonpanotiedostot Hardware station -laajennuskansioon:

    - **Jaettu Hardware station:** Kopioi tiedostot **bin**-kansioon IIS Hardware station -sivuston sijainnissa.
    - **Erillinen Hardware station Modern POS -sovelluksessa:** Kopioi tiedostot Modern POS -asiakasvälittäjän sijaintiin.

4. Etsi Hardware station -laajennusten laajennuskonfiguraatiotiedosto. Tiedoston nimi on **HardwareStation.Extension.config**.

    - **Jaettu Hardware station:** Tiedosto on IIS Hardware station -sivuston sijainnissa.
    - **Erillinen Hardware station Modern POS -sovelluksessa:** Tiedosto on Modern POS -asiakasvälittäjän sijainnissa.

5. Lisää seuraava rivi konfigurointitiedoston **composition**-osaan.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="production-environment"></a>Tuotantoympäristö

Edellisessä menettelyssä on otettu käyttöön laajennukset, jotka ovat kirjanpidon rekisteröinnin palvelun integrointiesimerkin komponentteja. Luo lisäksi Commerce-komponentteja sisältävät käyttöön otettavat paketit ja ota paketit käyttöön tuotantoympäristössä noudattamalla näitä ohjeita.

1. Tee seuraavat muutokset **RetailSdk\\Assets**-kansion paketin konfiguraatiotiedostoihin:

    - Lisää **commerceruntime.ext.config**- ja **CommerceRuntime.MPOSOffline.Ext.config**-määritystiedostoihin seuraavat rivit **composition**-osaan.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - Lisää **HardwareStation.Extension.config** -määritystiedostossa seuraavat rivit **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Tee seuraavat muutokset **Customization.settings**-paketin mukautusmääritystiedostoon **BuildTools**-kansiossa:

    - Lisää seuraavat rivit, jos haluat sisällyttää CRT-laajennukset käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Lisää seuraavat rivit, jos haluat sisällyttää Hardware station -laajennukset käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Käynnistä Visual Studion MSBuild Command Prompt -työkalu ja luo käyttöön otettavat paketit suorittamalla **msbuild** Retail SDK -kansiossa.
4. Ota paketit käyttöön LCS:n kautta tai manuaalisesti. Lisätietoja on ohjeaiheessa [Käyttöönottopakettien luominen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Suorita kaikki tarvittavat asetustehtävät, jotka on kuvattu kohdassa [Commercen määritys (Saksa)](emea-deu-fi-sample.md#set-up-commerce-for-germany).

## <a name="design-of-extensions"></a>Laajennusten rakenne

Saksan verorekisteröintipalvelun integraatioesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md). Lisätietoja kirjanpidon integroinnin ratkaisun rakenteesta on kohdassa [Kirjanpidon integrointiesimerkin rakenteen yleiskatsaus](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime -laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda palvelukohtaisia asiakirjoja ja käsitellä verorekisteröintipalvelun vastauksia.

CRT-laajennus on **Runtime.Extensions.DocumentProvider.EFRSample**. Lisätietoja kirjanpidon integroinnin ratkaisun rakenteesta on kohdassa [Commerce-kanavan kirjanpidon integroinnin yleiskatsaus](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

#### <a name="request-handler"></a>Pyyntökäsittelijä

Asiakirjapalvelua varten on yksi pyynnön käsittelijä, **DocumentProviderEFRFiscalDEU**. Tämän käsittelijän avulla luodaan veroasiakirjoja verorekisteröintipalvelua varten. Se on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä kirjanpidon rekisteröintipalveluun.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Tämä pyyntö palauttaa vastauksen yhdessä laajennettujen tietojen kanssa.

#### <a name="configuration"></a>Konfigurointi

**DocumentProviderFiscalEFRSampleGermany**-konfigurointitiedosto sijaitsee laajennusprojektin **Configuration**-kansiossa. Tämän tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla tiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

Seuraavat asetukset lisätään:

- **ALV-prosenttimääritys** – Arvonlisäverokoodeille määritettyjen veroprosenttiarvojen yhdistäminen **TaxG** (veroryhmä) -määritteeseen pyynnöissä, jotka lähetetään veropalveluun.
- **Lahjakorttien ja talletusten veroryhmä** – **TaxG**-määritteen arvo veropalvelulle lähetetyissä pyynnöissä. Arvo perustuu toimintoihin, joihin liittyy lahjakortteja tai talletuksia.
- **Maksuvälinetyypin määritys** – Maksutapojen määritys **PayG** (maksuryhmä) -määritteen arvoihin pyynnöissä, jotka lähetetään kirjanpitopalveluun.
- **ALV-vapautuksen veroryhmä** – Veropalveluun lähetettyjen pyyntöjen **TaxG**-määritteen arvo. Arvo perustuu toimintoihin, jotka eivät ole verovelvollisia.
- **Sisällytä asiakastiedot** – Jos tämä parametri on käytössä, veropalvelupyynnöt sisältävät asiakastietoja, kuten nimiä ja osoitteita, jos asiakas lisätään tapahtumaan.

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verorekisteröintipalvelun kanssa.

Hardware station -laajennus on **HardwareStation.Extension.EFRSample**. Se käyttää HTTP-protokollaa asiakirjojen lähettämiseen, jotka CRT-laajennus luo kirjanpidon rekisteröintipalveluun. Se käsittelee myös verorekisteröintipalvelusta saadut vastaukset.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**EFRHandler**-pyyntökäsittelijä on kirjanpidon rekisteröintipalvelun pyyntöjen käsittelyn aloituspiste. Tämä käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä:

- **SubmitDocumentFiscalDeviceRequest** – Tämä pyyntö lähettää asiakirjoja kirjanpidon rekisteröintipalveluun ja palauttaa vastauksen pyyntöön.
- **IsReadyFiscalDeviceRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun kunnon tarkastusta varten.
- **InitializeFiscalDeviceRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun alustamiseen.

#### <a name="configuration"></a>Konfigurointi

Konfigurointitiedosto sijaitsee laajennusprojektin **Configuration**-kansiossa. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla veroyhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

Seuraavat asetukset lisätään:

- **Päätepisteen osoite** – verorekisteröintipalvelun URL-osoite.
- **Aikakatkaisu** – Aika millisekunteina (ms), jonka ajuri odottaa verorekisteröintipalvelun vastausta.
- **Näytä verorekisteröinti-ilmoitukset** – Jos tämä parametri on käytössä, veropalvelun ilmoitukset näytetään myyntipisteessä käyttäjän sanomina.
