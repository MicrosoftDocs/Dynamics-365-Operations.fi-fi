---
title: Sähköisessä raportissa luotavien isokokoisten asiakirjojen pakkaaminen
description: Tässä artikkelissa selitetään, miten sähköisen raportoinnin (ER) muodon luomia isokokoisia asiakirjoja pakataan.
author: kfend
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 58771
ms.assetid: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
ms.openlocfilehash: ebdd84cdf39e21bf3d4721b1f1545b29fe38440b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273275"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Sähköisessä raportissa luotavien isokokoisten asiakirjojen pakkaaminen 

[!include [banner](../includes/banner.md)]

Voit määrittää tapahtumatietoja lähtevän asiakirjan luomista varten noutavan ratkaisun käyttämällä [Sähköisen raportoinnin (ER) kehystä](general-electronic-reporting.md). Tämä luotu tiedosto voi olla melko suuri. Kun tällainen asiakirja luodaan, [Application Object Server (AOS)](../dev-tools/access-instances.md#location-of-packages-source-code-and-other-aos-configurations) -muistia käytetään sen säilyttämiseen. Jossakin vaiheessa tiedosto on ladattava Microsoft Dynamics 365 Finance -sovelluksesta. Tällä hetkellä sähköisessä raportoinnissa luotavan yksittäisen asiakirjan koko on rajoitettu 2 gigatavuun (Gt). Lisäksi Finance [rajoittaa](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3) tällä hetkellä ladatun tiedoston koon 1 gigatavuun. Siksi sinun on konfiguroitava ER-ratkaisu, joka pienentää todennäköisyyttä, että nämä rajoitukset ylittyvät ja poikkeukset **Tietovirta oli liian pitkä** tai **Yli- tai alivuoto aritmeettisessa toiminnassa**.

Kun määrität ratkaisun, voit muokata ER-muotoa toimintojen suunnitteluohjelmassa lisäämällä **Kansio**-tyypin pääelementin sen jonkin sisäkkäisen elementin luoman sisällön pakkaamiseksi. Pakkauksessa sovelletaan just in time -periaatetta, jotta muistin käyttöä voidaan vähentää ja ladattavan tiedoston kokoa pienentää.

> [!NOTE]
> Tiedoston pakkaaminen vaatii lisäosuuden suoritinkäyttöä.

Saat lisätietoja tästä menetelmästä suorittamalla tässä artikkelissa olevan esimerkin.

## <a name="example-compress-an-outbound-document"></a>Esimerkki: Lähtevän asiakirjan pakkaaminen

Tässä esimerkissä näytetään, miten käyttäjä, jolla on rooli **Järjestelmänvalvoja** tai **Sähköisen raportoinnin toiminnallinen konsultti** voi määrittää ER-muodon luodun asiakirjan pakkaamista varten.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän artikkelin menettelyt loppuun, seuraavien vaiheiden on oltava suoritettuna.

1. [Aktivoi määrityslähde](er-defer-xml-element.md#activate-a-configuration-provider).
2. [ER-mallimääritysten tuonti](er-defer-xml-element.md#import-the-sample-er-configurations)
3. [Tuodun muodon tarkistaminen](er-defer-xml-element.md#review-the-imported-format)

> [!NOTE]
> Tällä hetkellä muotorakenne alkaa **Tiedosto**-tyypin **Raportti**-elementistä ja sisältää XML-elementtejä. Tämän vuoksi lähtevä asiakirja luodaan XML-muodossa eikä pakkausta käytetä.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>ER-muodon luominen pakkaamattoman asiakirjan saamista varten

1. [Tuodun muodon suorittaminen](er-defer-xml-element.md#run-the-imported-format)
2. Huomaa, että luodun asiakirjan koko XML-muodossa on 3 kilotavua (kt).

    ![Pakkaamattoman lähtevän asiakirjan esikatselu.](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Muodon muokkaaminen luodun tulosteen pakkaamiseksi

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun määrityspuu ja laajenna **Malli lykättyjen elementtien oppimiseen**.
3. Valitse **Muoto lykättyjen XML-elementtien oppimiseen** -määritys.
4. Muokkaa muotorakennetta valitsemalla **Suunnittelutoiminto**.
5. Valitse **Muodon suunnittelija** -sivun **Muoto**-välilehdessä **Lisää juuri** lisätäksesi juurimuotoelementin.
6. Valitse **Lisää**-valintaikkunassa **Yhteinen\\Kansio**.
7. Vahvista uuden juurielementin lisääminen valitsemalla **OK**.
8. Valitse **Tallenna**.

> [!NOTE]
> Muotorakenne alkaa **Kansio**-tyypin elementistä. Tämä elementti luo tulosteen pakattuna tiedostona (zip). Kun **Raportti**-elementin luoma asiakirja sijoitetaan lähtevään zip-tiedostoon, sen sisältö pakataan lähtevän tiedoston koon pienentämisen tarkoituksessa.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>ER-muodon luominen pakatun asiakirjan saamista varten

1. Vallitse **Muodon suunnittelu** -sivulla **Suorita**.
2. Lataa verkkoselaimen tarjoama zip-tiedosto ja avaa se tarkistusta varten.
3. Huomaa, että luodun asiakirjan koko ZIP-muodossa on 1 kilotavua.

    > [!NOTE] 
    > Tämän zip-tiedoston sisältämän XML-tiedoston pakkaussuhde on 87 prosenttia. Pakkaussuhde määräytyy pakattavien tietojen mukaan.

    ![Pakatun lähtevän asiakirjan esikatselu.](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Jos ER-[kohde](electronic-reporting-destinations.md) on määritetty tulosteen luovan muotoelementin (tässä esimerkissä **Raportti**-elementin) osalta, tulosteen pakkaus ohitetaan.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)

[Sähköisen raportoinnin muotojen XML-elementtien suorittamisen lykkääminen](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
