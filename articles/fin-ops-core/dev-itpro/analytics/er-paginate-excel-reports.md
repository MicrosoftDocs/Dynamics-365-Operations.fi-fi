---
title: ER-muodon suunnitteleminen muodostettujen asiakirjojen sivuttamista varten Excelissä
description: Tässä artikkelissa selitetään, miten suunnitellaan sähköisen raportoinnin (ER) muoto, joka sivuttaa muodostetun asiakirjan Microsoft Excelissä.
author: NickSelin
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.openlocfilehash: e8edc8bba62f74b4f81d423cf75b5fb87c01e43f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909275"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>ER-muodon suunnitteleminen muodostettujen asiakirjojen sivuttamista varten Excelissä

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin toiminnallisen konsultin roolin käyttäjä voi määrittää [sähköisen raportoinnin (ER)](general-electronic-reporting.md) muodon lähtevien asiakirjojen muodostamiseksi Microsoft Excelissä ja asiakirjan sivuttamisen hallitsemiseksi.

Tässä esimerkissä muokataan Microsoftin toimittamaa ER-muotoa, jota käytetään valvontaraportin tulostukseen, kun Intrastat-ilmoitus on [muodostettu](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Tässä raportissa voit ottaa huomioon raportoidut Intrastat-tapahtumat. Muutosten avulla voit hallita muodostettujen valvontaraporttien sivuttamista.

Tässä artikkelissa kuvatut toimenpiteet voidaan suorittaa **DEMF**-yrityksessä. Koodausta ei tarvita. Ennen aloittamista seuraavat tiedostot täytyy ladata ja tallentaa.

| kuvaus       | Tiedostonimi |
|-------------------|-----------| 
| Raporttimalli 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Raporttimalli 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>Määritä ER-kehys

Seuraa vaiheita kohdassa [Määritä ER-kehys](er-quick-start2-customize-report.md#ConfigureFramework) luodaksesi ER-parametrien vähimmäisjoukon. Nämä asetukset on suoritettava, ennen kuin ER-kehystä käytetään normaalin ER-muodon mukautetun version suunnitteluun.

## <a name="import-the-standard-er-format-configuration"></a>Tuo ER-muodon vakiokonfiguraatio

Seuraa vaiheita kohdassa [Tuo ER-muodon vakiokonfiguraatio](er-quick-start2-customize-report.md#ImportERSolution1) lisätäksesi ER-vakiokonfiguraatiot nykyiseen Dynamics 365 Finance -ilmentymääsi. Tuo versio **1.9** **Intrastat-raportin** konfiguroinnin muodosta. Perusversio 1 **Intrastat-mallin** peruskonfiguraatiosta tuodaan automaattisesti säilöstä.

## <a name="customize-the-standard-er-format"></a>Mukauta ER-vakiomuotoa

### <a name="create-the-custom-er-format"></a>Mukautetun ER-muodon luominen

Tässä skenaariossa edustat Litware-yritystä, joka on valittu aktiiviseksi ER-konfiguraation toimittajaksi. Uuden ER-muodon konfiguraatio on luotava käyttämällä **Intrastat-raportin** konfiguraatiota pohjana.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Konfiguraatiot**-sivun määrityspuun vasemmassa ruudussa **Intrastat-malli** ja valitse sitten **Intrastat-raportti**. Litware, Inc. käyttää tämän ER-muodon konfiguraation versiota 1.9 mukautetun version pohjana.
3. Avaa pudotusvalintaikkuna valitsemalla **Luo konfigurointi**. Voit käyttää tätä valintaikkunaa luodaksesi uuden konfiguroinnin mukautetulle maksumuodolle.
4. Valitse **Uusi**-kenttäryhmässä **Johda nimestä: Intrastat-raportti, Microsoft** -vaihtoehto.
5. Kirjoita **Nimi**-kenttään **Intrastat-raportti Litware**.
6. Valitse **Luo konfigurointi** luodaksesi uuden muodon.

**Intrastat-raportti Litware** -ER-muotokonfiguraation versio 1.9.1 luodaan. Tämän version [tila](general-electronic-reporting.md#component-versioning) on **Luonnos**, ja sitä voidaan muokata. Mukautetun ER-muodon nykyinen sisältö vastaa Microsoftin toimittaman muodon sisältöä.

### <a name="make-the-custom-format-runnable"></a>Merkitse mukautettu muoto suoritettavaksi

Nyt kun mukautetun muotosi ensimmäinen versio on luotu, ja sen tila on **Luonnos**, voit suorittaa muodon testaustarkoituksia varten. Jos haluat suorittaa raportin, käsittele toimittajamaksu käyttämällä maksutapaa, joka viittaa mukautettuun ER-muotoosi. Oletuksena kun kutsut ER-muodon sovelluksesta, vain versiot, joiden tila on **Valmis** tai **Jaettu**, otetaan [huomioon](general-electronic-reporting.md#component-versioning). Tämä käytös auttaa estämään sellaisten ER-muotojen käyttöä, joiden mallit eivät ole valmiit. Testiajoissasi voit kuitenkin pakottaa sovelluksen käyttämään ER-muotosi versiota, jonka tila on **Luonnos**. Tällä tavoin voit säätää nykyistä muotoversiota, jos muokkauksia tarvitaan. Lisätietoja on kohdassa [Soveltuvuus](electronic-reporting-destinations.md#applicability).

Käyttääksesi ER-muodon luonnosversiota sinun on merkittävä ER-muoto selkeästi.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. **Käyttäjän parametrit** -valintaikkunassa määritä **Suorita asetukset** -valinnaksi **Kyllä**, ja valitse sitten **OK**.
4. Tee tarvittaessa nykyisestä sivusta muokattava valitsemalla **Muokkaa**.
5. Valitse vasemman ruudun määrityspuussa **Intrastat-raportti Litware**.
6. Määritä **Suorita luonnos**-vaihtoehdoksi **Kyllä** ja valitse sitten **Tallenna**.

    ![Suorita luonnos -vaihtoehto Konfiguroinnit-sivulla.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Ulkomaankaupan parametrien määrittäminen käyttämään mukautettua ER-muotoa

Seuraavia vaiheita noudattamalla voit määrittää ulkomaankaupan parametrit, jotta voit käyttää mukautettua muotoa.

1. Siirry kohtaan **Vero** \> **Asetukset** \> **Ulkomaankauppa** \> **Ulkomaankaupan parametrit**.
2. Valitse **Ulkomaankaupan parametrit**-sivun **Sähköinen raportointi** -pikavälilehden **Tiedostomuodon määritys** -kentässä **Intrastat-raportti Litware**.
3. Valitse **Raporttimuodon yhdistäminen** -kentässä **Intrastat-raportti Litware**.
4. Valitse **Tallenna**.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>Voit määrittää mukautetun muodon käyttämään ladattua raporttimallia

### <a name="review-the-first-downloaded-excel-template"></a>Ensimmäisen ladatun Excel-mallin tarkasteleminen

1. Avaa Excelin työpöytäsovelluksessa aiemmin ladattu **ERIntrastatReportDemo1.xlsx**-mallitiedosto.
2. Varmista, että malli sisältää nimettyjä alueita, jotta voit luoda muodostettuihin asiakirjoihin raportin otsikon, raportin tiedot ja alatunnisteosat.

    ![Excel-mallin 1 asettelu työpöytäsovelluksessa.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Korvaa nykyinen Excel-malli mukautetussa ER-muodossa

Lisää uusi Excel-malli mukautettuun ER-muotoon.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Konfiguraatiot**-sivun määrityspuun vasemmassa ruudussa **Intrastat-malli** \> **Intrastat-raportti** ja valitse sitten **Intrastat-raportti Litware** -konfiguraatio.
3. Valitse **Suunnittelu**.
4. Valitse **Muodon suunnittelija**-sivulla hallintapaneelista **Näytä tiedot**.
5. Varmista, että **Intrastat: Excel** -juurimuotokomponentti on valittuna ja valitse sitten toimintoruudussa **Tuo**-välilehden **Tuo**-ryhmässä **Päivitä Excelistä**.
6. Valitse **Päivitä Excelistä** -valintaikkunassa **Päivitä malli**.
7. Selaa ja valitse **Avaa**-valintaruudusta **ERIntrastatReportDemo1.xlsx**-tiedosto, jonka latasit aiemmin ja valitse sitten **Avaa**.
8. Valitse **OK**.
9. Valitse **Tallenna**.

![Muotorakenne ER-muodon suunnitteluohjelmassa sen jälkeen, kun uusi Excel-malli on lisätty.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Muuta tietojen sidontaa niin, että nimikkeen kuvaus näytetään muodostetussa raportissa

1. Valitse **Muodon suunnittelu** -sivulla **Yhdistämismääritys**-välilehti.
2. Laajenna **Intrastat** \> **Raporttirivit** ja valitse **Kauppatavarakoodi**-komponentti.
3. Valitse **Muokkaa kaavaa**.
4. Muuta sidontakaava muodosta `@.CommodityCode` muotoon `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Valitse **Tallenna**.

![Konfiguroitu sidonta, jonka avulla nimikkeen kuvaus näytetään ER-muodon suunnitteluohjelmassa.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Intrastat-ilmoituksen valvontaraportin muodostaminen

Varmista ensin, että raportoinnin Intrastat-tapahtumat on määritetty **Intrastat**-sivulle.

![Tapahtumat Intrastat-sivulla.](./media/er-paginate-excel-reports-transactions1.gif)

Muodosta sitten Intrastat-ilmoituksen valvontaraportti käyttämällä mukautettua ER-muotoa.

1. Siirry kohtaan **Vero** \> **Ilmoitukset** \> **Ulkomaankauppa** \> **Intrastat**.
2. Valitse **Intrastat**-sivun toimintoruudussa **Tuloste** \> **Raportti**.
3. Noudata **Intrastat-raportti**-valintaikkunassa seuraavia vaiheita suorittaaksesi raportin:

    1. Määritä **Alkamispäivä**- ja **Päättymispäivämäärä**-kentät sisällyttääksesi tiettyjä Intrastat-tapahtumia raporttiin.
    2. Määritä **Luo tiedosto** -asetukseksi **Ei**.
    3. Määritä **Luo raportti** -asetukseksi **Kyllä**.
    4. Valitse **OK**.

4. Lataa ja tallenna muodostettu asiakirja.
5. Avaa muodostettu asiakirja Excelissä ja tarkasta se.

    ![Muodostettu Excel-tiedosto työpöytäsovelluksessa.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Mukautetun muodon konfiguroiminen sivuttamaan muodostetut tiedostot

### <a name="review-the-second-downloaded-excel-template"></a>Toisen ladatun Excel-mallin tarkasteleminen

1. Avaa Excelissä **ERIntrastatReportDemo2.xlsx**-mallitiedosto, jonka latasit aiemmin.
2. Vertaa tätä mallia **ERIntrastatReportDemo1.xlsx**-malliin ja varmista, että se sisältää useita uusia Excel-nimiä, joiden avulla voidaan luoda ja täyttää sivukohtaisia osia muodostetuissa asiakirjoissa:

    - **ReportPageHeader**-alue lisätään sivun ylätunnisteita varten.
    - **ReportPageFooter**-alue lisätään sivun alatunnisteita varten.
    - **ReportPageFooter\_PageLines** -solu määritetään näyttämään sivukohtaisten tapahtumien lukumäärä.
    - **ReportPageFooter\_PageAmount** -solu määritetään näyttämään sivukohtaisten tapahtumien kokonaismäärä.
    - **ReportPageFooter\_PageWeight** -solu määritetään näyttämään sivukohtaisten tapahtumien kokonaispaino.
    - **ReportPageFooter\_RunningCounterLines** -solu määritetään näyttämään tapahtumien laskuri raportin alusta nykyiseen sivuun asti.
    - **ReportPageFooter\_RunningTotalAmount** -solu määritetään näyttämään kaikkien tapahtumien kokonaismäärä raportin alusta nykyiseen sivuun asti.
    - **ReportPageFooter\_RunningTotalWeight** -solu määritetään näyttämään kaikkien tapahtumien kokonaispaino raportin alusta nykyiseen sivuun asti.

    ![Excel-mallin 2 asettelu työpöytäsovelluksessa.](./media/er-paginate-excel-reports-template2a.gif)

    Tämän mallin **CommodityCode**-solu määritetään rivittämään solun teksti. Koska tapahtumatietorivi on määritetty siten, että se sopii automaattisesti rivin korkeuteen, koko rivin korkeuden on muututtava automaattisesti, kun **CommodityCode**-solun teksti rivitetään.

    ![CommodityCode-solu määritettynä rivittämään solun teksti.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Toista nykyisen Excel-mallin korvaaminen mukautetussa ER-muodossa

1. Noudata vaiheita tämän artikkelin [Nykyisen Excel-mallin korvaaminen mukautetussa ER-muodossa](#replace-template) -osassa. Valitse kuitenkin vaiheessa 7 **ERIntrastatReportDemo2.xlsx**-tiedosto.
2. Laajenna **Muodon suunnittelu** -sivulla **Intrastat**.
3. Nimeä muokattavaan ER-malliin lisätyn [Alueen](er-fillable-excel.md#range-component) muotokomponentit niin, että ne synkronoivat rakenteen sovelletun Excel-mallin rakenteen kanssa.

    1. Valitse **Alue**-komponentti, joka on liitetty Excel-nimeen **ReportPageHeader**.
    2. Syötä **Muoto**-välilehden **Nimi**-kenttään **Raporttisivun ylätunniste**.
    3. Valitse **Alue**-komponentti, joka on liitetty Excel-nimeen **ReportPageFooter**.
    4. Syötä **Muoto**-välilehden **Nimi**-kenttään **Raporttisivun alatunniste**.

4. Valitse **Tallenna**.

![Muotorakenne ER-muodon suunnitteluohjelmassa sen jälkeen, kun uusi Excel-malli on korvattu.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Muuta muotorakenne asiakirjan sivuttamista varten

1. Valitse **Muodon suunnittelija** -sivun vasemmanpuoleisen ruudun muotopuussa **Intrastat**-juurikomponentti.
2. Valitse **Lisää**.
3. Valitse **Lisää**-valintaikkunassa [Sivu](er-fillable-excel.md#page-component)-komponentti **Excel**-komponenttiryhmässä.
4. Syötä **Komponentin ominaisuudet**-valintaikkunan **Nimi**-kenttään **Raporttisivu**. Valitse sitten **OK**.
5. Jos haluat käyttää **Raporttisivun ylätunniste** -komponenttia kaikkien muodostettujen sivujen ylätunnisteena, noudata seuraavia vaiheita:

    1. Valitse **Raporttisivun ylätunniste** -komponentti ja valitse sitten **Leikkaa**.
    2. Valitse **Raporttisivu**-komponentti ja valitse sitten **Liitä**.
    3. Laajenna **Raporttisivu**.
    4. Pakottaaksesi **Sivu**-komponentin [pitämään](er-fillable-excel.md#page-component-structure) tätä aluetta sivun ylätunnisteena, valitse **Raporttisivun ylätunniste** ja valitse sitten **Muoto**-välilehden **Replikointisuunta** -kentässä **Ei replikointia**.

6. Tehdäksesi muodostetun asiakirjan sivutuksen niin, että raporttirivien sisältö otetaan huomioon, noudata seuraavia vaiheita:

    1. Valitse **Raporttirivit**-komponentti ja valitse sitten **Leikkaa**.
    2. Valitse **Raporttisivu**-komponentti ja valitse sitten **Liitä**.

7. Jos haluat sisällyttää raportin alatunnisteen raporttirivien jälkeen mutta ennen viimeisen sivun alatunnistetta, noudata seuraavia vaiheita:

    1. Valitse **Raportin alatunniste**-komponentti ja valitse sitten **Leikkaa**.
    2. Valitse **Raporttisivu**-komponentti ja valitse sitten **Liitä**.

8. Jos haluat käyttää **Raporttisivun alatunniste** -komponenttia kaikkien muodostettujen sivujen alatunnisteena, noudata seuraavia vaiheita:

    1. Valitse **Raporttisivun alatunniste** -komponentti ja valitse sitten **Leikkaa**.
    2. Valitse **Raporttisivu**-komponentti ja valitse sitten **Liitä**.
    3. Pakottaaksesi **Sivu**-komponentin [pitämään](er-fillable-excel.md#page-component-structure) tätä aluetta sivun alatunnisteena, valitse **Raporttisivun alatunniste** ja valitse sitten **Muoto**-välilehden **Replikointisuunta** -kentässä **Ei replikointia**.

![Muotorakenne ER-muodon suunnitteluohjelmassa sen jälkeen, kun asiakirjan sivutus on toteutettu.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Tietolähteiden lisääminen sivun alatunnisteen kokonaismäärien laskemista varten

Sinun on määritettävä uudet tietolähteet, jotta voit laskea sivujen yhteismäärän, laskurin ja juoksevat kokonaisarvot sekä näyttää ne sivun alatunnisteosassa. Tähän tarkoitukseen on suositeltavaa käyttää [Tietokokoelma](er-data-collection-data-sources.md)-tietolähteitä.

1. Valitse **Muodon suunnittelu** -sivulla **Yhdistämismääritys**-välilehti.
2. Valitse **Lisää juuri** ja toimi sitten seuraavasti:

    1. Valitse **Lisää tietolähde**-valintaikkunan **Yleiset**-osassa **Tyhjä säilö**.
    2. Syötä **'Tyhjä säilö' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Yhteensä**.
    3. Valitse **OK**.

3. Valitse **Yhteensä**-tietolähde, valitse **Lisää** ja noudata sitten seuraavia vaiheita:

    1. Valitse **Lisää tietolähde**-valintaikkunan **Yleiset**-osassa **Tyhjä säilö**.
    2. Syötä **'Tyhjä säilö' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Sivu**.
    3. Valitse **OK**.

4. Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Lisää tietolähde**-valintaikkunan **Yleiset**-osassa **Tyhjä säilö**.
    2. Syötä **'Tyhjä säilö' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Juokseva**.
    3. Valitse **OK**.

5. Valitse **Total.Page**-tietolähde, valitse **Lisää** ja noudata sitten seuraavia vaiheita:

    1. Valitse **Lisää tietolähde**-valintaikkunan **Funktiot**-osassa **Tietokokoelma**.
    2. Syötä **'Tietokokoelma' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Määrä**.
    3. Valitse **Nimiketyyppi**-kentässä **Reaaliluku**.
    4. Määritä **Kerää kaikki arvot** -asetukseksi **Kyllä**.
    5. Valitse **OK**.

6. Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Lisää tietolähde**-valintaikkunan **Funktiot**-osassa **Tietokokoelma**.
    2. Syötä **'Tietokokoelma' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Paino**.
    3. Valitse **Nimiketyyppi**-kentässä **Reaaliluku**.
    4. Määritä **Kerää kaikki arvot** -asetukseksi **Kyllä**.
    5. Valitse **OK**.

7. Valitse **Total.Running**-tietolähde, valitse **Lisää** ja noudata sitten seuraavia vaiheita:

    1. Valitse **Lisää tietolähde**-valintaikkunan **Funktiot**-osassa **Tietokokoelma**.
    2. Syötä **'Tietokokoelma' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Määrä**.
    3. Valitse **Nimiketyyppi**-kentässä **Reaaliluku**.
    4. Määritä **Kerää kaikki arvot** -kentän arvoksi **Kyllä**.
    5. Valitse **OK**.

8. Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Lisää tietolähde**-valintaikkunan **Funktiot**-osassa **Tietokokoelma**.
    2. Syötä **'Tietokokoelma' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Paino**.
    3. Valitse **Nimiketyyppi**-kentässä **Reaaliluku**.
    4. Määritä **Kerää kaikki arvot** -kentän arvoksi **Kyllä**.
    5. Valitse **OK**.

9. Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Lisää tietolähde**-valintaikkunan **Funktiot**-osassa **Tietokokoelma**.
    2. Syötä **'Tietokokoelma' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Rivit**.
    3. Valitse **Nimiketyyppi**-kentässä **Kokonaisluku**.
    4. Määritä **Kerää kaikki arvot** -kentän arvoksi **Kyllä**.
    5. Valitse **OK**.

10. Valitse **Tallenna**.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Tietolähteiden lisääminen sivun alatunnisteen näkyvyyden hallintaa varten

Jos aiot hallita sivun alatunnisteen näkyvyyttä ja jos et suunnittele alatunnisteen lisäämistä viimeiselle sivulle, jos se sisältää tapahtumia, määritä uusi tietolähde laskemaan vaadittu juokseva laskuri.

1. Valitse **Muodon suunnittelu** -sivulla **Yhdistämismääritys**-välilehti.
2. Valitse **Total.Running**-tietolähde ja valitse **Lisää**.
3. Valitse **Lisää tietolähde**-valintaikkunan **Funktiot**-osassa **Tietokokoelma**.
4. Syötä **'Tietokokoelma' -tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Lines2**.
5. Valitse **Nimiketyyppi**-kentässä **Kokonaisluku**.
6. Määritä **Kerää kaikki arvot** -asetukseksi **Kyllä**.
7. Valitse **OK**.
8. Valitse **Tallenna**.

![Lisätyt tietolähteet ER-muodon suunnitteluohjelmassa.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Sidontojen määrittäminen kokonaisarvojen keräämistä varten

1. Laajenna **Muodon suunnittelija** -sivun muotopuussa **Raporttirivit**-komponentti ja valitse sisäkkäinen **Laskun arvo** -komponentti.
2. Valitse **Muokkaa kaavaa**.
3. Muuta sidontakaava muodosta `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` muotoon `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > Sen lisäksi, että tämä sidonta lisää määräarvon Excel-soluun jokaista toistettavaa tapahtumaa varten, sidonta kerää tietokokoelman **Total.Page.Amount**-tietolähteen arvon.

4. Valitse sisäkkäinen **Paino**-komponentti.
5. Valitse **Muokkaa kaavaa**.
6. Muuta sidontakaava muodosta `@.'$RoundedWeight'` muotoon `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > Sen lisäksi, että tämä sidonta lisää painoarvon Excel-soluun jokaista toistettavaa tapahtumaa varten, sidonta kerää tietokokoelman **Total.Page.Weight**-tietolähteen arvon.

![Määritetyt sidonnat kokonaisarvojen keräämistä varten ER-muodon suunnitteluohjelmassa.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Täytettävien sidontojen määrittäminen sivun alatunnisteen kokonaismäärissä

1. Laajenna **Muodon suunnittelija** -sivun muotopuussa **Raporttisivun alatunniste** -komponentti, valitse sisäkkäinen **Alue**-komponentti, joka viittaa Excelin **ReportPageFooter\_PageAmount** -soluun ja noudata sitten seuraavia vaiheita:

    1. Valitse oikeanpuoleisen ruudun tietolähdepuusta **Total.Page.Amount.Sum()** -nimike.
    2. Valitse **Sido**.
    3. Valitse **Muokkaa kaavaa**.
    4. Päivitä kaava muotoon `Total.Page.Amount.Sum(false)`.

    > [!NOTE]
    > Tämän funktion argumentti on määritettävä arvoon **Epätosi**, jotta nykyisen sivun kerätyt tiedot voidaan pitää, koska näitä tietoja tarvitaan määrän juoksevan kokonaismäärän, sivukohtaisen rivimäärän ja laskurin rivien laskemiseen.

2. Valitse muotopuussa sisäkkäinen **Alue**-komponentti, joka viittaa Excelin **ReportPageFooter\_PageWeight** -soluun ja noudata sitten seuraavia vaiheita:

    1. Valitse oikeanpuoleisen ruudun tietolähdepuusta **Total.Page.Weight.Sum()** -nimike.
    2. Valitse **Sido**.
    3. Valitse **Muokkaa kaavaa**.
    4. Päivitä kaava muotoon `Total.Page.Weight.Sum(false)`.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Täytettävien sidontojen määrittäminen sivun juoksevissa kokonaismäärissä

1. Laajenna **Muodon suunnittelija** -sivun muotopuussa **Raporttisivun alatunniste** -komponentti, valitse sisäkkäinen **Alue**-komponentti, joka viittaa Excelin **ReportPageFooter\_RunningTotalAmount** -soluun ja noudata sitten seuraavia vaiheita:

    1. Valitse oikeanpuoleisen ruudun tietolähdepuusta **Total.Running.Amount.Collect()** -nimike.
    2. Valitse **Sido**.
    3. Valitse **Muokkaa kaavaa**.
    4. Päivitä kaava muotoon `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`.

    > [!NOTE]
    > `Total.Running.Amount.Sum(false)`-operandi palauttaa aiemmin kerätyn määrän juoksevan kokonaismäärän. `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`-operandi palauttaa nykyisen sivun kokonaismäärän. Toisen operandin sisäkkäisen funktion argumentti on määritettävä arvoon **Tosi** `Total.Page.Amount`-tietokokoelman nollaamiseksi heti, kun tämä arvo on lisätty `Total.Running.Amount` -juoksevan summan kokoelmaan. Määritetyn argumentin täytyy alkaa kerätä seuraavaa sivujen kokonaismäärää arvosta 0 (nolla).
    >
    > Funktio `Total.Running.Amount.Sum(false)` kutsutaan syöttämään määrän juokseva summa Excelin **ReportPageFooter\_RunningTotalAmount** -soluun nykyisellä sivulla.

2. Valitse muotopuussa sisäkkäinen **Alue**-komponentti, joka viittaa Excelin **ReportPageFooter\_RunningTotalWeight** -soluun ja noudata sitten seuraavia vaiheita:

    1. Valitse oikeanpuoleisen ruudun tietolähdepuusta **Total.Running.Weight.Collect()** -nimike.
    2. Valitse **Sido**.
    3. Valitse **Muokkaa kaavaa**.
    4. Päivitä kaava muotoon `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Täytettävien sidontojen määrittäminen sivun juoksevassa laskurissa

1. Laajenna **Muodon suunnittelija** -sivun muotopuussa **Raporttisivun alatunniste** -komponentti, valitse sisäkkäinen **Alue**-komponentti, joka viittaa Excelin **ReportPageFooter\_RunningCounterLines** -soluun ja noudata sitten seuraavia vaiheita:
2. Valitse **Muokkaa kaavaa**.
3. Lisää kaava `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))`.

    > [!NOTE]
    > Tämä kaava palauttaa kerättyjen määräarvojen lukumäärän koko raportissa. Tämä lukumäärä on sama kuin nykyisellä hetkellä toistettavien tapahtumien lukumäärä. Samanaikaisesti kaava kerää palautetun arvon **Total.Running.Lines**-kokoelmassa.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Täytettävien sidontojen määrittäminen sivun alaviitteen laskurissa

1. Laajenna **Muodon suunnittelija** -sivun muotopuussa **Raporttisivun alatunniste** -komponentti, valitse sisäkkäinen **Alue**-komponentti, joka viittaa Excelin **ReportPageFooter\_PageLines** -soluun ja noudata sitten seuraavia vaiheita:
2. Valitse **Muokkaa kaavaa**.
3. Lisää kaava `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)`.

    > [!NOTE]
    > Tämä kaava laskee nykyisen sivun tapahtumien lukumäärän eroksi kohteessa **Total.Page.Amount.Result** kerätyn koko raportin tapahtumien lukumäärän ja kohteeseen **Total.Running.Lines.Sum** tässä vaiheessa tallennettujen tapahtumien lukumäärän välillä. Koska nykyisen sivun tapahtumien lukumäärä on tallennetu kohteeseen **Total.Running.Lines** **Alue**-komponentin sidonnassa, joka viittaa Excelin **ReportPageFooter\_RunningCounterLines** -soluun, nykyisen sivun tapahtumien lukumäärää ei ole vielä sisällytetty. Näin ollen tämä ero on sama kuin nykyisen sivun tapahtumien lukumäärä.

![Määritetyt, täytettävät sidonnat sivun alatunnistelaskurissa ER-muodon suunnitteluohjelmassa.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Komponentin näkyvyyden määrittäminen

Voit muuttaa sivun ylä- ja alatunnisteen näkyvyyttä muodostetun asiakirjan tietyllä sivulla, kun haluat piilottaa seuraavat elementit:

- Sivun ylätunniste ensimmäisellä sivulla, koska raportin ylätunniste sisältää jo sarakeotsikot
- Sivun ylätunniste sivulla, jossa ei ole tapahtumia, jotka voivat tapahtua viimeisellä sivulla
- Sivun alatunniste sivulla, jossa ei ole tapahtumia, jotka voivat tapahtua viimeisellä sivulla

Muuta näkyvyyttä päivittämällä **Käytössä**-ominaisuus komponenteissa **Raporttisivun ylätunniste** ja **Raporttisivun alatunniste**.

1. Laajenna **Muodon suunnittelija** -sivun muotopuussa **Raporttisivu**-komponentti, valitse sisäkkäinen **Raporttisivun ylätunniste** -komponentti ja noudata sitten seuraavia vaiheita:

    1. Valitse **Muokkaa** kentässä **Käytössä**.
    2. Syötä **Kaavan suunnittelutoiminto** -sivun **Kaava**-kenttään seuraava lauseke:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Valitse muotopuussa sisäkkäinen **Raporttisivun alatunniste** -komponentti ja noudata seuraavia vaiheita:

    1. Valitse **Muokkaa** kentässä **Käytössä**.
    2. Syötä **Kaavan suunnittelutoiminto** -sivun **Kaava**-kenttään seuraava lauseke:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)`-rakennetta käytetään nykyisen sivun tapahtumien lukumäärän laskemiseen. `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)`-rakennetta käytetään nykyisen sivun tapahtuminen lukumäärän lisäämiseen kokoelmaan, jotta seuraavan sivun alatunnisteen näkyvyys käsitellään oikein.
    >
    > `Total.Running.Lines`-kokoelmaa ei voi käyttää tässä uudelleen, koska **Käytössä**-ominaisuus käsitellään peruskomponentissa **sen jälkeen**, kun sisäkkäisten komponenttien sidonnat on käsitelty. Kun **Käytössä**-ominaisuus on käsitelty, `Total.Running.Lines`-kokoelmaan on jo lisätty nykyisen sivun tapahtumien lukumäärä.

3. Valitse **Tallenna**.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Intrastat-ilmoituksen valvontaraportin muodostaminen (päivitetty)

1. Varmista, että **Intrastat**-sivulla on 24 tapahtumaa. Toista vaiheet tämän artikkelin [Intrastat-ilmoituksen valvontaraportin muodostaminen](#generate-intrastat-control-report) -osassa, jotta voit muodostaa ja tarkastaa valvontaraportin.

    Kaikki tapahtumat näytetään ensimmäisellä sivulla. Sivujen kokonaismäärät ja laskurit ovat samat kuin raportin kokonaismäärät ja laskurit. Sivun ylätunnistealue on piilotettu ensimmäisellä sivulla, koska raportin ylätunniste sisältää jo sarakeotsikot. Sivun ylä- ja alatunniste on piilotettu toisella sivulla, koska sivulla ei ole tapahtumia.

    ![Muodostettu Excel-asiakirja työpöytäsovelluksessa.](./media/er-paginate-excel-reports-document2.gif)

2. Päivitä kaksi tapahtumaa **Intrastat**-sivulla vaihtamalla **Nimikkeen numero** -koodi muodosta **D00006** muotoon **L0010**. Huomaa, että uuden nimikkeen **Stereoaktiivikaiutinpari** on pitempi kuin alkuperäisen nimikkeen **Vakiokaiutin** tuotenimi. Tämä tilanne pakottaa tekstin rivittämisen muodostetun asiakirjan vastaavassa solussa. Asiakirjan sivutus ja sivuihin liittyvä summaaminen ja laskeminen on nyt päivitettävä. Toista vaiheet osassa [Intrastat-ilmoituksen valvontaraportin muodostaminen](#generate-intrastat-control-report), jotta voit muodostaa ja tarkastaa valvontaraportin.

    Tapahtumat esitetään tällä hetkellä kahdella sivulla ja sivun kokonaismäärät ja laskurit lasketaan oikein. Sivun ylätunnistealue on piilotettu oikein ensimmäisellä sivulla, ja se näkyy toisella sivulla. Sivun alatunniste näkyy kummallakin sivulla, koska sivut sisältävät tapahtumia.

    ![Päivitetty muodostettu Excel-asiakirja työpöytäsovelluksessa.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Onko mahdollista tunnistaa, milloin sivumuotokomponentti on käsitellyt viimeisen sivun?

**Sivu**-komponentti [ei paljasta](er-fillable-excel.md#page-component-limitations) tietoa käsiteltävän sivun numerosta eikä sivujen kokonaismäärästä muodostetussa asiakirjassa. Voit kuitenkin määrittää ER-[kaavoja](er-formula-language.md) viimeisen sivun tunnistamista varten. Tässä on esimerkki:

- Laske **raporttisivun** komponentin avulla käsiteltyjen tapahtumien kokonaismäärä. Voit tehdä tämän käyttämällä kaavaa `COUNT(Total.Page.Amount.Result)`. 
- Laske kokonaismäärä tapahtumille, jotka on käsiteltävä perustuen `model.CommodityRecord`-sidontaan, joka on määritetty **Raporttirivit**-komponentille. Voit tehdä tämän käyttämällä kaavaa `COUNT(model.CommodityRecord)`.
- Vertaa kahta numeroa viimeisen sivun tunnistusta varten. Kun molemmat arvot ovat yhtä suuret, viimeinen sivu muodostetaan.

> [!NOTE]
> Tätä menetelmää kannattaa käyttää vain, jos **Käytössä**-ominaisuus **Raporttirivit**-komponentissa ei sisällä kaavaa, joka voisi palauttaa arvon [Epätosi](er-formula-supported-data-types-primitive.md#boolean) suorituksen aikana jollekin toistettavalle [tietueelle](er-formula-supported-data-types-composite.md#record) sidotussa [Tietueluettelossa](er-formula-supported-data-types-composite.md#record-list).

## <a name="additional-resources"></a>Lisäresurssit

- [Konfiguraatioiden suunnitteleminen asiakirjojen luomiseksi Excel-muodossa](er-fillable-excel.md)
- [DATA COLLECTION -tietolähteiden käyttäminen sähköisissä raportoinnin (ER) muodoissa](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
