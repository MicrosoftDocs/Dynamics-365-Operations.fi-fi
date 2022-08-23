---
title: Sähköisten raportointimääritysten mukauttaminen luomaan sähköinen asiakirja
description: Tässä artikkelissa käsitellään niiden Microsoftin toimittamien sähköisen raportoinnin (ER) määritysten mukauttamista, joilla luodaan mukautettu sähköinen asiakirja.
author: kfend
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314,  ""intro-internal
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
ms.openlocfilehash: cd3200bea07d622632dc5781638ec825c21233e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278943"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Sähköisten raportointimääritysten mukauttaminen luomaan sähköinen asiakirja

[!include[banner](../includes/banner.md)]

[Sähköisen raportoinnin (ER) kehyksellä](general-electronic-reporting.md) voi ladata Microsoftin toimittamia ER-[määrityksiä](general-electronic-reporting.md#Configuration) Microsoft Dynamics 365 Finance -esiintymään. Tällä tavoin Microsoftin toimittamia määrityksiä voidaan käyttää ER-ratkaisuna, joista luodaan sähköisiä myyntilaskuja (e-laskuja). Tällä ER-ratkaisulla voi määrittää mukautetun ER-ratkaisun käyttämään mukautetun tietokannan kenttiä ja luodaan omien vaatimusten mukaisia e-laskuja – lähdekoodia muokkaamatta.

## <a name="overview"></a>Yleiskuvaus

Tämän artikkelin esimerkkiä varten on määritettävä liittovaltion verokoodi uudeksi mukautetuksi määritteeksi jokaiselle asiakkaille, jota laskutetaan sähköisesti. Tämän tällä hetkellä käytössä olevan rakennetta on mukautettava lisäämällä uusi kohde, johon verokoodi on lisättävä jokaisessa luotavassa e-laskussa.

Tämän artikkelin menettelyissä käsitellään tapaa, jolla järjestelmänvalvojan,sähköisen raportoinnin kehittäjän tai sähköisen raportoinnin toiminnallisen konsultin roolissa oleva käyttäjä voi tehdä seuraavat tehtävät Finance-esiintymässä:

- [ER-kehyksen käytön aloittamiseen tarvittavan ER-parametrien vähimmäisjoukon määrittäminen](#ConfigureER)
- [E-laskujen luontia varten toimitettujen ER-vakiomääritysten alkuperäisten versioiden tuominen](#ImportERConfigurations1)
- [ER-vakiomääritysten käytön aloittaminen määrittämällä myyntireskontran parametrit](#ConfigureAR1)
- [Asiakkaiden laskuttamiseen tarvittavien yritysparametrien määrittäminen](#ConfigureLE)
- [Asiakastietueen valmisteleminen sähköistä laskutusta varten](#ConfigureCustomer1)
- [Myyntilaskun lisääminen, kirjaaminen ja lähettäminen ER-vakiomääritysten avulla](#ProcessInvoice1)
- [Asiakkaiden liittovaltion verokoodin hallinta lisäämällä mukautettu tietokantakenttä](#AddCustomField)
- [ER-mallimäärityksen suunnitteluohjelman tietokantamuutosten ottaminen käyttöön päivittämällä ER-metatiedot](#RefreshERMetadata)
- [Mukautettujen ER-määritysten suunnitteleminen luomaan uuden verokoodin sisältäviä e-laskuja](#DesignCustomERConfigurations)
- [Mukautettujen ER-määritysten käytön aloittaminen määrittämällä myyntireskontran parametrit](#ConfigureAR2)
- [Asiakastietueen päivittäminen sähköistä laskutusta varten](#ConfigureCustomer2)
- [Myyntilaskun lisääminen, kirjaaminen ja lähettäminen mukautettujen ER-määritysten avulla](#ProcessInvoice2)
- [E-laskujen luontia varten toimitettujen ER-vakiomääritysten uusien versioiden tuominen](#ImportERConfigurations2)
- [Mukautetuissa ER-määrityksissä ER-vakiomääritysten uusiin versioihin tehtyjen muutosten ottaminen käyttöön](#RebaseCustomERConfigurations)
- [Myyntilaskun lisääminen, kirjaaminen ja lähettäminen mukautettujen ER-määritysten uusien versioiden avulla](#ProcessInvoice3)

Kaikki nämä menettelyt voidaan suorittaa **DEMF**-yrityksessä.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>Määritä ER-kehys

Käyttäjän, jolla on sähköisen raportoinnin toiminnallisen konsultin tai sähköisen raportoinnin kehittäjän rooli, on määritettävä ER-parametrien vähimmäisjoukko. Sen jälkeen voidaan aloittaa ER-kehystä käyttävä mukautettujen versioiden suunnittelu niistä ER-ratkaisun vakiomäärityksistä, joilla luodaan e-laskuja.

### <a name="configure-er-parameters"></a>Konfiguroi ER-parametrit

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin luonnos**-sivun **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.
3. Määritä **Sähköisen raportoinnin parametrit** -sivun **Yleinen**-välilehdessä **Ota käyttöön suunnittelutila** -asetukseksi **Kyllä**.
4. Valitse **Liitteet**-välilehden **Määritykset**-kentässä **Tiedosto**.
5. Valitse **Työarkisto**-, **Väliaikainen**-, **Perusrivi**- ja **Muut**-kentissä **Tiedosto**-tyyppi.

Lisätietoja ER-parametreista on kohdassa [Määritä ER-kehys](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>Aktivoi ER-konfiguraation lähde

Jokainen lisätty ER-konfiguraatio merkitään ER-konfiguraation lähteen omistamaksi. ER-konfiguraation lähdettä, joka on aktivoitu **Sähköinen raportointi** -työtilassa, käytetään tähän tarkoitukseen. Siksi sinun on aktivoitava ER-konfiguraation lähde **Sähköinen raportointi** -työtilassa, ennen kuin voit alkaa lisätä tai muokata ER-konfiguraatioita.

> [!NOTE]
> Vain ER-konfiguraation omistaja voi muokata sitä. Siksi ennen kuin ER-konfiguraatiota voi muokata, asianmukainen ER-konfiguraation lähde on aktivoitava **Sähköinen raportointi** -työtilassa.

#### <a name="review-the-list-of-er-configuration-providers"></a>Tarkista ER-konfiguraation lähteiden luettelo

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin luonnos**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.
3. **Konfiguraation lähdetaulu** -sivulla jokaisen lähteen tietueella on yksilöllinen nimi ja URL-osoite. Tarkista tämän sivun sisältö. Jos **Litware, Inc.** (`https://www.litware.com`) -tietue on jo olemassa, ohita seuraava menettely, [Lisää uusi ER-konfiguraation lähde](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Lisää uusi ER-konfiguraation lähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin luonnos**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.
3. Valitse **Konfiguraation lähteet**-sivulla **Uusi**.
4. Kirjoita **Nimi**-kenttään **Litware, Inc.**
5. Kirjoita **Internetosoite**-kenttään `https://www.litware.com`.
6. Valitse **Tallenna**.

#### <a name="activate-an-er-configuration-provider"></a>Aktivoi ER-konfiguraation lähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin luonnos**-sivun **Konfiguraation lähteet**-osassa **Litware, Inc.** -ruutu ja valitse sitten **Aseta aktiiviseksi**.

Lisätietoja ER-konfiguraation lähteistä on kohdassa [Konfiguraation lähteiden luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>ER-vakiomääritysten alkuperäisten versioiden tuominen

ER-vakiomääritys voidaan lisätä Finance-esiintymään tuomalla ne kyseiselle esiintymällä määritetystä ER-[säilöstä](general-electronic-reporting.md#Repository).

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin luonnos**-sivun **Konfiguraation lähteet** -osassa **Microsoft**-ruutu ja valitse sitten **Säilöt** nähdäksesi luettelon Microsoft-toimittajan säilöistä.
3. Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **Yleinen** ja valitse sitten **Avaa**. Jos sinulta pyydetään valtuutusta Regulatory Configuration Service -palveluun yhdistämiseen, noudata valtuutusohjeita.
4. Valitse **Konfiguraatiosäilö**-sivun vasemman ruudun määrityspuussa **Peppol-myyntilasku** -muotoinen määritys.
5. Valitse **Versiot**-pikavälilehdessä versio **11.2.2**.
6. Lataa valittu versio yleisestä säilöstä valitsemalla **Tuo**.

![Konfiguraatiosäilön sivu.](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Jos sinulla on ongelmia [yleiseen säilöön](er-download-configurations-global-repo.md) pääsyssä, voit [ladata konfiguraatiot](download-electronic-reporting-configuration-lcs.md) sen sijaan Microsoft Dynamics Lifecycle Services (LCS) -palvelusta.

### <a name="review-the-imported-er-configurations"></a>Tarkista tuodut ER-konfiguraatiot

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin luonnos**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Laajenna **Määritykset**-sivulla **Määrityksen osat** -pikavälilehti.
4. Laajenna vasemman ruudun määrityspuussa ensin **Laskumalli** ja sitten **UBL-myyntilasku**.

Huomaa, että valitun **Peppol-myyntilasku** -ER-muodon lisäksi myös muut tarvittavat ER-muodot tuotiin. Koska ER-määritysten uusia versioita julkaistaan jatkuvasti yleiseen säilöön ja LCS:ään, jotta niitä vastaavat ratkaisut pysyvät uusien vaatimusten mukaisina, pakollisen tietomallin määrityksen uusimmat versiot ja sen mallimääritykset tuotiin.

![Konfiguraatiot-sivu.](./media/er-quick-start3-imported-solution1a.png)

Seuraavien ohjeiden avulla voi simuloida tilan, jossa ER-määritykset olisivat nykyisessä Finance-esiintymässä, jos **Peppol-myyntilasku** -ER-muodon versio **11.2.2** tuotiin aiemmin (esimerkiksi 7. elokuuta 2019):

- Poista kaikki ER-määritykset, jotka julkaistiin 7. elokuuta 2019 jälkeen valitsemalla toimintopaneelissa **Poista**. Jäljelle saa jäädä vain seuraavat määritykset: **Laskumalli**, **Laskumallin yhdistämismääritys** (alkuperäinen nimi oli **Myyntilaskumallin yhdistämismääritys**), **UBL-myyntilasku** ja **Peppol-myyntilasku**.
- Valitse jäljellä olevien ER-määritysten osalta **Versiot**-pikavälilehdessä **Poista**, jolloin kaikki 7. elokuuta 2019 jälkeen julkaistut ER-määritysten versiot poistetaan.

Varmista sitten, seuraavat määritykset ovat määrityspuussa:

- **Laskumalli** ER-tietomallin määritys (alkuperäinen nimi oli **Asiakaslaskumalli**):

    - Versio 11 sisältää tietomallin ER-osan version 10, joka ilmaisee laskutuksen liiketoiminnan toimialueen tietorakenteen. Tämä ER-määritys on tuotu tuotavaksi valitun **Peppol-myyntilasku** -ER-muodon edeltäjänä.
    - Versio 50 sisältää tietomallin ER-osan version 31. Tämä ER-määritys on tuotu **Laskumallin yhdistämismääritys** -ER-mallin yhdistämismäärityksen elokuun 7. päivän 2019 version edeltäjänä

    ![Laskumallin ER-tietomallin määritys Määritykset-sivulla.](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Jos tämän tietomallin versio 50 ei ole näkyvissä, avaa yleinen säilö ja tuo **Laskumallin yhdistämismääritys** -ER-määrityksen versio 50.19.

- **Laskumallin yhdistämismääritys** -ER-tietomallin yhdistämismäärityksen määritys (alkuperäinen nimi oli **Asiakaslaskumallin yhdistämismääritys**):

    - Versio 50.19 on tuotu **Laskumalli**-ER-tietomallin määrityksen version 50 uusimpana toteutuksena. Siinä on kaksi mallin yhdistämismäärityksen ER-osaa, joissa kuvataan sovelluksen tietojen täyttämistä suorituspalvelussa.

    ![Laskumallin ER-tietomallin määritys Määritykset-sivulla.](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Jos tämän mallin yhdistämismäärityksen versio 50.19 ei ole näkyvissä, avaa yleinen säilö ja tuo **Laskumallin yhdistämismääritys** -ER-määrityksen versio 50.19.

- **UBL-myyntilasku** ER-muodon määritys:

    - Versio 11.2 sisältää muodon ja muodon yhdistämismäärityksen ER-osat. Muoto-osa määrittää raportin asettelun. Muodon määritysosa sisältää mallin tietolähteen ja määrittää, miten raportin asettelu täytetään käyttämällä tätä tietolähdettä suorituspalvelussa. Tämä ER-muoto määritettiin luomaan e-laskuja UBL (Universal Business Language)-muodossa. Se on tuotu tuotavaksi valitun **Peppol-myyntilasku** -ER-muodon ylätasona.

- **Peppol--myyntilasku** ER-muodon määritys:

    - Versio 11.2.2 sisältää ne muodon ja muodon yhdistämismäärityksen ER-osat, jotka määritettiin luomaan PEPPOL (Pan-European Public Procurement OnLine) -muotoisia e-laskuja.

    ![Peppol-myyntilaskun ER-muodon määritys Määritykset-sivulla.](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Myyntireskontran parametrien määrittäminen

1. Valitse **Myyntireskontra** \> **Määritys** \> **Myyntireskontran parametrit**.
2. Valitse **Sähköiset asiakirjat** -välilehden **Sähköinen raportointi** -pikavälilehden **Hyvityslasku ja vapaatekstihyvityslasku** -kentässä **Peppol-myyntilasku**.
3. Valitse **Tallenna**.

![Sähköiset asiakirjat -välilehti Myyntireskontran parametrit -sivulla.](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Yritysparametrien määrittäminen

1. Valitse **Organisaation hallinto** \> **Organisaatiot** \> **Yritykset**.
2. Lisää **1234** valitun **DEMF**-yrityksen **Pankkikoodi**-kenttään **Pankkitilitiedot**-pikavälilehdessä.
3. Valitse **Tallenna**.
4. Sulje **Yritykset**-sivu.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Asiakastietueen valmisteleminen

1. Valitse **Myyntireskontra** \> **Asiakkaat** \> **Kaikki asiakkaat**.
2. Valitse **Kaikki asiakkaat** -sivulla **DE-014**-asiakastilin linkki.

### <a name="add-a-customer-contact"></a>Asiakkaan yhteyshenkilön lisääminen

1. Valitse **Myyntireskontra** \> **Asiakkaat** \> **Kaikki asiakkaat**.
2. Valitse toimintoruudun **Asiakas**-välilehden **Tilit**-ryhmässä **Yhteyshenkilöt**.
3. Valitse **Lisää yhteyshenkilöitä**.
4. Avaa **Yhteyshenkilöt**-sivun **Etunimi**-kentän haku, valitse **Adam Carter** ja sulje sitten haku valitsemalla **Valitse**.
5. Valitse **Tallenna**.
6. Sulje **Yhteyshenkilöt**-sivu.

### <a name="define-a-primary-contact"></a>Ensisijaisen yhteyshenkilön määrittäminen

1. Valitse **Myyntireskontra** \> **Asiakkaat** \> **Kaikki asiakkaat**.
2. Valitse **Myyntien demografia** -pikavälilehden **Ensisijainen yhteyshenkilö** -kentässä **Adam Carter**.

### <a name="set-the-e-invoicing-option"></a>Sähköisen laskutusvaihtoehdon määrittäminen

1. Valitse **Myyntireskontra** \> **Asiakkaat** \> **Kaikki asiakkaat**.
2. Määritä **Lasku ja toimitus** -pikavälilehden **eInvoice**-asetukseksi **Kyllä**.
3. Valitse **Tallenna**.
4. Sulje **Kaikki asiakkaat** -sivu.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Myyntilaskun käsitteleminen ER-vakiomääritysten avulla

Voit nyt käyttää tuotuja ER-vakiomäärityksiä vapaatekstilaskun lähettämiseen sähköisessä muodossa asiakkaalle.

### <a name="add-a-new-invoice"></a>Uuden laskun lisääminen

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Valitse **Vapaatekstilasku**-sivulla **Uusi**.
3. Valitse **Vapaatekstilaskun otsikko** -pikavälilehden **Asiakastili**-kentässä **DE-014**.
4. Laskurivi lisätään automaattisesti **Laskurivit**-pikavälilehdessä. Määritä tälle riville seuraavat kentät:

    - Kirjoita **Kuvaus**-kentässä **Muistikirja**.
    - Valitse **Päätili**-kentässä **401100**.
    - Kirjoita **Yksikköhinta**-kentässä **1000**.

5. Valitse **Tallenna**.

![Vapaatekstilaskun sivu.](./media/er-quick-start3-add-invoice.png)

Lisätietoja on kohdassa [Vapaatekstilaskun luominen](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Uuden laskun kirjaaminen

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Valitse **Vapaatekstilasku**-sivun toimintoruudussa **Kirjaa**
3. Valitse **Kirjaa vapaatekstilasku** -valintaikkunassa **OK**.

![Vapaatekstilaskun tietosivu.](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Kirjatun laskun lähettäminen

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Valitse **Vapaatekstilasku**-sivun toimintoruudun **Asiakirja**-ryhmässä **Lähetä** \> **Alkuperäinen**.

    ![Alkuperäisen laskun esikatselu.](./media/er-quick-start3-send-invoice.png)

3. Sulje **Vapaatekstilasku**-sivu.

### <a name="analyze-a-generated-e-invoice"></a>Luodun e-laskun analysoiminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin työt**.
2. Valitse **Sähköisen raportoinnin työt** -sivulla alkuperäinen tietue, jonka tehtävän kuvaus on **Lähetä eInvoice XML**.
3. Siirry luotujen tiedostojen luetteloon valitsemalla **Näytä tiedostot**.

    ![Sähköisen raportoinnin töiden sivu.](./media/er-quick-start3-jobs-list.png)

4. Lataa e-laskun luotu XML-tiedosto valitsemalla **Avaa**.
5. Analysoi e-laskun XML-tiedosto. Huomaa, että asiakkaan veromalli ilmaistaan tällä hetkellä XML-määritteillä **schemeID** ja **schemeAgencyID**. Huomaa myös, että XML-elementti **cbc:CustomizationID** sisältää tällä hetkellä seuraavan tekstin: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Luodun e-laskun XML-tiedoston esikatselu.](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Mukautetun tietokantakentän lisääminen

[Mukautettu kenttä](../../fin-ops/get-started/user-defined-fields.md) -ominaisuudella voi mukauttaa nykyistä Finance-esiintymää seuraavasti:

- Tietokannan rakenteen mukauttaminen lisäämällä mukautetun tietokantakentän, johon tallennetaan jokaisen asiakkaan verotunnuskoodi.
- **Asiakas**-sivun mukauttaminen lisäämällä uusi tietojen syöttökenttä, jolla voidaan antaa verokoodin arvo uudessa mukautetussa tietokantakentässä.

Tee mukautukset seuraavasti:

1. Valitse **Myyntireskontra** \> **Asiakkaat** \> **Kaikki asiakkaat**.
2. Valitse **Kaikki asiakkaat** -sivulla **DE-014**-asiakastilin linkki.
3. Napsauta **Yleiset**-pikavälilehdessä **Kieli**-kentän alapuolella olevaa tyhjää aluetta hiiren kakkospainikkeella ja valitse sitten **Mukauta: UpperGroup**.

    **Yleiset**-pikavälilehden sisältö korostetaan ja **Mukauta**-valikko avautuu.

4. Valitse **Mukauta**-valikossa **Lisää kenttä**.
5. Valitse **Lisää sarakkeita** -valintaikkunassa **Luo uusi kenttä**.
6. Valitse **Luo uusi kenttä** -valintaikkunan **Taulukon nimi** -kentässä **Asiakkaat**.
7. Kirjoita **Nimen etuliite** -kenttään **FederalTaxID**.

    > [!NOTE]
    > Koko kentän nimi on määritetty automaattisesti muotoon **FederalTaxID\_Custom**.

8. Kirjoita **Selite**-kenttään **Liittovaltion verotunnus**.
9. Valitse **Tyyppi**-kentässä **Teksti**.
10. Kirjoita **Pituus**-kenttään **20**.
11. Valitse **Tallenna**.
12. Valitsemalla avautuvassa sanomaruudussa **Kyllä** vahvistat, että haluat luoda uuden **FederalTaxID**-kentän **Asiakkaat**-taulukkoon.
13. Lisää <a name="insert_custom_field"></a>**FederalTaxID\_Custom** -kenttä nykyiselle sivulle valitsemalla **Lisää**.

    ![Kaikki asiakkaat -sivu.](./media/er-quick-start3-create-new-field.gif)

14. Sulje **Kaikki asiakkaat** -sivu.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>ER-metatietojen päivittäminen

ER-metatiedot on päivitettävä, jotta lisätty mukautettu kenttä tulee [näkyviin](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) ER-mallin yhdistämismäärityksen suunnitteluohjelmassa.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Muodosta taulukkoviitteet uudelleen**.
2. Valitse **Päivitä tietomalli** -valintaikkunassa **OK**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Mukautettujen ER-määritysten suunnitteleminen

Microsoftin toimittamia ER-määrityksiä voi käyttää mukautettujen ER-määritysten suunnittelussa siten, että niillä luodaan uuden verokoodin sisältäviä e-laskuja.

### <a name="customize-the-data-model-configuration"></a>Tietomallin määrityksen mukauttaminen

Sähköisen raportoinnin toiminnallisen konsultin roolia käyttävä käyttäjä voi suunnitella mukautetun ER-tietomallin.

#### <a name="add-a-custom-data-model-configuration"></a>Mukautetun ER-tietomallimäärityksen lisääminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun vasemman ruudun määrityspuussa **Myyntilaskumalli**.
3. Valitse toimintoruudussa **Luo konfigurointi**.
4. Valitse avattavan valintaikkunan **Uusi**-kentässä **Johda nimestä: myyntilaskumalli, Microsoft**. Tämä ilmaisee, että uuden mukautetun ER-tietomallin määrityksen on perustuttava ER-tietomallin määritykseen.
5. Kirjoita **Nimi**-kenttään **Laskumalli (Litware)**.
6. Lisää uusi ER-määritys valitsemalla **Luo määritys**.

ER-tietomallin suunnitteluohjelmassa voi nyt muokata **Luonnos**-tilassa olevaa **Laskumalli (Litware)** -ER-määrityksen versiota 50.1.

![ER-määrityksen versio 50.1 Määritykset-sivulla.](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Mukautetun tietomallin määrittäminen

Mukautettua tietomallia on muokattava lisäämällä uusi kenttä antamaa liittovaltion verotunnuskoodin arvo. Tämä koodi on osa jokaisen tätä tietomallia tietolähteenä käyttävän ER-muodon asiakastietoja.

1. Valitse **Määritys**-sivun vasemman ruudun määrityspuussa **Laskumalli (Litware)**.
2. Valitse **Versiot**-pikavälilehdessä **Luonnos**-tilassa olevan valitun ER-tietomallin määrityksen versio **50.1**.
3. Valitse toimintoruudussa valitulle määritysversiolle **Suunnitteluohjelma**.
4. Valitse **Tietomallin suunnitteluohjelma** -sivun tietomalli puussa **Asiakastiedot (asiakas)**.
5. Valitse **Uusi**.
6. Hyväksy avattavan valintaikkunan **Uusi solmu muodossa** -kentässä oletusarvo **Aktiivisen solmun alikohde**.
7. Kirjoita **Nimi**-kenttään **FederalTaxID\_Litware**.
8. Hyväksy **Nimiketyyppi**-kentän oletusarvo **Merkkijono**.
9. Valitse ensin **Lisää** ja sitten **Tallenna**.

    ![Tietomallin suunnitteluohjelman sivu.](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > **Selite**- ja **Kuvaus**-kentissä on tietoja uuden kentän tarkoituksesta. Näiden kenttien käyttämiseen voidaan käyttää useita kieliä. Lisätietoja on kohdassa [Monikielisten raporttien suunnitteleminen sähköisessä raportoinnissa](er-design-multilingual-reports.md).

10. Sulje **Tietomallin suunnittelu** -sivu.

#### <a name="complete-a-custom-data-model-configuration"></a>Mukautetun tietomallimäärityksen viimeisteleminen

Mukautetun ER-tietomallin määrityksen version 50.1 käsitteleminen on päätettävä, ennen kuin se on käytettävissä ja ennen kuin siihen voidaan lisätä muita mukautettuja ER-määrityksiä.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Laskumalli** ja valitse **Laskumalli (Litware)**.
3. Valitse **Versiot**-pikavälilehdessä **Muuta tila** \> **Valmis** ja valitse sitten **OK**.

Version 50.1 tila muuttuu tilasta **Luonnos** tilaksi **Valmis** ja versio muuttuu vain luku -tilaan. Uusi muokattava versio 50.2 on lisätty, ja sen tila on **Luonnos**. Tällä versiolla voi tehdä muita muutoksia mukautetun ER-tietomallin määritykseen.

![Valmis versio 50.1 Määritykset-sivulla.](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Mallin yhdistämismäärityksen mukauttaminen

Sähköisen raportoinnin kehittäjän roolia käyttävä käyttäjä voi suunnitella mukautetun ER-mallin yhdistämismäärityksen.

#### <a name="add-a-custom-model-mapping-configuration"></a>Mukautetun mallin yhdistämismäärityksen lisääminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Myyntilaskumalli** ja valitse **Myyntilaskumallin yhdistämismääritys**.
3. Valitse toimintoruudussa **Luo konfigurointi**.
4. Valitse avattavan valintaikkunan **Uusi**-kentässä **Johda nimestä: myyntilaskumallin yhdistämismääritys, Microsoft**. Tämä ilmaisee, että uuden mukautetun ER-mallin yhdistämismäärityksen on perustuttava ER-mallin yhdistämismääritykseen.
5. Kirjoita **Nimi**-kenttään **Laskumallin yhdistämismääritys (Litware)**.
6. Valitse **Kohdemalli**-kentässä **Laskumalli (Litware)**.

    > [!IMPORTANT]
    > Tämä vaihe on erittäin tärkeä. Jos sitä ei tehdä, mukautettua tietomallia ei voi käyttää määritetyssä mallin yhdistämismäärityksessä.

7. Lisää uusi ER-määritys valitsemalla **Luo määritys**.

![Mukautetun mallin yhdistämismäärityksen määrityksen lisääminen Määritykset-sivulla.](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Mukautetun mallin yhdistämismäärityksen määrittäminen

Mukautettua mallin yhdistämismääritystä on muokattava. Lisäksi on määritettävä, miten mukautetun tietomallin mukautettu **FederalTaxID\_Litware** -kenttä täytetään sovelluksen tiedoissa suorituspalvelussa.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Myyntilaskumalli** \> **Myyntilaskumallin yhdistämismääritys** ja valitse **Laskumallin yhdistämismääritys (Litware)**.
3. Valitse toimintoruudussa **Suunnittelija**.
4. Valitse **Malli tietolähteen yhdistämismääritystä varten** -sivulla **Myyntilaskun** yhdistämismääritys.

    ![Malli tietolähteen yhdistämismääritystä varten -sivu.](./media/er-quick-start3-select-customer-mapping.png)

5. Valitse **Suunnittelu**.
6. Laajenna **Mallin yhdistämismäärityksen suunnitteluohjelma** -sivun **Tietolähteet**-ruudussa **CustInvoiceJour**-tietolähde, joka vastaa **CustInvoiceJour** -sovellustaulukkoa.
7. Laajenna **CustInvoiceJour**-kohdassa **Suhteet**, jolloin näkyviin tulee **CustInvoiceJour**-taulukon monta yhteen (N:1) -tyyppisten suhteiden luettelo.
8. Laajenna **CustInvoiceJour** \> **Suhteet** -kohdassa **Asiakkaat (CustTable)**. Pääse nyt käyttämään **Asiakkaat (CustTable)** -taulukon kenttiä ja suhteita.
9. Valitse [aiemmin](#insert_custom_field) käyttöönotettu **FederalTaxID\_Custom**-tietolähdekenttä.
10. Laajenna **Tietomalli**-ruudussa **Asiakastiedot (asiakas)** ja valitse **FederalTaxID\_Litware**-tietomallikenttä.
11. Valitse **Sido**.

    ![Mallimäärityksen suunnittelun sivu.](./media/er-quick-start3-customize-model-mapping.gif)

12. Valitse **Tallenna**.
13. Sulje **Mallimäärityksen sunnittelun** sivu.
14. Sulje **Malli tietolähteen yhdistämismääritystä varten** -sivu.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Mukautetun mallin yhdistämismäärityksen määrityksen viimeisteleminen

Mukautetun ER-mallin yhdistämismäärityksen version 50.19.1 määritys on päätettävä, ennen kuin määritys on käytettävissä.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Myyntilaskumalli** \> **Myyntilaskumallin yhdistämismääritys** ja valitse **Laskumallin yhdistämismääritys (Litware)**.
3. Valitse **Versiot**-pikavälilehdessä **Muuta tila** \> **Valmis** ja valitse sitten **OK**.

Version 50.19.1 tila muuttuu tilasta **Luonnos** tilaksi **Valmis** ja versio muuttuu vain luku -tilaan. Uusi muokattava versio 50.19.2 on lisätty, ja sen tila on **Luonnos**. Tällä versiolla voi tehdä muita muutoksia mukautetun ER-mallin yhdistämismäärityksen määritykseen.

![Valmis versio 50.19.1 Määritykset-sivulla.](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> Määrityksen tuettu [elinkaari](general-electronic-reporting-manage-configuration-lifecycle.md) ei koske tietokantamuutosten elinkaarta. Jos **Laskumallin yhdistämismääritys (Litware)** -määrityksen versio 50.19.1 viedään nykyisestä Finance-esiintymästä, ja se yritetään tuoda toiseen esiintymään, jossa ei ole mukautettua **FederalTaxID\_Custom**-kenttää **CustTable**-taulukossa, tapahtuu poikkeus. Poikkeus ilmoittaa, että tuotu ER-määritys ei ole yhteensopiva Financen kohde-esiintymän metatietojen kanssa.

### <a name="customize-the-format-configuration"></a>Muotomäärityksen mukauttaminen

Sähköisen raportoinnin toiminnallisen konsultin roolia käyttävä käyttäjä voi suunnitella mukautetun ER-mallin.

#### <a name="add-a-custom-format-configuration"></a>Mukautetun muotomäärityksen lisääminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Myyntilaskumalli** \> **UBL-myyntilasku** ja valitse sitten **Peppol-myyntilasku**.
3. Valitse toimintoruudussa **Luo konfigurointi**.
4. Valitse avattavan valintaikkunan **Uusi**-kentässä **Johda nimestä: Peppol-myyntilasku, Microsoft**. Tämä ilmaisee, että uuden mukautetun ER-muodon määrityksen on perustuttava ER-muodon määritykseen.
5. Kirjoita **Nimi**-kenttään **Peppol-myyntilasku (Litware)**.
6. Valitsemalla **Tietomalli**-kentässä **Laskumalli (Litware)** voit käyttää mukautettua tietomallia ja mallin yhdistämismäärityksen osia.

    > [!NOTE]
    > Tämä vaihe on erittäin tärkeä. Jos sitä ei tehdä, mukautettua tietomallia ei voi käyttää määritetyssä muodossa.

7. Valitse **Tietomalli**-kentässä **InvoiceCustomer**-juurimääritelmä.
8. Lisää uusi ER-määritys valitsemalla **Luo määritys**.

![Mukautetun muodon määrityksen lisääminen Määritykset-sivulla.](./media/er-quick-start3-adding-custom-format.png)

ER-toimintojen suunnitteluohjelmassa voi nyt muokata **Luonnos**-tilassa olevaa **Peppol-myyntilasku (Litware)** -ER-määrityksen versiota 11.2.2.1.

![ER-määrityksen versio 11.2.2.1 Määritykset-sivulla.](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Mukautetun muodon määrittäminen

Mukautettua muotoa on muokattava lisäämällä uusi muotoelementti täyttämään laskutetun asiakkaan liittovaltion verotunnuskoodin arvo.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Myyntilaskumalli** \> **UBL-myyntilasku** \> **Peppol-myyntilasku** ja valitse **Peppol-myyntilasku (Litware)**.
3. Valitse toimintoruudussa **Suunnittelija**.
4. Laajenna muotopuussa **XMLHeader** \> **Lasku** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** ja valitse **cbc:ID**.
5. Valitse ensin **Lisää** ja sitten **XML** \> **Määrite**.
6. Kirjoita avattavan **Osan ominaisuus** -valintaikkunan **Nimi**-kenttään **FederalTaxID**.
7. Luo uusi **FederalTaxID**-XML-määrite luodussa tiedostossa valitsemalla **OK**.
8. Valitse kohdassa **XMLHeader** \> **Lasku** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** **FederalTaxID**.
9. Valitse **Siirrä ylös**.

![Uusi muotoelementti Muodon suunnitteluohjelma -sivulla.](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Mukautetun muodon yhdistämismäärityksen määrittäminen

1. Laajenna **Malli**-tyypin **Lasku**-tietolähde **Muodon suunnitteluohjelma** -sivun **Yhdistämismääritys**-välilehdessä.
2. Laajenna **Lasku**-kohdassa **Asiakastiedot (asiakas)** ja valitse **FederalTaxID\_Litware**.
3. Valitse **Sido**.

    ![Muodon suunnittelutoiminto -sivu.](./media/er-quick-start3-customized-format-mapping.png)

4. Valitse **Malli**-tyypin **Lasku**-tietolähde ja valitse sitten **Muokkaa**.
5. Valitse **Versio**-kentässä mukautetun tietomallin version **1** ja valitse sitten **OK**.
6. Valitse **Tallenna**.
7. Sulje **Muodon suunnittelija** -sivu.

#### <a name="complete-a-custom-format-configuration"></a>Mukautetun muotomäärityksen viimeisteleminen

Mukautetun ER-muotomäärityksen version 11.2.2.1 määritys on päätettävä, ennen kuin määritys on käytettävissä.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Myyntilaskumalli** \> **UBL-myyntilasku** \> **Peppol-myyntilasku** ja valitse **Peppol-myyntilasku (Litware)**.
3. Valitse **Versiot**-pikavälilehdessä **Muuta tila** \> **Valmis** ja valitse sitten **OK**.

Version 11.2.2.1 tila muuttuu tilasta **Luonnos** tilaksi **Valmis** ja versio muuttuu vain luku -tilaan. Uusi muokattava versio 11.2.2.2 on lisätty, ja sen tila on **Luonnos**. Tällä versiolla voi tehdä lisämuutoksia mukautetun ER-muodon määritykseen.

![Valmis versio 11.2.2.1 Määritykset-sivulla.](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Mukautettujen ER-määritysten käytön aloittaminen määrittämällä myyntireskontran parametrit

1. Valitse **Myyntireskontra** \> **Määritys** \> **Myyntireskontran parametrit**.
2. Valitse **Sähköiset asiakirjat** -välilehden **Sähköinen raportointi** -pikavälilehden **Hyvityslasku ja vapaatekstihyvityslasku** -kentässä **Peppol-myyntilasku (Litware)**.
3. Valitse **Tallenna**.

![Myyntireskontran parametrit -sivulla, Sähköiset asiakirjat -välilehti, Sähköinen raportointi -pikavälilehti.](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Asiakastietueen päivittäminen lisäämällä liittovaltion verotunnuskoodi

1. Valitse **Myyntireskontra** \> **Asiakkaat** \> **Kaikki asiakkaat**.
2. Valitse **Kaikki asiakkaat** -sivulla **DE-014**-asiakastilin linkki.
3. Anna **Yleiset**-pikavälilehden **Liittovaltion verotunnus** -kentässä **LITWARE-6789**.
4. Valitse **Tallenna**.

    ![DE-014 asiakastietojen sivu.](./media/er-quick-start3-added-tax-id-value.png)

5. Sulje **Kaikki asiakkaat** -sivu.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Myyntilaskun käsitteleminen mukautettujen ER-määritysten avulla

### <a name="select-and-send-a-posted-invoice"></a>Kirjatun laskun valitseminen ja lähettäminen

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Valitse **Vapaatekstilasku**-sivulla aiemmin lisätty ja kirjattu lasku.
3. Valitse toimintoruudun **Asiakirjat**-ryhmässä **Lähetä** \> **Alkuperäinen**.
4. Sulje **Vapaatekstilasku**-sivu.

### <a name="analyze-a-generated-e-invoice"></a>Luodun e-laskun analysoiminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin työt**.
2. Valitse **Sähköisen raportoinnin työt** -sivulla viimeisin tietue, jonka tehtävän kuvaus on **Lähetä eInvoice XML**.
3. Siirry luotujen tiedostojen luetteloon valitsemalla **Näytä tiedostot**.
4. Lataa e-laskun luotu XML-tiedosto valitsemalla **Avaa**.
5. Analysoi e-laskun XML-tiedosto. Huomaa, että mukautuksen vuoksi asiakkaan veromalli sisältää mukautetun XML-määritteen **FederalTaxID** XML-määritteiden **schemeID** ja **schemeAgencyID** lisäksi. Tämän uuden XML-määritteen arvon määrittää laskutetulle asiakkaalle annettu liittovaltion verotunnus **LITWARE-6789**.

    ![Mukautusten perusteella luodun e-laskun XML-tiedoston esikatselu.](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>ER-vakiomääritysten viimeisimpien versioiden tuominen

Voit pitää Finance-esiintymän ER-vakiomäärityksen [ajan tasalla](general-electronic-reporting-manage-configuration-lifecycle.md) tuomalla niiden uudet versiot aina, kun ne ovat saatavana kyseiselle esiintymälle määritetyssä ER-[säilössä](general-electronic-reporting.md#Repository).

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet** -osassa **Microsoft**-ruutu ja valitse sitten **Säilöt** nähdäksesi luettelon Microsoft-toimittajan säilöistä.
3. Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **Yleinen** ja valitse sitten **Avaa**. Jos sinulta pyydetään valtuutusta Regulatory Configuration Service -palveluun yhdistämiseen, noudata valtuutusohjeita.
4. Valitse **Konfiguraatiosäilö**-sivun vasemman ruudun määrityspuussa **Peppol-myyntilasku** -muotoinen määritys.
5. Valitse **Versiot**-pikavälilehdessä sen valitun ER-muotomäärityksen versio **32.6.7**, joka on julkaistu tukemaan asiakkaan sähköisiä laskuja PEPPOL BIS 3 -muodossa. Lisätietoja on kohdassa [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Lataa valittu versio yleisestä säilöpalvelusta nykyiseen Finance-esiintymään valitsemalla **Tuo**.

![Määrityksen säilösivulla valittu versio 32.6.7.](./media/er-quick-start3-import-solution2.png)

Lisätietoja tämän prosessin automatisoinnista on kohdassa [ER-määritysten päivitettyjen versioiden tuominen](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>Tarkista tuodut ER-konfiguraatiot

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Laajenna **Määrityksen osat** -pikavälilehti.
4. Laajenna vasemman ruudun määrityspuussa **Laskumalli**. Huomaa, että **Myyntilaskumalli**-nimi on muuttunut muotoon **Laskumalli** yhdessä tuoduista ER-tietomallin määrityksistä.
5. Laajenna vasemman ruudun määrityspuussa **Laskumallin yhdistämismääritys**. Huomaa, että **Myyntilaskumallin yhdistämismääritys** -nimi on muuttunut muotoon **Laskumallin yhdistämismääritys** yhdessä tuoduista ER-mallin yhdistämismäärityksen määrityksistä.
6. Laajenna **UBL-myyntilasku** \> **Peppol-myyntilasku**.

Huomaa, että valitun **Peppol-myyntilasku** -ER-muodon lisäksi myös muiden tarvittavien ER-määritysten uusimmat versiot tuotiin. Koska ER-määritysten uusia versioita julkaistaan jatkuvasti yleiseen säilöön ja LCS:ään, jotta niitä vastaavat ER-ratkaisut pysyvät uusien vaatimusten mukaisina, pakollisen tietomallin määrityksen uusimmat versiot ja sen mallimääritykset tuotiin.

Varmista, että seuraavat ER-määritykset tuleva ajan mittaan käytettäviksi määrityspuussa.

- **Laskumalli** ER-tietomallien määritys:

    - Versio 206 (tai uudempi) sisältää tietomallin ER-osan version 24 (tai uudemman), joka ilmaisee laskutuksen liiketoiminnan toimialueen tietorakenteen. Tämä ER-määritys on tuotu **Laskumallin yhdistämismääritys** -ER-mallin yhdistämismäärityksen uusimman käytettävissä olevan määrityksen edeltäjänä.

    ![Versio 206 Määritykset-sivulla.](./media/er-quick-start3-imported-solution2b1.png)

- **Laskumallin yhdistämismääritys** ER-mallien yhdistämismäärityksen määritys:

    - Versio 206.132 (tai uudempi) on tuotu **Laskumalli**-ER-tietomallin määrityksen version 206 uusimpana toteutuksena. Siinä on useita mallin yhdistämismäärityksen ER-osia, joissa kuvataan sovelluksen tietojen täyttämistä suorituspalvelussa.

    ![Versio 206.132 Määritykset-sivulla.](./media/er-quick-start3-imported-solution2b2.png)

- **UBL-myyntilasku** ER-muodon määritys:

    - Versio 32.6 sisältää muodon ja muodon yhdistämismäärityksen ER-osat. Muoto-osa määrittää raportin asettelun. Muodon määritysosa sisältää mallin tietolähteen ja määrittää, miten raportin asettelu täytetään käyttämällä tätä tietolähdettä suorituspalvelussa. Tämä ER-muoto määritettiin luomaan e-laskuja UBL-muodossa. Se on tuotu tuotavaksi valitun **Peppol-myyntilasku** -ER-muodon ylätasona.

- **Peppol--myyntilasku** ER-muodon määritys:

    - Versio 32.6.7 sisältää ne muodon ja muodon yhdistämismäärityksen ER-osat, jotka määritettiin luomaan e-laskuja PEPPOL-muodossa.

    ![Versio 32.6.7 Määritykset-sivulla.](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Mukautetuissa ER-määrityksissä ER-vakiomääritysten uusiin versioihin tehtyjen muutosten ottaminen käyttöön

### <a name="adopt-your-custom-er-data-model"></a>Mukautetun ER-tieto mallin ottaminen käyttöön

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Laskumalli** ja valitse **Laskumalli (Litware)**.
3. Valitse **Versiot**-pikavälilehdessä valitun tietomallin määrityksen luonnosversion **50.2** kohdalla **Pohjusta**.
4. Vahvista **Kohdeversio**-kentässä ER-tietomallin perusmäärityksen versio **206** ja valitse sitten **OK**.

    Mukautetun ER-tietomallin määrityksen luonnosversion **50.2** uusi numero on **206.2**, mikä ilmaisee, että se sisältää nyt mukautuksen, johon yhdistettiin kaikki ER-tietomallin perusmäärityksen uusimman version (206) muutokset.

    > [!NOTE]
    > Uudelleenpohjustustoimintoa ei voi perua. Voit peruuttaa tämän pohjustuksen valitsemalla **Laskumalli (Litware)** mallin version **50.1** **Versiot**-pikavälilehdessä ja valitsemalla sitten **Nouda tämä versio**. Version 206.2 numeroksi palautetaan sitten **50.2**, ja luonnosversion 50.2 sisältö vastaa version 50.1 sisältöä.

5. Valitse **Versiot**-pikavälilehdessä **Muuta tila** \> **Valmis** ja valitse sitten **OK**.

Version 206.2 tila muuttuu tilasta **Luonnos** tilaksi **Valmis** ja versio muuttuu vain luku -tilaan. Uusi muokattava versio 206.3 on lisätty, ja sen tila on **Luonnos**. Tällä versiolla voi tehdä muita muutoksia mukautetun ER-tietomallin määritykseen.

![Valmis versio 206.2 Määritykset-sivulla.](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Mukautetun ER-mallin yhdistämismäärityksen ottaminen käyttöön

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Laskumalli** \> **Laskumallin yhdistämismääritys** ja valitse **Laskumallin yhdistämismääritys (Litware)**.
3. Valitse **Versiot**-pikavälilehdessä valitun mallin yhdistämismäärityksen määrityksen luonnosversion **50.19.2** kohdalla **Pohjusta**.
4. Vahvista **Kohdeversio**-kentässä ER-mallin yhdistämismäärityksen perusmäärityksen versio **206.132** ja valitse sitten **OK**.

    Mukautetun ER-mallin yhdistämismäärityksen määrityksen luonnosversion **50.19.2** uusi numero on **206.132.2**, mikä ilmaisee, että se sisältää nyt mukautuksen, johon yhdistettiin kaikki ER-mallin yhdistämismäärityksen perusmäärityksen uusimman version (206.132) muutokset.

    Huomaa, että joitakin pohjustusristiriitoja löytyi. Nämä ristiriidat on ratkaistava nyt manuaalisesti.

    ![Pohjustusristiriitailmoitus Määritykset-sivulla.](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Valitse toimintoruudussa ensin **Suunnitteluohjelma** ja sitten yhdistämismääritysluettelossa **Myyntilasku**.
6. Valitse kussakin pohjustusristiriidassa **Säilytä oma arvo**, koska mukautetun tietomallin versionumero on säilytettävä jokaisessa mainitussa osassa.

    ![Pohjustusristiriitoja Mallin yhdistämismäärityksen suunnitteluohjelman sivulla.](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Valitse **Tallenna** ja sulje sitten **Mallin yhdistämismäärityksen suunnitteluohjelma** -sivu.
8. Valitse yhdistämismääritysluettelossa **Projektilasku**.
9. Valitse kussakin pohjustusristiriidassa **Säilytä oma arvo**, koska mukautetun tietomallin versionumero on säilytettävä jokaisessa mainitussa osassa.
10. Valitse **Tallenna** ja sulje sitten **Mallin yhdistämismääritykset** -sivu.

    > [!NOTE]
    > Uudelleenpohjustustoimintoa ei voi perua. Voit peruuttaa tämän pohjustuksen valitsemalla **Laskumallin yhdistämismääritys (Litware)** mallin yhdistämismäärityksen version **50.19.1** **Versiot**-pikavälilehdessä ja valitsemalla sitten **Nouda tämä versio**. Version 206.132.2 numeroksi palautetaan sitten **50.19.2**, ja luonnosversion 50.19.2 sisältö vastaa version 50.19.1 sisältöä.

11. Valitse **Versiot**-pikavälilehdessä **Muuta tila** \> **Valmis** ja valitse sitten **OK**.

Version 206.132.2 tila muuttuu tilasta **Luonnos** tilaksi **Valmis** ja versio muuttuu vain luku -tilaan. Uusi muokattava versio 206.132.3 on lisätty, ja sen tila on **Luonnos**. Tällä versiolla voi tehdä muita muutoksia mukautetun ER-mallin yhdistämismäärityksen määritykseen.

![Valmis versio 206.132.2 Määritykset-sivulla.](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Mukautetun ER-muodon ottaminen käyttöön

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Määritykset**-sivun määrityspuun vasemmassa ruudussa **Laskumalli** \> **UBL-myyntilasku** \> **Peppol-myyntilasku** ja valitse **Peppol-myyntilasku (Litware)**.
3. Valitse **Versiot**-pikavälilehdessä valitun muodon määrityksen luonnosversion **11.2.2.2** kohdalla **Pohjusta**.
4. Vahvista **Kohdeversio**-kentässä ER-muodon perusmäärityksen versio **32.6.7** ja valitse sitten **OK**.

    Mukautetun ER-muodon määrityksen luonnosversion **11.2.2.2** uusi numero on **32.6.7.2**, mikä ilmaisee, että se sisältää nyt mukautuksen, johon yhdistettiin kaikki ER-muodon perusmäärityksen uusimman version (32.6.7) muutokset.

    Huomaa, että joitakin pohjustusristiriitoja löytyi. Nämä ristiriidat on ratkaistava nyt manuaalisesti.

5. Valitse toimintoruudussa **Suunnittelija**.
6. Valitse kussakin pohjustusristiriidassa **Säilytä oma arvo**, koska mukautetun tietomallin versionumero on säilytettävä jokaisessa mainitussa osassa.
7. Valitse **Tallenna**.
8. Valitse **Yhdistämismääritys**-välilehden **Malli**-tyypin **Lasku**-tietolähde ja valitse sitten **Muokkaa**.
9. Valitse **Versio**-kentässä mukautetun tietomallin version **2** ja valitse sitten **OK**.
10. Valitse **Tallenna**.

    > [!NOTE]
    > Uudelleenpohjustustoimintoa ei voi perua. Voit peruuttaa tämän pohjustuksen valitsemalla **Peppol-laskumalli (Litware)** -muodon version **11.2.2.1** **Versiot**-pikavälilehdessä ja valitsemalla sitten **Nouda tämä versio**. Version 32.6.7.2 numeroksi palautetaan sitten **11.2.2.2**, ja luonnosversion 11.2.2.2 sisältö vastaa version 11.2.2.1 sisältöä.

11. Sulje **Muodon suunnittelija** -sivu.
12. Valitse **Versiot**-pikavälilehdessä **Muuta tila** \> **Valmis** ja valitse sitten **OK**.

Version 32.6.7.2 tila muuttuu tilasta **Luonnos** tilaksi **Valmis** ja versio muuttuu vain luku -tilaan. Uusi muokattava versio 32.6.7.3 on lisätty, ja sen tila on **Luonnos**. Tällä versiolla voi tehdä lisämuutoksia mukautetun ER-muodon määritykseen.

![Valmis versio 32.6.7.2 Määritykset-sivulla.](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Myyntilaskun käsitteleminen mukautettujen ER-määritysten uusien versioiden avulla

### <a name="select-and-send-a-posted-invoice"></a>Kirjatun laskun valitseminen ja lähettäminen

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Valitse **Vapaatekstilasku**-sivulla aiemmin lisätty ja kirjattu lasku.
3. Valitse toimintoruudun **Asiakirjat**-ryhmässä **Lähetä** \> **Alkuperäinen**.

    > [!NOTE] 
    > Koska **Peppol-myyntilasku (Litware)** -ER-muodon määrityksistä on nyt kaksi versiota eikä kummallakaan versiolla ole voimaantulopäivän arvoa, e-lasku luodaan uusimmalla versiolla.

4. Sulje **Vapaatekstilasku**-sivu.

### <a name="analyze-a-generated-e-invoice"></a>Luodun e-laskun analysoiminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin työt**.
2. Valitse **Sähköisen raportoinnin työt** -sivulla viimeisin tietue, jonka tehtävän kuvaus on **Lähetä eInvoice XML**.
3. Siirry luotujen tiedostojen luetteloon valitsemalla **Näytä tiedostot**.
4. Lataa e-laskun luotu XML-tiedosto valitsemalla **Avaa**.
5. Analysoi e-laskun XML-tiedosto. Huomaa, että mukautuksen vuoksi asiakkaan veromalli sisältää edelleen mukautetun XML-määritteen **FederalTaxID** XML-määritteiden **schemeID** ja **schemeAgencyID** lisäksi. Ja koska **UBL-myyntilasku**-perusmuodon uusi versio yhdistettiin mukautukseen, XML-elementin **cbc:CustomizationID** teksti `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` on muuttunut tekstiksi `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.

    ![Mukautusten perusteella luodun e-laskun XML-tiedoston esikatselu.](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [ER-konfiguraatioiden lataaminen Lifecycle Services -palvelusta](download-electronic-reporting-configuration-lcs.md)
- [Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta](er-download-configurations-global-repo.md)
- [Luo tekstimuotoinen lasku](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [Mukautettujen kenttien luominen ja käsitteleminen](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
