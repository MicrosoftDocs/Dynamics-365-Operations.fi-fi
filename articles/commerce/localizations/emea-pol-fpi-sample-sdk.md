---
title: Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Puola) (vanha)
description: Tässä artikkelissa on ohjeita Puolan verotulostimen integroinnin esimerkin käyttöönottamiseksi Microsoft Dynamics 365 Commerce Retail -ohjelmistokehityspaketista (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 883f09f73e3b372d6896b6702e54e2e664cff4d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286523"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Puola) (vanha)

[!include[banner](../includes/banner.md)]

Tässä artikkelissa on ohjeita, jotka koskevat Puolan verotulostimen integrointiesimerkin käyttöönottoa Microsoft Dynamics 365 Commerce Retail -ohjelmistokehityspaketista (SDK) kehittäjän virtuaalitietokoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja verointegroinnin esimerkistä on kohdassa [Verotulostimen integroinnin esimerkki (Puola)](emea-pol-fpi-sample.md). 

Puolan verointegraation esimerkki kuuluu Retail SDK -pakettiin. Lisätietoja SDK:n asentamisesta ja käytöstä on kohdassa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md). Tämä esimerkki koostuu Commerce runtime (CRT)- ja Hardware Station -laajennusosista. Voit suorittaa tämän näyteversion muokkaamalla ja rakentamalla CRT- ja Hardware Station -projektit. Suosittelemme, että teet tässä artikkelissa kuvatut muutokset käyttämällä Retail SDK -pakettia, jota ei ole muutettu. On myös suositeltavaa käyttää lähteenhallintajärjestelmää, kuten Azure DevOpsia, jossa tiedostoja ei ole vielä muutettu.

## <a name="development-environment"></a>Kehitysympäristö

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa näytettä.

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime -laajennusten komponentit

CRT-laajennuskomponentit sisältyvät Retail SDK -pakettiin. Voit suorittaa seuraavat vaiheet avaamalla **CommerceRuntimeSamples.sln**-ratkaisun kohdassa **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Etsi **Runtime.Extensions.DocumentProvider.PosnetSample** -projekti ja luo se.
2. Etsi **Extensions.DocumentProvider.PosnetSample\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Commerce Scale Unit:** Kopioi tiedosto **\\bin\\ext**-kansioon Internet Information Services (IIS) Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi tiedosto **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Commerce Scale Unit:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Commerce Scale Unit -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Käynnistä Commerce-palvelu uudelleen:

    - **Commerce Scale Unit:** Käynnistä Commerce-palvelun sivusto uudelleen IIS Managerissa.
    - **Asiakkaan välittäjä:** Lopeta **dllhost.exe**-prosessi Task Managerissa ja käynnistä sen jälkeen Modern POS uudelleen.

### <a name="hardware-station-extension-components"></a>Hardware station -laajennuksen komponentit

Hardware station -laajennuskomponentit sisältyvät Retail SDK -pakettiin. Voit suorittaa seuraavat vaiheet avaamalla **HardwareStationSamples.sln**-ratkaisun kohdassa **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Etsi **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**-projekti ja luo se.
2. Etsi **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** -kansiosta **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto käyttöönotettuun Hardware station -koneeseen:

    - **Remote Hardware station:** Kopioi tiedosto **bin**-kansioon IIS Hardware station -sivuston sijainnissa. Kopioi tulostinajurikirjastot (**libposcmbth.dll**, **libcmbth\_serial.dll** ja **cmbth\_pl.lng**).

4. Etsi Hardware station -laajennusten konfiguraatiotiedosto. Tiedoston nimi on **HardwareStation.Extension.config**:

    - **Remote Hardware station:** Tiedosto on IIS Hardware station -sivuston sijainnissa.

5. Lisää seuraava rivi konfigurointitiedoston **composition**-osaan.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Käynnistä Hardware station -palvelu uudelleen:

    - **Remote Hardware station:** Käynnistä Hardware station -sivusto uudelleen IIS Managerissa.

## <a name="production-environment"></a>Tuotantoympäristö

Edellisessä menettelyssä on otettu käyttöön laajennukset, jotka ovat kirjanpidon rekisteröinnin palvelun integrointiesimerkin komponentteja. Luo lisäksi Commerce-komponentteja sisältävät käyttöön otettavat paketit ja ota paketit käyttöön tuotantoympäristössä noudattamalla näitä ohjeita.

1. Tee seuraavat muutokset **RetailSdk\\Assets**-kansion paketin konfiguraatiotiedostoihin:

    - Lisää **commerceruntime.ext.config**- ja **CommerceRuntime.MPOSOffline.Ext.config**-määritystiedostoihin seuraavaa rivi **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Lisää **HardwareStation.Extension.config** -määritystiedostossa seuraava rivi **composition**-osaan.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Tee seuraavat muutokset **Customization.settings**-paketin mukautusmääritystiedostoon **BuildTools**-kansiossa:

    - Lisää seuraava rivi, jos haluat sisällyttää CRT-laajennuksen käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Lisää seuraava rivi, jos haluat sisällyttää Hardware station -laajennuksen käyttöön otettaviin paketteihin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Käynnistä Visual Studion MSBuild Command Prompt -työkalu ja luo käyttöön otettavat paketit suorittamalla **msbuild** Retail SDK -kansiossa.
1. Ota paketit käyttöön LCS:n kautta tai manuaalisesti. Lisätietoja on ohjeaiheessa [Käyttöönottopakettien luominen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Laajennusten rakenne

Puolan verotulostimen integrointiesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md). Lisätietoja kirjanpidon integroinnin ratkaisun rakenteesta on kohdassa [Kirjanpidon integrointiesimerkin rakenteen yleiskatsaus](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime -laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda tulostinkohtaisia asiakirjoja ja käsitellä verotulostimen vastauksia.

CRT-laajennus on **Runtime.Extensions.DocumentProvider.PosnetSample**. Tämä laajennus luo tulostinkohtaiset JavaScript Object Notation (JSON) -muodossa, joka on määritelty POSNET-määrityksessä 19-3678.

Lisätietoja kirjanpidon integroinnin rakenteesta on kohdassa [Kirjanpidon rekisteröintiprosessi ja kirjanpidon laitteiden ja palveluiden kirjanpidon integrointimallit](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Pyyntökäsittelijä

**DocumentProviderPosnetProtocol**-pyyntökäsittelijä on asiakirjan luontipyynnön aloituspiste verotulostimelle.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa tulostinkohtaisen asiakirjan, jotka on rekisteröitävä verotulostimeen.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Tällä hetkellä seuraavat tapahtumat ovat tuettuja: myynti, X-raportin tulostaminen ja Z-raportin tulostaminen.

#### <a name="configuration"></a>Konfigurointi

Konfigurointitiedosto löytyy laajennusprojektin **Configuration**-kansiosta. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla tiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- ALV-prosenttien yhdistäminen
- Maksuvälinetyyppien yhdistäminen
- Talletuksen maksutyyppi

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verotulostimen kanssa.

Hardware station -laajennus on **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Tämä laajennus kutsuu POSNET-ohjaimen toimintoja lähettämällä komennot, jotka CRT-laajennus luo verotulostimelle. Se käsittelee myös laitteen virheet.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**FiscalPrinterHandler**-pyyntökäsittelijä on oheislaitteen pyyntöjen käsittelyn aloituspiste.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä:

- **SubmitDocumentFiscalDeviceRequest** – Tämä pyyntö lähettää asiakirjoja tulostimille ja palauttaa vastauksen verotulostimesta.
- **IsReadyFiscalDeviceRequest** – Tätä pyyntöä käytetään laitteen kunnon tarkastusta varten.
- **InitializeFiscalDeviceRequest** – Tätä pyyntöä käytetään tulostimen alustamiseen.

#### <a name="configuration"></a>Konfigurointi

Konfigurointitiedosto sijaitsee laajennusprojektin **Configuration**-kansiossa. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla yhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- **Yhteysmerkkijono** – Merkkijono, joka kuvaa laiteyhteyden tietoja ohjaimen tukemassa muodossa. Lisätietoja on POSNET-ohjaimen dokumentaatiossa.
- **Päivämäärän ja ajan synkronointi** – Arvo, joka määrittää, synkronoidaanko tulostimen päivämäärä ja aika liitetyn Hardware stationin kanssa.
- **Laiteen aikakatkaisu** – Aika millisekunteina, jonka ajuri odottaa laitteen vastausta. Lisätietoja on POSNET-ohjaimen dokumentaatiossa.
