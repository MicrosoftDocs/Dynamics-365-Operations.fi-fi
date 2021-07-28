---
title: ER-muodon suunnittelu Excel-muotoisen raportin luomiseksi ja kuvien upottamiseksi sivun ylä- ja alatunnisteisiin
description: Tässä aiheessa kuvataan, kuinka sähköisellä raportoinnilla (ER) voidaan luoda liiketoiminta-asiakirjoja, joiden sivujen ylä- ja alatunnisteisiin upotettu kuvia ja muotoja.
author: NickSelin
ms.date: 06/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: e67c10ecb9f297d1855a55431cd07c53ee87d40a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361388"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>ER-muodon suunnittelu Excel-muotoisen raportin luomiseksi ja kuvien upottamiseksi sivun ylä- ja alatunnisteisiin

[!include[banner](../includes/banner.md)]

Tämän ohjeessa selitetään, miten, miten järjestelmänvalvojan tai sähköisen raportoinnin toiminnallisen konsultin roolissa oleva käyttäjä voi suorittaa nämä tehtävät:

- Määritä [sähköisen raportoinnin (ER)](general-electronic-reporting.md) kehyksen parametrit.
- Tuo ER-[konfiguraatiot](general-electronic-reporting.md#Configuration), jotka Microsoft on [tarjonnut](general-electronic-reporting.md#Provider) ja joita käytetään [vapaamuotolaskujen](../../../finance/accounts-receivable/create-free-text-invoice-new.md) luomiseen [mallin](er-fillable-excel.md#excel-file-component) perusteella Microsoft Excel -muodossa.
- Luo [mukautettu (johdettu)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) versio ER-muodon vakiokonfiguraatiosta, jonka Microsoft tarjoaa.
- Muokkaa mukautettua ER-muotokonfiguraatiota siten, että se luo vapaatekstilaskuraportin, jossa on yrityksen logokuva alatunnisteessa.

Tässä ohjeaiheessa kuvatut toimenpiteet voidaan suorittaa **USMF**-yrityksessä. Koodausta ei tarvita. Lataa ja tallenna seuraava tiedosto ennen aloittamista.

| kuvaus        | Tiedostonimi |
|--------------------|-----------|
| Yrityksen logokuva | [Yrityksen logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Sisältö

- [Määritä yritys](#ConfigureLegalEntity)
- [Määritä ER-kehys](#ConfigureFramework)

    - [Konfiguroi ER-parametrit](#ConfigureParameters)
    - [Aktivoi ER-konfiguraation lähde](#ActivateProvider)

        - [Tarkista ER-konfiguraation lähteiden luettelo](#ReviewProvidersList)
        - [Lisää uusi ER-konfiguraation lähde](#AddProvider)
        - [Aktivoi uusi ER-konfiguraation lähde](#ActivateAddedProvider)

- [Tuo ER-muodon vakiokonfiguraatiot](#ImportERSolution1)

    - [Tuo ER-vakiokonfiguraatiot](#ImportERFormat)
    - [Tarkista tuodut ER-konfiguraatiot](#ReviewImportedERSolution)

- [Tulosta vapaatekstilaskun käyttämällä ER-vakiomuotoa](#PrintInvoice1)

    - [Tulostuksen hallinnan asetukset](#ConfigurePrintManagement1)
    - [Tulosta vapaatekstilasku](#ProcessInvoice1)

- [Mukauta ER-vakiomuotoa](#CustomizeProvidedFormat)

    - [Luo mukautettu muoto](#DeriveProvidedFormat)
    - [Muokkaa mukautettua muotoa](#ConfigureDerivedFormat)
    - [Merkitse mukautettu muoto suoritettavaksi](#MarkFormatRunnable)

- [Tulosta vapaatekstilaskun käyttämällä mukautettua ER-muotoa](#PrintInvoice2)

    - [Tulostuksen hallinnan asetukset](#ConfigurePrintManagement2)
    - [Tulosta vapaatekstilasku](#ProcessInvoice2)

- [Lisäresurssit](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Määritä yritys

1. Valitse **Organisaation hallinto** \> **Organisaatiot** \> **Yritykset**.
2. Valitse **Yritykset**-sivun **Raportin yrityksen logokuva** -pikavälilehdestä **Muuta**.
3. Valitse **Valitse palvelimelle ladattava kuvatiedosto** -valintaruudusta **Selaa** ja valitse **Company logo.png** -tiedosto, jonka latasit aiemmin.
4. Valitse **Tallenna** ja sulje sitten **Yritykset**-sivu.

![Yritykset-sivulla valittu yrityksen logokuva.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Määritä ER-kehys

Sähköisen raportoinnin toiminnallisen konsultin roolissa olevan käyttäjän on määritettävä sähköisen raportoinnin parametrien vähimmäisjoukko, ennen kuin voit alkaa käyttää ER-kehystä mukautetun version kehittämiseen ER-vakiomuodosta.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfiguroi ER-parametrit

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.
3. Määritä **Sähköisen raportoinnin parametrit** -sivun **Yleinen**-välilehdessä **Ota käyttöön suunnittelutila** -asetukseksi **Kyllä**.
4. Määritä **Liitteet**-välilehdessä seuraavat parametrit:

    - Valitse **Konfiguraatiot**-kentässä **Tiedosto**-tyyppi **USMF**-yritykselle.
    - Valitse **Työarkisto**-, **Väliaikainen**-, **Perusrivi**- ja **Muut**-kentissä **Tiedosto**-tyyppi.

Lisätietoja ER-parametreista on kohdassa [Määritä ER-kehys](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivoi ER-konfiguraation lähde

Jokainen lisätty ER-konfiguraatio merkitään ER-konfiguraation lähteen omistamaksi. ER-konfiguraation lähdettä, joka on aktivoitu **Sähköinen raportointi** -työtilassa, käytetään tähän tarkoitukseen. Siksi sinun on aktivoitava ER-konfiguraation lähde **Sähköinen raportointi** -työtilassa, ennen kuin voit alkaa lisätä tai muokata ER-konfiguraatioita.

> [!NOTE]
> Vain konfiguraation omistaja voi muokata ER-konfiguraatiota. Ennen kuin ER-konfiguraatiota voi muokata, asianmukainen ER-konfiguraation lähde on aktivoitava **Sähköinen raportointi** -työtilassa.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Tarkista ER-konfiguraation lähteiden luettelo

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.
3. **Konfiguraation lähdetaulu** -sivulla jokaisen lähteen tietueella on yksilöllinen nimi ja URL-osoite. Tarkista tämän sivun sisältö. Jos **Litware, Inc.** (`https://www.litware.com`) -tietue on jo olemassa, ohita seuraava menettely, [Lisää uusi ER-konfiguraation lähde](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Lisää uusi ER-konfiguraation lähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.
3. Valitse **Konfiguraation lähteet**-sivulla **Uusi**.
4. Kirjoita **Nimi**-kenttään **Litware, Inc.**
5. Kirjoita **Internetosoite**-kenttään `https://www.litware.com`.
6. Valitse **Tallenna**.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivoi uusi ER-konfiguraation lähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet**-osassa **Litware, Inc.** -ruutu ja valitse sitten **Aseta aktiiviseksi**.

Lisätietoja ER-konfiguraation lähteistä on kohdassa [Konfiguraation lähteiden luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Tuo ER-muodon vakiokonfiguraatiot

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Tuo ER-vakiokonfiguraatiot

Jos haluat lisätä ER-vakiokonfiguraatiot nykyiseen Dynamics 365 Finance -esiintymääsi, sinun on tuotava ne ER-[säilöstä](general-electronic-reporting.md#Repository), joka määritettiin kyseiselle esiintymälle.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot** -sivun **Konfiguraation lähteet** -osassa **Microsoft**-ruutu ja valitse sitten **Säilöt** nähdäksesi luettelon **Microsoft**-toimittajan säilöistä.
3. Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **Yleinen** ja valitse sitten **Avaa**. Jos sinulta pyydetään valtuutusta [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md) -palveluun yhdistämiseen, noudata valtuutusohjeita.
4. Valitse **Konfiguraatiosäilö**-sivun vasemman ruudun määrityspuussa **Vapaatekstilasku (Excel)** -muotoinen määritys.
5. Valitse **Versiot**-pikavälilehdestä valitun ER-muodon konfiguraation uusin versio (esimerkiksi **240.112**).
6. Lataa valittu versio yleisestä säilöpalvelusta nykyiseen Finance-esiintymään valitsemalla **Tuo**.

![ER-vakiokonfiguraatioiden tuominen Konfiguraatiosäilö-sivulla.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Jos sinulla on ongelmia [yleiseen säilöön](er-download-configurations-global-repo.md) pääsyssä, voit [ladata konfiguraatiot](download-electronic-reporting-configuration-lcs.md) sen sijaan Microsoft Dynamics Lifecycle Services (LCS) -palvelusta.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Tarkista tuodut ER-konfiguraatiot

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Laajenna **Konfiguraatiot**-sivun määrityspuun vasemmassa ruudussa **Laskumalli**.
4. Valitun **Vapaatekstilasku (Excel)** -ER-muodon lisäksi myös muut tarvittavat ER-konfiguraatiot tuotiin. Varmista, että konfiguraatiopuussa ovat saatavilla seuraavat ER-konfiguraatiot:

    - **Laskumalli** – Tämä konfiguraatio sisältää [tietomallin](general-electronic-reporting.md#data-model-and-model-mapping-components) ER-osan, joka esittää laskutuksen liiketoimintatoimialueen tietorakenteen.
    - **Laskumallin määritys** – Tämä konfiguraatio sisältää [mallin määrityksen](general-electronic-reporting.md#data-model-and-model-mapping-components) ER-osan, joka kuvaa, miten tietomalli täytetään hakemuksen tiedoilla suorituspalvelussa.
    - **Vapaatekstilasku (Excel)** – Tämä konfiguraatio sisältää [muodon](general-electronic-reporting.md#FormatComponentOutbound) ja muodon yhdistämismäärityksen ER-osat. Muotokomponentti määrittää raportin asettelun Excel-muodossa olevan mallin perusteella. Muodon määritysosa sisältää mallin tietolähteen ja määrittää, miten raportin asettelu täytetään käyttämällä tätä tietolähdettä suorituspalvelussa.

![Tuodut ER-määritykset määrityssivulla.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Tulosta vapaatekstilasku käyttämällä ER-vakiomuotoa

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Tulostuksen hallinnan asetukset

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Valitse **Vapaatekstilasku**-sivulta **FTI-00000002**-lasku ja valitse sitten **Lasku**-välilehden toimintoruudun **Tulostuksenhallinta**-ryhmästä **Tulostuksenhallinta**.
3. Laajenna **Tulostuksenhallinta-asetukset**-sivun vasemmasta puusta **Moduuli - Myyntireskontra \> Asiakirjat \> Vapaatekstilasku** ja valitse sitten **Alkuperäinen \<Default\>** -nimike.
4. Valitse **Raportin muoto** -kentästä **Vapaatekstilasku (Excel)**.
5. Valitse **Esc**-näppäin poistuaksesi **Tulostuksenhallinta-asetukset**-sivulta ja palataksesi **Vapaatekstilasku**-sivulle.

![Vapaatekstilaskun tulostuksen hallinta-asetukset ER-vakiomuodossa Tulostuksenhallinta-asetukset-sivulla.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Tulosta vapaatekstilasku

1. Varmista **Vapaatekstilasku**-sivulla, että **FTI-00000002**-lasku on edelleen valittuna ja valitse sitten **Lasku**-välilehden toimintoruudun **Asiakirja**-ryhmästä **Tulosta** \> **Valittu**.
2. Lataa luotu lasku Excel-muodossa ja avaa se esikatselua varten.
3. Huomaa, että luodun laskun sivun alatunniste sisältää tietoja tämänhetkisestä sivunumerosta ja raportin sivujen kokonaismäärästä tarjotun ER-muodon Excel-mallin rakenteen mukaisesti.

![Luotu vapaatekstilasku.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Mukauta ER-vakiomuotoa

Tämän osion esimerkissä voit käyttää Microsoftin tarjoamia ER-konfiguraatioita vapaatekstilaskun luomiseksi Excel-muodossa. Sinun on kuitenkin lisättävä mukautus lisätäksesi yrityksen logokuvan luotujen laskujen sivun ylätunnisteeseen.

Tässä tapauksessa Litware, Inc. -yhtiön edustajana sinun on luotava uusi ER-muodon konfiguraatio, joka perustuu Microsoftin tarjoamaan **Vapaatekstilasku (Excel)** -konfiguraatioon.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Luo mukautettu muoto

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Konfiguraatiot**-sivun määrityspuun vasemmasta ruudusta **Laskumalli** ja valitse sitten **Vapaatekstilasku (Excel)**. Litware, Inc. käyttää tämän ER-muodon konfiguraation tuotua versiota (esimerkiksi **240.112**) mukautetun version pohjana.
3. Avaa pudotusvalintaikkuna valitsemalla **Luo konfigurointi**. Käytä tätä valintaikkunaa luodaksesi uuden konfiguroinnin mukautetulle maksumuodolle.
4. Valitse **Uusi**-kenttäryhmästä **Johda nimestä: Vapaatekstilasku (Excel), Microsoft** -vaihtoehto.
5. Kirjoita **Nimi**-kenttään **Vapaatekstilasku (Excel) mukautettu**.
6. Valitse **Luo konfiguraatio**.

![Mukautetun maksumuodon konfiguraation luominen Luo konfiguraatio -valintaikkunan avattavasta valikosta.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

**Vapaatekstilasku (Excel) mukautettu** -ER-muodon konfiguraation versio 240.112.1 luodaan. Tämän version [tila](general-electronic-reporting.md#component-versioning) on **Luonnos**, ja sitä voidaan muokata. Mukautetun ER-muodon nykyinen sisältö vastaa Microsoftin toimittaman muodon sisältöä.

![ER-muodon konfiguraation uusi versio luotuna Konfiguraatiot-sivulla.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Muokkaa mukautettua muotoa

Määritä mukautettu muoto siten, että yrityksen logokuva lisätään raportin jokaisen sivun alatunnisteeseen.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Konfiguraatiot**-sivun määrityspuun vasemmasta ruudusta **Maksumalli** ja valitse sitten **Vapaatekstilasku (Excel) mukautettu**.
3. Valitse **Versiot**-pikavälilehdestä valitun konfiguraation versio **240.112.1**.
4. Valitse **Suunnittelu**.
5. Valitse **Muodon suunnittelija** -sivulla **Näytä tiedot**, jotta näkisit lisätietoja muoto-osista.
6. Laajenna ja tarkastele seuraavia elementtejä:

    - **Excel**-tyypin **Vapaatekstilasku**-elementti. Tätä elementtiä käytetään laskun luomiseen Excel-työkirjamuodossa.
    - **Taulukko**-tyypin **Vapaatekstilasku \\ Lasku** -elementti. Tätä elementtiä käytetään luodun Excel-työkirjan laskentataulukon luomiseen.
    - **Alatunniste**-tyypin **Vapaatekstilasku \\ Lasku \\ Alatunniste** -elementti. Tätä elementtiä käytetään laskun alatunnisteen täyttämiseen.

7. Valitse **Vapaatekstilasku \\ Lasku \\ Alatunniste** -elementti.

    ![Alatunniste-elementti ER-toimintojen suunnitteluohjelmassa.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Luodun laskun jokaisen sivun alatunniste sisältää tietoja tämänhetkisestä sivunumerosta ja raportin sivujen kokonaismäärästä. Kuten näet, **Vapaatekstilasku \\ Lasku \\ Alatunniste** -elementti ei sisällä alielementtejä. Tästä johtuen käytetty Excel-malli on määritetty näyttämään sivujen tiedot jokaisen raportin alatunnisteen keskellä.

8. Valitse **Lisää** ja valitse sitten lisäämäsi muotoelementin **Excel \\ Kuva** -tyyppi:

    1. Valitse **Tasaus**-kentästä **Oikea**.
    2. Valitse **Skaalaa korkeus** -kentästä **Suhteellinen**.
    3. Kirjoita **Skaala prosentteina** -kenttään **70**.
    4. Valitse **OK**.

        > [!NOTE]
        > **Excel \\ Kuva** -elementtiä käytetään yrityksen logokuvan lisäämiseksi ja tasaamiseksi sivun alatunnisteen oikeaan laitaan.

    ![Kuva-elementin ominaisuudet Komponentin ominaisuudet -valintaikkunassa.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Valitse lisäämäsi **Kuva**-elementti muodon rakenteen hakemistosta ja laajenna sitten **Määritys**-välilehden **malli**-tietolähde.
10. Laajenna **model.Payment** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo** ja valitse sitten **model.InvoiceBase.CompanyInfo.Logo**-tietolähdekenttä. [Säilö](er-formula-supported-data-types-composite.md#container)-tyypin tietolähdekenttä näyttää yrityksen logokuvan mediasisältönä.
11. Valitse **Sido**. **Kuva**-muodon elementti on nyt sidottu **model.InvoiceBase.CompanyInfo.Logo**-tietolähdekenttään. Tästä johtuen yrityksen logokuva lisätään luotujen laskujen alatunnisteeseen suorituksen aikana.

    ![Kuva-muotoelementti sidottuna model.InvoiceBase.CompanyInfo.Logo-tietolähdekenttään ER-toimintojen suunnittelutoiminnossa.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Valitse **Tallenna** ja sulje **Suunnittelutoiminto**-sivu.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Merkitse mukautettu muoto suoritettavaksi

Koska mukautetun muodon ensimmäinen versio on luotu ja sen tila on **Luonnos**, voit suorittaa muodon testaustarkoituksia varten. Jos haluat suorittaa raportin, käsittele toimittajamaksu käyttämällä maksutapaa, joka viittaa mukautettuun ER-muotoosi. Oletuksena kun kutsut ER-muodon sovelluksesta, vain versiot, joiden tila on **Valmis** tai **Jaettu**, otetaan [huomioon](general-electronic-reporting.md#component-versioning). Tämä käytös auttaa estämään sellaisten ER-muotojen käyttöä, joiden mallit eivät ole valmiit. Testiajoissasi voit kuitenkin pakottaa sovelluksen käyttämään ER-muotosi versiota, jonka tila on **Luonnos**. Tällä tavoin voit säätää nykyistä muotoversiota, jos muokkauksia tarvitaan. Lisätietoja on kohdassa [Soveltuvuus](electronic-reporting-destinations.md#applicability).

Käyttääksesi ER-muodon luonnosversiota sinun on merkittävä ER-muoto selkeästi.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. **Käyttäjän parametrit** -valintaikkunassa määritä **Suorita asetukset** -valinnaksi **Kyllä**, ja valitse sitten **OK**.
4. Valitse **Muokkaa** tehdäksesi tämänhetkisestä sivusta muokattavan ja valitse sitten määrityspuun vasemmasta ruudusta **Vapaatekstilasku (Excel) mukautettu**.
5. Määritä **Suorita luonnos** -vaihtoehdoksi **Kyllä**.

![Mukautetun muodon merkitseminen suoritettavaksi Konfiguraatiot-sivulta.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Tulosta vapaatekstilasku käyttämällä mukautettua ER-muotoa

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Tulostuksen hallinnan asetukset

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Valitse **Vapaatekstilasku**-sivulta **FTI-00000002**-lasku ja valitse sitten **Lasku**-välilehden toimintoruudun **Tulostuksenhallinta**-ryhmästä **Tulostuksenhallinta**.
3. Laajenna **Tulostuksenhallinta-asetukset**-sivun vasemmasta hakemistosta **Moduuli - Myyntireskontra** \> **Asiakirjat** \> **Vapaatekstilasku** ja valitse sitten **Alkuperäinen** **\<Default\>** -nimike.
4. Valitse **Raportin muoto** -kentästä **Vapaatekstilasku (Excel) mukautettu**.
5. Valitse **Esc** poistuaksesi **Tulostuksenhallinta-asetukset**-sivulta ja palataksesi **Vapaatekstilasku**-sivulle.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Tulosta vapaatekstilasku

1. Varmista **Vapaatekstilasku**-sivulla, että **FTI-00000002**-lasku on edelleen valittuna ja valitse sitten **Lasku**-välilehden toimintoruudun **Asiakirja**-ryhmästä **Tulosta** \> **Valittu**.
2. Lataa luotu lasku Excel-muodossa ja avaa se esikatselua varten.
3. Huomaa, että luodun laskun sivun alatunniste sisältää tietoja raportin sivujen tietojen lisäksi yrityksen logokuvan mukautetun ER-muodon rakenteen mukaisesti.

![Luotu vapaatekstilasku, jossa on yrityksen logokuva sivun alatunnisteessa.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Lisäresurssit

- [Konfiguraatioiden suunnitteleminen asiakirjojen luomiseksi Excel-muodossa](er-fillable-excel.md)
- [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md)
