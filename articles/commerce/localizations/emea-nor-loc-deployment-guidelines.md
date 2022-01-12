---
title: Kassakoneiden käyttöönotto-ohjeet (Norja) (vanha)
description: Tämä ohjeaihe on käyttöönotto-opas, jossa kerrotaan, kuinka Microsoft Dynamics 365 Commerce -lokalisointi otetaan käyttöön Norjassa.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: 019bac01abdc0b2e16718c08953b44fbccef83a3
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944785"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Kassakoneiden käyttöönotto-ohjeet (Norja) (vanha)

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe on käyttöönotto-opas, jossa kerrotaan, kuinka Microsoft Dynamics 365 Commerce -lokalisointi otetaan käyttöön Norjassa. Lokalisointiin kuuluu useita Commerce-komponenttien laajennuksia. Laajennusten avulla voit esimerkiksi tulostaa mukautettuja kenttiä kuitteihin, rekisteröidä muita kirjaustapahtumia, myyntitapahtumia ja maksutapahtumia myyntipisteessä (POS), allekirjoittaa myyntitapahtumia digitaalisesti sekä tulostaa X- ja Z-raportteja paikallisissa muodoissa. Lisätietoja Norjan lokalisoinnista on kohdassa [Kassakoneen toiminnot, Norja](./emea-nor-cash-registers.md).

Tämä esimerkki kuuluu Retail-ohjelmiston kehityspakettiin (SDK). Lisätietoja SDK:sta on kohdassa [Retail-kehityspaketin (SDK) arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Tämä esimerkki koostuu Commerce runtime (CRT)-, Retail Server- ja POS-laajennusosista. Voit suorittaa tämän näyteversion muokkaamalla ja rakentamalla CRT-, Retail Server- ja POS-projektit. Suosittelemme, että teet tässä aiheessa kuvatut muutokset käyttämällä Retail SDK -pakettia, jota ei ole muutettu. On myös suositeltavaa käyttää lähteenhallintajärjestelmää, kuten Microsoft Visual Studio Onlinea (VSO), jossa tiedostoja ei ole vielä muutettu.

> [!NOTE]
> Commerce 10.0.8:ssa tai sitä uudemmissa versioissa Retail Serveristä käytetään nimeä Commerce Scale Unit. Koska tämä ohjeaihe koskee sovelluksen useita aiempia versioita, *Retail Server* -nimeä käytetään koko ohjeaiheessa.
>
> Jotkin tämän ohjeaiheen vaiheet vaihtelevat käyttämäsi Commerce-version mukaan. Lisätietoja esitetään kohdassa [Dynamics 365 Retailin uudet ja muuttuneet ominaisuudet](../get-started/whats-new.md).

### <a name="using-certificate-profiles-in-commerce-channels"></a>Commerce-kanavien sertifikaattiprofiilien käyttäminen

Commerce-versioissa 10.0.15 ja sitä myöhemmissä versioissa voit käyttää [vähittäismyymälöiden käyttäjän määrittämiä sertifikaattiprofiileja](./certificate-profiles-for-retail-stores.md). Tämä ominaisuus tukee varatoimintaa offline-tilassa, kun Key Vault tai Commerce headquarters eivät ole käytettävissä. Tämä ominaisuus laajentaa [Vähittäismyynnin kanavien salaisuuksien hallinta](../dev-itpro/manage-secrets.md) -toimintoa.

Noudata näitä ohjeita, jotta voit käyttää tätä toimintoa CRT-laajennuksessa.

1. Luo uusi CRT-laajennusprojekti (C#-luokkakirjaston projektityyppi). Käytä Retail-ohjelmistokehityspaketin (SDK) näytemalleja (RetailSDK\SampleExtensions\CommerceRuntime).

2. Lisää mukautettu käsittelijä kohteelle CertificateSignatureServiceRequest SequentialSignatureRegister-projektissa.

3. Jos haluat lukea salaisuuden, kutsu `GetUserDefinedSecretCertificateServiceRequest` käyttäen konstruktoria, jossa on profileId-parametri. Tämä käynnistää toiminnon toimimaan sertifikaattiprofiilien asetusten kanssa. Asetusten perusteella sertifikaatti noudetaan joko Azure Key Vaultista tai paikallisen koneen tallennustilasta.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. Kun sertifikaatti noudetaan, jatka tietojen allekirjoitusta.

5. Muodosta CRT-laajennusprojekti.

6. Kopioi tulosluokkakirjasto ja liitä se kohtaan ...\RetailServer\webroot\bin\Ext manuaalista testausta varten.

7. Päivitä CommerceRuntime.Ext.config-tiedostossa laajennuksen kokoonpano-osaan mukautetun kirjaston tiedot.

## <a name="development-environment"></a>Kehitysympäristö

Suorita nämä toimenpiteet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa näytettä.

### <a name="the-crt-extension-components"></a>CRT-laajennuksen komponentit

CRT -laajennuskomponentit sisältyvät CRT-näytteisiin. Voit suorittaa seuraavat vaiheet avaamalla CRT-ratkaisun, valitsemalla **CommerceRuntimeSamples.sln** kohdassa **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>ReceiptsNorway-komponentti

1. Etsi **Runtime.Extensions.ReceiptsNorway**-projekti ja luo se.
2. Etsi **Extensions.ReceiptsNorway\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.ReceiptsNorway.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon Microsoft Internet Information Services (IIS) Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="salespaymenttransext-component"></a>SalesPaymentTransExt-komponentti

1. Etsi **Runtime.Extensions.SalesPaymentTransExt**-projekti ja luo se.
2. Etsi **Extensions.SalesPaymentTransExt\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="xzreportsnorway-component"></a>XZReportsNorway-komponentti

1. Etsi **Runtime.Extensions.XZReportsNorway**-projekti ja luo se.
2. Etsi **Extensions.XZReportsNorway\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.XZReportsNorway.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

# <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent-mallikomponentti

1. Etsi **Runtime.Extensions.RegisterAuditEventSample**-projekti ja luo se.
2. Etsi **Extensions.RegisterAuditEventSample\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature-näytekomponentti

1. Etsi **Runtime.Extensions.SalesTransactionSignatureSample**-projekti.
2. Muokkaa **App.config**-tiedostoa määrittämällä myyntitapahtumien allekirjoittamiseen käytettävän sertifikaatin allekirjoitus, myymälän sijainti ja myymälän nimi.
3. Muodosta projekti.
4. Etsi **Extensions.SalesTransactionSignatureSample\\bin\\Debug** -kansiosta seuraavat tiedostot:

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** -kokoonpanotiedosto
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** -määritystiedosto

5. Kopioi tiedostot CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

6. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

7. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

# <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent-mallikomponentti

1. Etsi **Runtime.Extensions.RegisterAuditEventSample**-projekti ja luo se.
2. Etsi **Extensions.RegisterAuditEventSample\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature-näytekomponentti

1. Etsi **Runtime.Extensions.SalesTransactionSignatureSample**-projekti.
2. Muokkaa **App.config**-tiedostoa määrittämällä myyntitapahtumien allekirjoittamiseen käytettävän sertifikaatin allekirjoitus, myymälän sijainti ja myymälän nimi.
3. Muodosta projekti.
4. Etsi **Extensions.SalesTransactionSignatureSample\\bin\\Debug** -kansiosta seuraavat tiedostot:

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** -kokoonpanotiedosto
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** -määritystiedosto

5. Kopioi tiedostot CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

6. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

7. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSignatureSample.Messages-komponentti

1. Etsi **Runtime.Extensions.SalesTransactionSignatureSample.Messages** -projekti.
2. Etsi **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent-mallikomponentti

1. Etsi **Runtime.Extensions.RegisterAuditEventSample**-projekti ja luo se.
2. Etsi **Extensions.RegisterAuditEventSample\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature-näytekomponentti

1. Etsi **Runtime.Extensions.SalesTransactionSignatureSample**-projekti.
2. Muokkaa **App.config**-tiedostoa määrittämällä myyntitapahtumien allekirjoittamiseen käytettävän sertifikaatin allekirjoitus, myymälän sijainti ja myymälän nimi.
3. Muodosta projekti.
4. Etsi **Extensions.SalesTransactionSignatureSample\\bin\\Debug** -kansiosta seuraavat tiedostot:

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** -kokoonpanotiedosto
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** -määritystiedosto

5. Kopioi tiedostot CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

6. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

7. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts-komponentti

1. Etsi **Runtime.Extensions.SequentialSignatureRegister.Contracts**-projekti.
2. Etsi **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.Messages.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent-mallikomponentti

1. Etsi **Runtime.Extensions.RegisterAuditEventSample**-projekti ja luo se.
2. Etsi **Extensions.RegisterAuditEventSample\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister-komponentti

1. Etsi **Runtime.Extensions.SequentialSignatureRegister**-projekti.
2. Muokkaa **App.config**-tiedostoa määrittämällä myyntitapahtumien allekirjoittamiseen käytettävän sertifikaatin allekirjoitus, myymälän sijainti ja myymälän nimi.
3. Muodosta projekti.
4. Etsi **Extensions.SequentialSignatureRegister\\bin\\Debug** -kansiosta seuraavat tiedostot:

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** -kokoonpanotiedosto
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** -määritystiedosto

5. Kopioi tiedostot CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

6. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

7. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway-komponentti

1. Etsi **Runtime.Extensions.SalesTransactionSignatureNorway**-projekti.
2. Etsi **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts-komponentti

1. Etsi **Runtime.Extensions.SequentialSignatureRegister.Contracts**-projekti.
2. Etsi **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.Messages.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway-komponentti

1. Etsi **Runtime.Extensions.SalesPaymentTransExtNorway**-projekti ja luo se.
2. Etsi **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway-komponentti

1. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

2. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister-komponentti

1. Etsi **Runtime.Extensions.SequentialSignatureRegister**-projekti.
2. Muokkaa **App.config**-tiedostoa määrittämällä myyntitapahtumien allekirjoittamiseen käytettävän sertifikaatin allekirjoitus, myymälän sijainti ja myymälän nimi.
3. Muodosta projekti.
4. Etsi **Extensions.SequentialSignatureRegister\\bin\\Debug** -kansiosta seuraavat tiedostot:

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** -kokoonpanotiedosto
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** -määritystiedosto

5. Kopioi tiedostot CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

6. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

7. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway-komponentti

1. Etsi **Runtime.Extensions.SalesTransactionSignatureNorway**-projekti.
2. Etsi **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts-komponentti

1. Etsi **Runtime.Extensions.SequentialSignatureRegister.Contracts**-projekti.
2. Etsi **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.Messages.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway-komponentti

1. Etsi **Runtime.Extensions.SalesPaymentTransExtNorway**-projekti ja luo se.
2. Etsi **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway-komponentti

1. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

2. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister-komponentti

1. Etsi **Runtime.Extensions.SequentialSignatureRegister**-projekti.
2. Muokkaa **App.config**-tiedostoa määrittämällä myyntitapahtumien allekirjoittamiseen käytettävän sertifikaatin allekirjoitus, myymälän sijainti ja myymälän nimi.
3. Muodosta projekti.
4. Etsi **Extensions.SequentialSignatureRegister\\bin\\Debug** -kansiosta seuraavat tiedostot:

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** -kokoonpanotiedosto
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** -määritystiedosto

5. Kopioi tiedostot CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

6. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

7. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway-komponentti

1. Etsi **Runtime.Extensions.SalesTransactionSignatureNorway**-projekti.
2. Etsi **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts-komponentti

1. Etsi **Runtime.Extensions.SequentialSignatureRegister.Contracts**-projekti.
2. Etsi **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.Messages.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway-komponentti

1. Etsi **Runtime.Extensions.SalesPaymentTransExtNorway**-projekti ja luo se.
2. Etsi **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto CRT-laajennuskansioon:

    - **Retail Server:** Kopioi kokoonpano **\\bin\\ext** -kansioon IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Kopioi kokoonpano **\\ext** -kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.

4. Etsi CRT-laajennuskonfigurointitiedosto:

    - **Retail Server:** Tiedoston nimi on **commerceruntime.ext.config** ja se on **bin\\ext** -kansiossa IIS Retail Server -sivuston sijainnissa.
    - **Paikallinen CRT Modern POS -sovelluksessa:** Tiedoston nimi on **CommerceRuntime.MPOSOffline.Ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

5. Rekisteröi CRT-muutos laajennuksen konfigurointitiedostoon.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Älä** muokkaa commerceruntime.config- tai CommerceRuntime.MPOSOffline.config-tiedostoja. Näitä tiedostoja ei ole tarkoitettu mukautuksille.

---

### <a name="the-retail-server-extension-components"></a>Retail Server -laajennuskomponentit

#### <a name="salestransactionsignature-retail-server-sample-component"></a>Retail Server -näytekomponentti SalesTransactionSignature

1. Etsi **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** -kansiosta **RetailServer.Extensions.SalesTransactionSignatureSample** -projekti ja muodosta se.
2. Etsi **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** -kansiosta **Contoso.RetailServer.SalesTransactionSignatureSample.dll** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedosto Retail Server -laajennuskansioon.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    Kansio on **\\bin**-kansiossa IIS Retail Server -sivuston sijainnissa.

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    Kansio on **\\bin**-kansiossa IIS Retail Server -sivuston sijainnissa.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Kansio on **\\bin\\ext**-kansiossa IIS Retail Server -sivuston sijainnissa.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    Kansio on **\\bin\\ext**-kansiossa IIS Retail Server -sivuston sijainnissa.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    Kansio on **\\bin\\ext**-kansiossa IIS Retail Server -sivuston sijainnissa.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    Kansio on **\\bin\\ext**-kansiossa IIS Retail Server -sivuston sijainnissa.

    ---

4. Etsi Retail Serverin konfigurointitiedosto. Tiedoston nimi on **web.config** ja se juurikansiossa IIS Retail Server -sivuston sijainnissa.
5. Rekisteröi Retail Server -laajennukset konfigurointitiedoston **extensionComposition**-osaan.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Rekisteröi Retail Server -laajennusten riippuvuudet.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4/)

    1. Etsi **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** -kansiosta seuraavat tiedostot:

        - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** -kokoonpanotiedosto
        - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** -määritystiedosto

    2. Kopioi tiedostot **\\bin**-kansioon IIS Retail Server -sivuston sijainnissa.
    3. Rekisteröi CRT-muutos laajennuksen CRT-konfigurointitiedostoon. Tiedoston nimi on **commerceruntime.ext.config** ja se **bin**-kansiossa IIS Retail Server -sivuston sijainnissa.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later/)

    1. Etsi **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** -kansiosta **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** -kokoonpanotiedosto.
    2. Kopioi tiedosto **\\bin**-kansioon IIS Retail Server -sivuston sijainnissa.
    3. Rekisteröi CRT-muutos laajennuksen CRT-konfigurointitiedostoon. Tiedoston nimi on **commerceruntime.ext.config** ja se **bin**-kansiossa IIS Retail Server -sivuston sijainnissa.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Toimintoja ei edellytetä.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    > [!NOTE]
    > Toimintoja ei edellytetä.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    > [!NOTE]
    > Toimintoja ei edellytetä.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    > [!NOTE]
    > Toimintoja ei edellytetä.

    ---

### <a name="the-modern-pos-extension-components"></a>Modern POS -laajennuksen komponentit

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Ota käyttöön offline-tilan välityspalvelinkoodi

Tämä osa vastaa Retail Server -ohjainta, mutta se laajentaa paikallisen CRT:n, jota käytetään, kun asiakasohjelmaa ei ole yhdistetty.

1. Muuta **customization.settings** -tiedostossa **@(RetailServerLibraryPathForProxyGeneration)** -osaa niin, että se käyttää uutta Retail Server -kokoonpanoa välityspalvelinten luonnissa.
2. Ota käyttöön seuraavat liittymämenetelmät **StoreOperationsManager**-luokassa. Lisää ensimmäiseen iteraatioon seuraava koodi:

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    ---

3. Voit muodostaa välityspalvelinkoodin uudelleen rakentamalla **Proxies**-kansion komentoriviltä käyttämällä **msbuild /t:Rebuild** -komentoa.
4. Ratkaise **Proxies.RetailProxy**-projektin riippuvuudet:

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    Avaa **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, lisää **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** -projekti ratkaisuun ja lisää projektiviite **RetailProxy**-projektiin viitteeseen **SalesTransactionSignatureSample**.

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    Avaa **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, lisää **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** -projekti ratkaisuun ja lisää projektiviite **RetailProxy**-projektiin viitteeseen **SalesTransactionSignatureSample.Messages**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    ---

5. Muuta liittymämenetelmät **StoreOperationsManager**-luokassa:

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    > [!NOTE]
    > Tämä vaihe ei koske tätä versiota.

    ---

6. Päivitä **dllhost.exe.config**-tiedosto niin, että asiakkaan välittäjä lataa uuden RetailProxy-kokoonpanon.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Retail-välityspalvelimen laajennuskomponentti (Retail 7.3.1 ja sitä myöhemmät)

Tee seuraava toimenpide vain, jos käytät Retail 7.3.1-sovellusta tai uudempaa versiota.

1. Etsi **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** -kansiosta **RetailServer.Extensions.SalesTransactionSignatureSample** -projekti ja muodosta se.
2. Etsi **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** -kansiosta **Contoso.RetailProxy.SalesTransactionSignatureSample** -kokoonpanotiedosto.
3. Kopioi kokoonpanotiedostot **\\ext**-kansioon paikallisen CRT-asiakasvälittäjän sijainnissa.
4. Rekisteröi Retail-välityspalvelimen muutos laajennuksen konfigurointitiedostoon. Tiedoston nimi on **RetailProxy.MPOSOffline.ext.config** ja se sijaitsee paikallisen CRT-asiakkaan välittäjän sijainnin alla.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Modern POS -laajennuskomponentit

1. Avaa ratkaisu kohdassa **RetailSdk\\POS\\ModernPOS.sln** ja varmista, että se voidaan kääntää virheettä Varmista myös, että voit suorittaa Modern POS -sovelluksen Microsoft Visual Studiosta **Run**-komennon avulla.

    > [!NOTE]
    > Modern POS -sovellusta ei saa mukauttaa. Käyttäjätilien valvonta (UAC) on otettava käyttöön, ja aiemmin asennettujen Modern POS -instanssien asennus täytyy poistaa.

2. Sisällytä seuraavat aiemmin luodut lähdekoodikansiot **Pos.Extensions**-projektiin.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Ota käännettävät laajennukset käyttöön **tsconfig.json**-tiedostoissa poistamalla seuraavat kansiot poissulkevasta luettelosta.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Salli laajennusten lataaminen **extensions.json**-tiedostoon lisäämällä seuraavat rivit oikeaan paikkaan.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Lisätietoja sekä esimerkkejä, jotka näyttävät lähdekoodikansioiden lisäämisen ja laajennusten lataamisen, on **Pos.Extensions**-projektin readme.md-tiedoston ohjeissa.

5. Luo ratkaisu uudelleen.
6. Suorita Modern POS virheenkorjaustyökalussa ja testaa toiminto.

### <a name="cloud-pos-extension-components"></a>Cloud POS -laajennuskomponentit

1. Avaa ratkaisu kohdassa **RetailSdk\\POS\\CloudPOS.sln** ja varmista, että se voidaan kääntää virheettä
2. Sisällytä seuraavat aiemmin luodut lähdekoodikansiot **Pos.Extensions**-projektiin.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Ota käännettävät laajennukset käyttöön **tsconfig.json**-tiedostoissa poistamalla seuraavat kansiot poissulkevasta luettelosta.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Salli laajennusten lataaminen **extensions.json**-tiedostoon lisäämällä seuraavat rivit oikeaan paikkaan.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Lisätietoja sekä esimerkkejä, jotka näyttävät lähdekoodikansioiden lisäämisen ja laajennusten lataamisen, on **Pos.Extensions**-projektin readme.md-tiedoston ohjeissa.

5. Luo ratkaisu uudelleen.
6. Suorita ratkaisu Käyttämällä **Run**-komentoa ja noudattamalla Retail SDK -käsikirjan ohjeita.
7. Testaa toiminnallisuus.

### <a name="set-up-required-parameters-in-headquarters"></a>Määritä tarvittavat parametrit Headquartersissa

Lisätietoja on kohdassa [Kassakoneen toiminnot, Norja](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>Tuotantoympäristö

Luo Commerce-komponentteja sisältävät käyttöön otettavat paketit ja ota paketit käyttöön tuotantoympäristössä noudattamalla näitä ohjeita.

1. Noudata aiemmin tässä ohjeaiheessa olevassa [Cloud POS -laajennusosien](#cloud-pos-extension-components) tai [Modern POS -laajennusosien](#modern-pos-extension-components) osissa olevia vaiheita.
2. Tee seuraavat muutokset **RetailSdk\\Assets**-kansion paketin konfiguraatiotiedostoihin:

    1. Lisää **commerceruntime.ext.config**- ja **CommerceRuntime.MPOSOffline.Ext.config**-määritystiedostoihin seuraavat rivit **composition**-osaan:

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Ota Commerce Proxy -mukautus käyttöön:

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        Lisää **dllhost.exe.config** -määritystiedostossa seuraavat rivit **appSettings**-aliosaan **configuration**-osassa.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

        Lisää **dllhost.exe.config** -määritystiedostossa seuraavat rivit **appSettings**-aliosaan **configuration**-osassa.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Lisää **RetailProxy.MPOSOffline.ext.config**-konfigurointitiedostossa seuraavat rivit **composition**-osaan:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

        Lisää **RetailProxy.MPOSOffline.ext.config**-konfigurointitiedostossa seuraavat rivit **composition**-osaan:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

        Lisää **RetailProxy.MPOSOffline.ext.config**-konfigurointitiedostossa seuraavat rivit **composition**-osaan:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

        Lisää **RetailProxy.MPOSOffline.ext.config**-konfigurointitiedostossa seuraavat rivit **composition**-osaan:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Tee seuraavat muutokset **Customization.settings**-paketin mukautusmääritystiedostoon:

    1. Ota Retail Proxy -mukautus käyttöön.

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        Lisää seuraavat rivit **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** -osaan.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

        Lisää seuraavat rivit **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** -osaan.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Lisää seuraavat rivit **ItemGroup**-osaan, jos haluat sisällyttää Retail Proxy -laajennuksen käyttöön otettaviin paketteihin:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

        Lisää seuraavat rivit **ItemGroup**-osaan, jos haluat sisällyttää Retail Proxy -laajennuksen käyttöön otettaviin paketteihin:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

        Lisää seuraavat rivit **ItemGroup**-osaan, jos haluat sisällyttää Retail Proxy -laajennuksen käyttöön otettaviin paketteihin:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

        Lisää seuraavat rivit **ItemGroup**-osaan, jos haluat sisällyttää Retail Proxy -laajennuksen käyttöön otettaviin paketteihin:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Lisää seuraavat rivit **ItemGroup**-osaan, jos haluat sisällyttää CRT-laajennukset käyttöön otettaviin paketteihin:

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Lisää seuraavat rivit **ItemGroup**-osaan, jos haluat sisällyttää Retail Server -laajennuksen käyttöön otettaviin paketteihin:

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Muokkaa seuraavia tiedostoja, kun haluat sisällyttää Norjan resurssitiedostot käyttöön otettaviin paketteihin:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - **Sdk.ModernPos.Shared.csproj**-tiedostolle 
    - Lisää rivi **ItemGroup**-osaan
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > Korvaa <File_name> resurssitiedoston nimellä. Sama koskee myös muita jäljempänä annettuja esimerkkejä.
 
    - Lisää rivi **Target Name="CopyPackageFiles"** -osaan
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - **Sdk.RetailServerSetup.proj**-tiedostolle 
    - Lisää rivi **ItemGroup**-osaan
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Lisää rivi **Target Name="CopyPackageFiles"** -osaan
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Muokkaa sertifikaatin määritystiedostoa määrittämällä myyntitapahtumien allekirjoittamiseen käytettävän sertifikaatin allekirjoitus, myymälän sijainti ja myymälän nimi. Kopioi sitten konfigurointitiedosto **Viitteet**-kansioon.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    Tiedoston nimi on **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** ja se on kohdassa **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="application-update-5-and-later"></a>[Sovelluspäivitys 5 ja uudemmat](#tab/app-update-5-and-later)

    Tiedoston nimi on **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** ja se on kohdassa **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Tiedoston nimi on **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** ja se on kohdassa **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ja uudemmat versiot](#tab/retail-7-3-2)

    Tiedoston nimi **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** ja se on kohdassa **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ja uudemmat versiot](#tab/retail-7-3-5)

    Tiedoston nimi **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** ja se on kohdassa **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ja uudemmat versiot](#tab/retail-8-1-1)

    Tiedoston nimi **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** ja se on kohdassa **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    ---

6. Päivitä Retail Serverin konfigurointitiedosto. Lisää **RetailSDK\\Packages\\RetailServer\\Code\\web.config** -tiedostossa seuraavat rivit **extensionComposition**-osaan.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Luo käyttöön otettavat paketit ajamalla koko Retail SDK -sovelluksen **msbuild**.
8. Ota paketit käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) kautta tai manuaalisesti. Lisätietoja on ohjeaiheessa [Käyttöönottopakettien luominen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Ota digitaalinen allekirjoitus käyttöön offline-tilassa Modern POS -sovelluksessa

Jos haluat ottaa digitaalisten allekirjoituksen käyttöön offline-tilassa Modern POS -sovellusta varten, noudata näitä ohjeita, kun olet aktivoinut Modern POS:n uudella laitteella.

1. Kirjaudu sisään POS:ään.
2. Varmista **Tietokantayhteyden tila** -sivulla, että offline-tietokanta on täysin synkronoitu. Kun **Odottavat lataukset** kentän arvo on **0** (nolla), tietokanta on täysin synkronoitu.
3. Kirjaudu ulos myyntipisteestä.
4. Odota, kunnes offline-tietokanta synkronoidaan täysin.
5. Kirjaudu sisään POS:ään.
6. Varmista **Tietokantayhteyden tila** -sivulla, että offline-tietokanta on täysin synkronoitu. Kun **Offline-tietokannan odottavat tapahtumat** kentän arvo on **0** (nolla), tietokanta on täysin synkronoitu.
7. Käynnistä Modern POS uudelleen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
