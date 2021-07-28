---
title: Piilota Word-sisällön ohjausobjektit luoduissa raporteissa
description: Tässä aiheessa kerrotaan, miten määritetään sähköisen raportoinnin (ER) muoto, jotta raportit voidaan luoda Microsoft Word -tiedostoina, joissa sisällön ohjausobjektit on piilotettu.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: e6ab75c970c6c14d4977b6c739ba46e33f4962e9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348041"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Piilota Word-sisällön ohjausobjektit luoduissa raporteissa

[!include [banner](../includes/banner.md)]

Jos haluat luoda raportteja Microsoft Word -asiakirjoina, suunnittele raporttien malli Word-tiedostona. Tämän mallin on sisällettävä Word-sisällön ohjausobjektit suorituksen aikana täytettävinä tietojen paikkamerkkeinä. Luotua Word-asiakirjaa voi käyttää mallina [määrittämällä](er-design-configuration-word.md) uuden [sähköisen raportoinnin (ER)](general-electronic-reporting.md) [ratkaisun](er-quick-start1-new-solution.md). Ratkaisussa on oltava ER-[määritys](general-electronic-reporting.md#Configuration), joka sisältää ER-[muodon](general-electronic-reporting.md#FormatComponentOutbound) osan. Tämä ER-muoto on määritettävä käyttämään suunniteltua mallia raportin luontiin.

Dynamics 365 Financen versiossa 10.0.6 ja sitä myöhemmissä versioissa ER-muotoisia kaavoja voi konfiguroida piilottamaan luotujen tiedostojen Word-sisällön ohjausobjektit.

Seuraavissa vaiheissa selitetään, miten järjestelmänvalvojan tai sähköisen raportoinnin toiminnallisen konsultin rooliin määritetty käyttäjä voi konfiguroida ER-muodon, joka luo raportit Word-tiedostoina ja piilottaa joitakin Word-mallin avulla konfiguroitujen luotujen raporttien sisällön ohjausobjekteja.

Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.

## <a name="prerequisites"></a>Edellytykset

Näiden vaiheiden edellytyksenä on seuraavien tehtäväoppaiden vaiheiden suorittaminen:

- [Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa](./tasks/er-design-reports-openxml-2016-11.md)
- [Raporttien luominen Word-muodossa käyttämällä ER-konfiguraatioita uudelleen Excel-mallien avulla](./tasks/er-design-configuration-word-2016-11.md)

Kun suoritat näiden tehtäväoppaiden vaiheet, seuraavat kohteet valmistellaan:

- **Laskentataulukon malliraportti** -ER-muoto, joka on määritetty luomaan asiakirja Word-muodossa
- **Mallilaskentataulukon** ER-muodon [luonnosversio](general-electronic-reporting.md#component-versioning), joka on merkitty **Runnable**
- **Sähköiset** maksutavat, jotka on määritetty käyttämään toimittajan maksujen käsittelyssä **laskentataulukon esimerkkiraportin** ER-muotoa

Lisäksi malliraporttia varten on ladattava ja tallennettava seuraava malli:

- [Maksuraportin sidottu malli 2 (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Ladatun Word-mallin tarkasteleminen

1. Avaa Wordin työpöytäsovelluksessa aiemmin ladattu **SampleVendPaymDocReportBounded2.docx**-mallitiedosto.
2. Varmista, että mallitiedosto sisältää yhteenveto-osan, jossa näkyvät käsiteltyjen maksujen maksujen kokonaissummat jokaisen käsiteltyjen maksujen valuuttakoodin osalta.

    - Yhteenveto-osa sijaitsee erillisessä Word-asiakirjan taulussa.
    - Tämän taulun ensimmäisellä rivillä on taulukon sarakkeiden otsikot osan otsikkona.
    - Tämän taulun toisella rivillä on toistuvan sisällön ohjausobjekti osan tietoina.
    - Tämä sisällön ohjausobjekti on yhdistetty mukautetun **Report**-XML-osan **SummaryLines**-kenttään.
    - Tämän määrityksen perusteella sisällön ohjausobjekti liittyy muokattavan ER-muodon **SummaryLines**-elementtiin.

    > [!NOTE]
    > Toistuvan sisällön ohjausobjekti on koodattu **SummaryLines**-avaimella, joka vastaa sen mukautetun XML-osan kenttää, johon se on yhdistetty.

    ![Word-mallin asettelu.](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Aiemmin luodun ER-raporttimäärityksen valitseminen

Seuraavissa vaiheissa käytät uudelleen aiemmin – kun suoritit aiemmin mainittujen tehtäväoppaiden vaiheet – määritettyä ER-konfiguraatiota.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Raportointikonfiguraatiot**.
3. Laajenna **Konfiguraatiot**-sivun määrityspuussa **Maksumalli** ja valitse sitten **Laskentataulukkoraportin esimerkki**.
4. Valitse **Suunnitteluohjelma**, jos haluat muokata valitun ER-muodon luonnosversiota.

## <a name="replace-the-current-template-with-the-new-template"></a>Nykyisen malliin korvaaminen uudella mallilla

Tällä hetkellä Word-muotoisen raportin luonnissa käytetään mallina SampleVendPaymDocReportBounded.docx-tiedostoa. Seuraavissa vaiheissa tämä Word-malli korvataan aiemmin ladatulla uudella Word-mallilla SampleVendPaymDocReportBounded2.docx.

1. Vallitse **Muodon suunnittelu** -sivulla **Liitteet**.
2. Poista aiemmin luotu malli valitsemalla **Liitteet**-sivulla **Poista**.
3. Vahvista poisto valitsemalla **Kyllä**.
4. Valitse **Uusi** \> **Tiedosto**.
5. Valitse **Selaa**, siirry aiemmin ladattuun **SampleVendPaymDocReportBounded2.docx**-tiedostoon ja valitse se.
6. Valitse **OK**.
7. Sulje **Liitteet**-sivu.
8. Kirjoita tai valitse **Muodon suunnittelu** -sivun **Malli**-kentässä **SampleVendPaymDocReportBounded2.docx**-tiedosto.

## <a name="run-the-format-to-create-word-output"></a>Word-asiakirjan luovan muodon suorittaminen

1. Valitse **Ostoreskontra** \> **Maksut** \> **Maksukirjauskansio**.
2. Valitse kaikki maksut **Toimittajamaksut**-sivun **Luettelo**-välilehdestä.
3. Valitse **Maksun tila** \> **Ei mitään**.
4. Valitse **Muodosta maksut**.
5. Valitse **Maksutapa**-kentässä **Sähköinen**.
6. Valitse **Pankkitili**-kentässä **GBSI OPER**.
7. Valitse **OK**.
8. Valitse **Sähköisen raportin parametrit** -valintaikkunassa **OK** ja analysoi luotu tuloste.

    ![Toimittajan maksut -sivulla käsiteltävät maksut.](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Tuloste esitetään Word-muodossa, ja se sisältää yhteenveto-osan.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Konfiguroi muokattavissa oleva muoto piilottamaabn yhteenveto-osa

Jos haluat piilottaa yhteenveto-osan luodussa tiedostossa tämän ER-muodon suorittaneen käyttäjän pyynnön perusteella, muokkaa muokattavaa ER-muotoa.

1. Siirry kohtaan **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi** ja avaa ER-muodon luonnosversio muokkausta varten.
2. Valitse **Raportointikonfiguraatiot**. 
3. Laajenna **Konfiguraatiot**-sivun määrityspuussa **Maksumalli** \> **Laskentataulukkoraportin esimerkki**.
4. Valitse **Suunnittelu**.
5. Laajenna **Muodon suunnittelu** -sivulla **Word** ja valitse **SummaryLines**.
6. Lisää **Määritys**-välilehdessä uusi tietolähde, joka kysyy käyttäjältä ajon aikana, tuleeko yhteenveto-osa piilottaa:

    1. Valitse **Lisää pääkansio**.
    2. Valitse **Lisää tietolähde** -valintaikkunassa **Yleinen\Käyttäjän syöteparametri** avataksesi **Käyttäjän syöttöparametri -tietolähteen ominaisuudet** -valintaikkunan.
    3. Kirjoita **Nimi**-kenttään **uipSuppress**.
    4. Kirjoita **Otsikko**-kenttään **Piilota yhteenveto-osa**.
    5. Valitse tai kirjoita **Toiminnon tietotyypin nimi** -kentässä **NoYes**.
    6. Valitse **OK**.

7. Lisää uusi **NoYes**-sovelluksen valintalistatyyppinen tietolähde:

    1. Valitse **Lisää pääkansio**.
    2. Valitse **Lisää tietolähde** -valintaikkunassa **Dynamics 365 for Operations\Valintalista**, niin näyttöön tulee **Valintalista-tietolähteen ominaisuudet** -valintaikkuna.
    3. Kirjoita **Nimi**-kenttään **enumNoYes**.
    4. Kirjoita **Otsikko**-kenttään **Piilota asetukset**.
    5. Valitse tai kirjoita **Toiminnon tietotyypin nimi** -kentässä **NoYes**.
    6. Valitse **OK**.

8. Määritä valitulle **SummaryLines**-muotoelementille kaava, joka määrittää, milloin valittuun muotoelementtiin liittyvän Word-sisällön ohjausobjekti tulee piilottaa:

    1. Valitse **Määritys**-välilehden **Poistettu**-osassa **Muokkaa** avataksesi **[Muodon suunnittelu](general-electronic-reporting-formula-designer.md)** -sivun.
    2. Kirjoita **Kaava**-kenttään kaava `uipSuppress = enumNoYes.Yes`.
    3. Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.

        > [!NOTE]
        > Tätä kaavaa käytetään luodussa tiedostossa kaikkien **muiden muotoelementtien suorittamisen jälkeen**. Voit käyttää tätä kaavaa, kun Word-sisällön ohjausobjekti, joka on merkitty muotoelementinä, jota varten kaava on määritetty (tässä tapauksessa **SummaryLines**), löytyy luodussa tiedostossa. Tämä sisältöohjausobjekti poistetaan sitten kokonaan yhdessä sen Word-taulukon rivin kanssa, joka sisältää sen. Yhteenveto-osan erittelyrivi poistetaan luodusta asiakirjasta.
        >
        > Suunnittelun aikana voit konfiguroida **Poistettu**-kaavan muotoelementille, vaikka käytössä olevassa Word-mallin yhdessäkään sisällön ohjausobjektissa ei ole tunnistetta, joka vastaa sellaisen muotoelementin nimeä, jolle **Poistettu**-ominaisuus on määritetty. Kun tarkistat muodon suunnittelun aikana, saat [varoituksen](er-components-inspections.md#i14) tästä ristiriidasta.
        >
        > Suoritusaika tuotetaan poikkeus, jos käytössä olevan Word-mallin missään sisältöohjausobjektissa ei ole tunnistetta, joka vastaisi sellaisen muotoelementin nimeä, jolle **Poistettu**-ominaisuus on määritetty.

    4. Määritä **Määritys**-välilehden **Poistettu**-osassa **Ylätason kanssa** -asetukseksi **Kyllä**.

        > [!NOTE]
        > Tämä asetus on määritettävä **Kyllä**-arvoksi, jos haluat poistaa koko Word-taulun sen rivin ylätason objektina, joka sisältää yhteenveto-osan tiedot. Jos määrität tämän asetuksen arvoksi **Ei**, osan otsikkorivi jää luotuun tiedostoon.

9. Tallenna muokattavan muodon muutokset valitsemalla **Tallenna**.

    ![Word-muotoinen luotu tuloste.](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Word-asiakirjan luovan muokatun muodon suorittaminen

1. Valitse **Ostoreskontra** \> **Maksut** \> **Maksukirjauskansio**.
2. Valitse luomasi maksukirjauskansio ja valitse sitten **Rivit**.
3. Valitse **Toimittajamaksut**-sivulla kaikki rivit ja valitse sitten **Maksun tila** \> **Ei mitään**.
4. Valitse **Muodosta maksut**.
5. Valitse **Maksutapa**-kentässä **Sähköinen**.
6. Valitse **Pankkitili**-kentässä **GBSI OPER**.
7. Valitse **OK**.
8. Valitse **Sähköisen raportoinnin parametrit** -valintaikkunan **Piilota yhteeneveto-osa** -kentässä **Kyllä**.
9. Valitse **OK** ja analysoi luotu tuloste.

    ![Word-muotoinen luotu tuloste.](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Huomaa, että tuloste ei sisällä yhteenveto-osaa, koska se on piilotettu.

## <a name="additional-resources"></a>Lisäresurssit

- [Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa](./tasks/er-design-reports-openxml-2016-11.md)
- [Uuden ER-konfiguraation suunnitteleminen raporttien luomiseksi Word-muodossa](er-design-configuration-word.md)
- [Raporttien luominen Word-muodossa käyttämällä ER-konfiguraatioita uudelleen Excel-mallien avulla](./tasks/er-design-configuration-word-2016-11.md)
- [Tarkista määritetty ER-komponentti estääksesi suorituksen aikaiset ongelmat](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]