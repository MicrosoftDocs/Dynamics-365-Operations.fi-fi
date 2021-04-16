---
title: Uusien kenttien lisääminen liiketoiminta-asiakirjamalliin Microsoft Excelissä
description: Tässä ohjeaiheessa on tietoja uusien kenttien lisäämisestä liiketoiminta-asiakirjamalliin Microsoft Exceliin liiketoiminta-asiakirjojen hallintatoiminnolla.
author: NickSelin
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 991fe4ea56a2726c5df835cfc90a390cef2d5df5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751127"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Uusien kenttien lisääminen liiketoiminta-asiakirjamalliin Microsoft Excelissä

[!include[banner](../includes/banner.md)]

Voit lisätä uusia kenttiä malliin, jolla luodaan lMicrosoft Excel -muotoisia liiketoiminta-asiakirjoja. Nämä kentät voidaan lisätä paikkamerkkeinä, joiden avulla muodostettuihin asiakirjoihin täytetään tarvittavat tiedot sovelluksesta. Voit määrittää jokaiseen lisättävään kenttään myös sidonnan tietolähteisiin. Tällä tavoin määritetään, mitä sovelluksen tietoja lisätään kenttään, kun liiketoiminta-asiakirjoja luodaan mallin avulla.

Saat lisätietoja tästä toiminnosta suorittamalla tämän ohjeaiheen seuraavan esimerkin. Tämä esimerkki näyttää, miten malli päivitetään täyttämään luotavien vapaatekstilaskujen lomakkeiden kenttiä.

## <a name="configure-business-document-management-to-edit-templates"></a>Mallien muokkaaminen liiketoiminta-asiakirjojen hallinnan avulla

Koska liiketoiminta-asiakirjojen hallinta (BDM) perustuu [sähköisen raportoinnin (ER) yleiskatsauksen](general-electronic-reporting.md) kehykseen, tarvittavat ER- ja BDM-parametrit on määritettävä ennen liiketoiminta-asiakirjojen hallinnan käytön aloittamista.

1.  Kirjaudu Microsoftin Dynamics 365 Financen esiintymään järjestelmänvalvojana.
2.  Suorita seuraavat ohjeaiheen [Liiketoiminta-asiakirjojen hallinnan yleiskatsaus](er-business-document-management.md) esimerkin vaiheet:

    1.  Määritä ER-parametrit.
    2.  Ota liiketoiminta-asiakirjojen hallinta käyttöön.

Voit nyt aloittaa liiketoiminta-asiakirjamallien muokkaaminen käyttämällä liiketoiminta-asiakirjojen hallintaa.

## <a name="import-er-solutions-that-contain-a-template"></a>Mallin sisältävien ER-ratkaisujen tuominen

Tämän menettelyn esimerkissä käytetään virallisesti julkaistua ER-ratkaisua. Ratkaisun ER-määritykset on tuotava Financen nykyiseen esiintymään.

Ratkaisun **Vapaatekstilasku** -ER-muotomäärityksessä on Excel-muotoinen liiketoiminta-asiakirjamalli, jota voi muokata liiketoiminta-asiakirjojen hallinnassa. Tuo tämän ER-muotomäärityksen uusin versio Microsoft Dynamics Lifecycle Servicesta (LCS). Vastaavat ER-tietomalli ja ER-mallin yhdistämismääritykset tuodaan automaattisesti.

Lisätietoja ER-määritysten tuonnista on kohdassa [ER-konfiguraation elinkaaren hallinta](general-electronic-reporting-manage-configuration-lifecycle.md).

![Jaettu LCS-ominaisuuskirjasto -sivu](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>ER-ratkaisumallin muokkaaminen

1.  Kirjaudu käyttäjänä, jolla on **liiketoiminta-asiakirjojen hallinnan** työtilan käyttöoikeus.
2.  Avaa **liiketoiminta-asiakirjojen hallinnan** työtila.

    ![Liiketoiminta-asiakirjojen hallinnan työtila](./media/BDM-AddFldExcel-Workspace.png)

3.  Valitse ruudukossa **Vapaatekstilasku (Excel)** -malli.
4.  Luo valittuun malliin perustuva uusi malli valitsemalla oikeassa ruudussa **Uusi malli**.
5.  Kirjoita **Otsikko**-kenttään uuden mallin otsikoksi **Vapaatekstilasku (Excel) Contoso**.
6.  Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.

BDM-mallieditorin sivu avautuu. Voit muokata valittua mallia verkossa upotetun ohjausobjektin avulla käyttämällä Microsoft 365:ttä.

![BDM-mallieditorin sivu](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Uuden kentän otsikon lisääminen malliin

1.  Valitse BDM-mallieditorisivun Excel-valintanauhan **Näytä**-välilehdessä muokattavan Excel-mallin **Otsikko- ja Ruudukko-** valintaruudut.

    ![Otsikot- ja Ruudukko-valintaruudut valittuina](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Valitse solut **E8:F8**.
3.  Valitse Excel-valintanauhan **Aloitus**-välilehdessä **Yhdistä ja keskitä**. Valitut yhdistetään nyt uuteen yhdistettyyn **E8:F8**-soluun.
4.  Kirjoita yhdistettyyn **E8:F8**-soluun **URL**.
5.  Valitse ensin yhdistetty solu **E7:F7**, sitten **Muotoilusivellin** ja lopuksi valittu yhdistetty solu **E8:F8**. Tämän muotoilu on nyt sama yhdistetyssä solussa **E7:F7**.

    ![Malliin lisätty uuden kentän otsikko](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Tilan varaaminen uudelle kentälle mallia muotoilemalla

1.  Valitse BDM-mallieditorin sivulla yhdistetty solu **G8:H8**.
2.  Valitse Excel-valintanauhan **Aloitus**-välilehdessä **Yhdistä ja keskitä**. Valitut yhdistetään nyt uuteen yhdistettyyn **G8:H8**-soluun.
3.  Valitse ensin yhdistetty solu **G7:H7**, sitten **Muotoilusivellin** ja lopuksi valittu yhdistetty solu **G8:H8**. Tämän muotoilu on nyt sama yhdistetyssä solussa **G7:H7**.

    ![Uudelle kentälle varattu tila](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  Valitse **Nimi**-kentässä **CompanyInfo**.

    Nykyisen Excel-mallin **CompanyInfo**-alue sisältää kaikki kentät, joilla täytetään muodostetun raportin otsikkoon nykyisen yrityksen tiedot myyvänä osapuolena.

    ![CompanyInfo-alue valittu](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Uuden kentän lisääminen malliin

1.  Valitse **BDM-mallieditorin** sivun toimintoruudussa **Näytä muotoilu**.
2.  Valitse **Mallin rakenne** -ruudussa **Lisää**.

    > [!NOTE]
    > Uutena kenttänä käytettävää mallin osaa on muokattava. Tämä muokkaus tehtiin jo muotoilemalla yhdistetty solu **G8:H8**.

    ![Uuden kentän lisääminen malliin](./media/BDM-AddFldExcel-AddCell.png)

3.  Lisää uusi kenttä soluna malliin valitsemalla **Excel\Solu**.

    Voit valita **Excel\Alue**, jos haluat lisätä uuden alueen malliin. Annettu alue voi sisältää useita soluja. Voit lisätä nämä solut myöhemmin.
    
    Huomaa, että mallin **CompanyInfo**-osa valitaan automaattisesti **Mallin rakenne** -ruudussa, koska on parhaiten sopiva pääosa nykyisessä mallirakenteessa lisättävän kentän kannalta.
    
4.  Kirjoita **Excel-alue**-kenttään **CompanyURL_Value**.
5.  Valitse **OK**.

    ![CompanyURL_Value-kenttä lisätään mallin rakenteeseen.](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  Valitse **Mallin rakenne** -ruudussa kolmen pisteen painike (...) ja valitse sitten **Näytä sidonnat**.

    ![Näytä sidonnat valittu](./media/BDM-AddFldExcel-ShowBindings.png)

    **Mallin rakenne** -ruudussa näkyy nyt pohjana olevassa ER-muodossa käytettävissä olevat tietolähteet.

7.  Valitse **CompanyInfo_Value** kentäksi, johon pohjana olevan ER-muodon tietolähde on tarkoitus sitoa.
8.  Laajenna **Mallin rakenne** -ruudun **Tietolähteet**-osassa **Malli \> InvoiceBase \> CompanyInfo**.
9.  Valitse **CompanyInfo**-kohdassa **WebsiteURI**.

    ![WebsiteURI valittuna](./media/BDM-AddFldExcel-BindURL.png)

10. Valitse **Sido**.
11. Valitse **Mallin rakenne** -ruudussa **Tallenna** ja sulje sitten BDM-mallieditorin sivu.

Päivitetty malli näkyy **Liiketoiminta-asiakirjojen hallinnan** työtilan oikeanpuolisen ruudun **Malli**-välilehdessä. Huomaa, että ruudukossa muokatun mallin **Tila**-kentän arvo on nyt **Luonnos** eikä **Tarkistusversio**-kenttä ole enää tyhjä. Nämä muutoksen ilmaisevat, että mallin muokkausprosessi on aloitettu.

![Muokattu malli liiketoiminta-asiakirjojen hallinnan työtilassa](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Yrityksen asetusten tarkistaminen

1.  Valitse **Organisaation hallinto \> Organisaatiot \> Yritykset**.
2.  Tarkista, että yrityksen URL-osoite on annettu **Yhteystiedot**-pikavälilehdessä.

![Yritykset-sivulla annettu yrityksen URL-osoite](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Päivitetyn mallin testaaminen luomalla liiketoiminta-asiakirjoja

1.  Vaihda sovelluksessa yritykseksi **USMF** ja valitse sitten **Myyntireskontra \> Laskut \> Kaikki vapaatekstilaskut**.
2.  Valitse ensin lasku **FTI-00000002** ja sitten **Tulostuksenhallinta**.
3.  Laajenna vasemmassa ruudussa **Moduuli - Myyntireskontra \> Asiakirjat \> Vapaatekstilasku**.
4.  Määritä käsiteltävien laskujen vaikutusalue valitsemalla **Vapaatekstilasku**-kohdassa **Alkuperäinen tiedosto** -taso.
5.  Valitse oikeassa ruudussa ensin **Raportin muoto** -kenttä ja sitten määritetyn asiakirjatason **Vapaatekstilasku (Excel) Contoso** -malli.

    ![Vapaatekstilasku (Excel) Contoso -malli valittuna](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Sulje nykyinen sivu painamalla **Esc**-näppäintä.
7.  Valitse **Tulosta \> Valitut**.
8.  Lataa muodostettu asiakirja ja avaa se Excelissä.

    ![Excelin vapaatekstilasku](./media/BDM-AddFldExcel-PreviewReport.png)

Muokatun mallin avulla luodaan valitulle nimikkeelle vapaatekstilaskun raportti. Jos haluat analysoida, miten malliin tekemäsi muutokset vaikuttavat tähän raporttiin, suorita raportti yhdessä sovellusistunnossa heti sen jälkeen, kun olet muuttanut mallia toisessa sovellusistunnossa.

## <a name="related-links"></a>Liittyvät linkit

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)

[Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md)

[Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]