---
title: Raporttien luominen Word-muodossa käyttämällä sähköisen raportoinnin konfiguraatioita uudelleen Excel-mallien avulla
description: Tässä artikkelissa käsitellään sellaisten raporttimuotojen määrittämistä luomaan raportteja Word-asiakirjoina, jotka suunniteltiin luomaan raportteja Excel-työkirjoina.
author: kfend
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
ms.openlocfilehash: eea037751bc7ae4cb5e45fcaa0166d1f2f0b8292
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291171"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>Excel-malleja sisältävien ER-määritysten käyttäminen uudelleen Word-muotoisten raporttien luontiin

[!include [banner](../../includes/banner.md)]

Raporttien luonti Microsoft Word -asiakirjoina edellyttää uuden [sähköisen raportoinnin (ER)](../general-electronic-reporting.md) muodon [määrittämistä](../er-design-configuration-word.md). Vaihtoehtoisesti voidaan käyttää uudelleen ER-muotoa, joka suunniteltiin alun perin luomaan raportteja Excel-työkirjoina. Siinä tapauksessa Excel-malli on korvattava Word-mallilla.

Seuraavat menettelyt osoittavat, miten käyttäjät, jolla on joko järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi määrittää ER-muodon luomaan raportteja Word-tiedostoina käyttämällä uudelleen ER-muotoa, joka suunniteltiin luomaan raportteja Excel-tiedostoina.

Nämä menettelyt voidaan suorittaa GBSI-yrityksessä.

## <a name="prerequisites"></a>Edellytykset

Näiden menettelyjen suorittaminen edellyttää, että tehtäväoppaassa [OPENXML-muodossa luotavien raporttien määritysten suunnittelu](er-design-reports-openxml-2016-11.md) olevat vaiheet suoritetaan ensin.

Lisäksi malliraporttia varten on ladattava ja tallennettava paikallisesti seuraavat mallit:

- [Maksuraportin malli (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Maksuraportin sidottu malli (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

Nämä menettelyt koskevat toimintoa, joka lisättiin Dynamics 365 for Operationsin versiossa 1611 (marraskuu 2016).

## <a name="select-the-existing-er-report-configuration"></a>Aiemmin luodun ER-raporttimäärityksen valitseminen

1. Siirry Dynamics 365 Financessa kohtaan **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Varmista, että konfiguraation lähde **Litware Inc.** on valittu **aktiivisena**. Jos näin ei ole, noudata tehtäväoppaan [Määrityspalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md).
3. Valitse **Raportointikonfiguraatiot**. Käytössä on aiemmin luodut ER-määritykset, jotka suunniteltiin alun perin luomaan OPENXML-muotoisia raportteja.
4. Laajenna **Konfiguraatiot**-sivun määrityspuun vasemmassa ruudussa **Maksumalli** ja valitse sitten **Laskentataulukkoraportin esimerkki**.

    > [!NOTE]
    > Valitun ER-muodon luonnosversiota voi muokata **Versiot**-pikavälilehdessä.

5. Valitse **Suunnittelu**.
6. Huomaa, että **Muodon suunnittelija** -sivulla oleva juuren muotoelementin otsikko ilmaisee, että käytössä on Excel-malli.

![Aiemmin luodun määrityksen valitseminen.](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>Ladatun Word-mallin tarkasteleminen

1. Avaa Wordin työpöytäsovelluksessa aiemmin ladattu **SampleVendPaymDocReport.docx**-mallitiedosto.
2. Tarkista, että mallissa on vain sen asiakirjan asettelu, jonka haluat luoda ER-raporttina.

![Word-mallin asettelu työpöytäsovelluksessa.](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Excel-mallin korvaaminen Word-mallilla ja mukautetun XML-osan lisääminen

Tällä hetkellä OPENXML-muotoisen raportin luonnissa käytetään mallina Excel-tiedostoa. Tämä malli korvataan aiemmin ladatulla Wordin SampleVendPaymDocReport.docx-mallitiedostolla. Lisäksi Word-mallia laajennetaan lisäämällä mukautettu XML-osa.

1. Valitse Financessa **Muodon suunnittelija** -sivun **Muoto**-välilehdessä **Liitteet**.
2. Poista aiemmin luotu Excel-malli valitsemalla **Liitteet**-sivulla **Poista**. Vahvista muutos valitsemalla **Kyllä**.
3. Valitse **Uusi** \> **Tiedosto**.

    > [!NOTE]
    > Valittavan asiakirjatyypin on oltava sellainen, että se on [määritetty](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER-parametreissa tallentamaan ER-muotojen mallit.

4. Valitse **Selaa**, siirry aiemmin ladattuun **SampleVendPaymDocReport.docx**-tiedostoon ja valitse se.
5. Valitse **OK**.
6. Sulje **Liitteet**-sivu.
7. Anna tai valitse **Muodon suunnittelija** -sivun **Malli**-kentässä **SampleVendPaymDocReport.docx**-tiedosto. Näin käytetään tätä Word-mallia eikä aiemmin käytettyä Excel-mallia.
8. Valitse **Tallenna**.

    Määritysmuutosten tallennuksen lisäksi **Tallenna**-toiminto päivittää liitteenä olevan Word-mallin. Suunnittelun muodon hierarkkinen rakenne lisätään liitettyyn Word-asiakirjaan uutena mukautettuna, **Raportti**-nimisenä XML-osana. Liitetty Word-malli sisältää sen asiakirjan asettelun, joka luodaan ER-raporttina, ja niiden tietojen rakenteen, jotka ER lisää kyseiseen malliin suorituksen aikana.

9. Huomaa, että juuren muotoelementin otsikko ilmaisee käytössä olevan Word-malli.

    ![Excel-mallin korvaaminen Word-mallilla ja mukautetun XML-osan lisääminen.](../media/er-design-configuration-word-2016-11-image03.gif)

10. Valitse **Muoto **-välilehdestä** Liitteet**.

Mukautetun **Raportti**-XML-osan elementit voidaan nyt yhdistää Word-asiakirjan sisällön ohjausobjekteihin.

Jos olet suunnitellut aiemminkin Word-asiakirjoja lomakkeina, jotka sisältävät [mukautettujen XML-osien](/visualstudio/vsto/custom-xml-parts-overview) elementteihin yhdistettäviä [sisällön ohjausobjekteja](/office/client-developer/word/content-controls-in-word), luo asiakirja seuraavan menettelyn ohjeiden mukaisesti. Lisätietoja on kohdassa [Käyttäjien Wordissa täyttämien tai tulostamien lomakkeiden luominen](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Muussa tapauksessa voit ohittaa seuraavan menettelyn.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Mukautetun XML-osan sisältävän Word-asiakirjan hakeminen ja tietojen yhdistämismäärityksen tekeminen

1. Lataa valittu malli Financesta ja tallenna se paikallisesti Word-asiakirjana valitsemalla Financen **Liitteet**-sivulla **Avaa**.
3. Avaa juuri ladattu asiakirja Wordin työpöytäsovelluksessa.
4. Valitse **Kehittäjä**-välilehdessä **XML-määritysruutu**.

    > [!NOTE]
    > Jos **Kehittäjä**-välilehti ei näy valintanauha, lisää se mukauttamalla valintanauhaa.

5. Valitse **XML-määritys**-ruudun **Mukautettu XML-osa** -kentässä mukautettu **Raportti**-XML-osa.
6. Yhdistä valitun mukautetun **Raportti**-XML-osan elementit ja Word-asiakirjan sisällön ohjausobjektit.
7. Tallenna päivitetty Word-asiakirja paikallisesti nimellä **SampleVendPaymDocReportBounded.docx**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Sellaisen Word-mallin tarkasteleminen, jossa mukautettu XML-osa on yhdistetty sisällön ohjausobjekteihin

1. Avaa Wordin työpöytäsovelluksessa **SampleVendPaymDocReportBounded.docx**-mallitiedosto.
2. Tarkista, että mallissa on sen asiakirjan asettelu, jonka haluat luoda ER-raporttina. ER:n tähän malliin suorituksen aikana lisäävien tietojen paikkamerkkeinä käytetyt sisällön ohjausobjektit perustuvat yhdistämismäärityksiin, jotka määritetään mukautetun **Raportti**-XML-osan ja Word-asiakirjan sisällön ohjausobjektien elementtien välille.

![Word-mallin esikatselu työpöytäsovelluksessa.](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Sellaisen Word-mallin lataaminen, jossa mukautettu XML-osa on yhdistetty sisällön ohjausobjekteihin

1. Poista valitsemalla Financen **Liitteet**-sivulla **Poista** Word-malli, jossa mukautetun **Raportti**-XML-osan ja sisällön ohjausobjektien elementtien välillä ei ole yhdistämismäärityksiä. Vahvista muutos valitsemalla **Kyllä**.
2. Lisää valitsemalla **Uusi** \> **Tiedosto** uusi mallitiedosta, jossa on yhdistämismäärityksiä mukautetun **Raportti**-XML-osan ja sisällön ohjausobjektien elementtien välillä.

    > [!NOTE]
    > Valittavan asiakirjatyypin on oltava sellainen, että se on [määritetty](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER-parametreissa tallentamaan ER-muotojen mallit.

3. Valitse **Selaa**, siirry aiemmin ladatun tai valmisteltuun **SampleVendPaymDocReportBounded.docx** -tiedostoon ja valitse se. Valmistelun ohjeet ovat edellä kohdassa [Mukautetun XML-osan sisältävän Word-asiakirjan hakeminen ja tietojen yhdistämismäärityksen tekeminen](#get-word-doc).
4. Valitse **OK**.
5. Sulje **Liitteet**-sivu.
6. Valitse **Muodon suunnittelija** -sivun **Malli**-kentässä juuri ladattu asiakirjan.
7. Valitse **Tallenna**.
8. Sulje **Muodon suunnittelija** -sivu.

## <a name="mark-the-configured-format-as-runnable"></a>Määritetyn muodon merkitseminen suorittavissa olevaksi

Muokattavissa olevan muodon luonnosversion suorittaminen edellyttää, että se [suorittavissa oleva](../er-quick-start2-customize-report.md#MarkFormatRunnable).

1. Valitse Financen **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjän parametrit**.
2. **Käyttäjän parametrit** -valintaikkunassa määritä **Suorita asetukset** -valinnaksi **Kyllä**, ja valitse sitten **OK**.
3. Tee tarvittaessa nykyisestä sivusta muokattava valitsemalla **Muokkaa**.
4. Määritä valitun **Laskentataulukkoraportin esimerkki** -määrityksen **Suorita luonnos** -asetukseksi **Kyllä**.
5. Valitse **Tallenna**.

## <a name="run-the-format-to-create-output-in-word-format"></a>Word-muotoisen tulosteen luominen suorittamalla muoto

1. Valitse Financessa **Ostoreskontra** \> **Maksut** \> **Maksukirjauskansio**.
2. Valitse aiemmin annetussa maksukirjauskansiossa **Rivit**.
3. Valitse **Toimittajan maksut** -sivulla kaikki ruudukon rivit.
4. Valitse **Maksun tila** \> **Ei mitään**.

    ![Toimittajan maksut -sivulla käsiteltävät maksut.](../media/er-design-configuration-word-2016-11-image05.png)

5. Valitse toimintoruudussa **Luo maksut**.
6. Toimi seuraavasti avautuvassa valintaikkunassa:

    1. Valitse **Maksutapa**-kentässä **Sähköinen**.
    2. Valitse **Pankkitili**-kentässä **GBSI OPER**.
    3. Valitse **OK**.

7. Valitse **Sähköisen raportin parametrit** -valintaikkunasta **OK**.
8. Luotu tuloste on Word-muotoinen ja että siinä on käsiteltyjen maksujen tiedot. Analysoi luotu raportti.

    ![Word-muotoinen luotu tuloste.](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Lisäresurssit

- [Uuden ER-konfiguraation suunnitteleminen raporttien luomiseksi Word-muodossa](../er-design-configuration-word.md)
- [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
