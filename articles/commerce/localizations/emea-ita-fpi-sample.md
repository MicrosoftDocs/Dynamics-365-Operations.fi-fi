---
title: Näyte verotusta varten olevan tulostimen integroinnista Italiassa
description: Tämä ohjeaihe on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Italia).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 02226fd9f2c92db2518ca48baefb680a3d2f0ac1
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076900"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Näyte verotusta varten olevan tulostimen integroinnista Italiassa

[!include[banner](../includes/banner.md)]

Tämä ohjeaihe on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Italia).

Italian Commerce-toiminnot sisältävät esimerkki-integroinnit myyntipisteestä verotulostimeen. Esimerkki laajentaa [verointegraation toimintoja](fiscal-integration-for-retail-channel.md) siten, että se toimii [Epson FP-90III Series](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) -tulostimen kanssa ja mahdollistaa tietoliikenteen verotulostimen kanssa verkkopalvelintilassa EpsonFPMate-verkkopalvelun kautta käyttäen Fiscal ePOS-Print API -ohjelmointirajapintaa. Esimerkki tukee vain Registratore Telematico (RT) -tilaa. Näyte toimitetaan lähdekoodin muodossa, ja se on osa Retail-ohjelmiston kehityssarjaa (SDK).

Microsoft ei julkaise Epsonin laitteistoja, ohjelmistoja tai dokumentaatioita. Jos haluat lisätietoja verotulostimen hankkimisesta ja käyttämisestä, ota yhteyttä [Epson Italia S.p.A:han.](https://www.epson.it)

## <a name="scenarios"></a>Skenaariot

Seuraavat skenaariot ovat Italian verotulostimen integrointiesimerkistä:

- Myyntiskenaariot:

    - Tulosta käteismyynnin ja palautusten verokuitti.
    - Tallenna vastaus verotulostimesta ja tallenna se kanavatietokantaan.
    - Verot:

        - Liitä verotulostimen verokoodeihin (osastot).
        - Siirrä liitetyt verotiedot verotulostimeen.
        - Tulosta verot verokuitteihin.

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

    - Tulosta verokuitin kuittinumeron viivakoodi.
    - Tulosta verokuitin myyntitapahtumalle määritetyt [asiakastiedot](emea-ita-customer-information.md). Näistä tiedoista on esimerkkinä asiakkaan koodi. 

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
- Päivittäiset raportit (X- ja Z-kirjanpitoraportit) tulostetaan käyttäen verotulostimen laitteisto-ohjelmistoon upotettua muotoa.
- Verotulostin ei tue yhdistettyjä tapahtumia. **Myyntien ja palautusten yhdistelmän estäminen yhdessä kuitissa** -vaihtoehdossa tulee määrittää **Kyllä** POS-toimintoprofiileissa.
- Esimerkki tukee integrointia vain sellaisen verotulostimen kanssa, joka toimii Registratore Telematico (RT) -tilassa.

## <a name="set-up-fiscal-integration-for-italy"></a>Kirjanpidon integroinnin määrittäminen (Italia)

Italian verotulostimen esimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Retail SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\EpsonFP90IIISample** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä (esim. [julkaisun 9.33 esimerkki](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta, joka on Commerce runtimen (CRT) ja veroliittimen laajennus, joka on Commerce Hardware Stationin laajennus. Lisätietoja Retail SDK:n käytöstä on kohdissa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Määritä itsenäisen pakkaus-SDK:n koontiversioputki](../dev-itpro/build-pipeline.md).

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja: [Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Italia) (vanha)](emea-ita-fpi-sample-sdk.md).
>
> Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

Suorita verointegraation määritysvaiheet [Commerce-kanavien kirjanpidon integroinnin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md) -kohdassa kuvatulla tavalla.

1. [Kirjanpidon rekisteröintiprosessin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ota myös huomioon verorekisteröintiprosessin asetukset, jotka [liittyvät tähän verotulostimen integraatioesimerkkiin](#set-up-the-registration-process).
1. [Alennusten kirjanpitotekstien määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Kirjanpidon X/Z-raporttien määrittäminen myyntipisteessä](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Ota käyttöön lykätyn tilikausirekisteröinnin manuaalinen käyttö](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Määritä myyntipisteen asiakastietojen hallinnan toiminnot](emea-ita-customer-information.md#setup).
1. [Määritä kanavakomponentit](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Rekisteröintiprosessin määrittäminen

Voit ottaa rekisteröintiprosessin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita. Lisätietoja on kohdassa [Commerce-kanavan verointegroinnin määritys](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lataa kirjanpidon yhdistimien ja kirjanpitoasiakirjan toimittajien määritystiedostot.

    1. Avaa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilö.
    1. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan (esim. **[julkaisu 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avaa **src \> FiscalIntegration \> EpsonFP90IIISample**.
    1. Lataa veroasiakirjan tarjoajan konfigurointitiedosto kohdasta **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Configuration \> DocumentProviderEpsonFP90IIISample.xml** (esim. [julkaisun 9.33 tiedosto](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)).
    1. Lataa veroliittimen konfiguraatiotiedosto kohdasta **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Configuration \> ConnectorEpsonFP90IIISample.xml** (esim. [julkaisun 9.33 tiedosto](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml).

    > [!WARNING]
    > [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Tämän verointegraatioesimerkin konfiguraatiotiedostot sijaitsevat seuraavissa Retail SDK -sovelluksen kansioissa kehittäjän virtuaalikoneessa LCS:ssä:
    >
    > - **Veroasiakirjan tarjoajan konfigurointitiedosto:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml
    > - **Veroyhdistimen konfigurointitiedosto:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml
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

- **Maksuvälinetyypin määritys** – Myymälälle määritettyjen maksutapojen yhdistämismääritys verotulostimen tukemille maksutyypeille. Seuraavassa esimerkissä näkyy oletusarvoinen yhdistämismääritys.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Tässä on kyseisen esimerkin määritteiden selitys:

    - **StorePaymentMethod** on maksutapa, joka määritetään myymälälle kohdassa **Retail ja Commerce \> Kanavan asetukset \> Maksutavat \> Maksutavat**.
    - **PrinterPaymentType** ja **PrinterPaymentIndex** ovat vastaava maksutyyppi ja indeksi, jotka on määritetty Epson-verotulostimen dokumentaatiossa.
    - **DepositPaymentMethod**-määrityksen avulla määritetään tulostimen maksutyyppi ja indeksi asiakastilauksen noutosumman osalle, joka täsmäytetään asiakastilauksen talletuksen yhteydessä.

    Seuraavan taulukon maksutapojen esimerkkiyhdistämismääritys vastaa vakio-esittelytiedoissa konfiguroidun myymälän maksutapoja.

    | Maksutapa | Maksutavan nimi |
    |----------------|---------------------|
    | 1              | Maksu                |
    | 3              | Kortti                |
    | 4              | Asiakastili    |
    | 6              | Valuutta            |
    | 8              | Lahjakortti           |

    Esimerkkiyhdistämismääritystä on muokattava sovelluksessa konfiguroitujen maksutapojen mukaan.

- **Kuittinumeron viivakoodityyppi** – Viivakoodin tyyppi, jota käytetään verokuitin numeron näyttämiseen. Oletusmääritys on **CODE128**.
- **Tulosta kirjanpitotiedot kuitin otsikkoon** – Jos tämä parametri on käytössä, myymälän tiedot tulostetaan verokuittiin. Näitä tietoja ovat myymälän nimi, osoite, verotunnus ja kassanhoitajan nimi.
- **Verotulostinosaston määritys** – Verotulostinten osastojen määrittäminen arvonlisäveroprosentteihin, ALV-vapautustyyppeihin ja tuotetyyppeihin. Seuraavassa esimerkissä näkyy oletusarvoinen yhdistämismääritys.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Tässä on kyseisen esimerkin määritteiden selitys:

    - **VATRate** on tuettu ALV-prosentti, joka on määritetty arvonlisäverokoodiksi. Määrityksen arvossa on kaksi desimaalia, mutta ei desimaalierotinta. Esimerkiksi **2200** edustaa 22 prosenttia ja **1000** edustaa 10 prosenttia.
    - **VATExemptNature** on käytössä vain silloin, kun arvonlisäveroprosentti on 0 (nolla) tai veroa ei ole. **VATExemptNature**-määritystä tuetaan tällä hetkellä vain lahjakorteissa, ja määrityksen arvon on vastattava XML-konfigurointitiedoston **VATExemptNatureForGiftCard**-ominaisuutta.
    - **ProductType** on tuotteen tyyppi. Arvo **0** tarkoittaa tavaraa ja arvo **1** tarkoittaa palvelua.
    - **DepartmentNumber** on tulostimeen konfiguroitu osastonumero, joka vastaa aiempaa kolmea määritettä.

    Esimerkkimääritystä on muokattava sovelluksessa määritettyjen ALV-prosenttien sekä verotulostimeen konfiguroitujen vastaavien osastojen mukaan.

- **Lahjakortin ALV-vapautustyyppi** – ALV-vapautustyyppi, jota on sovellettava, kun lahjakortti myönnetään tai täytetään. Arvon tulisi vastata jotakin verotulostinosaston määrityksen tietoja. Oletusmääritys on **NS**.
- **Ota käyttöön veloituksettomat nimikkeet** – Jos tämä parametri on käytössä, erityinen *omaggio*-alennusoikaisutyyppi nimikkeille, joiden alennus on 100 prosenttia, on otettu käyttöön.
- **Palautuksen alkuperän tietokoodi** – Tietokoodi, jota käytetään palautustapahtuman alkuperän kuvaamiseen, jos alkuperäistä myyntikuittia ei ole. Tätä parametria käytetään yhdessä **alkuperäisen myyntipäivämäärän infokoodin** ja **palautuksen alkuperän määrityksen** parametrien kanssa, jotta muodostetaan oikea sanoma palautustapahtuman alkuperästä verokuittiin, jos alkuperäisiä myyntitapahtumia ei ole. 

    Tämä tietokoodi on määritettävä niin, että käyttäjä voi valita tai syöttää jonkin myymälöiden palautusten mahdollisista alkuperistä. Koodi voidaan konfiguroida esimerkiksi alikoodien luetteloksi (esimerkiksi **Palautus sivustosta** tai **Palautus kioskista**). **Palautuksen alkuperän määritys** -parametrin avulla tietokoodin arvo käännetään verotulostimen komennoksi.

    **Palautuksen alkuperää varten tietokoodiksi valittu tietokoodi** tulisi konfiguroida pakolliseksi tietokoodiksi, joka käynnistyy kerran myyntitapahtumaa kohti. Se on määritettävä myyntipistetoimintoprofiilin **Palauta tuote** -tietokoodiksi, jotta se voidaan käynnistää,kun **Palauta tuote** -toiminto suoritetaan.

    Tätä määritystä varten ei ole määritetty oletusarvoa. Valitse sovelluksessa määritetty tietokoodi.

- **Alkuperäisen myyntipäivän tietokoodi** – Tietokoodi, jota käytetään palautustapahtuman alkuperäisen myyntipäivän kuvaamiseen, jos alkuperäistä myyntikuittia ei ole. Tätä parametria käytetään yhdessä **palautuksen alkuperän infokoodin** ja **palautuksen alkuperän määrityksen** parametrien kanssa, jotta muodostetaan oikea sanoma palautustapahtuman alkuperästä verokuittiin, jos alkuperäisiä myyntitapahtumia ei ole.

    Tietokoodi tulee konfiguroida niin, että **Syötetyyppi**-kentän arvoksi tulee **Päivämäärä**. Se tulee konfiguroida pakolliseksi tietokoodiksi, joka tulee käynnistää kerran myyntitapahtumaa kohti. Koodi on myös annettava sen tietokoodin **linkitettynä tietokoodina**, joka on valittuna **palautuksen alkuperän tietokoodi** -parametrille, jotta nämä kaksi tietokoodia käynnistetään toistensa jälkeen.

    Tätä määritystä varten ei ole määritetty oletusarvoa. Valitse sovelluksessa määritetty tietokoodi.

- **Palautuksen alkuperän määritys** – Palautuksen alkuperien määritys, jota käytetään palautustapahtuman alkuperän tulostamiseen, jos alkuperäistä myyntikuittia ei ole. Tätä parametria käytetään yhdessä **palautuksen alkuperän infokoodin** ja **alkuperäisen myyntipäivän tietokoodin** parametrien kanssa, jotta muodostetaan oikea sanoma palautustapahtuman alkuperästä verokuittiin, jos alkuperäisiä myyntitapahtumia ei ole. Seuraavassa esimerkissä näkyy oletusarvoinen yhdistämismääritys.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Tässä on kyseisen esimerkin määritteiden selitys:

    - **ReturnOrigin** on myymälöiden palautusten mahdollinen alkuperä. Arvon tulisi vastata **palautusten alkuperän tietokoodin** parametrin arvoa.
    - **PrinterReturnOrigin** on yksi verotulostinten hyväksymistä palautuksen alkuperistä (**POS**, **VR** tai **ND**).
    - **PrinterReturnOriginWithoutFiscalData** on palautuksen alkuperä, jonka verotulostin hyväksyy ja joka vastaa palautustapahtumaa, joka on linkitetty alkuperäiseen myyntitapahtumaan, johon ei ole linkitetty verotietoja, koska sitä ei ole rekisteröity verotulostimen kautta. Tässä tapauksessa alkuperäinen myyntipäivämäärä on alkuperäisen myyntitapahtuman päivämäärä.

Seuraavat tietojen oletusmääritykset ovat vanhentuneita, ja ne pidetään vain yhteensopivuuden varmistamiseksi:

- Arvonlisäverokoodien määrittäminen
- Talletuksen maksutyyppi

#### <a name="fiscal-connector-settings"></a>Veroliittimen asetukset

Seuraavat asetukset sisältyvät veroyhdistimen konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **Päätepisteen osoite** – Tulostimen URL-osoite.
- **Päivämäärän ja ajan synkronointi** – Arvo, joka määrittää, synkronoidaanko tulostimen päivämäärä ja aika liitetyn Hardware stationin kanssa.

### <a name="configure-channel-components"></a>Määritä kanavakomponentit

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Italia) (vanha)](emea-ita-fpi-sample-sdk.md).
>
> Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

#### <a name="set-up-the-development-environment"></a>Kehitysympäristön määrittäminen

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa esimerkkiä.

1. Kloonaa tai lataa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilö. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan. Lisätietoja: [Retail SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja NuGetista](../dev-itpro/retail-sdk/sdk-github.md).
1. Avaa verotulostimen integraatioratkaisu kohdassa **Dynamics365Commerce.Solutions\\FiscalIntegration\\EpsonFP90IIISample\\EpsonFP90IIISample.sln** ja muodosta se.
1. Asenna CRT-laajennukset:

    1. Etsi CRT-laajennuksen asennusohjelma:

        - **Commerce Scale Unit:** Etsi **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** -kansiosta **ScaleUnit.EpsonFP90III.Installer**-asennusohjelma.
        - **Paikallinen CRT Modern POS -sovelluksessa:** Etsi **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461**-kansiosta **ModernPOS.EpsonFP90III.Installer**-asennusohjelma.

    1. Käynnistä CRT-laajennusten asennusohjelma komentoriviltä:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Paikallinen CRT Modern POS -sovelluksessa:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Asenna Hardware station -laajennukset:

    1. Etsi **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461**-kansiosta **HardwareStation.EpsonFP90III.Installer**-asennusohjelma.
    1. Käynnistä laajennusten asennusohjelma komentoriviltä:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tuotantoympäristö

Luo ja julkaise verointegraatioesimerkin Cloud Scale Unit ja itsepalveluna käyttöönotettavat paketit noudattamalla [Määritä koontijakso verointegraatioesimerkille](fiscal-integration-sample-build-pipeline.md) -ohjeen vaiheita. **EpsonFP90III build-pipeline.yml**-niminen YAML-mallitiedosto löytyy **Pipeline\\YAML_Files** -kansiosta[Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilöstä.

## <a name="design-of-extensions"></a>Laajennusten rakenne

Italian verotulostimen esimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Retail SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\EpsonFP90IIISample** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä (esim. [julkaisun 9.33 esimerkki](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta, joka on CRT:n ja veroliittimen laajennus, joka on Commerce Hardware Stationin laajennus. Lisätietoja Retail SDK:n käytöstä on kohdissa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Määritä itsenäisen pakkaus-SDK:n koontiversioputki](../dev-itpro/build-pipeline.md).

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verotulostimen integrointiesimerkkiä koskevat käyttöönoton ohjeet (Italia) (vanha)](emea-ita-fpi-sample-sdk.md). Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime -laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda tulostinkohtaisia asiakirjoja ja käsitellä verotulostimen vastauksia.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**DocumentProviderEpsonFP90III**-pyyntökäsittelijä on asiakirjan luontipyynnön aloituspiste verotulostimelle.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa tulostinkohtaisen asiakirjan, jotka on rekisteröitävä verotulostimeen.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Tällä hetkellä seuraavat tapahtumat ovat tuettuja: myynti, X-raportin tulostaminen ja Z-raportin tulostaminen.

#### <a name="configuration"></a>Konfigurointi

Veroasiakirjan tarjoajan konfiguraatiotiedosto sijaitsee kohdassa **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml** [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla tiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verotulostimen kanssa. Tämä laajennus käyttää HTTP-protokollaa asiakirjojen lähettämiseen, jotka CRT-laajennus luo verotulostimeen. Se käsittelee myös verotulostimesta saadut vastaukset.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**EpsonFP90IIISample**-pyyntökäsittelijä on oheislaitteen pyyntöjen käsittelyn aloituspiste.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä:

- **SubmitDocumentFiscalDeviceRequest** – Tämä pyyntö lähettää asiakirjoja tulostimille ja palauttaa vastauksen verotulostimesta.
- **IsReadyFiscalDeviceRequest** – Tätä pyyntöä käytetään laitteen kunnon tarkastusta varten.
- **InitializeFiscalDeviceRequest** – Tätä pyyntöä käytetään tulostimen alustamiseen.

#### <a name="configuration"></a>Konfigurointi

Veroyhdistimen konfiguraatiotiedosto sijaitsee kohdassa **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla yhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
