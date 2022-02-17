---
title: Näyte verotusta varten olevan tulostimen integroinnista Puolassa
description: Tämä ohjeaihe on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Puola).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 43d9a54334d97a65a1f9a356daf54154f6c069b3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076833"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Näyte verotusta varten olevan tulostimen integroinnista Puolassa

[!include[banner](../includes/banner.md)]

Tämä ohjeaihe on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Puola).

Puolan Dynamics 365 Commerce -toiminnot sisältävät esimerkki-integroinnit myyntipisteestä verotulostimeen. Esimerkki laajentaa [verointegraation toimintoja](fiscal-integration-for-retail-channel.md) ja tukee [Posnet Polska S.A](https://www.posnet.com.pl):n verotulostimia varten POSNET THERMAL HD 2.02 -protokollaa. Esimerkki ottaa käyttöön tietoliikenteen verotulostimen kanssa, joka on yhdistetty COM-portin kautta alkuperäisen ohjelmistoajurin avulla. Se on otettu käyttöön ja testattu käyttäen Posnetin Posnet Thermal HD FV EJ -verotulostinta varten toimittamaa ohjelmistoemulaattoria. Näyte toimitetaan lähdekoodin muodossa, ja se on osa Retail-ohjelmiston kehityssarjaa (SDK).

Microsoft ei julkaise Posnetin laitteistoja, ohjelmistoja tai dokumentaatioita. Jos haluat lisätietoja verotulostimen hankkimisesta ja käyttämisestä, ota yhteyttä [Posnet Polska S.A:han.](https://www.posnet.com.pl)

## <a name="scenarios"></a>Skenaariot

Seuraavat skenaariot ovat Puolan verotulostimen integrointiesimerkistä:

- Myyntiskenaariot:

    - Tulosta käteismyynnin ja palautusten verokuitti.
    - Tallenna vastaus verotulostimesta ja tallenna se kanavatietokantaan.
    - Verot:

        - Liitä verotulostimen verokoodeihin (osastot).
        - Siirrä liitetyt verotiedot verotulostimeen.

    - Maksut:

        - Liitä verotulostimen maksutapoihin.
        - Tulosta maksut verokuitteihin.
        - Tulosta muutostiedot.

    - Tulosta rivialennukset.
    - Lahjakortit:

        - Jättää myönnetyn/uudelleen ladatun lahjakortin rivin pois myynnin verokuitista.
        - Tulosta maksu, joka käyttää lahjakorttia tavallisena maksutapana.

    - Tulosta asiakkaan tilaustoimintojen verokuitit:

        - Asiakkaan tilaustalletukseen ei tulosteta verokuittia.
        - Tulosta verokuitti hybridiasiakastilauksen myymäläostoriveille.
        - Tulosta asiakkaan tilauksen noutotoiminnon verokuitti.
        - Tulosta palautustilauksen verokuitti.

    - Tulosta verokuitin myyntitapahtumalle määritetyt [asiakastiedot](emea-pol-customer-information.md). Näistä tiedoista on esimerkkinä asiakkaan ALV-numero.

- Päivän lopun tiliotteet (kirjanpidon X- ja Z-raportit).
- Virheiden käsittely, esimerkiksi seuraavat vaihtoehdot:

    - Yritä uudelleen verorekisteröintiä esimerkiksi silloin, kun verotulostinta ei ole liitetty, ei ole valmis tai se ei vastaa, tulostimessa ei ole paperia tai siinä on paperitukos.
    - Lykkää kirjanpidon rekisteröintiä.
    - Ohita verorekisteröinti tai merkitse tapahtuma rekisteröidyksi ja sisällytä tietokoodit, jotka poimivat virheen syyn ja lisätiedot.
    - Tarkista verotulostimen käytettävyys ennen uuden myyntitapahtuman avaamista tai myyntitapahtuman viimeistelyä.

### <a name="gift-cards"></a>Lahjakortit

Verotulostimen integrointiesimerkki toteuttaa seuraavia lahjakortteihin liittyviä sääntöjä:

- Sulje verokuitista pois myyntirivit, jotka liittyvät *Myönnä lahjakortti*- ja *Lisää lahjakorttiin* -toimintoihin.
- Verokuittia ei tulosteta, jos se koostuu vain lahjakorttiriveistä.
- Vähennä tapahtumassa myönnettyjen tai uudelleen ladattujen lahjakorttien kokonaissumma verokuitin maksuriveistä.
- Tallenna maksurivien lasketut oikaisut kanavatietokantaan ja viittaus vastaavaan kirjanpitotapahtumaan.
- Lahjakortilla maksamista pidetään tavallisena maksuna.

### <a name="customer-deposits-and-customer-order-deposits"></a>Asiakastalletukset ja asiakastilausten talletukset

Verotulostimen integrointiesimerkissä otetaan käyttöön seuraavat säännöt, jotka liittyvät asiakastalletukseen ja asiakastilaustalletuksiin:

- Verokuittia ei tulosteta, jos tapahtuma on asiakastalletus.
- Älä tulosta verokuittia, jos tapahtuma sisältää vain asiakastilaustalletuksen tai asiakastilauksen talletushyvityksen.
- Tulosta asiakkaan tilauksen noutotoiminnon verokuitille aikaisemmin maksetun talletuksen summa.
- Vähennä asiakkaan tilauksen talletussumma maksuriveiltä, kun hybridiasiakastilaus luodaan.
- Tallenna maksurivien lasketut oikaisut kanavatietokantaan ja viittaus vastaavaan hybridiasiakastilauksen kirjanpitotapahtumaan.

### <a name="limitations-of-the-sample"></a>Esimerkin rajoitukset

- Verotulostin tukee vain skenaarioita, joissa arvonlisävero sisältyy hintaan. Siksi **Hinta sisältää arvonlisäveron** -asetuksen on oltava **Kyllä** sekä myymälöille että asiakkaille.
- Päivittäiset raportit (X- ja Z-kirjanpitoraportit) tulostetaan käyttämällä upotettua *Vuororaportti*-muotoa.
- Verokuitteihin viivakoodin tulostaminen on mahdollinen mukautus, koska toimintoa ei tueta upotetuissa muodoissa, ja se voidaan ottaa käyttöön vain mukautettavissa olevan **Super-muoto**-raportin avulla.
- Verotulostin ei tue yhdistettyjä tapahtumia. **Myyntien ja palautusten yhdistelmän estäminen yhdessä kuitissa** -vaihtoehdossa tulee määrittää **Kyllä** POS-toimintoprofiileissa.

## <a name="set-up-fiscal-integration-for-poland"></a>Kirjanpidon integroinnin määrittäminen (Puola)

Puolan verotulostimen esimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Retail SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\Posnet** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä (esim. [julkaisun 9.33 esimerkki](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta, joka on Commerce runtimen (CRT) ja veroliittimen laajennus, joka on Commerce Hardware Stationin laajennus. Lisätietoja Retail SDK:n käytöstä on kohdissa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Määritä itsenäisen pakkaus-SDK:n koontiversioputki](../dev-itpro/build-pipeline.md).

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja: [Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Puola) (vanha)](emea-pol-fpi-sample-sdk.md).
>
> Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

Suorita verointegraation määritysvaiheet [Commerce-kanavien kirjanpidon integroinnin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md) -kohdassa kuvatulla tavalla.

1. [Kirjanpidon rekisteröintiprosessin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ota myös huomioon verorekisteröintiprosessin asetukset, jotka [liittyvät tähän verotulostimen integraatioesimerkkiin](#set-up-the-registration-process).
1. [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Kirjanpidon X/Z-raporttien määrittäminen myyntipisteessä](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Ota käyttöön lykätyn tilikausirekisteröinnin manuaalinen käyttö](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Määritä kanavakomponentit](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Rekisteröintiprosessin määrittäminen

Voit ottaa rekisteröintiprosessin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita. Lisätietoja on kohdassa [Commerce-kanavan verointegroinnin määritys](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lataa kirjanpidon yhdistimien ja kirjanpitoasiakirjan toimittajien määritystiedostot.

    1. Avaa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilö.
    1. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan (esim. **[julkaisu 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avaa **src \> FiscalIntegration \> Posnet**.
    1. Lataa veroasiakirjan tarjoajan konfigurointitiedosto kohdasta **CommerceRuntime \> DocumentProvider.PosnetSample \> Configuration \> DocumentProviderPosnetSample.xml** (esim. [julkaisun 9.33 tiedosto](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)).
    1. Lataa veroliittimen konfiguraatiotiedosto kohdasta **HardwareStation \> ThermalDeviceSample \> Configuration \> ConnectorPosnetThermalFVEJ.xml** (esim. [julkaisun 9.33 tiedosto](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)).

    > [!WARNING]
    > [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Tämän verointegraatioesimerkin konfiguraatiotiedostot sijaitsevat seuraavissa Retail SDK -sovelluksen kansioissa kehittäjän virtuaalikoneessa LCS:ssä:
    >
    > - **Veroasiakirjan tarjoajan konfigurointitiedosto:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **Veroyhdistimen konfigurointitiedosto:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml
    > 
    > Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan jaetut parametrit**. Määritä **Yleiset**-pikavälilehdessä **Ota kirjanpidon integrointi käyttöön**-asetukseksi **Kyllä**.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpitoasiakirjan toimittajat**, ja lataa aiemmin lataamasi kirjanpitoasiakirjan toimittajan konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistimet**, ja lataa aiemmin lataamasi kirjanpidon yhdistimen konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen toiminnalliset profiilit**. Luo uusi yhdistimen toimintoprofiili. Valitse tiedoston tarjoaja ja aiemmin ladattu liitin. Päivitä [tietojen määritysasetukset](#default-data-mapping) tarvittaessa.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen tekniset profiilit**. Luo uusi liittimen tekninen profiili ja valitse aiemmin ladattu veroliitin. Päivitä [yhdistimen asetukset](#fiscal-connector-settings) tarvittaessa.
6. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmät**. Luo uusi veroliitinryhmä aiemmin luomallesi liittimen toimintoprofiilille.
7. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**. Luo uusi kirjanpidon rekisteröintiprosessi ja verorekisteröintiprosessi vaihe ja valitse aiemmin luomasi kirjanpidon yhdistinryhmä.
8. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**. Valitse siihen myymälään linkitetty toimintoprofiili, jossa rekisteröintiprosessi tulee aktivoida. Valitse **Kirjanpidon rekisteröintiprosessi** -pikavälilehdessä aiemmin luomasi kirjanpidon rekisteröintiprosessi.
9. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Laiteprofiilit**. Valitse Hardware stationiin liitetty laiteprofiili, johon verotulostin liitetään. Valitse **Kirjanpidon oheislaitteet** -pikavälilehdessä aiemmin luomasi liittimen tekninen profiili.
10. Avaa jakeluaikataulu (**Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**) ja valitse työt **1070** ja **1090** siirtääksesi tiedot kanavatietokantaan.

#### <a name="default-data-mapping"></a>Tietojen oletusmääritys

Seuraavat tietojen oletusmääritykset sisältyvät veroasiakirjan tarjoajan konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **Arvonlisäveroprosenttien määrittäminen** – Arvonlisäverokoodeille määritettyjen veroprosenttiarvojen yhdistämismääritys verotulostinkohtaisille ALV-veroprosenteille. Tässä on oletusmääritys:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Kunkin parin ensimmäinen komponentti edustaa verotulostimelle määritettyä arvonlisäveroprosenttia. Toinen komponentti edustaa vastaavaa arvonlisäveroprosenttia. Lisätietoja verotulostimen ALV-prosentin konfiguroinnista on POSNET-ohjaimen ohjeissa.

- **Maksuvälinetyypin määritys** – Myymälälle määritettyjen maksutapojen yhdistämismääritys verotulostimen tukemille maksumuodoille. Tässä on oletusmääritys:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Kunkin parin ensimmäinen komponentti edustaa myymälälle määritettyä maksutapaa. Toinen komponentti edustaa vastaavaa maksumuotoa, jota verotulostin tukee. Lisätietoja verotulostimen tukemista maksumuodoista on POSNET-ohjaimen ohjeissa. Esimerkkiyhdistämismääritystä on muokattava sovelluksessa konfiguroitujen maksutapojen mukaan.

#### <a name="fiscal-connector-settings"></a>Veroliittimen asetukset

Seuraavat asetukset sisältyvät veroyhdistimen konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **Yhteysmerkkijono** – Merkkijono, joka kuvaa laiteyhteyden tietoja ohjaimen tukemassa muodossa. Lisätietoja on POSNET-ohjaimen dokumentaatiossa.
- **Päivämäärän ja ajan synkronointi** – Arvo, joka määrittää, synkronoidaanko tulostimen päivämäärä ja aika liitetyn Hardware stationin kanssa.
- **Laiteen aikakatkaisu** – Aika millisekunteina, jonka ajuri odottaa laitteen vastausta. Lisätietoja on POSNET-ohjaimen dokumentaatiossa.

### <a name="configure-channel-components"></a>Määritä kanavakomponentit

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Puola) (vanha)](emea-pol-fpi-sample-sdk.md).
>
> Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

#### <a name="set-up-the-development-environment"></a>Kehitysympäristön määrittäminen

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa esimerkkiä.

1. Kloonaa tai lataa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilö. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan. Lisätietoja: [Retail SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja NuGetista](../dev-itpro/retail-sdk/sdk-github.md).
1. Avaa verotulostimen integraatioratkaisu kohdassa **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln** ja muodosta se.
1. Asenna CRT-laajennukset:

    1. Etsi CRT-laajennuksen asennusohjelma:

        - **Commerce Scale Unit:** Etsi **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461** -kansiosta **ScaleUnit.Posnet.Installer**-asennusohjelma.
        - **Paikallinen CRT Modern POS -sovelluksessa:** Etsi **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461** -kansiosta **ModernPOS.Posnet.Installer**-asennusohjelma.

    1. Käynnistä CRT-laajennusten asennusohjelma komentoriviltä:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Paikallinen CRT Modern POS -sovelluksessa:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Asenna Hardware station -laajennukset:

    1. Etsi **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461** -kansiosta **HardwareStation.PosnetThermalFVFiscalPrinter.Installer** -asennusohjelma.
    1. Käynnistä laajennusten asennusohjelma komentoriviltä:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tuotantoympäristö

Luo ja julkaise verointegraatioesimerkin Cloud Scale Unit ja itsepalveluna käyttöönotettavat paketit noudattamalla [Määritä koontijakso verointegraatioesimerkille](fiscal-integration-sample-build-pipeline.md) -ohjeen vaiheita. **Posnet build-pipeline.yml**-niminen YAML-mallitiedosto löytyy **Pipeline\\YAML_Files** -kansiosta[Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilöstä.

## <a name="design-of-extensions"></a>Laajennusten rakenne

Puolan verotulostimen esimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Retail SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\Posnet** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä (esim. [julkaisun 9.33 esimerkki](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta, joka on CRT:n ja veroliittimen laajennus, joka on Commerce Hardware Stationin laajennus. Lisätietoja Retail SDK:n käytöstä on kohdissa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Määritä itsenäisen pakkaus-SDK:n koontiversioputki](../dev-itpro/build-pipeline.md).

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Puola) (vanha)](emea-pol-fpi-sample-sdk.md). Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime -laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda tulostinkohtaisia asiakirjoja ja käsitellä verotulostimen vastauksia. Tämä laajennus luo tulostinkohtaiset JavaScript Object Notation (JSON) -muodossa, joka on määritelty POSNET-määrityksessä 19-3678.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**DocumentProviderPosnetProtocol**-pyyntökäsittelijä on asiakirjan luontipyynnön aloituspiste verotulostimelle.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa tulostinkohtaisen asiakirjan, jotka on rekisteröitävä verotulostimeen.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Tällä hetkellä seuraavat tapahtumat ovat tuettuja: myynti, X-raportin tulostaminen ja Z-raportin tulostaminen.

#### <a name="configuration"></a>Konfigurointi

Veroasiakirjan tarjoajan konfiguraatiotiedosto sijaitsee kohdassa  **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml** [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tämän tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla verotiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verotulostimen kanssa. Tämä laajennus kutsuu POSNET-ohjaimen toimintoja lähettämällä komennot, jotka CRT-laajennus luo verotulostimelle. Se käsittelee myös laitteen virheet.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**FiscalPrinterHandler**-pyyntökäsittelijä on oheislaitteen pyyntöjen käsittelyn aloituspiste.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä:

- **SubmitDocumentFiscalDeviceRequest** – Tämä pyyntö lähettää asiakirjoja tulostimille ja palauttaa vastauksen verotulostimesta.
- **IsReadyFiscalDeviceRequest** – Tätä pyyntöä käytetään laitteen kunnon tarkastusta varten.
- **InitializeFiscalDeviceRequest** – Tätä pyyntöä käytetään tulostimen alustamiseen.

#### <a name="configuration"></a>Konfigurointi

Veroliittimen konfiguraatiotiedosto sijaitsee kohdassa **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla veroyhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
