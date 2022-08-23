---
title: Yhtä mallin juurta koskevien useiden johdettujen yhdistämismääritysten hallinta
description: Tässä artikkelissa käsitellään yhdelle mallin juurelle määritettyjen useiden johdettujen yhdistämismääritysten hallintaa.
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, ERModelMappingTable
ms.openlocfilehash: 868d47ccfebb9a9753d93344c72b10ae4353b0e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277505"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Yhtä mallin juurta koskevien useiden johdettujen yhdistämismääritysten hallinta

[!include [banner](../includes/banner.md)]

[Sähköisen raportoinnin (ER)](general-electronic-reporting.md) tietomalli on osa, jota käytetään jokaisessa määritetyssä ER-muodon osassa tietolähteenä lähteviä asiakirjoja luotaessa. Yksittäisen liiketoiminta-alueen kuvaamista varten määritetään useita juurimääritelmiä sisältävä tietomalliosa. 

Kussakin juurimääritelmässä kyseisen toimialueen tiedot voidaan ilmaista tiettyihin raportointitarkoituksiin parhaiten soveltuvalla tavalla. Jokaiselle juurimääritelmälle voidaan määrittää ER-mallin yhdistämismäärityksen osa tietomallin Microsoft Dynamics 365 Financea koskevana toteutuksena. Tällä tavoin voidaan kuvata, miten tietomalli täytetään suorituksen aikana.

ER-mallin yhdistämismääritysosat voivat sijaita ER-tietomallin [määrityksissä](general-electronic-reporting.md#Configuration) ja ER-mallin yhdistämismäärityksissä. Yhdessä ER-määrityksessä voi olla useita yhdistämismääritysosia, joista kukin on määritetty tiettyä juurimääritelmää varten. Vaihtoehtoisesti yhdessä ER-määrityksessä voi olla vain yksi yhdistämismääritysosa, joka on määritetty yhtä juurimääritelmää varten.

Monilla määrityspalveluilla voi olla saman ER-tietomallin ER-mallin yhdistämismäärityksiä. Kyseisissä mallin yhdistämismäärityksissä voi olla eri juurimääritelmien yhdistämismääritysosia. Yhden [palvelun](general-electronic-reporting.md#Provider) tarjoamaa mallin yhdistämismääritystä on mahdollista käyttää yhdessä juurimääritelmässä ja toisen palvelun tarjoamaa mallin yhdistämismääritelmää toisessa juurimääritelmässä.

Tässä artikkelissa käsitellään menettelyjä, joilla hallitaan ER-tietomallin useita ER-mallin yhdistämismäärityksiä, kun niissä on erilaisia samalle juurimääritelmälle määritettyjä mallin yhdistämismääritysosia. 

Tässä artikkelissa käsiteltyjen menetelmien suorittaminen edellyttää, että käyttäjälle on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.

Kaikkia seuraavia menetelmiä voidaan käyttää USMF-yrityksessä. Koodausta ei tarvita.

## <a name="configure-the-er-framework"></a>Määritä ER-kehys

Jos käyttäjällä on sähköisen raportoinnin kehittäjän rooli, liiketoiminta-asiakirjojen luominen ER-kehystä käyttämällä edellyttää sähköisen raportoinnin [parametrien vähimmäisjoukon](er-quick-start2-customize-report.md#ConfigureFramework) määrittämistä.

## <a name="import-the-standard-er-format-configurations"></a>Tuo ER-muodon vakiokonfiguraatiot

ER-vakiomääritys voidaan lisätä Financen nykyiseen esiintymään tuomalla ne kyseiselle esiintymällä määritetystä ER-säilöstä. Tuo seuraavat ER-muotomääritykset noudattamalla kohdassa [ER-määritysten lataaminen määrityspalvelun yleisestä säilöstä](er-download-configurations-global-repo.md) olevia ohjeita:

- **Vapaatekstilasku (Excel)**, versio 220.106
- **Projektilasku (Excel)**, versio 226.27

## <a name="review-the-imported-er-configurations"></a>Tarkista tuodut ER-konfiguraatiot

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Laajenna **Konfiguraatiot**-sivun määrityspuun vasemmassa ruudussa **Laskumalli**.

    ![Konfiguraatiot-sivun tuotujen määritysten tarkastelu.](./media/er-multiple-model-mappings-image1.png)

4. **Vapaatekstilasku (Excel)** -muodon tarkastelu:

    1. Valitse vasemman ruudun määrityspuussa **Vapaatekstilasku (Excel)**.
    2. Valitse toimintoruudussa **Suunnittelija**.
    3. Valitse **Muodon suunnittelija** -sivun **Yhdistämismääritys**-välilehden tietolähdeluettelossa **Malli**.
    4. Valitse **Näytä**.
    
       Nykyinen ER-muoto on määritetty käyttämään **laskumallin** **InvoiceCustomer**-juurimääritelmää. Kun tämä muoto suoritetaan, **Malli**-tietolähde kutsutaan, **InvoiceCustomer**-juurimääritelmälle määritetyn mallin yhdistämismäärityksen avulla käytetään sovelluksen tietoja ja täytetään tietomalli.

        ![Mallin tietolähteen tarkastelu Muodon suunnittelija -sivulla.](./media/er-multiple-model-mappings-image2.png)

    6. Sulje **Muodon suunnittelija** -sivu.

5. **Laskumallin yhdistämismääritys** -määrityksen sisällön tarkasteleminen:

    1. Valitse vasemman ruudun määrityspuussa **Laskumallin yhdistämismääritys**.
    2. Valitse toimintoruudussa **Suunnittelija**.
    3. Huomaa **Yhdistäminen mallista tietolähteeseen** -sivulla, että nykyisessä ER-mallin yhdistämismäärityksessä on useita mallin yhdistämismääritysosia:

        + **Myyntilasku**-mallin yhdistämismääritys on määritetty **laskumallin** **InvoiceCustomer**-juurimääritelmälle. Niinpä **Vapaatekstilasku (Excel)** -ER-muotoa suoritettaessa tämän ER-määrityksen **Myyntilasku**-mallin yhdistämismääritys voidaan valita käyttämään sovelluksen tietoja ja täyttämään tietomalli.
        + **Projektilasku**-mallin yhdistämismääritys on määritetty **laskumallin** **InvoiceProject**-juurimääritelmälle. Niinpä **Projektilasku (Excel)** -ER-muotoa suoritettaessa tämän ER-määrityksen **Projektilasku**-mallin yhdistämismääritys voidaan valita käyttämään sovelluksen tietoja ja täyttämään tietomalli.

        ![Laskumallin yhdistämismääritys Yhdistäminen mallista tietolähteeseen -sivulla.](./media/er-multiple-model-mappings-image3.png)

    4. Sulje **Malli tietolähteen yhdistämismääritystä varten** -sivu.
    5. Valitsemalla **Versiot**-pikavälilehdessä **Poista** voidaan poistaa kaikki tämän ER-määrityksen versiot, jotka ovat uudempia kuin versio 240.175.

6. **Projektilaskumallin yhdistämismääritys (RDP)** -määrityksen sisällön tarkasteleminen:

    1. Valitse vasemman ruudun määrityspuussa **Projektilaskumallin yhdistämismääritys (RDP)**.
    2. Valitse toimintoruudussa **Suunnittelija**.
    3. Huomaa **Yhdistäminen mallista tietolähteeseen** -sivulla, että nykyinen ER-mallin yhdistämismääritys sisältää **InvoiceProject**-mallin yhdistämismäärityksen ja että tämä mallin yhdistämismääritys on määritetty **laskumallin** **InvoiceProject**-juurimääritelmälle. Valitse tämän vuoksi **Projektilasku (Excel)** -ER-muotoa suoritettaessa tämän ER-määrityksen **InvoiceProject**-mallin yhdistämismääritys sovelluksen tietojen käyttämistä ja tietomallin täyttämistä varten.

        ![Projektilaskumallin yhdistämismääritys Yhdistäminen mallista tietolähteeseen -sivulla.](./media/er-multiple-model-mappings-image4.png)

    4. Sulje **Malli tietolähteen yhdistämismääritystä varten** -sivu.
    5. Valitsemalla **Versiot**-pikavälilehdessä **Poista** voidaan poistaa kaikki tämän ER-määrityksen versiot, jotka ovat uudempia kuin versio 226.35.

## <a name="customize-the-imported-er-configurations"></a>Tuotujen ER-määritysten määrittäminen

Tässä osassa käsitellään Microsoftin toimittamien mallin yhdistämismääritysten [mukauttamista](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration). Mukauttaminen voi olla välttämätöntä esimerkiksi mukautetun logiikan toteuttamista tai puuttuvien sidontojen lisäämistä varten.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Laskumallin yhdistämismäärityksen mukauttaminen

1. Valitse **Konfiguraatiot**-sivun vasemman ruudun määrityspuussa **Laskumallin yhdistämismääritys**.
2. Valitse toimintoruudussa **Luo konfigurointi**.
3. Valitse avattavan **Luo määritys** -valintaikkunan **Uusi**-kentässä **Johdettu nimestä: Laskumallin yhdistämismääritys, Microsoft**.
4. Kirjoita **Nimi**-kenttään **Laskumallin yhdistämismääritys Litware**.
5. Valitse **Luo konfiguraatio**.
6. [Merkitse](er-quick-start2-customize-report.md#MarkFormatRunnable) johdetun yhdistämismäärityksen [luonnos](general-electronic-reporting.md) käytettäväksi suorituksen aikana:

    1. Valitse toimintoruudussa **Konfiguroinnit**-välilehden **Lisäasetukset**-ryhmässä **Käyttäjän parametrit**.
    2. **Käyttäjän parametrit** -valintaikkunassa määritä **Suorita asetukset** -valinnaksi **Kyllä**, ja valitse sitten **OK**.
    3. Tee tarvittaessa sivusta muokattava valitsemalla **Muokkaa**.
    4. Määritä **Suorita luonnos** -asetukseksi **Kyllä** siinä **Laskumallin yhdistämismääritys Litware** -määrityksessä, joka on valittuna määrityspuussa.

7. Tarkista tämän määrityksen mallin yhdistämismääritykset valitsemalla toimintoruudussa **Suunnitteluohjelma**.

    ![Laskumallin yhdistämismääritysten tarkasteleminen Yhdistäminen mallista tietolähteeseen -sivulla.](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Mukautetun logiikan voi nyt määrittää avaamalla jokin tämän ER-määrityksen ER-mallin yhdistämismäärityksen osa suunnittelutoiminnossa. Lisätietoja on kohdassa [Mallin yhdistämismäärityksen mukauttaminen](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. Sulje **Malli tietolähteen yhdistämismääritystä varten** -sivu.

**Laskumallin yhdistämismääritys**- ja **Laskumallin yhdistämismääritys Litware** -määritykset on nyt tehty, ja kummassakin niissä on **InvoiceCustomer**-juurimääritelmää varten määritetty mallin yhdistämismääritys. Yksi mallin yhdistämismääritys on nimenomaisesti määritettävä mallin oletusyhdistämismääritykseksi, jota mikä tahansa ER-muoto käyttää, kuten **Vapaatekstilasku (Excel)** -muoto, jossa on **InvoiceCustomer**-juurimääritelmän sisältävä mallin tietolähde. Muussa tapauksessa ER-muotoa suoritettaessa, muokattaessa tai tarkistettaessa annetaan seuraava poikkeus, joka ilmoittaa, että mallin oletusyhdistämismääritystä ei ole nimenomaisesti määritetty:
 
> Tietomallilla \<model name\> (\<root descriptor\>) on useita mallien yhdistämismäärityksiä määrityksissä \<configuration names separated by commas\>. Määritä jokin määrityksistä oletukseksi.

![Muodon avaaminen muokattavaksi Konfiguraatiot-sivulla.](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Projektilaskumallin yhdistämismäärityksen (RDP) mukauttaminen

1. Valitse **Konfiguraatiot**-sivun vasemman ruudun määrityspuussa **Projektilaskumallin yhdistämismääritys (RDP)**.
2. Valitse toimintoruudussa **Luo konfigurointi**.
3. Valitse avattavan **Luo määritys** -valintaikkunan **Uusi**-kentässä **Johdettu nimestä: Projektilaskumallin yhdistämismääritys (RDP), Microsoft**.
4. Kirjoita **Nimi**-kenttään **Projektilaskumallin yhdistämismääritys Litware**.
5. Valitse **Luo konfiguraatio**.
6. Määritä **Suorita luonnos** -asetukseksi **Kyllä** siinä **Projektilaskumallin yhdistämismääritys Litware** -määrityksessä, joka on valittuna määrityspuussa.
7. Tarkista tämän määrityksen mallin yhdistämismääritykset valitsemalla toimintoruudussa **Suunnitteluohjelma**.

    ![Mukautetun projektilaskumallin yhdistämismääritysten tarkasteleminen Yhdistäminen mallista tietolähteeseen -sivulla.](./media/er-multiple-model-mappings-image7.png)

8. Sulje **Malli tietolähteen yhdistämismääritystä varten** -sivu.

**Laskumallin yhdistämismääritys**-, **Projektilaskumallin yhdistämismääritys (RDP)**- ja **Projektilaskumallin yhdistämismääritys Litware** -määritykset on nyt tehty. Jokaisessa näissä määrityksessä on **InvoiceProject**-juurimääritelmää varten määritetty mallin yhdistämismääritys. Yksi mallin yhdistämismääritys on nimenomaisesti määritettävä mallin oletusyhdistämismääritykseksi, jota mikä tahansa ER-muoto käyttää. Tätä varten voi käyttää esimerkiksi **Projektilasku (Excel)** -muotoa, jossa on **InvoiceCustomer**-juurimääritelmän sisältävä mallin tietolähde. Muussa tapauksessa ER-muotoa suoritettaessa tai muokattaessa annetaan poikkeus, joka ilmoittaa, että mallin oletusyhdistämismääritystä ei ole nimenomaisesti määritetty.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Johdetun Laskumallin yhdistämismääritys Litware -määrityksen valitseminen mallin oletusyhdistämismääritykset sisältäväksi määritykseksi

1. Valitse **Konfiguraatiot**-sivun vasemman ruudun määrityspuussa **Laskumallin yhdistämismääritys Litware**.
2. Määritä **Mallin yhdistämisasetuksen** oletusarvoksi **Kyllä**.

    ![Mallin yhdistämismäärityksen määrittäminen mallin oletusyhdistämismääritykseksi Konfiguraatiot-sivulla.](./media/er-multiple-model-mappings-image8.png)

    Tämän asetuksen vuoksi käytetään **Myyntilaskun kopio** -mallin yhdistämismääritystä, kun **Vapaatekstilasku (Excel)** suoritetaan tai kun sitä muokataan tai se tarkistetaan. **Laskumallin yhdistämismääritys** -määrityksen **Myyntilasku**-mallin yhdistämismääritys ohitetaan.

    **Vapaatekstilasku (Excel)** -muoto voidaan nyt avata tarkasteltavaksi muodon suunnittelijassa.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Johdetun Projektilaskumallin yhdistämismääritys Litware -määrityksen valitseminen mallin oletusyhdistämismääritykset sisältäväksi määritykseksi

1. Valitse **Konfiguraatiot**-sivun vasemman ruudun määrityspuussa **Projektilaskumallin yhdistämismääritys Litware**.
2. Määritä **Mallin yhdistämisasetuksen** oletusarvoksi **Kyllä**.

    Toisin kuin edellisessä osassa kuvatun **Laskumallin yhdistämismääritys** -määrityksen kohdalla, **Projektilaskumallin yhdistämismääritys Litware** -määrityksen **InvoiceProject kopio** -mallin yhdistämismäärityksen käyttöä ei voi aloittaa. Kaksi **InvoiceProject**-juurimääritelmän sisältävää mallin yhdistämismääritystä on tällä hetkellä merkitys oletusmääritykseksi. Niinpä niiden käytön prioriteetti on sama. Ongelman voi ratkaista suorittamalla tämän menettelyn jäljellä olevat vaiheet.

3. Valitse vasemman ruudun määrityspuussa **Laskumallin yhdistämismääritys Litware**.
4. Valitse toimintoruudussa **Suunnittelija**.
5. Muuta sivu tarpeen muokattavaksi valitsemalla **Yhdistäminen mallista tietolähteeseen** -sivulla **Muokkaa**.
6. Valitse ensin **Projektilaskun kopio** -mallin yhdistämismääritys ja sitten sen **On poistettu**-valintaruutu.

    ![Mallin yhdistämismäärityksen määrittäminen virtuaalisesti poistetuksi Yhdistäminen mallista tietolähteeseen -sivulla.](./media/er-multiple-model-mappings-image9.png)

    Tämän asetuksen vuoksi **Laskun mallin yhdistämismääritys Litware** -määritystä käsitellään aivan kuin sillä ei olisi **InvoiceProject**-juurimääritelmän mallin yhdistämismääritystä. **InvoiceProject kopio** -mallin yhdistämismääritys annettiin oletusarvoisesti. Tämä mallin yhdistämismäärityksen sisältävä **Projektilaskumallin yhdistämismääritys Litware** -määritys merkitään oletusmääritykseksi. Koska se on määritetty oletukseksi, sen prioriteetti on korkeampi kuin **Projektilaskumallin yhdistämismääritys (RDP)** -määrityksen **InvoiceProject**-mallin yhdistämismääritys.

## <a name="other-considerations"></a>Muuta huomioon otettavaa

**Projektilaskumallin yhdistämismääritys Litware** -määrityksen **InvoiceProject kopio** -mallin yhdistämismääritys on suunniteltu käyttämään **ReportDataProvider**-tietolähdettä. Tietolähde on osa *Objekti*-tyyppiä, joka viittaa **PsaProjInvoiceDP**-sovellusluokkaan. Tämä luokka toteutetaan projektilaskun tulostuksen hallintakehyksen SSRS (SQL Server Reporting Services) -raportin tietolähteenä. Tämä tietolähde valitaan ER-[integrointikohdaksi](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents). Tulostuksenhallintaraporttien nykyinen ER-toteutus ottaa tämän asetuksen huomioon. Lisätietoja saa tarkastelemalla **ERPrintMgmtDataProviderReport**-sovellusluokan lähdekoodia. **ReportDataProvider**-tietolähteen määrittäminen suorituksen aikana mallin integrointikohdaksi pakottaa Finance käsittelemään tämän yhdistämismääritysosan korkeammalla prioriteetilla kuin **Projektilaskumallin yhdistämismääritys (RDP)** -määrityksen **InvoiceProject**-yhdistämismääritysosan.

## <a name="see-also"></a>Lisätietoja

- [Sähköisen raportointimallin kartoituksen hallinta erillisissä sähköisen raportoinnin konfiguraatioissa](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [Maakontekstista riippuvaisten sähköisen raportoinnin mallimääritysten määrittäminen](er-country-dependent-model-mapping.md)
- [Sähköisen raportointikehyksen ohjelmointirajapinnan muutokset](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
