---
title: Sähköisen raportoinnin muodon suunnitteleminen rivien pitämiseksi yhdessä samalla Excel-sivulla
description: Tässä ohjeaiheessa selitetään, miten suunnitellaan sähköisen raportoinnin (ER) muoto, joka pitää rivit samalla Microsoft Excel -sivulla.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.openlocfilehash: 06782a4933fb5c3e86ad436b853f207fd3d5cddb
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612345"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Sähköisen raportoinnin muodon suunnitteleminen rivien pitämiseksi yhdessä samalla Excel-sivulla

[!include [banner](../includes/banner.md)]


Tässä aiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin toiminnallisen konsultin roolin käyttäjä voi määrittää [sähköisen raportoinnin (ER)](general-electronic-reporting.md) [muodon](er-overview-components.md#format-component) lähtevien asiakirjojen muodostamiseksi Microsoft Excelissä ja asiakirjan sivuttamisen hallitsemiseksi siten, että luodut rivit pidetään samalla sivulla.

Tässä esimerkissä muokkaat Microsoftin tarjoamaa ER-muotoa, jota käytetään vapaatekstilaskujen tulostamiseen Excelissä. Muutosten avulla voit hallita luodun vapaatekstilaskuraportin sivutusta siten, että yksittäisen laskurivin kaikki rivit säilyvät mahdollisuuksien mukaan samalla sivulla.

Tässä ohjeaiheessa kuvatut toimenpiteet voidaan suorittaa **USMF**-yrityksessä. Koodausta ei tarvita.

Tässä esimerkissä luodaan pakollisia ER-[konfiguraatioita](general-electronic-reporting.md#Configuration) malliyritykselle **Litware, Inc**. Tarkista, että malliyrityksen **Litware, Inc.** (`http://www.litware.com`) konfiguraatiopalvelu luetteloitu ER-kehyksessä ja merkitty tilaan **Aktiivinen**. Jos tämä määrityspalvelu ei ole luettelossa tai jos se ei ole merkittynä **aktiiviseksi**, noudata ohjeaiheen [Konfiguraatiopalvelun luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheita.

## <a name="enter-a-new-free-text-invoice"></a>Uuden tekstimuotoisen laskun luonti

1. Lisää vapaatekstilasku noudattamalla kohdan [vapaatekstilaskun luonti](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) ohjeita.

    1. Lisää laskuun yksi rivi.
    2. Lisää laskuriville viisi huomautusta.

    ![Tarkistetaan laskurivin huomautukset Liitteet-sivulla.](./media/er-keep-excel-rows-together-notes.png)

2. Noudattamalla [Kopioi rivejä](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) -kohdan vaiheita voit luoda viisi lisälaskuriviä, jotka kopioivat edellisessä vaiheessa lisätyn laskurivin.

    ![Vapaatekstilaskun rivien tarkasteleminen vapaatekstilaskusivulla.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>Määritä ER-kehys

Seuraa vaiheita kohdassa [Määritä ER-kehys](er-quick-start2-customize-report.md#ConfigureFramework) luodaksesi ER-parametrien vähimmäisjoukon. Nämä asetukset on suoritettava, ennen kuin ER-kehystä käytetään normaalin ER-muodon mukautetun version suunnitteluun.

## <a name="import-the-standard-er-format-configuration"></a>Tuo ER-muodon vakiokonfiguraatio

Seuraa vaiheita kohdassa [Tuo ER-muodon vakiokonfiguraatio](er-quick-start2-customize-report.md#ImportERSolution1) lisätäksesi ER-vakiokonfiguraatiot nykyiseen Dynamics 365 Finance -ilmentymääsi. Tuo esimerkiksi **Vapaatekstilasku (Excel)** -muotokonfiguraation versio **252.116**. **Laskumallin** peruskonfiguraation perusversio **252** tuodaan automaattisesti tietovarastosta yhdessä vaaditun **Laskumallin määritys** -konfiguraation kanssa.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Määritä tulostuksenhallinta käyttämään ER-vakiomuotoa.

[Määritä tulostuksenhallinta](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) -kohdan vaiheiden avulla voit määrittää **Myyntireskontra**-moduulin tulostuksenhallinnan niin, että vapaatekstilaskujen tulostamiseen käytetään ER-vakiomuotoa.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Muotokohteen konfiguroiminen ER-vakiomuodolle

[Muotokohteen määrittäminen näytön esikatselua varten](er-quick-start1-new-solution.md#ConfigureDestination) -kohdan vaiheiden avulla voit määrittää ER-vakiomuodon ER-kohteen [Näyttö](er-destination-type-screen.md), jotta luodut raportit muunnetaan PDF-muotoon ja esikatseltaan uudessa selaimen välilehdessä.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Tulosta vapaatekstilasku käyttämällä ER-vakiomuotoa

1. Noudata [Tulosta vapaatekstilasku](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) -kohdan vaiheita, kun haluat käyttää ER-vakiomuotoa vapaatekstilaskuraportin tuottamiseen Excel-muodossa lisätylle laskulle.
2. Lataa luotu Excel-työkirja ja tarkista se Excel-työpöytäsovelluksessa.

    Huomaa, että laskun kuudes rivi alkaa raportin ensimmäiseltä sivulta ja jatkuu toisella sivulla. Viimeinen huomautus tulee näkyviin toisella sivulla, eikä ole selvää, että se kuuluu kuudenteen laskuriviin. Näin ollen laskurivin sisällön keskellä oleva sivunvaihto vaikeuttaa tiedoston lukemista.

    ![Tarkastellaan luodun vapaatekstilaskun sivutusta Excel-työpöytäsovelluksessa.](./media/er-keep-excel-rows-together-invoice1.gif)

Tämän ohjeaiheen muut toimenpiteet osoittavat, kuinka voit hienosäätää laskuraportin ulkoasua ja luettavuutta säätämällä ER-vakiomuotoa säilyttämällä yksittäisen laskurivin kaiken sisällön samalla sivulla.

## <a name="create-a-custom-format"></a>Luo mukautettu muoto

[Luo mukautettu muoto](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) -kohdan vaiheiden avulla voit johtaa muodon tuodusta ER-muodosta ja luoda ER-määrityksen **Vapaatekstilasku (Excel) – mukautettu**, jota voi muokata ja muuttaa.

## <a name="edit-the-custom-format"></a>Muokkaa mukautettua muotoa

1. Avaa johdettu ER-muoto muokkaamista varten ER-muodon suunnitteluohjelmassa noudattamalla kohdan [Mukautetun muodon luominen](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) ohjeita.
2. Laajenna **Muodon suunnittelija** -sivun muotokomponenttipuussa **Vapaatekstilasku \> Taulukko \> InvoiceLines**, ja valitse **InvoiceLines_Values**-komponentti.
3. Määritä **Muoto**-välilehdessä **Pidä rivit yhdessä** -kohdan arvoksi **Kyllä**.

    ![Pidä rivit yhdessä -vaihtoehdon määrittäminen muokattavalle ER-muodolle Muotosuunnittelu-sivulla.](./media/er-keep-excel-rows-together-format.png)

4. Valitse **Tallenna** ja sulje sivu.

## <a name="mark-the-custom-format-as-runnable"></a>Merkitse mukautettu muoto suoritettavaksi

Tee mukautetun ER-muodon muokatusta versiosta suoritettava noudattamalla [Merkitse mukautettu muoto suoritettavaksi](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) -kohdan vaiheita.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Määritä tulostuksenhallinta käyttämään mukautettua ER-muotoa.

[Määritä tulostuksenhallinta](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) -kohdan vaiheiden avulla voit määrittää **Myyntireskontra**-moduulin tulostuksenhallinnan niin, että vapaatekstilaskujen tulostamiseen käytetään mukautettua ER-muotoa.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Muotokohteen konfiguroiminen mukautetulle ER-muodolle

[Muotokohteen määrittäminen näytön esikatselua varten](er-quick-start1-new-solution.md#ConfigureDestination) -kohdan vaiheiden avulla voit määrittää mukautetun ER-muodon ER-kohteen **Näyttö**, jotta luodut raportit muunnetaan PDF-muotoon ja esikatsellaan uudessa selaimen välilehdessä.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Tulosta vapaatekstilasku käyttämällä mukautettua ER-muotoa

1. Noudata [Tulosta vapaatekstilasku](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) -kohdan vaiheita, kun haluat käyttää mukautettua ER-muotoa vapaatekstilaskuraportin tuottamiseen Excel-muodossa lisätylle laskulle.
2. Lataa luotu Excel-työkirja ja tarkista se Excel-työpöytäsovelluksessa.

    Huomaa, että laskun kuudes rivi alkaa toisella sivulla, ja kaikki tätä laskuriviä vastaavat Excel-rivit näkyvät yhdessä kyseisellä sivulla.

    ![Tarkastellaan luodun vapaatekstilaskun päivitettyä sivutusta Excel-työpöytäsovelluksessa.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Lisäresurssit

[Konfiguraatioiden suunnitteleminen asiakirjojen luomiseksi Excel-muodossa](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
