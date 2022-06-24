---
title: Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Italia) (vanha)
description: Tässä artikkelissa on ohjeita Italian verotulostimen integroinnin esimerkin käyttöönottamiseksi Microsoft Dynamics 365 Commerce Retail -ohjelmistokehityspaketista (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: bb07ca91c9e5bf1a79f672f9ba29b7bcc21688c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848895"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Italia) (vanha)

[!include[banner](../includes/banner.md)]

Tässä artikkelissa on ohjeita, jotka koskevat Italian verotulostimen integrointiesimerkin käyttöönottoa Microsoft Dynamics 365 Commerce Retail -ohjelmistokehityspaketista (SDK) kehittäjän virtuaalitietokoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja verointegroinnin esimerkistä on kohdassa [Verotulostimen integroinnin esimerkki (Italia)](emea-ita-fpi-sample.md). 

Italian verointegraation esimerkki kuuluu Retail SDK -pakettiin. Lisätietoja SDK:n asentamisesta ja käytöstä on kohdassa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md). Tämä esimerkki koostuu Commerce runtime (CRT)- ja Hardware Station -laajennusosista. Voit suorittaa tämän näyteversion muokkaamalla ja rakentamalla CRT- ja Hardware Station -projektit. Suosittelemme, että teet tässä artikkelissa kuvatut muutokset käyttämällä Retail SDK -pakettia, jota ei ole muutettu. On myös suositeltavaa käyttää lähteenhallintajärjestelmää, kuten Azure DevOpsia, jossa tiedostoja ei ole vielä muutettu.

## <a name="development-environment"></a>Kehitysympäristö

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa näytettä.

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime -laajennusten komponentit

CRT-laajennuskomponentit sisältyvät Retail SDK -pakettiin. Voit suorittaa seuraavat vaiheet avaamalla **CommerceRuntimeSamples.sln**-ratkaisun kohdassa **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Etsi **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**-projekti ja luo se.
2. Etsi **Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Commerce Scale Unit:** Kopioi tiedosto **\\bin\\ext**-kansioon Internet Information Services (IIS) Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi tiedosto **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Commerce Scale Unit:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Käynnistä Commerce Scale Unit uudelleen:

    - **Commerce Scale Unit:** Käynnistä Commerce Scale Unit -sivusto uudelleen IIS Managerissa.
    - **Asiakkaan välittäjä:** Lopeta **dllhost.exe**-prosessi Task Managerissa ja käynnistä sen jälkeen Modern POS uudelleen.

### <a name="hardware-station-extension-components"></a>Hardware station -laajennuksen komponentit

Hardware station -laajennuskomponentit sisältyvät Retail SDK -pakettiin. Voit suorittaa seuraavat vaiheet avaamalla **HardwareStationSamples.sln**-ratkaisun kohdassa **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Etsi **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** -projekti ja luo se.
2. Etsi **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** -kansiosta **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto käyttöönotettuun Hardware station -koneeseen:

    - **Remote Hardware station:** Kopioi tiedosto **bin**-kansioon IIS Hardware station -sivuston sijainnissa.
    - **Paikallinen Hardware station:** Kopioi tiedosto Modern POS -asiakasvälittäjän sijaintiin.

4. Etsi Hardware station -laajennusten konfiguraatiotiedosto. Tiedoston nimi on **HardwareStation.Extension.config**:

    - **Remote Hardware station:** Tiedosto on IIS Hardware station -sivuston sijainnissa.
    - **Paikallinen Hardware station:** Tiedosto on Modern POS -asiakasvälittäjän sijainnissa.

5. Lisää seuraava osa konfigurointitiedoston **composition**-osaan.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Käynnistä Hardware station -palvelu uudelleen:

    - **Remote Hardware station:** Käynnistä Hardware station -sivusto uudelleen IIS Managerissa.
    - **Paikallinen Hardware station:** Lopeta **dllhost.exe**-prosessi Task Managerissa ja käynnistä sen jälkeen Modern POS uudelleen.

## <a name="production-environment"></a>Tuotantoympäristö

Luo Commerce-komponentteja sisältävät käyttöön otettavat paketit ja ota paketit käyttöön tuotantoympäristössä noudattamalla näitä ohjeita.

1. Noudata tässä artikkelissa aiemmin [Kehitysympäristö](#development-environment)-kohdassa kuvattuja vaiheita.
2. Tee seuraavat muutokset **RetailSdk\\Assets**-kansion paketin konfiguraatiotiedostoihin:

    1. Lisää **commerceruntime.ext.config**- ja **CommerceRuntime.MPOSOffline.Ext.config**-määritystiedostoihin seuraavaa rivi **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. Lisää **HardwareStation.Extension.config** -määritystiedostossa seuraava rivi **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Tee seuraavat muutokset **Customization.settings**-paketin mukautusmääritystiedostoon **BuildTools**-kansiossa:

    1. Lisää seuraava rivi, jos haluat sisällyttää CRT-laajennuksen käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Lisää seuraava rivi, jos haluat sisällyttää Hardware station -laajennuksen käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Tee seuraavat muutokset **Sdk.ModernPos.Shared.csproj**-tiedostoon **Packages\_SharedPackagingProjectComponents**-kansiossa sisällyttääksesi Italian resurssitiedostot käyttöönotettaviin paketteihin:

    1. Lisää **Nimikeryhmä**-osa, joka sisältää haluttujen käännösten resurssitiedostoihin viittaavat solmut. Varmista, että määrität oikeat nimitilat ja esimerkkinimet. Seuraavassa esimerkissä lisätään resurssisolmuja **it**- ja **it-CH**-kielialueille.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Lisää **Target Name="CopyPackageFiles"** -osaan yksi rivi kullekin kielialueelle seuraavan esimerkin mukaisesti.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. Tee seuraavat muutokset **Sdk.RetailServerSetup.proj**-tiedostoon **Packages\_SharedPackagingProjectComponents**-kansiossa sisällyttääksesi Italian resurssitiedostot käyttöönotettaviin paketteihin:

    1. Lisää **Nimikeryhmä**-osa, joka sisältää haluttujen käännösten resurssitiedostoihin viittaavat solmut. Varmista, että määrität oikeat nimitilat ja esimerkkinimet. Seuraavassa esimerkissä lisätään resurssisolmuja **it**- ja **it-CH**-kielialueille.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Lisää **Target Name="CopyPackageFiles"** -osaan yksi rivi kullekin kielialueelle seuraavan esimerkin mukaisesti.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Käynnistä Visual Studion MSBuild Command Prompt -työkalu ja luo käyttöön otettavat paketit suorittamalla **msbuild** Retail SDK -kansiossa.
7. Ota paketit käyttöön LCS:n kautta tai manuaalisesti. Lisätietoja on ohjeaiheessa [Käyttöönottopakettien luominen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Laajennusten rakenne

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime -laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda tulostinkohtaisia asiakirjoja ja käsitellä verotulostimen vastauksia.

CRT-laajennus on **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Lisätietoja kirjanpidon integroinnin rakenteesta on kohdassa [Kirjanpidon rekisteröintiprosessi ja kirjanpidon laitteiden ja palveluiden kirjanpidon integrointimallit](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Pyyntökäsittelijä

**DocumentProviderEpsonFP90III**-pyyntökäsittelijä on asiakirjan luontipyynnön aloituspiste verotulostimelle.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa tulostinkohtaisen asiakirjan, jotka on rekisteröitävä verotulostimeen.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Tällä hetkellä seuraavat tapahtumat ovat tuettuja: myynti, X-raportin tulostaminen ja Z-raportin tulostaminen.

#### <a name="configuration"></a>Konfigurointi

Konfigurointitiedosto sijaitsee laajennusprojektin **Configuration**-kansiossa. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla tiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- ALV-koodien yhdistäminen
- ALV-prosenttien yhdistäminen
- Maksuvälinetyyppien yhdistäminen
- Kuittinumeron viivakoodityyppi
- Talletuksen maksutyyppi

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verotulostimen kanssa.

Hardware station -laajennus on **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Tämä laajennus käyttää HTTP-protokollaa asiakirjojen lähettämiseen, jotka CRT-laajennus luo verotulostimeen. Se käsittelee myös verotulostimesta saadut vastaukset.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**EpsonFP90IIISample**-pyyntökäsittelijä on oheislaitteen pyyntöjen käsittelyn aloituspiste.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä:

- **SubmitDocumentFiscalDeviceRequest** – Tämä pyyntö lähettää asiakirjoja tulostimille ja palauttaa vastauksen verotulostimesta.
- **IsReadyFiscalDeviceRequest** – Tätä pyyntöä käytetään laitteen kunnon tarkastusta varten.
- **InitializeFiscalDeviceRequest** – Tätä pyyntöä käytetään tulostimen alustamiseen.

#### <a name="configuration"></a>Konfigurointi

Konfigurointitiedosto sijaitsee laajennusprojektin **Configuration**-kansiossa. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla yhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- **Päätepisteen osoite** – Tulostimen URL-osoite.
- **Päivämäärän ja ajan synkronointi** – Arvo, joka määrittää, synkronoidaanko tulostimen päivämäärä ja aika liitetyn Hardware stationin kanssa.
