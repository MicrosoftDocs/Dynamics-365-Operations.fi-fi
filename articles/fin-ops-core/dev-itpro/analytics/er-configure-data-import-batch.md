---
title: Tietojen tuominen manuaalisesti valituista tiedostoista erätilassa
description: Tässä artikkelissa kerrotaan, miten tiedot tuodaan manuaalisesti valituista tiedostoista erätilassa.
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 2dec838439876fd8e57ea4a7078d97267e5ea1a2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890180"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Tietojen tuominen manuaalisesti valituista tiedostoista erätilassa

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Kun haluat käyttää [sähköisen raportoinnin (ER)](general-electronic-reporting.md) kehystä tietojen tuomiseen manuaalisesti valituista saapuvista tiedostoista erätilassa, määritä tuontia tukeva ER-[muoto](er-overview-components.md#format-component). Suorita sitten **Kohteeseen**-tyyppisen [mallimäärityksen](er-overview-components.md#model-mapping-component), joka käyttää tätä muotoa tietolähteenä. Tietojen tuomiseksi selaa tiedostoon, jonka haluat tuoda, ja valitse se manuaalisesti. 

Uusi sähköisen raportoinnin ominaisuus, joka tukee tietojen tuomista erätilassa, mahdollistaa tämän prosessin määrityksen automaattiseksi. Voit käyttää ER-konfiguraatioita tietojen tuomiseen ajoittamalla uuden erätyön ER-käyttöliittymästä.

Tässä artikkelissa kerrotaan, miten suoritetaan tietojen tuonti manuaalisesti valitusta tiedostosta erätilassa. Esimerkissä käytetään toimittajatapahtumia liiketoimintatietoina. Näiden esimerkkien vaiheet voidaan suorittaa **USMF**-yrityksessä. Koodausta ei tarvita.

## <a name="prerequisites"></a>Edellytykset

Tämän artikkelin esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:

- Jokin seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- Sähköisen raportoinnin (ER) muoto ja mallin määritykset 1099-maksuille

### <a name="create-the-required-er-configurations"></a>Luo tarvittavat ER-konfiguraatiot

Voit luoda tarvittavat ER-konfiguraatiot ja hankkia muut edellytykset seuraavasti:

- Toista **ER -tuo tiedot Microsoft Excel -tiedostosta** -tehtäväoppaat, jotka ovat osa, **7.5.4.3 Acquire/Develop IT service/solution components (10677)** -liiketoimintaprosessia. Näissä tehtäväoppaissa selitetään ER-konfiguraatioiden suunnittelu ja käyttö, jotta voit vuorovaikutteisesti tuoda toimittajatapahtumia Microsoft Excel -tiedostoista. Lisätietoja on kohdassa [Saapuvien asiakirjojen jäsennys Excel-muodossa](parse-incoming-documents-excel.md).
- Tee esimerkit valmiiksi kohteessa [Määritä tietojen tuonti SharePointista](er-configure-data-import-sharepoint.md). Näissä esimerkeissä selitetään ER-konfiguraatioiden suunnittelu ja käyttö, jotta voit vuorovaikutteisesti tuoda toimittajatapahtumia Excel-tiedostoista, jotka on tallennettu SharePoint-kansioon.

### <a name="download-the-required-er-configurations"></a>Lataa tarvittavat ER-konfiguraatiot

1. Lataa seuraavat ER-konfiguraatiot ja tallenna ne paikallisesti.

    | Sisällön kuvaus | Tiedosto |
    |---------------------|------|
    | **1099 maksumalli** – ER-tietomallimääritys | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Toimittajatapahtumien tuomiseksi (Excelistä)** – ER-muotokonfiguraatio | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Käytä [Lataa XML-tiedostosta](er-defer-sequence-element.md#import-the-sample-er-configurations) -asetusta tuodaksesi ladatut ER-konfiguraatiot Dynamics 365 Finance -esiintymään seuraavassa järjestyksessä:

    1. ER-tietomallin konfigurointi
    2. ER-muodon konfigurointi

### <a name="download-the-required-excel-files"></a>Tarvittavien Excel-tiedostojen lataaminen

- Lataa seuraava mallitietojoukko ja tallenna se paikallisesti.

    | Sisällön kuvaus | Tiedosto |
    |---------------------|------|
    | Saapuva **1099import-data.xlsx**-tiedosto, joka sisältää esimerkkitiedot tuontia varten | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Edellytysten tarkistaminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Tarkista **Konfiguroinnit**-sivulla valmisteltu ER-ratkaisu tietojen tuontiin erätilassa.
3. Tarkista **Toimittajatapahtumien tuomiseksi (Excelistä)** -muotokonfiguraatio.

    - Tämän konfiguraation muotokomponentti on suunniteltu jäsentämään saapuvan Excel-tiedoston.
    - Tämän konfiguraation mallimäärityskomponenttia käytetään perustietomallin täyttämiseen käyttämällä jäsennetyn Excel-tiedoston tietoja.

    ![ER-muotomääritys tietojen tuomista varten erätilassa ER-käyttöliittymästä.](./media/er-configure-data-import-batch-configurations-1.png)

4. Tarkista **1099 maksumalli** -tietomallimääritys.

    - Tämän konfiguraation mallikomponentti edustaa sen tietomallin rakennetta, jota käytetään tietojen välittämiseen suoritettavien ER-komponenttien välillä.
    - Tämän konfiguraation mallimäärityskomponenttia käytetään tietojen keruussa suoritetusta muotokomponentista ja sen jälkeen sovellustaulujen päivittämiseen.

    ![ER-tietomallimääritys tietojen tuomista varten erätilassa ER-käyttöliittymästä.](./media/er-configure-data-import-batch-configurations-2.png)

5. Avaa Excelissä **1099import-data.xlsx**-tiedosto.

    ![Excel-mallitiedosto, joka sisältää tiedot erätilassa tuontia varten.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Ota käyttöön erätietojen tuonti ER:lle käyttöliittymästä

1. Valitse **Järjestelmänvalvoja** \> **Työtilat** \> **Ominaisuuksien hallinta**.
2. Valitse **Ominaisuuksien hallinta** -työtilassa **Suorita ladattujen asiakirjojen sähköisen raportoinnin tuominen erätoimintona** -toiminto ja valitse sitten **Ota käyttöön nyt**.

## <a name="import-data-from-manually-selected-excel-files"></a>Tuo tiedot manuaalisesti valituista Excel-tiedostoista

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivulla **1099 maksumalli** -tietomallimääritys.
3. Valitse **Konfiguraatiokomponentit** -pikavälilehdessä **1099-tapahtumien manuaaliseen tuontiin** -linkki.
4. **Määritys mallista tietolähteeseen** -sivulla **1099-tapahtumien manuaaliseen tuontiin** -mallimääritys on esivalittu. Valitse **Suorita**.
5. Valitse **Parametrit**-välilehdessä **Selaa**. Etsi ja valitse **1099import-data.xlsx** -tiedosto ja valitse **OK**.
6. Kirjoita **Kirjoita tositetunnus** -kenttään **V-00001**.
7. Määritä **Suorita taustalla** -välilehdessä **Erän käsittely** -kohdan arvoksi **Kyllä**.

    Huomaa, että **Tehtävän kuvaus** -kentän arvoksi on asetettu **1099-tapahtumien manuaaliseen tuontiin -mallimäärityksen suoritus, konfiguraatio 1099 maksumalli**. Tämä arvo ilmaisee, että valitun mallimäärityksen suoritus ajoitetaan uutena erätyönä.

    ![Tietojen tuonnin tietojen määritys erätilassa Sähköisen raportin parametrit -valintaikkunassa.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Valitse **OK**. Sanoma ilmoittaa, että uusi erätyö on ajoitettu.

    ![Uuden ajoitetun erätyön sanoma Malli tietolähteen yhdistämismääritystä varten -sivulla.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Tietojen tuonnin tulosten tarkasteleminen Erätyö-sivulla

1. Siirry kohtaan **Yleinen** \> **Kyselyt** \> **Erätyöt** \> **Omat erätyöt**.
2. Etsi ajoitettu erä suodattamalla **Erätyö**-sivulla luetteloa ja valitse se.
3. Tarkista työn tiedot valitsemalla **Työtunnus**-linkki.
4. Valitse **Erätehtävät**-pikavälilehdellä **Loki**.

    ![Erätyö-sivun Loki-painike.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Suorituksen tietojen tarkasteleminen.

    ![Ajoitetun erätyön suoritusloki Erätyö-sivulla.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Tietojen tuontiparametrien muuttaminen

Kun erä on ajoitettu eikä sitä ole vielä suoritettu, voit muuttaa ajoitetun tietojen tuonnin parametreja.

1. Siirry kohtaan **Yleinen** \> **Kyselyt** \> **Erätyöt** \> **Omat erätyöt**.
2. Etsi ajoitettu erä suodattamalla **Erätyö**-sivulla luetteloa ja valitse se.
3. Valitse **Muutoksen tila**.
4. Valitse **Valitse uusi tila** -valintaikkunassa **Pidätä** ja valitse sitten **OK**.
5. Näet työn tiedot valitsemalla **Työtunnus**-linkin.
6. Valitse **Erätehtävät**-pikavälilehdellä **Parametrit**.
7. Toimi **Sähköisen raportin parametrit** -valintaikkunassa seuraavasti:

    1. Valitse vaihtoehtoinen tiedosto tietojen tuomista varten valitsemalla **Selaa**.
    2. Valitse **Kirjoita tositetunnus**, jos haluat muuttaa tositenumeroa toimittajatapahtumien tuomista varten.

        ![Ajoitetun erätyön tietojen tuomisen parametrien muuttaminen Sähköisen raportin parametrit -valintaikkunassa.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Valitse **OK**.

8. Varmista, että erä on yhä valittuna, ja valitse sitten **Muuta tilaa** uudelleen.
9. Valitse **Valitse uusi tila** -valintaikkunassa **Odottaa** ja valitse sitten **OK**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Tietojen tuonnin tulosten tarkasteleminen ER-lähdesivulla

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin lähde**.
2. Valitse **Toimittajatapahtumien tuomiseksi (Excelistä)** -tietue, joka luotiin automaattisesti tietojen tuonnin yhteydessä.

    ![Toimittajatapahtumien tuomiseksi (Excelistä) -määrityksen tietue sähköisen raportoinnin lähdesivulla.](./media/er-configure-data-import-batch-files-source-1.png)

3. Valitse **Tiedostojen tilat lähteitä varten**.
4. Tarkista tuontitiedot **Tiedostot**- ja **Tuontimuodon lähteiden lokit** -pikavälilehdissä.
5. Valitse tietue **Tiedostot**-pikavälilehdessä. Huomaa, että tuotu tiedosto on liitetty tähän tietueeseen.

    ![Tuotu tiedosto, joka on liitetty tietueeseen Tiedostojen tilat lähteitä varten -sivulla.](./media/er-configure-data-import-batch-files-source-2.png)

6. Tarkista tuotu tiedosto valitsemalla **Liitteet**.

    ![Tuotu tiedosto Asiakirjanäkymä -sivulla.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Jos haluat säilyttää nämä liitteet, ER-kehys käyttää asiakirjatyyppiä, joka on [määritetty](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) nykyiselle yritykselle ER-parametrien **Muut**-kentässä.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Tietojen tuonnin tulosten tarkasteleminen Toimittajien tilitykset valmisteveroja (1099) varten -sivulla

1. Valitse **Ostoreskontra** \> **Kausittaiset tehtävät** \> **Valmistevero (1099)** \> **Toimittajien tilitykset valmisteveroja (1099) varten**.
2. Syötä **Alkamispäivä**-kenttään **12/31/2017** (31.12.2017).
3. Valitse **Manuaaliset 1099-tapahtumat**.

    ![Tuodut toimittajatapahtumat Valmisteverotapahtumat (1099) -sivulla.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
