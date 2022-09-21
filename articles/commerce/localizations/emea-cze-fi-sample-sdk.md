---
title: Verorekisteröintipalvelun integroinnin esimerkkiä koskevat käyttöönoton ohjeet (Tšekin tasavalta) (vanha)
description: Tässä artikkelissa on ohjeita Tšekin tasavallan verointegroinnin esimerkin käyttöönottamiseksi Microsoft Dynamics 365 Commerce Retail -ohjelmistokehityspaketista (SDK).
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 7406a6443f851fcfa9757deed57c108ba7b6e069
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473901"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>Verorekisteröintipalvelun integroinnin esimerkkiä koskevat käyttöönoton ohjeet (Tšekin tasavalta) (vanha)

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Seuraa tämän artikkelin ohjeita vain, jos käytössä on Microsoft Dynamics 365 Commercen versio 10.0.28 tai aiempi versio. Tšekin tasavallan verorekisteröintipalvelun integraatioesimerkki on saatavilla Commercen versiosta 10.0.29 alkaen Commerce SDK:ssa. Lisätietoja on kohdassa [Kanavan osien määrittäminen](./emea-cze-fi-sample.md#configure-channel-components).

Tässä artikkelissa on ohjeita, jotka koskevat Tšekin tasavallan verorekisteröintipalvelun integroinnin käyttöönottoa Dynamics 365 Commerce Retail SDK:sta kehittäjän virtuaalitietokoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja verointegroinnin esimerkistä on kohdassa [Verorekisteröintipalvelun integroinnin esimerkki (Tšekin tasavalta)](emea-cze-fi-sample.md). 

Tšekin tasavallan verointegraation esimerkki kuuluu Retail SDK -pakettiin. Lisätietoja SDK:n asentamisesta ja käytöstä on kohdassa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md). Tämä esimerkki koostuu Commerce runtime (CRT)- ja Hardware Station -laajennusosista. Voit suorittaa tämän näyteversion muokkaamalla ja rakentamalla CRT- ja Hardware Station -projektit. Suosittelemme, että teet tässä artikkelissa kuvatut muutokset käyttämällä Retail SDK -pakettia, jota ei ole muutettu. On myös suositeltavaa käyttää lähteenhallintajärjestelmää, kuten Azure DevOpsia, jossa tiedostoja ei ole vielä muutettu.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Veroyhdistimen laajennusten ottaminen käyttöön

Voit ottaa veroliittimen laajennukset käyttöön [Hardware stationissa](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) tai [POS-kassapäätteessä](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

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

### <a name="production-environment"></a>Tuotantoympäristö

Edellisessä menettelyssä on otettu käyttöön laajennukset, jotka ovat kirjanpidon rekisteröinnin palvelun integrointiesimerkin komponentteja. Luo lisäksi Commerce-komponentteja sisältävät käyttöön otettavat paketit ja ota paketit käyttöön tuotantoympäristössä noudattamalla näitä ohjeita.

1. Tee seuraavat muutokset **RetailSdk\\Assets**-kansion paketin konfiguraatiotiedostoihin.

    - Lisää **commerceruntime.ext.config**- ja **CommerceRuntime.MPOSOffline.Ext.config**-määritystiedostoihin seuraavat rivit **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - Lisää **HardwareStation.Extension.config** -määritystiedostossa seuraava rivi **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. Tee seuraavat muutokset **Customization.settings**-paketin mukautusmääritystiedostoon **BuildTools**-kansiossa.

    - Lisää seuraavat rivit, jos haluat sisällyttää CRT-laajennukset käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Lisää seuraava rivi, jos haluat sisällyttää Hardware station -laajennuksen käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Käynnistä Visual Studion MSBuild Command Prompt -työkalu ja luo käyttöön otettavat paketit suorittamalla **msbuild** Retail SDK -kansiossa.
4. Ota paketit käyttöön LCS:n kautta tai manuaalisesti. Lisätietoja on ohjeaiheessa [Käyttöönottopakettien luominen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Suorita kaikki tarvittavat asetustehtävät, jotka on kuvattu kohdassa [Commercen määritys (Tšekin tasavalta)](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic).

## <a name="design-of-extensions"></a>Laajennusten rakenne

Tšekin tasavallan verorekisteröintipalvelun integraatioesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md). Lisätietoja kirjanpidon integroinnin ratkaisun rakenteesta on kohdassa [Kirjanpidon integrointiesimerkin rakenteen yleiskatsaus](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime -laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda palvelukohtaisia asiakirjoja ja käsitellä verorekisteröintipalvelun vastauksia.

CRT-laajennus on **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Pyyntökäsittelijä

Asiakirjapalvelua varten on yksi pyynnön käsittelijä, **DocumentProviderEFRFiscalCZE**. Sen avulla luodaan veroasiakirjoja verorekisteröintipalvelua varten.

Tämä käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä kirjanpidon rekisteröintipalveluun.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Tällä hetkellä seuraavia tapahtumia tuetaan: myynti, asiakastilitalletus ja asiakastilausten talletukset.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Tämä pyyntö palauttaa vastauksen verorekisteröintipalvelusta. Tämä vastaus sarjoitettu muodostamaan merkkijonon, joten se on valmis tallennettavaksi.

#### <a name="configuration"></a>Konfigurointi

**DocumentProviderFiscalEFRSampleCzech**-konfigurointitiedosto sijaitsee laajennusprojektin **Configuration**-kansiossa. Tämän tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla tiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- ALV-prosenttien yhdistäminen
- ALV-oletusryhmä
- Talletusten ALV-ryhmä

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verorekisteröintipalvelun kanssa.

Hardware station -laajennuksen nimi on **HardwareStation.Extension.EFRSample**. Se käyttää HTTP- tai HTTPS-protokollaa asiakirjojen lähettämiseen, jotka CRT-laajennus luo kirjanpidon rekisteröintipalveluun. Se käsittelee myös verorekisteröintipalvelusta saadut vastaukset.

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
- **Aikakatkaisu** – Aika millisekunteina, jonka liitin odottaa verorekisteröintipalvelun vastausta.

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
