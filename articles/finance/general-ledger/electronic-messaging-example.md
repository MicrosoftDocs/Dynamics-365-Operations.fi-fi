---
title: Excel-raportin luovan yksinkertaisen ER-vientimuodon kutsuvan käsittelyn määrittäminen ja suorittaminen
description: Tässä artikkelissa on esimerkki, joka näyttää miten määrittää ja käyttää sähköisiä sanomia.
author: AdamTrukawka
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.custom: ''
ms.search.form: ''
ms.openlocfilehash: 6090c45a98b672f718f89fc1d2e1c060498bb8a0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279331"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Excel-raportin luovan yksinkertaisen ER-vientimuodon kutsuvan käsittelyn määrittäminen ja suorittaminen

[!include [banner](../includes/banner.md)]

Kun olet luonut ER-muodon, yhdistänyt sen tietolähteisiin ja viimeistellyt sen, voit suorittaa sen **Sähköinen raportointi** -työtilasta. Kun raportti on luotu, voit tallentaa sen paikallisesti.

Jos haluat hallita seuraavia raportointiprosessin ominaisuuksia, määritä sähköisten sanomien käsittely:

- Raportin luonutta henkilöä koskevien tietojen kirjaaminen.
- Raportin luontiajankohtaa koskevien tietojen kirjaaminen.
- Edellisinä kausina luotujen raporttien tallentaminen.

Seuraava esimerkki näyttää, miten voi määrittää sähköiset sanomat luomaan raportin, joka perustuu Microsoft Excelin ER-vientimuotoon. Jos haluat toimia tämän esimerkin mukaisesti, Excelin ER-vientimuodon on oltava jo luotuna, yhdistettynä tietolähteisiin ja viimeisteltynä. Lisäksi numerosarja on oltava jo määritetty sähköisille sanomille.

Kun muodostat käsittelyn, määritettävät käsittelyn toiminnot ja tilat kannattaa määrittää ensin. Seuraava kuva näyttää tämän esimerkin käsittelytavan.

![Käsittelymalli](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Sanomien tilojen luominen

1. Valitse **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sanomien tilat**.
2. Luo seuraavat sanomien tilat:

    - Uusi
    - Valmisteltu
    - Luotu

    ![Sanomien tilat](media/message-statuses.png)

3. Valitse **Uusi**-tilan riviltä **Salli poistaminen** -valintaruutu, jolloin käyttäjät voivat poistaa tässä tilassa olevia sanomia.

## <a name="create-additional-fields"></a>Lisäkenttien luominen

1. Valitse **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Lisäkentät**.
2. Lisää lisäkenttä ja sen arvot.
3. Käyttäjät voivat muokata kenttään, jos määrität **Käyttäjän muokkaus** -asetukseksi **Kyllä**.

![Lisäkentät](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Sanoman käsittelytoimintojen luominen

Tässä esimerkissä luot seuraavat sanomien käsittelytoiminnot:

- **Luo viesti**
- **Päivitä tilaksi Valmisteltu**
- **Luo raportti**
- **Päivitä alkuperäiseen tilaan** (valinnainen)

Luo toiminnot noudattamalla näitä ohjeita.

1. Valitse **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sanoman käsittelytoiminnot**.
2. Luo toiminto, jonka nimi on **Luo viesti**. Valitse **Yleinen**-pikavälilehden **Toimintotyyppi**-kentässä **Luo viesti**.
3. Luo toiminto, jonka nimi on **Päivitä tilaksi Valmisteltu**, ja määritä seuraavat kentät:

    - Valitse **Yleinen**-pikavälilehden **Toimintotyyppi**-kentässä **Viestitason käyttäjän käsittely**.
    - Valitse **Alkuperäiset tilat** -pikavälilehden **Sanoman tila** -kentässä **Uusi**.
    - Valitse **Tulostilat**-pikavälilehden **Sanoman tila** -kentässä **Valmisteltu**. Anna **Vastaustyyppi**-kentässä **Suoritettu onnistuneesti**.

4. Luo toiminto, jonka nimi on **Luo raportti**, ja määritä seuraavat kentät:

    - Valitse **Yleinen**-pikavälilehden **Toimintotyyppi**-kentässä **Sähköisen raportoinnin vienti**. Valitse **Muodon määritys** -kentässä ER-vientimuoto. Vaihtoehdot ovat **Excel**, **XML**, **JSON**, **Teksti** ja **Muu**.
    - Valitse **Alkuperäiset tilat** -pikavälilehden **Sanoman tila** -kentässä **Valmisteltu**.
    - Valitse **Tulostilat**-pikavälilehden **Sanoman tila** -kentässä **Luotu**. Anna **Vastaustyyppi**-kentässä **Suoritettu onnistuneesti**.

    ![Luo raporttitoiminto](media/generate-report-action.png)

5. Valinnainen: Jos haluat sallia käyttäjien luoda raportin useita kertoja, luo toiminto nimeltään **Päivitä alkuperäiseen tilaan** ja määritä seuraavat kentät:

    - Valitse **Yleinen**-pikavälilehden **Toimintotyyppi**-kentässä **Viestitason käyttäjän käsittely**.
    - Valitse **Alkuperäiset tilat**-pikavälilehden **Sanoman tila** -kentässä **Luotu**.
    - Lisää **Tulostilat**-pikavälilehdessä erillinen rivi kummallekin sanoman tilalle (**Valmisteltu** ja **Uusi**). Valitse kummankin rivin **Vastaustyyppi**-kentässä **Suoritettu onnistuneesti**.

## <a name="electronic-message-processing"></a>Sähköisen sanoman käsittely

Tässä esimerkissä kaikki toiminnot on määritettävä erikseen suoritettaviksi. Oletuksena on, että käyttäjä käynnistää jokaisen toiminnon.

1. Valitse **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sähköisen sanoman käsittely**.
2. Lisää käsittelyn tietue sekä kaikki aiemmin määritetyt toiminnot ja lisäkenttä.
3. Valinnainen: määritä **Käyttöoikeusroolit**-pikavälilehdessä käsittelyn käyttöoikeusroolit rajoittamaan tietyn raportoinnin käyttöä.
4. Valitse **Vero** \> **Kyselyt ja raportit** \> **Sähköiset sanomat** \> **Sähköiset sanomat**.
5. Luo sanoma valitsemalla **Uusi**. Voit lisätä tässä vaiheessa päivämäärät ja kuvauksen. Voit myös päivittää lisäkentän arvon tarvittaessa.

    ![Sähköisen sanoman luominen](media/create-electronic-message.png)

    **Toimintoloki**-pikavälilehden ruudukko täytetään automaattisesti kaikkien sanomassa suoritettujen toimintojen lokilla.

    Nyt voit poistaa tai päivittää sanoman tilan. 

6. Päivitä sanoman tila valitsemalla **Päivitä tila**. Valitse **Uusi tila** -kentässä ensin **Valmisteltu** ja sitten **OK**.

    ![Sanoman tilan päivittäminen](media/update-status.png)

    Sanoman tilaksi päivitetään **Valmisteltu**.

7. Luo raportti valitsemalla **Luo raportti**.

    Raportti luodaan sekä sanoman tila ja toimintoloki päivitetään.

8. Voit tarkastella luotua raporttia valitsemalla sivun oikeasta yläkulmasta **Liite**-painikkeen (paperiliitinsymboli).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
