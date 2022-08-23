---
ms.openlocfilehash: a20971ac9a44c409363bbce6cd8b8343f16d800f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274202"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Tarkistusyksikön integrointiesimerkin käyttöönoton ohjeet (Ruotsi) (vanha)
---

otsikko: Tarkistusyksikön integrointiesimerkin käyttöönoton ohjeet (Ruotsi) (vanha) [!include [banner](../includes/banner.md)]
kuvaus: Tässä artikkelissa on ohjeita Ruotsin tarkistusyksikön integrointiesimerkin käyttöönottamiseksi Retail -ohjelmistokehityspaketista (SDK)

tekijä: EvgenyPopovMBS Tässä artikkelissa on ohjeita, jotka koskevat Ruotsin tarkistusyksikön integrointiesimerkin käyttöönottoa Retail -ohjelmistokehityspaketista (SDK) kehittäjän virtuaalitietokoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja tästä kirjanpidon integroinnin esimerkistä on kohdassa [Ruotsin tarkistusyksikön integrointiesimerkki](emea-swe-fi-sample.md). ms.date: 20.12.2021

ms.topic: artikkeli Ruotsin verointegraation esimerkki kuuluu Retail SDK -pakettiin. Lisätietoja SDK:n asentamisesta ja käytöstä on kohdassa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md). Tämä esimerkki koostuu Commerce runtime (CRT)-, Hardware Station- ja myyntipiste (POS) -laajennusosista. Voit suorittaa tämän näyteversion muokkaamalla ja rakentamalla CRT-, Hardware Station- ja POS-projektit. Suosittelemme, että teet tässä artikkelissa kuvatut muutokset käyttämällä Retail SDK -pakettia, jota ei ole muutettu. On myös suositeltavaa käyttää lähteenhallintajärjestelmää, kuten Azure DevOpsia, jossa tiedostoja ei ole vielä muutettu.
kohderyhmä: sovelluksen käyttäjä, kehittäjä, IT Pro

ms.reviewer: v-chgriffin
## <a name="development-environment"></a>Kehitysympäristö
ms.search.region: Yleinen

ms.author: josaw Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa näytettä.
ms.search.validFrom: 2019-03-01

### <a name="enable-crt-extensions"></a>CRT-laajennusten ottaminen käyttöön
---


CRT -laajennuskomponentit sisältyvät CRT-näytteisiin. Voit suorittaa seuraavat vaiheet avaamalla **CommerceRuntimeSamples.sln**-ratkaisun kohdassa **RetailSdk\\SampleExtensions\\CommerceRuntime**.
2. Ota käyttöön nykyinen Hardware station -esimerkkilaajennus lisäämällä seuraava rivi **HardwareStation.Extension.config**-konfigurointitiedoston **composition**-osaan.


#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample component
    ``` xml

    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
1. Etsi **Runtime.Extensions.DocumentProvider.CleanCashSample**-projekti ja luo se.
    ```
2. In the **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** assembly file.

3. Copy the assembly file to the CRT extensions folder:
3. Make the following changes in the **Customization.settings** package customization configuration file under the **BuildTools** folder:


    - **Commerce Scale Unit:** Copy the file to the **\\bin\\ext** folder under the Internet Information Services (IIS) Commerce Scale Unit site location.
    - Remove the following line to exclude the earlier Hardware station extension from deployable packages.
    - **Local CRT on Modern POS:** Copy the file to the **\\ext** folder under the local CRT client broker location.


        ``` xml
4. Find the extension configuration file for CRT:
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />

        ```
    - **Commerce Scale Unit:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Commerce Scale Unit site location.

    - **Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.
    - Add the following lines to include the current sample Hardware station extension in deployable packages.


5. Register the CRT change in the extension configuration file.
        ``` xml

        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
    ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        ```
    ```


#### <a name="update-modern-pos"></a>Päivitä Modern POS
#### <a name="extension-configuration-file"></a>Laajennuksen määritystiedosto


1. Avaa **CloudPOS.sln**-ratkaisu **RetailSdk\\POS**-kohdassa.
1. Etsi CRT-laajennuskonfigurointitiedosto:
2. Poista aiempi POS-laajennus käytöstä:


    - **Commerce Scale Unit:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Commerce Scale Unit -sivuston sijainnissa.
    - Lisää **tsconfig.json**-tiedostossa **FiscalRegisterSample**-kansio poissulkemisluetteloon.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.
    - Poista seuraavat rivit **extensions.json** -tiedostosta **RetailSDK\\POS\\Extensions**-kansiossa.


2. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.
        ``` json

        {
    ``` xml
            "baseUrl": "FiscalRegisterSample"
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        }
    ```
        ```


### <a name="enable-hardware-station-extensions"></a>Ota käyttöön Hardware station -laajennukset
3. Ota nykyinen POS-esimerkkilaajennus käyttöön lisäämällä seuraavat rivit **extensions.json**-tiedostoon **RetailSDK\\POS\\Extensions**-kansiossa.


Hardware station -laajennuskomponentit sisältyvät Hardware station -esimerkkeihin. Voit suorittaa seuraavat vaiheet avaamalla **HardwareStationSamples.sln**-ratkaisun kohdassa **RetailSdk\\SampleExtensions\\HardwareStation**.
    ``` json

    {
#### <a name="cleancash-component"></a>CleanCash-komponentti
        "extensionPackages": [

            {
1. Etsi **HardwareStation.Extension.CleanCashSample**-projekti ja luo se.
                "baseUrl": "Microsoft/AuditEvent.SE"
2. Etsi **Extension.CleanCashSample\\bin\\Debug** -kansiosta **Contoso.Commerce.HardwareStation.CleanCashSample.dll**- ja **Interop.CleanCash\_1\_1.dll** -kokoonpanotiedostot.
            }
3. Kopioi kokoonpanotiedostot Hardware station -laajennuskansioon:      ]

    }
    - **Jaettu Hardware station:** Kopioi tiedostot **bin**-kansioon IIS Hardware station -sivuston sijainnissa.
    ```
    - **Dedicated hardware station on Modern POS:** Copy the files to the Modern POS client broker location.


#### Update Cloud POS
4. Find the extension configuration file for the Hardware station's extensions. The file is named **HardwareStation.Extension.config**.


1. Open the **ModernPOS.sln** solution under **RetailSdk\\POS**.
    - **Shared hardware station:** The file is under the IIS Hardware station site location.
2. Disable the earlier POS extension:
    - **Dedicated hardware station on Modern POS:** The file is under the Modern POS client broker location.


    - In the **tsconfig.json** file, add the **FiscalRegisterSample** folder to the exclude list.
5. Add the following line to the **composition** section of the configuration file.
    - Remove the following lines from the **extensions.json** file under the **RetailSDK\\POS\\Extensions** folder.


    ``` xml
        ``` json
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        {
    ```
            "baseUrl": "FiscalRegisterSample"

        }
### <a name="enable-modern-pos-extension-components"></a>Modern POS -laajennuksen komponenttien käyttöönotto
        ```


1. Avaa **ModernPOS.sln**-ratkaisu kohdassa **RetailSdk\\POS** ja varmista, että se voidaan kääntää virheettä. Varmista myös, että voit suorittaa Modern POS -sovelluksen Visual Studiosta **Run**-komennon avulla.
3. Ota nykyinen POS-esimerkkilaajennus käyttöön lisäämällä seuraavat rivit **extensions.json**-tiedostoon **RetailSDK\\POS\\Extensions**-kansiossa.


    > [!NOTE]
    ``` json
    > Modern POS must not be customized. You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.
    {

        "extensionPackages": [
2. Enable the extensions that must be loaded by adding the following lines in the **extensions.json** file.
            {

                "baseUrl": "Microsoft/AuditEvent.SE"
    ``` json
            }
    {
        ]
        "extensionPackages": [
    }
            {
    ```
                "baseUrl": "Microsoft/AuditEvent.SE"

            }
#### <a name="create-deployable-packages"></a>Käyttöönotettavien pakettien luominen
        ]

    }
Luo käyttöön otettavat paketit ajamalla koko Retail SDK -sovelluksen **msbuild**. Ota paketit käyttöön LCS:n kautta tai manuaalisesti. Lisätietoja: [Retail SDK -paketit](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
    ```

    > [!NOTE]
    > For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.

3. Luo ratkaisu uudelleen.
4. Suorita Modern POS virheenkorjaustyökalussa ja testaa toiminto.

### <a name="enable-cloud-pos-extension-components"></a>Cloud POS -laajennuskomponenttien käyttöönotto

1. Avaa **CloudPOS.sln**-ratkaisu kohdassa **RetailSdk\\POS** ja varmista, että se voidaan kääntää virheettä.
2. Salli laajennusten lataaminen lisäämällä seuraavat rivit **extensions.json**-tiedostoon.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Lisätietoja sekä esimerkkejä, jotka näyttävät lähdekoodikansioiden lisäämisen ja laajennusten lataamisen, on **Pos.Extensions**-projektin readme.md-tiedoston ohjeissa.

3. Luo ratkaisu uudelleen.
4. Suorita ratkaisu Käyttämällä **Run**-komentoa ja noudattamalla Retail SDK -käsikirjan ohjeita.

## <a name="production-environment"></a>Tuotantoympäristö

Edellisessä menettelyssä on otettu käyttöön laajennukset, jotka ovat tarkistusyksikön integrointiesimerkin komponentteja. Luo lisäksi Commerce-komponentteja sisältävät käyttöön otettavat paketit ja ota paketit käyttöön tuotantoympäristössä noudattamalla näitä ohjeita.

1. Tee seuraavat muutokset **RetailSdk\\Assets**-kansion paketin konfiguraatiotiedostoihin:

    - Lisää **commerceruntime.ext.config**- ja **CommerceRuntime.MPOSOffline.Ext.config**-määritystiedostoihin seuraavat rivit **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Lisää **HardwareStation.Extension.config** -määritystiedostossa seuraava rivi **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Tee seuraavat muutokset **Customization.settings**-paketin mukautusmääritystiedostoon **BuildTools**-kansiossa:

    - Lisää seuraava rivi, jos haluat sisällyttää CRT-laajennukset käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Lisää seuraavat rivit, jos haluat sisällyttää Hardware station -laajennuksen käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Ota POS-laajennus käyttöön lisäämällä seuraavat rivit **extensions.json**-tiedostoon **RetailSDK\\POS\\Extensions**-kansiossa.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Käynnistä Visual Studion MSBuild Command Prompt -työkalu ja luo käyttöön otettavat paketit suorittamalla **msbuild** Retail SDK -kansiossa.
5. Ota paketit käyttöön LCS:n kautta tai manuaalisesti. Lisätietoja on ohjeaiheessa [Käyttöönottopakettien luominen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Suorita kaikki pakolliset määritystehtävät, jotka on kuvattu kohdassa [Tarkistusyksiköiden integroinnin määrittäminen](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Laajennusten rakenne

### <a name="crt-extension-design"></a>CRT-laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda palvelukohtaisia asiakirjoja ja käsitellä tarkistusyksikön vastauksia.

CRT-laajennus on **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Lisätietoja kirjanpidon integroinnin rakenteesta on kohdassa [Kirjanpidon rekisteröintiprosessi ja kirjanpidon laitteiden ja palveluiden kirjanpidon integrointimallit](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Pyyntökäsittelijä

Asiakirjapalvelua varten on yksi pyynnön käsittelijä, **DocumentProviderCleanCash**. Tämän käsittelijän avulla luodaan veroasiakirjoja tarkistusyksikköä varten.

Tämä käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä tarkistusyksikköön.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Myyntitapahtumia ja kirjaustapahtumia tuetaan tällä hetkellä.

#### <a name="configuration"></a>Konfigurointi

**DocumentProviderFiscalCleanCashSample**-konfigurointitiedosto sijaitsee laajennusprojektin **Configuration**-kansiossa. Tämän tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla tiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- ALV-koodien yhdistäminen

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida tarkistusyksikön kanssa.

Hardware station -laajennus on **HardwareStation.Extension.CleanCashSample**. Se käyttää HTTP-protokollaa asiakirjojen lähettämiseen, jotka CRT-laajennus luo tarkistusyksikköön. Se käsittelee myös tarkistusyksiköstä saadut vastaukset.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**CleanCashHandler**-pyyntökäsittelijä on tarkistusyksikön pyyntöjen käsittelyn aloituspiste.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä:

- **SubmitDocumentFiscalDeviceRequest** – Tämä pyyntö lähettää asiakirjoja tarkistusyksikköön ja palauttaa vastauksen pyyntöön.
- **IsReadyFiscalDeviceRequest** – Tätä pyyntöä käytetään tarkistusyksikön kunnon tarkastusta varten.
- **InitializeFiscalDeviceRequest** – Tätä pyyntöä käytetään tarkistusyksikön alustamiseen.

#### <a name="configuration"></a>Konfigurointi

Konfigurointitiedosto sijaitsee laajennusprojektin **Configuration**-kansiossa. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla veroyhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- **Yhteysmerkkijono** – tarkistusyksikön yhteysasetukset.
- **Aikakatkaisu** – Aika millisekunteina, jonka ajuri odottaa tarkistusyksikön vastausta.

## <a name="migrating-from-the-earlier-integration-sample"></a>Siirtyminen aiemmasta integrointiesimerkistä

Jos käytät aiempaa [Ruotsin POS-integrointia tarkistusyksiköiden kanssa](retail-sdk-control-unit-sample.md), sinun on ehkä siirryttävä siitä nykyiseen integrointiesimerkkiin. Jotta voisit ottaa muutoksen käyttöön ja vastaanottaa ajan tasalla olevia päivityksiä Ruotsin ominaisuuksille tulevaisuudessa, sinun on ehkä päivitettävä, tehtävä pieniä koodi- ja konfiguraatiomuutoksia ominaisuuksiin, jotka olet rakentanut ja muodostettava ratkaisusi uudelleen. Luomaasi laajennuslogiikkaan ei tarvitse tehdä suuria muutoksia. Aiempi integrointiesimerkki ja mukautuksesi jatkavat toimintaansa, ellei sinun puoleltasi tehdä muutoksia. Näin ollen voit suunnitella, valmistautua ja tehdä valmistelun ympäristösi päivitystä varten.

### <a name="migration-process"></a>Siirtämisprosessi

Siirtyminen aiemmasta integrointiesimerkistä nykyiseen tarkistusyksikön integrointiesimerkkiin tulisi perustua vaiheittaisen päivityksen käsitteeseen. Toisin sanoen kaikki Commerce Headquarters- ja Commerce Scale Unit -komponentit on päivitettävä, ennen kuin POS- ja Hardware station -komponenttien päivitys aloitetaan.

Jotta estettäisiin tilanne, jossa tapahtuma tai transaktio allekirjoitetaan kahdesti (eli se on sekä aikaisemman laajennuksen että uuden laajennuksen allekirjoittama) tai jossa tapahtumaa ei voi allekirjoittaa puuttuvan konfiguraation vuoksi, on suositeltavaa poistaa kaikki aiempaa esimerkkiä käyttävät POS- ja Hardware station -laitteet käytöstä ja päivittää ne sitten samanaikaisesti. Tämä samanaikainen päivitys voidaan tehdä esimerkiksi myymäläkohtaisesti päivittämällä myymälän toimintoprofiili ja Hardware station -laiteprofiili.

Siirtoprosessin tulisi koostua seuraavista vaiheista.

1. Päivitä Commerce Headquarters -komponentit.
1. Päivitä Commerce Scale Unit -komponentit ja ota käyttöön nykyisen esimerkin laajennukset.
1. Varmista, että kaikki offline-tapahtumat on synkronoitu offline-käyttöön tarkoitetuista MPOS-laitteista.
1. Poista käytöstä kaikki laitteet, jotka käyttävät aiemman esimerkin komponentteja.
1. Suorita kaikki pakolliset määritystehtävät, jotka on kuvattu kohdassa [Tarkistusyksiköiden integroinnin määrittäminen](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Päivitä POS- ja Hardware station -komponentit, poista aiempaan esimerkkiin liittyvät laajennukset käytöstä ja ota käyttöön nykyisen esimerkin laajennukset.

    > [!NOTE]
    > Ympäristötyypin mukaan siirtoprosessista on teknisiä lisätietoja joko tämän artikkelin [Kehitysympäristön siirto](#migration-in-a-development-environment) -osassa tai [Tuotantoympäristön siirto](#migration-in-a-production-environment) -osassa.

### <a name="migration-in-a-development-environment"></a>Kehitysympäristön siirto

#### <a name="update-crt"></a>Päivitä CRT

1. Etsi **Runtime.Extensions.DocumentProvider.CleanCashSample**-projekti ja luo se.
2. Etsi **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Commerce Scale Unit:** Kopioi tiedosto **\\bin\\ext**-kansioon Internet IIS Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi tiedosto **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Commerce Scale Unit:** Tiedoston nimi on **CommerceRuntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnissa **bin\\ext**-kansiossa.

    > [!WARNING]
    > **Älä** muokkaa CommerceRuntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

5. Etsi aiempi CRT-laajennus ja poista se laajennuksen konfigurointitiedostosta.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Älä suorita tätä vaihetta, ennen kuin päivität kaikki tätä CRT-esiintymää käyttävät POS-laitteet.

6. Rekisteröi nykyiset CRT-esimerkkilaajennukset laajennuskonfiguraatiotiedostoon lisäämällä seuraavat rivit.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Hardware Stationin päivitys

1. Etsi **HardwareStation.Extension.CleanCashSample**-projekti ja luo se.
2. Etsi **Extension.CleanCashSample\\bin\\Debug** -kansiosta **Contoso.Commerce.HardwareStation.CleanCashSample.dll**- ja **Interop.CleanCash\_1\_1.dll** -kokoonpanotiedostot.
3. Kopioi kokoonpanotiedostot Hardware station -laajennuskansioon:

    - **Jaettu Hardware station:** Kopioi tiedostot **bin**-kansioon IIS Hardware station -sivuston sijainnissa.
    - **Erillinen Hardware station Modern POS -sovelluksessa:** Kopioi tiedostot Modern POS -asiakasvälittäjän sijaintiin.

4. Etsi **HardwareStation.Extension.config**-laajennuskonfiguraatiotiedosto:

    - **Remote Hardware station:** Tiedosto on IIS Hardware station -sivuston sijainnissa.
    - **Paikallinen Hardware station Modern POS -sovelluksessa:** Tiedosto on Modern POS -asiakasvälittäjän sijainnissa.

    > [!WARNING]
    > **Älä** muokkaa CommerceRuntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

5. Etsi aiempi Hardware station -laajennus ja poista se laajennuksen konfigurointitiedostosta.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 ja aiemmat versiot](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 ja uudemmat versiot](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 ja uudemmat versiot](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Lisää seuraava rivi laajennuskonfigurointitiedoston **composition**-osaan.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Päivitä Modern POS

1. Avaa **CloudPOS.sln**-ratkaisu **RetailSdk\\POS**-kohdassa.
2. Voit poistaa aiemman POS-laajennuksen käytöstä poistamalla seuraavat rivit **extensions.json**-tiedostosta.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Salli nykyinen POS-esimerkkilaajennus lisäämällä seuraavat rivit **extensions.json**-tiedostoon.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Päivitä Cloud POS

1. Avaa **ModernPOS.sln**-ratkaisu **RetailSdk\\POS**-kohdassa.
2. Voit poistaa aiemman POS-laajennuksen käytöstä poistamalla seuraavat rivit **extensions.json**-tiedostosta.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Salli nykyinen POS-esimerkkilaajennus lisäämällä seuraavat rivit **extensions.json**-tiedostoon.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Tuotantoympäristön siirto

#### <a name="update-crt"></a>Päivitä CRT

1. Poista aiempi CRT-laajennus **CommerceRuntime.ext.config**- ja **CommerceRuntime.MPOSOffline.Ext.config**-konfiguraatiotiedostoista **RetailSdk\\Assets**-kansiossa.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Älä suorita tätä vaihetta, ennen kuin päivität kaikki tätä CRT-esiintymää käyttävät POS-laitteet.

2. Ota nykyinen CRT-esimerkkilaajennukset tekemällä seuraavat muutokset **CommerceRuntime.ext.config**- ja **CommerceRuntime.MPOSOffline.Ext.config**-konfiguraatiotiedostoihin **RetailSdk\\Assets**-kansiossa.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Lisää **Customization.settings**-paketin mukautuskonfiguraatiotiedostoon **BuildTools**-kansiossa seuraava rivi, jotta voit sisällyttää nykyisen CRT-esimerkkilaajennuksen käyttöönotettaviin paketteihin.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Hardware Stationin päivitys

1. Poista aiempi Hardware station -laajennus muokkaamalla **HardwareStation.Extension.config**-konfigurointitiedostoa.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 ja aiemmat versiot](#tab/retail-7-3)

    Poista seuraava osa **HardwareStation.Shared.config**- ja **HardwareStation.Dedicated.config**-tiedostoista.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 ja uudemmat versiot](#tab/retail-7-3-1)

    Poista **HardwareStation.Extension.config** -määritystiedostosta seuraava osa.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 ja uudemmat versiot](#tab/retail-10-0)

    Poista **HardwareStation.Extension.config** -määritystiedostosta seuraava osa.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---
