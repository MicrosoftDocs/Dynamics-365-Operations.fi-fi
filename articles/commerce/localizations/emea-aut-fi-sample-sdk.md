---
title: Verorekisteröintipalvelun integroinnin esimerkkiä koskevat käyttöönoton ohjeet (Itävalta) (vanha)
description: Tässä artikkelissa on ohjeita Itävallan verointegroinnin esimerkin käyttöönottamiseksi Microsoft Dynamics 365 Commerce Retail -ohjelmistokehityspaketista (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 203904f60888464a473cb2997652db497fba6f57
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276098"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Verorekisteröintipalvelun integroinnin esimerkkiä koskevat käyttöönoton ohjeet (Itävalta) (vanha)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on ohjeita, jotka koskevat Itävallan verorekisteröintipalvelun integroinnin käyttöönottoa Microsoft Dynamics 365 Commerce Retail -ohjelmistokehityspaketista (SDK) kehittäjän virtuaalitietokoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja verointegroinnin esimerkistä on kohdassa [Verorekisteröintipalvelun integroinnin esimerkki (Itävalta)](emea-aut-fi-sample.md). 

Itävallan verointegraation esimerkki kuuluu Retail SDK -pakettiin. Lisätietoja SDK:n asentamisesta ja käytöstä on kohdassa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md). Verointegraation esimerkki koostuu Commerce runtime (CRT)-, Hardware Station- ja myyntipiste (POS) -laajennusosista. Voit suorittaa tämän näyteversion muokkaamalla ja rakentamalla CRT-, Hardware Station- ja POS-projektit. Suosittelemme, että teet tässä artikkelissa kuvatut muutokset käyttämällä Retail SDK -pakettia, jota ei ole muutettu. On myös suositeltavaa käyttää lähteenhallintajärjestelmää, kuten Azure DevOpsia, jossa tiedostoja ei ole vielä muutettu.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Veroyhdistimen laajennusten ottaminen käyttöön

Voit ottaa veroliittimen laajennukset käyttöön [Hardware stationissa](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) tai [POS-kassapäätteessä](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Ota käyttöön Hardware station -laajennukset

Hardware station -laajennuskomponentit sisältyvät Hardware station -esimerkkeihin. Voit suorittaa seuraavat vaiheet avaamalla **HardwareStationSamples.sln**-ratkaisun kohdassa **RetailSdk\\SampleExtensions\\HardwareStation**.

##### <a name="efrsample-component"></a>EFRSample-komponentti

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

#### <a name="enable-pos-extensions"></a>POS-laajennusten ottaminen käyttöön

POS-laajennuksen esimerkki sijaitsee **src\\FiscalIntegration\\PosFiscalConnectorSample** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä.

Noudata näitä ohjeita, jotta voit käyttää tätä POS-laajennuksen esimerkkiä vanhassa SDK:ssa.

1. Kopioi **Pos.Extension**-kansio myyntipisteen **Extensions**-kansioon vanhassa SDK:ssa (esim. `C:\RetailSDK\src\POS\Extensions`).
1. Nimeä **Pos.Extension**-kansion kopion nimeksi **PosFiscalConnector**.
1. Poista seuraavat kansiot ja tiedostot **PosFiscalConnector**-kansiosta:

    - bin
    - DataService
    - devDependencies
    - Kirjastot
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. Avaa **CloudPos.sln**- tai **ModernPos.sln**-ratkaisu.
1. Sisällytä **Pos.Extensions**-projektiin **PosFiscalConnector**-kansio.
1. Avaa **extensions.json**-tiedoston ja lisää **PosFiscalConnector**-laajennus.
1. Muodosta SDK.

### <a name="enable-modern-pos-extension-components"></a>Modern POS -laajennuksen komponenttien käyttöönotto

1. Avaa **ModernPOS.sln**-ratkaisu kohdassa **RetailSdk\\POS** ja varmista, että se voidaan kääntää virheettä. Varmista myös, että voit suorittaa Modern POS -sovelluksen Visual Studiosta **Run**-komennon avulla.

    > [!NOTE]
    > Modern POS -sovellusta ei saa mukauttaa. Käyttäjätilien valvonta (UAC) on otettava käyttöön, ja aiemmin asennettujen Modern POS -instanssien asennus täytyy poistaa.

2. Salli laajennusten lataaminen lisäämällä seuraavat rivit **extensions.json**-tiedostoon.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Lisätietoja sekä esimerkkejä, jotka näyttävät lähdekoodikansioiden lisäämisen ja laajennusten lataamisen, on **Pos.Extensions**-projektin readme.md-tiedoston ohjeissa.

3. Luo ratkaisu uudelleen.
4. Suorita Modern POS virheenkorjaustyökalussa ja testaa toiminto.

### <a name="enable-cloud-pos-extension-components"></a>Cloud POS -laajennuskomponenttien käyttöönotto

1. Avaa **CloudPOS.sln**-ratkaisu kohdassa **RetailSdk\\POS** ja varmista, että se voidaan kääntää virheettä.
2. Salli laajennusten lataaminen lisäämällä seuraavat rivit **extensions.json**-tiedostoon.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Lisätietoja sekä esimerkkejä, jotka näyttävät lähdekoodikansioiden lisäämisen ja laajennusten lataamisen, on **Pos.Extensions**-projektin readme.md-tiedoston ohjeissa.

3. Luo ratkaisu uudelleen.
4. Suorita ratkaisu Käyttämällä **Run**-komentoa ja noudattamalla Retail SDK -käsikirjan ohjeita.

## <a name="production-environment"></a>Tuotantoympäristö

Edellisessä menettelyssä on otettu käyttöön laajennukset, jotka ovat kirjanpidon rekisteröinnin palvelun integrointiesimerkin komponentteja. Luo lisäksi Commerce-komponentteja sisältävät käyttöön otettavat paketit ja ota paketit käyttöön tuotantoympäristössä noudattamalla näitä ohjeita.

1. Tee seuraavat muutokset **RetailSdk\\Assets**-kansion paketin konfiguraatiotiedostoihin:

    - Lisää **commerceruntime.ext.config**- ja **CommerceRuntime.MPOSOffline.Ext.config**-määritystiedostoihin seuraavat rivit **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - Lisää **HardwareStation.Extension.config** -määritystiedostossa seuraava rivi **composition**-osaan.

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

    - Lisää seuraava rivi, jos haluat sisällyttää Hardware station -laajennuksen käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Käynnistä Visual Studion MSBuild Command Prompt -työkalu ja luo käyttöön otettavat paketit suorittamalla **msbuild** Retail SDK -kansiossa.
4. Ota paketit käyttöön LCS:n kautta tai manuaalisesti. Lisätietoja on ohjeaiheessa [Käyttöönottopakettien luominen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Suorita kaikki tarvittavat asetustehtävät, jotka on kuvattu kohdassa [Commercen määritys (Itävalta)](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>Laajennusten rakenne

Itävallan verorekisteröintipalvelun integraatioesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md). Lisätietoja kirjanpidon integroinnin ratkaisun rakenteesta on kohdassa [Kirjanpidon integrointiesimerkin rakenteen yleiskatsaus](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime -laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda palvelukohtaisia asiakirjoja ja käsitellä verorekisteröintipalvelun vastauksia.

CRT-laajennus on **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Pyyntökäsittelijä

Asiakirjatarjoajia varten on kaksi pyynnön käsittelijää:

- **DocumentProviderEFRFiscalAUT** – Tämän käsittelijän avulla luodaan veroasiakirjoja verorekisteröintipalvelua varten.
- **DocumentProviderEFRNonFiscalAUT** – Tämän käsittelijän avulla luodaan muita kuin veroasiakirjoja verorekisteröintipalvelua varten.

Nämä käsittelijät on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä kirjanpidon rekisteröintipalveluun.
- **GetNonFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä muu kuin veroasiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä kirjanpidon rekisteröintipalveluun.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Tällä hetkellä seuraavat tapahtumat ovat tuettuja: myynti, X-raportin tulostaminen, Z-raportin tulostaminen, asiakastilitalletus, asiakastilausten talletukset, kirjaustapahtumat sekä muut kuin myyntitapahtumat.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Tämä pyyntö palauttaa vastauksen verorekisteröintipalvelusta. Tämä vastaus sarjoitettu muodostamaan merkkijonon, joten se on valmis tallennettavaksi.

#### <a name="configuration"></a>Konfigurointi

Konfigurointitiedostot sijaitsevat laajennusprojektin **Configuration**-kansiossa:

- **DocumentProviderFiscalEFRSampleAustria** – Veroasiakirjoja varten.
- **DocumentProviderNonFiscalEFRSampleAustria** – muita kuin veroasiakirjoja varten.

Näiden tiedostojen tarkoitus on ottaa käyttöön asetukset, joiden avulla tiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraava asetus lisätään:

- ALV-prosenttien yhdistäminen

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verorekisteröintipalvelun kanssa. Hardware station -laajennuksen nimi on **HardwareStation.Extension.EFRSample**. Se käyttää HTTP- tai HTTPS-protokollaa asiakirjojen lähettämiseen, jotka CRT-laajennus luo kirjanpidon rekisteröintipalveluun. Se käsittelee myös verorekisteröintipalvelusta saadut vastaukset.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**EFRHandler**-pyyntökäsittelijä on kirjanpidon rekisteröintipalvelun pyyntöjen käsittelyn aloituspiste.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä:

- **SubmitDocumentFiscalDeviceRequest** – Tämä pyyntö lähettää asiakirjoja kirjanpidon rekisteröintipalveluun ja palauttaa vastauksen pyyntöön.
- **IsReadyFiscalDeviceRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun kunnon tarkastusta varten.
- **InitializeFiscalDeviceRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun alustamiseen.

#### <a name="configuration"></a>Konfigurointi

Konfigurointitiedosto sijaitsee laajennusprojektin **Configuration**-kansiossa. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla veroyhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- **Päätepisteen osoite** – verorekisteröintipalvelun URL-osoite.
- **Aikakatkaisu** – Aika millisekunteina, jonka ajuri odottaa verorekisteröintipalvelun vastausta.

### <a name="pos-fiscal-connector-extension-design"></a>Myyntipisteen veroyhdistimen laajennuksen rakenne

Myyntipisteen veroyhdistimen laajennuksen tarkoituksena on kommunikoida verorekisteröintipalvelun kanssa myyntipisteestä. Se käyttää tietoliikenteeseen HTTPS-protokollaa.

#### <a name="fiscal-connector-factory"></a>Veroliittimen luontitoiminto

Veroliittimen luontitoiminto yhdistää liittimien nimen veroliittimien toteutukseen ja se sijaitsee **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**-tiedostossa. Yhdistimen nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

#### <a name="efr-fiscal-connector"></a>EFR-veroliitin

EFR-veroliitin sijaitsee **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**-tiedostossa. Se toteuttaa **IFiscalConnector**-rajapinnan, joka tukee seuraavia pyyntöjä:

- **FiscalRegisterSubmitDocumentClientRequest** – Tämä pyyntö lähettää asiakirjoja kirjanpidon rekisteröintipalveluun ja palauttaa vastauksen pyyntöön.
- **FiscalRegisterIsReadyClientRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun kunnon tarkastusta varten.
- **FiscalRegisterInitializeClientRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun alustamiseen.

#### <a name="configuration"></a>Konfiguraatio

Määritystiedosto sijaitsee **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla veroyhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- **Päätepisteen osoite** – verorekisteröintipalvelun URL-osoite.
- **Aikakatkaisu** – Aika millisekunteina, jonka liitin odottaa verorekisteröintipalvelun vastausta.
