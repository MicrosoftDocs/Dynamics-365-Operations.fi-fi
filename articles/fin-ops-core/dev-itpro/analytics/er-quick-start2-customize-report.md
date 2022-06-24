---
title: Luo mukautettu sähköinen asiakirja muokkaamalla ER-muotoa
description: Tässä artikkelissa kerrotaan, miten Microsoftin tarjoaman sähköisen raportoinnin (ER) muotoa voidaan säätää siten, että se luo mukautetun sähköisen asiakirjan.
author: NickSelin
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 492964d3cea0e474a50d6d83231f33d9508b9d9d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886788"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Luo mukautettu sähköinen asiakirja muokkaamalla ER-muotoa

[!include[banner](../includes/banner.md)]

Tämän artikkelin menettelyissä selitetään, miten järjestelmänvalvojan tai sähköisen raportoinnin toiminnallisen konsultin roolissa oleva käyttäjä voi tehdä nämä tehtävät:

- Määritä [sähköisen raportoinnin (ER) kehyksen](general-electronic-reporting.md) parametrit.
- Tuo ER-konfiguraatiot, jotka Microsoft tarjoaa ja joita käytetään maksutiedoston luomiseen, kun [toimittajan maksua](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) käsitellään.
- Luo mukautettu versio ER-muodon vakiokonfiguraatiosta, jonka MIcrosoft tarjoaa.
- Muokkaa mukautettua ER-muodon konfiguraatiota siten, että se luo maksutiedostot, jotka täyttävät tietyn pankin vaatimukset.
- Ota käyttöön muutokset, jotka ER-muodon vakiokonfiguraatioon on tehty mukautetussa sähköisen raportoinnin muodon konfiguraatiossa.

Kaikki seuraavat toimenpiteet voidaan tehdä **GBSI**-yrityksessä. Koodausta ei tarvita.

- [Määritä ER-kehys](#ConfigureFramework)

    - [Konfiguroi ER-parametrit](#ConfigureParameters)
    - [Aktivoi ER-konfiguraation lähde](#ActivateProvider)

        - [Tarkista ER-konfiguraation lähteiden luettelo](#ReviewProvidersList)
        - [Lisää uusi ER-konfiguraation lähde](#ActivateProvider)
        - [Aktivoi ER-konfiguraation lähde](#ActivateAddedProvider)

- [Tuo ER-muodon vakiokonfiguraatiot](#ImportERSolution1)

    - [Tuo ER-vakiokonfiguraatiot](#ImportERFormat1)
    - [Tarkista tuodut ER-konfiguraatiot](#ReviewImportedERSolution)

- [Valmistele toimittajamaksu käsittelyä varten](#PrepareVendorPayment)

    - [Lisää toimittajatilin pankkitiedot](#AddBankAccount)
    - [Lisää toimittajamaksu](#EnterVendorPayment)

- [Käsittele toimittajamaksu käyttämällä ER-vakiomuotoa](#ProcessVendorPayment1)

    - [Määritä sähköinen maksutapa](#ConfigureMethodOfPayment1)
    - [Käsittele toimittajamaksu](#ProcessPayment1)

- [Mukauta ER-vakiomuotoa](#CustomizeProvidedFormat)

    - [Luo mukautettu muoto](#DeriveProvidedFormat)
    - [Muokkaa mukautettua muotoa](#ConfigureDerivedFormat)
    - [Merkitse mukautettu muoto suoritettavaksi](#MarkFormatRunnable)

- [Käsittele toimittajamaksu käyttämällä mukautettua ER-muotoa](#ProcessVendorPayment2)

    - [Määritä sähköinen maksutapa](#ConfigureMethodOfPayment2)
    - [Käsittele toimittajamaksu](#ProcessPayment2)

- [Tuo ER-muodon vakiokonfiguraatioiden uudet versiot](#ImportERSolution2)

    - [Tuo ER-vakiokonfiguraatioiden uudet versiot](#ImportERFormat2)
    - [Tarkista tuodut ER-muodon konfiguraatiot](#ReviewImportedERFormat)

- [Ota uudessa versiossa käyttöön tuodun muodon muutokset mukautetussa muodossa](#AdoptNewBaseVersion)

    - [Viimeistele mukautetun muodon nykyinen luonnosversio](#CompleteDerivedFormat)
    - [Pohjusta mukautettu muoto uuteen perusversioon](#RebaseDerivedFormat)
    - [Käsittele toimittajamaksu käyttämällä pohjustettua ER-muotoa](#ProcessPayment3)

- [Lisäresurssit](#References)

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
> Vain ER-konfiguraation omistaja voi muokata sitä. Siksi ennen kuin ER-konfiguraatiota voi muokata, asianmukainen ER-konfiguraation lähde on aktivoitava **Sähköinen raportointi** -työtilassa.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Tarkista ER-konfiguraation lähteiden luettelo

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.
3. **Konfiguraation lähdetaulu** -sivulla jokaisen lähteen tietueella on yksilöllinen nimi ja URL-osoite. Tarkista tämän sivun sisältö. Jos **Litware, Inc.** (`https://www.litware.com`) -tietue on jo olemassa, ohita seuraava menettely, [Lisää uusi ER-konfiguraation lähde](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Lisää uusi ER-konfiguraation lähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.
3. Valitse **Konfiguraation lähteet**-sivulla **Uusi**.
4. Kirjoita **Nimi**-kenttään **Litware, Inc.**
5. Kirjoita **Internetosoite**-kenttään `https://www.litware.com`.
6. Valitse **Tallenna**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivoi ER-konfiguraation lähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet**-osassa **Litware, Inc.** -ruutu ja valitse sitten **Aseta aktiiviseksi**.

Lisätietoja ER-konfiguraation lähteistä on kohdassa [Konfiguraation lähteiden luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Tuo ER-muodon vakiokonfiguraatiot

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Tuo ER-vakiokonfiguraatiot

ER-vakiomääritys voidaan lisätä Microsoft Dynamics 365 Financen nykyiseen esiintymään tuomalla ne kyseiselle esiintymällä määritetystä ER-[säilöstä](general-electronic-reporting.md#Repository).

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet** -osassa **Microsoft**-ruutu ja valitse sitten **Säilöt** nähdäksesi luettelon Microsoft-toimittajan säilöistä.
3. Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **Yleinen** ja valitse sitten **Avaa**. Jos sinulta pyydetään valtuutusta Regulatory Configuration Service -palveluun yhdistämiseen, noudata valtuutusohjeita.
4. Valitse **Konfiguraatiosäilö**-sivun vasemmassa ruudussa olevasta konfiguraatiopuusta **BACS (Iso-Britannia)** -muotoinen konfiguraatio.
5. Valitse **Versiot**-pikavälilehdestä valitun ER-muodon konfiguraation versio **1.1**.
6. Lataa valittu versio yleisestä säilöpalvelusta nykyiseen Finance-esiintymään valitsemalla **Tuo**.

![Konfiguraatiosäilön sivu.](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Jos sinulla on ongelmia [yleiseen säilöön](er-download-configurations-global-repo.md) pääsyssä, voit [ladata konfiguraatiot](download-electronic-reporting-configuration-lcs.md) sen sijaan Microsoft Dynamics Lifecycle Services (LCS) -palvelusta.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Tarkista tuodut ER-konfiguraatiot

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta ja laajenna **Maksumalli**.
4. Huomaa, että valitun **BACS (Iso-Britannia)** -ER-muodon lisäksi myös muita tarvittavia ER-konfiguraatioita tuotiin. Varmista, että konfiguraatiopuussa ovat saatavilla seuraavat ER-konfiguraatiot:

    - **Maksumalli** – tämä konfiguraatio sisältää tietomallin ER-osan, joka esittää maksun liiketoimintatoimialueen tietorakenteen.
    - **Maksumallin määritys 1611** – tämä konfiguraatio sisältää mallin määrityksen ER-osan, joka kuvaa, miten tietomalli täytetään hakemuksen tiedoilla suorituspalvelussa.
    - **BACS (Iso-Britannia)** – tämä konfiguraatio sisältää muodon ja muodon määrityksen ER-osat. Muoto-osa määrittää raportin asettelun. Muodon määritysosa sisältää mallin tietolähteen ja määrittää, miten raportin asettelu täytetään käyttämällä tätä tietolähdettä suorituspalvelussa.

![Konfiguroinnit-sivu, jolla on käytettävissä olevat ER-konfiguraatiot puumuodossa.](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Valmistele toimittajamaksu käsittelyä varten

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Lisää toimittajatilin pankkitiedot

Sinun on lisättävä pankkitiedot toimittajatilille, johon viitataan myöhemmin rekisteröidyssä maksussa.

1. Siirry kohtaan **Ostoreskontra** \> **Toimittajat** \> **Kaikki toimittajat**.
2. Valitse **Kaikki toimittajat** -sivulla **GB_SI_000001**-toimittajatili ja sitten toimintoruudun **Toimittaja**-välilehden **Määritä**-ryhmässä **Pankkitilit**.
3. Valitse **Toimittajan pankkitilit** -sivulla **Uusi** ja lisää sitten seuraavat tiedot:

    1. Lisää **Pankkitili**-kenttään **GBP OPER**.
    2. Valitse **Pankkiryhmä**-kentässä **BankGBP**.
    3. Lisää **Pankkitilin numero** -kenttään **202015**.
    4. Kirjoita **SWIFT-koodi**-kenttään <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.
    5. Kirjoita **IBAN**-kenttään **GB33BUKB20201555555555**.
    6. Pidä **Pankkikoodi**-kentän oletusarvo, <a id="DefineRoutingNumber"></a>**123456**.

    ![Toimittajan pankkitilit -sivu.](./media/er-quick-start2-bank-account.png)

4. Valitse **Tallenna**.
5. Sulje sivu.
6. Avaa **Kaikki toimittajat** -sivulla **GB_SI_000001**-toimittajan tili.
7. Valitse toimittajan tietosivulla **Muokkaa**, jotta voit muokata sivua tarvittaessa.
8. Valitse **Maksu**-pikavälilehden **Pankkitili**-kentässä **GBP OPER**.

    ![Toimittajan tiedot -sivu.](./media/er-quick-start2-bank-account-reference.png)

9. Valitse **Tallenna**.
10. Sulje sivu.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Lisää toimittajamaksu

Sinun on lisättävä uusi toimittajamaksu käyttämällä [maksuehdotusta](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).

1. Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.
2. Valitse **Toimittajan maksukirjauskansio**-sivulla **Uusi**.
3. Valitse **Nimi**-kenttään **VendPay**.
4. Valitse **Rivit**.
5. Valitse **Maksuehdotus** \> **Luo maksuehdotus**.
6. Määritä **Toimittajan maksuehdotus** -valintaikkunassa ehdot tietueiden suodattamiseen vain **GB_SI_000001** -toimittajatililtä ja valitse sitten **OK**.
7. Valitse **00000007_Inv**-laskun rivi ja valitse sitten **Luo maksu**.

    ![Toimittajamaksun ehdotus -valintaikkuna.](./media/er-quick-start2-payment-proposal.png)

8. Varmista, että lisättävä maksu määritetään käyttämään **sähköistä** maksutapaa.

    ![Toimittajan maksut -sivu.](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Käsittele toimittajamaksu käyttämällä ER-vakiomuotoa

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Määritä sähköinen maksutapa

Sinun on määritettävä sähköinen maksutapa, jolloin se käyttää tuotua ER-muodon konfiguraatiota.

1. Valitse **Ostoreskontra** \> **Maksun asetukset** \> **Maksutavat**.
2. Valitse **Maksutapa - Toimittajat** -sivulla **Sähköinen** maksumenetelmä vasemmasta ruudusta.
3. Valitse **Muokkaa**.
4. Määritä **Tiedostomuoto**-pikavälilehdessä **Yleinen sähköinen vientimuoto** -asetukseksi **Kyllä**.
5. Valitse **Vientimuodon konfigurointi** -kentässä **BACS (Iso-Britannia)** -muotoinen konfiguraatio.

    ![Maksutavat – toimittajat -sivulla voit määrittää sähköisen maksutavan, jolla toimittajamaksut käsitellään vakiomuodossa.](./media/er-quick-start2-method-of-payment1.png)

6. Valitse **Tallenna**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Käsittele toimittajamaksu

1. Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.
2. Valitse **Toimittajan maksukirjauskansio** -sivulla aiemmin lisäämäsi kirjauskansio ja valitse sitten **Rivit**.
3. Valitse **Toimittajamaksut**-sivulla **Muodosta maksut**.
4. Anna seuraavat tiedot **Muodosta maksut** -valintaikkunassa:

    - Valitse **Maksutapa**-kentässä **Sähköinen**.
    - Valitse **Pankkitili**-kentässä **GBSI OPER**.

5. Valitse **OK**.
6. Määritä **Sähköisen raportin parametrit** -valintaikkunassa **Tulosta valvontaraportti** -asetukseksi **Kyllä** ja valitse sitten **OK**.

    ![Sähköisen raportin parametrit -valintasivu.](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Maksutiedoston lisäksi voit nyt luoda valvontaraportin.

7. Lataa zip-tiedosto ja pura siitä sitten seuraavat tiedostot:

    - Valvontaraportti Excel-muodossa
    - Maksutiedosto TXT-muodossa

        Huomaa, että annetun ER-muodon [rakenteen](#PositionRoutingNumber) mukaisesti luodun tiedoston maksurivi alkaa pankkikoodilla, joka [määritettiin](#DefineRoutingNumber) määritetylle pankkitilille.

        ![Maksutiedosto TXT-muodossa.](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Mukauta ER-vakiomuotoa

Tässä osassa näkyvässä esimerkissä haluat käyttää ER-konfiguraatioita, jotka Microsoft tarjoaa toimittajan maksutiedostojen luomiseen BACS-muodossa, mutta sinun on lisättävä mukautus tukeaksesi tietyn pankin vaatimuksia. Haluat myös pystyä päivittämään mukautettua muotoasi, kun ER-konfiguraatioista tulee uusia versioita saataville. Haluat kuitenkin voida päivittää mahdollisimman pienillä kustannuksilla.

Tässä tapauksessa Litware, Inc. -yhtiön edustajana sinun on luotava uusi ER-muodon konfiguraatio käyttämällä Microsoftin toimittamaa **BACS (Iso-Britannia)** -konfiguraatiota pohjana.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Luo mukautettu muoto

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli** ja valitse sitten **BACS (Iso-Britannia)**. Litware, Inc. käyttää tämän ER-muodon konfiguraation versiota 1.1 mukautetun version pohjana.
3. Avaa pudotusvalintaikkuna valitsemalla **Luo konfigurointi**. Voit käyttää tätä valintaikkunaa luodaksesi uuden konfiguroinnin mukautetulle maksumuodolle.
4. Valitse **Uusi**-kenttäryhmässä **Johda nimestä: BACS (Iso-Britannia), Microsoft** -vaihtoehto.
5. Kirjoita **Nimi**-kenttään **BACS (Iso-Britannia, mukautettu)**.

    ![Avattava Luo konfigurointi -luettelo -valintaruutu.](./media/er-quick-start2-add-derived-format.png)

6. Valitse **Luo konfiguraatio**.

**BACS (Iso-Britannia, mukautettu)** -ER-muotokonfiguraation versio 1.1.1 luodaan. Tämän version [tila](general-electronic-reporting.md#component-versioning) on **Luonnos**, ja sitä voidaan muokata. Mukautetun ER-muodon nykyinen sisältö vastaa Microsoftin toimittaman muodon sisältöä.

![Konfiguraatiosivu, jossa BACS (Yhdistynyt kuningaskunta, mukautettu) -ER-muotokonfiguraation versio 1.1.1.](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Muokkaa mukautettua muotoa

Sinun on määritettävä mukautettu muoto, jotta se täyttää pankkikohtaiset vaatimukset. Pankki voi esimerkiksi edellyttää, että luotavat maksutiedostot sisältävät sen pankin Society of Worldwide Interbank Financial Telecommunication (SWIFT) -koodin, jolle on määritetty edustajan rooli käsitellyssä toimittajamaksussa. SWIFT-koodit ovat kansainvälisiä pankkikoodeja, jotka tunnistavat tietyn pankin kaikkialla maailmassa. Niitä kutsutaan myös pankin tunnistekoodeiksi (Bank Identifier Code, BIC). SWIFT-koodin on oltava 11 merkkiä pitkä ja se on lisättävä jokaisen maksurivin alkuun luodussa maksutiedostossa.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli** ja valitse sitten **BACS (Iso-Britannia, mukautettu)**.
3. Valitse **Versiot**-pikavälilehdestä valitun konfiguraation versio **1.1.1**.
4. Valitse **Suunnittelu**.
5. Valitse **Muodon suunnittelija** -sivulla **Näytä tiedot**, jotta näkisit lisätietoja muoto-osista.
6. Laajenna ja tarkastele seuraavia elementtejä:

    - **Kansio**-tyypin **BACSReportsFolder**-elementti. Tätä elementtiä käytetään tuotoksen luomiseen ZIP-muodossa.
    - **Tiedosto**-tyypin **tiedosto**-elementti. Tätä elementtiä käytetään maksutiedoston luomiseen TXT-muodossa.
    - **Järjestys**-tyypin **tapahtumat**-elementti. Tätä elementtiä käytetään yhden maksurivin luomiseen maksutiedostossa.
    - **Järjestys**-tyypin **tapahtuma**-elementti. Tätä elementtiä käytetään yhden maksurivin yksittäisten kenttien luomiseen.

7. Valitse **tapahtuma**-elementti.

    ![Tapahtumaelementti ER-toimintojen suunnitteluohjelmassa.](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Toimitettu raportti on määritetty siten, että <a id="PositionRoutingNumber"></a>jokainen maksurivi alkaa pankkikoodilla. **vendBankRouteNum**-muotoelementtiä käytetään tähän tarkoitukseen. 

8. Valitse **Lisää** ja valitse sitten lisäämäsi muotoelementin **Teksti\\merkkijono** -tyyppi:

    1. Syötä **Nimi**-kenttään **vendBankSWIFT**.
    2. Syötä **Vähimmäispituus**-kenttään **11**.
    3. Syötä **Enimmäispituus**-kenttään **11**.
    4. Valitse **OK**.

    > [!NOTE]
    > **vendBankSWIFT**-elementtiä käytetään toimittajapankin SWIFT-koodin syöttämiseen luotuihin tiedostoihin.

9. Valitse muotorakennepuussa **vendBankSWIFT**.
10. Siirrä valittu muotoelementti yhden tason verran ylöspäin valitsemalla **Siirrä ylös**. Toista tätä vaihetta, kunnes **vendBankSWIFT**-elementti on <a id="PositionSWIFTCode"></a>ensimmäinen elementti pää **tapahtuma** elementin alla.

    ![VendBankSWIFT ensimmäisenä elementtinä tapahtuman alla ER-toimintojen suunnitteluohjelmassa.](./media/er-quick-start2-derived-format1.png)

11. Kun **vendBankSWIFT** on edelleen valittuna muotorakennepuussa, valitse **Kartoitus**-välilehti ja laajenna sitten **malli**-tietolähdettä.
12. Laajenna **model.Payment** \> **model.Payment.CreditorAgent** ja valitse **model.Payment.CreditorAgent.BICFI**-tietolähdekenttä. Tämä tietolähdekenttä näyttää sen toimittajapankin SWIFT-koodin, jolle on määritetty edustajan rooli käsitellyssä toimittajamaksussa.
13. Valitse **Sido**. **vendBankSWIFT**-muotoelementti on nyt sidottu **model.Payment.CreditorAgent.BICFI**-tietolähdekenttään, jotta SWIFT-koodit syötetään luotuihin maksutiedostoihin.

    ![vendBankSWIFT-muotoelementti sidottuna model.Payment.CreditorAgent.BICFI-tietolähdekenttään ER-toimintojen suunnitteluohjelmassa.](./media/er-quick-start2-derived-format2.png)

14. Valitse **Tallenna**.
15. Sulje suunnitteluohjelmasivu.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Merkitse mukautettu muoto suoritettavaksi

Nyt kun mukautetun muotosi ensimmäinen versio on luotu, ja sen tila on **Luonnos**, voit suorittaa sen testaustarkoituksia varten. Raportin suorittamista varten sinun on käsiteltävä toimittajamaksu käyttämällä maksutapaa, joka viittaa mukautettuun ER-muotoosi. Oletuksena kun kutsut ER-muodon sovelluksesta, vain versiot, joiden tila on **Valmis** tai **Jaettu**, otetaan [huomioon](general-electronic-reporting.md#component-versioning). Tämä käytös auttaa estämään sellaisten ER-muotojen käyttöä, joiden mallit eivät ole valmiit. Testiajoissasi voit kuitenkin pakottaa sovelluksen käyttämään ER-muotosi versiota, jonka tila on **Luonnos**. Tällä tavoin voit säätää nykyistä muotoversiota, jos muokkauksia tarvitaan. Lisätietoja on kohdassa [Soveltuvuus](electronic-reporting-destinations.md#applicability).

Käyttääksesi ER-muodon luonnosversiota sinun on merkittävä ER-muoto selkeästi.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. **Käyttäjän parametrit** -valintaikkunassa määritä **Suorita asetukset** -valinnaksi **Kyllä**, ja valitse sitten **OK**.
4. Tee tarvittaessa nykyisestä sivusta muokattava valitsemalla **Muokkaa**.
5. Valitse vasemman ruudun konfiguraatiopuussa **BACS (Iso-Britannia, mukautettu)**.
6. Määritä **Suorita luonnos** -vaihtoehdoksi **Kyllä**.

    ![Suorita luonnos -vaihtoehto Konfiguroinnit-sivulla.](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Käsittele toimittajamaksu käyttämällä mukautettua ER-muotoa

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Määritä sähköinen maksutapa

Sinun on määritettävä sähköinen maksutapa siten, että mukautettua ER-muotoasi käytetään toimittajamaksujen käsittelyyn.

1. Valitse **Ostoreskontra** \> **Maksun asetukset** \> **Maksutavat**.
2. Valitse **Maksutapa - Toimittajat** -sivulla **Sähköinen** maksumenetelmä vasemmasta ruudusta.
3. Valitse **Muokkaa**.
4. Määritä **Tiedostomuoto**-pikavälilehdessä **Yleinen sähköinen vientimuoto** -asetukseksi **Kyllä**.
5. Valitse **Vientimuodon konfigurointi** -kentässä **BACS (Iso-Britannia, mukautettu)** -muotoinen konfiguraatio.

    ![Maksutavat – toimittajat -sivulla voit määrittää sähköisen maksutavan, jolla toimittajamaksut käsitellään mukautetussa muodossa.](./media/er-quick-start2-method-of-payment2.png)

6. Valitse **Tallenna**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Käsittele toimittajamaksu

1. Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.
2. Valitse **Toimittajan maksukirjauskansio** -sivulla aiemmin luomasi kirjauskansio.
3. Valitse **Rivit**.
4. Valitse **Toimittajan maksut** -sivulla, ruudukon yläpuolella **Maksun tila** \> **Ei mikään**.
5. Valitse **Luo maksu**.
6. Anna seuraavat tiedot **Muodosta maksut** -valintaikkunassa:

    - Valitse **Maksutapa**-kentässä **Sähköinen**.
    - Valitse **Pankkitili**-kentässä **GBSI OPER**.

7. Valitse **OK**.
8. Määritä **Sähköisen raportin parametrit** -valintaikkunassa **Tulosta valvontaraportti** -asetukseksi **Kyllä** ja valitse sitten **OK**.

    > [!NOTE]
    > Maksutiedoston lisäksi voit luoda vain valvontaraportin.

9. Lataa zip-tiedosto ja pura siitä sitten seuraavat tiedostot:

    - Valvontaraportti Excel-muodossa
    - Maksutiedosto TXT-muodossa

        Huomaa, että mukautetun ER-muotosi rakenteen mukaisesti luodun tiedoston maksurivi [alkaa](#PositionSWIFTCode) nyt SWIFT-koodilla, joka [syötettiin](#DefineSWIFTCode) sen toimittajan pankkitilille, jonka maksu on käsitelty.

        ![Toimittajamaksun käsittelemiseen käytettävä maksutiedosto TXT-muodossa.](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Tuo ER-muodon vakiokonfiguraatioiden uudet versiot

Tässä osiossa näkyvää esimerkkiä varten saat ilmoituksen Knowledge Base -artikkelista [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046). Tämä ilmoitus kertoo sinulle Microsoftin julkaiseman **BACS (Iso-Britannia)** -ER-muodon uuden version. Valvontaraportin lisäksi tämä uusi versio antaa käyttäjien luoda maksuehdotusraportin ja osallistumishuomautusraportin, kun toimittajamaksua käsitellään. Haluat alkaa käyttää kyseistä toimintoa.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Tuo ER-vakiokonfiguraatioiden uudet versiot

Jos haluat lisätä ER-konfiguraatioiden uusia versioita nykyiseen Finance-esiintymään, sinun on tuotava ne ER-[säilöstä](general-electronic-reporting.md#Repository), jonka olet määrittänyt.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet** -osassa **Microsoft**-ruutu ja valitse sitten **Säilöt** nähdäksesi luettelon Microsoft-toimittajan säilöistä.
3. Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **Yleinen** ja valitse sitten **Avaa**. Jos sinulta pyydetään valtuutusta Regulatory Configuration Service -palveluun yhdistämiseen, noudata valtuutusohjeita.
4. Valitse **Konfiguraatiosäilö**-sivun vasemmassa ruudussa olevasta konfiguraatiopuusta **BACS (Iso-Britannia)** -muotoinen konfiguraatio.
5. Valitse **Versiot**-pikavälilehdestä valitun ER-muodon konfiguraation versio **3.3**.
6. Lataa valittu versio yleisestä säilöpalvelusta nykyiseen Finance-esiintymään valitsemalla **Tuo**.

![Konfigurointitietovarastosivu, Versiot-pikavälilehti, Tuo-painike.](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Jos sinulla on ongelmia [yleiseen säilöön](er-download-configurations-global-repo.md) pääsyssä, voit [ladata konfiguraatiot](download-electronic-reporting-configuration-lcs.md) sen sijaan LCS-palvelusta.

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>Tarkista tuodut ER-muodon konfiguraatiot

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli** ja valitse sitten **BACS (Iso-Britannia)**.
4. Valitse **Versiot**-pikavälilehdessä versio **3.3**.
5. Valitse **Suunnittelu**.
6. Laajenna **Muodon suunnittelija** -sivulla **BACSReportsFolder**-muotoelementti.
7.  Huomaa, että versio 3.3 sisältää **PaymentAdviceReport**-muotoelementin, jota käytetään maksuehdotusraportin luomiseen, kun toimittajamaksua käsitellään.

    ![PaymentAdviceReport-muotoelementti ER-toimintojen suunnitteluohjelmassa.](./media/er-quick-start2-imported-solution2.png)

8. Sulje suunnitteluohjelmasivu.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Ota uudessa versiossa käyttöön tuodun muodon muutokset mukautetussa muodossa

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Viimeistele mukautetun muodon nykyinen luonnosversio

Jos haluat säilyttää mukautetun muotosi nykyisen tilan, viimeistele luonnosversio 1.1.1 muuttamalla sen tila **Luonnos** tilaksi **Valmis**.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli**, laajenna **BACS (Iso-Britannia)** ja valitse sitten **BACS (Iso-Britannia, mukautettu)**.
4. Valitse **Versiot**-pikavälilehdessä **Muuta tila** \> **Valmis** ja valitse sitten **OK**.

Version 1.1.1 tila muuttuu tilasta **Luonnos** tilaksi **Valmis** ja versio muuttuu vain luku -tilaan. Uusi muokattava versio 1.1.2 on lisätty, ja sen tila on **Luonnos**. Voit käyttää tätä versiota tehdäksesi lisämuutoksia mukautettuun ER-muotoosi.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Pohjusta mukautettu muoto uuteen perusversioon

Jos haluat alkaa käyttää **BACS (Iso-Britannia)** -muodon version 3.3 uutta toimintoa mukauttamisessasi, sinun on muutettava mukautetun **BACS (Iso-Britannia, mukautettu)** -konfiguraation peruskonfiguraatioversiota. Tätä prosessia kutsutaan [pohjustamiseksi](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase). Käytä **BACS (Iso-Britannia)** -version 1.1 sijaan versiota 3.3.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Maksumalli** ja valitse sitten **BACS (Iso-Britannia, mukautettu)**.
3. Valitse **Versiot**-pikavälilehdessä versio **1.1.2** ja valitse sitten **Pohjusta**.
4. Valitse **Pohjusta**-valintaikkunan **Kohdeversio**-kentässä peruskonfiguraation versio **3.3** käyttääksesi sitä uutena perusteena ja käyttääksesi sitä konfiguraation päivittämiseen.

    ![Pohjusta-valintaikkuna.](./media/er-quick-start2-rebase1.png)

5. Valitse **OK**.
6. Huomaa, että luonnosversion numero on muuttunut numerosta **1.1.2** numeroksi **3.3.2** heijastamaan perusversion muutosta.

    Kun mukautettu versio ja uusi perusversio yhdistetään, saatetaan havaita joitakin konflikteja, jotka johtuvat muodon muutoksista, joita ei voida yhdistää automaattisesti.

    ![Uudelleenpohjustettu konfiguraatio, jossa on konflikteja, Konfiguraatiot-sivulla.](./media/er-quick-start2-rebase2.png)

    Jos konflikteja havaitaan, ne on ratkaistava manuaalisesti muodon suunnitteluohjelmassa.

7. Valitse **Versiot**-pikavälilehdessä versio **3.3.2**.
8. Valitse **Suunnittelu**.
9. Valitse **Muodon suunnittelija** -sivun **Tiedot**-pikavälilehdessä uudelleenpohjustettu konfliktitietue ja valitse sitten **Kohdista perusarvo**.

    ![Uudelleenpohjustettu konfliktitietue ER-toimintojen suunnitteluohjelmassa.](./media/er-quick-start2-rebase3.png)

10. Valitse **Tallenna**.

    Uudelleenpohjustetun konfliktitietueen ei pitäisi enää näkyä **Tiedot**-pikavälilehdessä.

    ![Konflikti ratkaistu ER-toimintojen suunnitteluohjelmassa.](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Ratkaisit konfliktin vahvistamalla, että perusmallin versiota 3 pitää käyttää tässä ER-muodossa.

11. Laajenna **BACSReportsFolder** \> **-tiedosto** \> **tapahtumat** \> **tapahtuma**.
12. Huomaa **Kartoitus**-välilehdessä, että mukautetun ER-muotosi versio 3.3.2 sisältää sekä mukautetun (**vendBankSWIFT**-muotoelementti ja sen sidonta) että uuden Microsoftin tarjoaman ER-muodon version 3.3 toiminnon (**PaymentAdviceReport**-muotoelementti yhdessä sen sisäkkäisten elementtien ja määritettyjen sidontojen kanssa). Vain muutamalla hiiren napsautuksella olet ottanut uuden perusversion muokkaukset käyttöön yhdistämällä ne mukautuksesi kanssa.

    ![Yhdistetty muoto ER-toimintojen suunnitteluohjelmassa.](./media/er-quick-start2-rebase5.png)

13. Sulje suunnitteluohjelmasivu.

> [!NOTE]
> Uudelleenpohjustustoimintoa ei voi perua. Voit peruuttaa tämän uudelleenpohjustuksen valitsemalla version **1.1.1** **BACS (Iso-Britannia, mukautettu)** -muodosta **Versiot**-pikavälilehdessä ja valitsemalla sitten **Nouda tämä versio**. Versio 3.3.2 saa sitten uuden numeron 1.1.2 ja luonnosversion 1.1.2 sisältö vastaa version 1.1.1 sisältöä.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Käsittele toimittajamaksu käyttämällä pohjustettua ER-muotoa

1. Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.
2. Valitse **Toimittajan maksukirjauskansio** -sivulla aiemmin luomasi kirjauskansio.
3. Valitse **Rivit**.
4. Valitse **Toimittajan maksut** -sivulla, ruudukon yläpuolella **Maksun tila** \> **Ei mikään**.
5. Valitse **Luo maksu**.
6. Anna seuraavat tiedot **Muodosta maksut** -valintaikkunassa:

    - Valitse **Maksutapa**-kentässä **Sähköinen**.
    - Valitse **Pankkitili**-kentässä **GBSI OPER**.

7. Valitse **OK**.
8. Anna seuraavat tiedot **Sähköisen raportin parametrit** -valintaikkunassa:

    - Määritä **Tulosta valvontaraportti** -asetukseksi **Kyllä**.
    - Määritä **Tulosta maksuilmoitus** -asetukseksi **Kyllä**.

    ![Sähköisen raportin parametrit -valintaikkuna.](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Maksutiedoston lisäksi voit nyt luoda sekä valvontaraportin että maksuehdotusraportin.

9. Valitse **OK**.
10. Lataa zip-tiedosto ja pura siitä sitten seuraavat tiedostot:

    - Valvontaraportti Excel-muodossa
    - Maksuehdotusraportti Excel-muodossa

        ![Maksuehdotusraportti Excel-muodossa.](./media/er-quick-start2-payment-advice-report.png)

    - Maksutiedosto TXT-muodossa

        Huomaa, että luodun tiedoston maksurivi alkaa SWIFT-koodilla, joka syötettiin sen toimittajan pankkitilille, jonka maksu on käsitelty.

        ![Toimittajamaksun käsittelemiseen käytettävä maksutiedosto TXT-muodossa, joka käyttää pohjustettua ER-muotoa.](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [ER-konfiguraatioiden lataaminen Lifecycle Services -palvelusta](download-electronic-reporting-configuration-lcs.md)
- [Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
