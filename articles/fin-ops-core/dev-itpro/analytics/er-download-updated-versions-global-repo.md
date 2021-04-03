---
title: Tuo päivitetyt versiot sähköisen raportoinnin konfiguraatioista
description: Tässä ohjeaiheessa selitetään, miten sähköisen raportoinnin (ER) konfiguraatioiden päivitetyt versiot tuodaan Configuration Service -palvelun yleisestä säilöstä.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 0c65315c4fa6a42b4bbb0d008b58f8df9cc0ea3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561875"
---
# <a name="import-updated-versions-of-er-configurations"></a>Tuo päivitetyt versiot sähköisen raportoinnin konfiguraatioista

[!include [banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) [säilöjä](general-electronic-reporting.md#Repository) käytetään [sähköisen raportoinnin konfiguraatioiden](general-electronic-reporting.md#Configuration) jakamiseen. Voit [tuoda](download-electronic-reporting-configuration-lcs.md) sähköisen raportoinnin konfiguraatioita eri säilöistä omaan Microsoft Dynamics 365 Finance -esiintymääsi. Kun tuot sähköisen raportoinnin konfiguraatioita, [konfiguraation lähteet](general-electronic-reporting.md#Provider) voivat julkaista uusia [versioita](general-electronic-reporting.md#component-versioning) säilöistä, jotta ne voidaan jakaa.

Tässä ohjeaiheessa selitetään, miten sähköisen raportoinnin konfiguraatioiden päivitetyt versiot tuodaan Configuration Service -palvelun yleisestä säilöstä. Lisätietoja on kohdassa [Microsoft Dynamics 365 for Finance and Operations -Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Tarkasta saatavilla olevat päivitetyt versiot

1. Kirjaudu Financeen yhdellä seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Tuo konfiguraatioversioiden päivitykset**-ruutu.

    ![Lokalisoinnin konfiguraatiot -sivu](./media/er-download-updated-versions-global-repo1.png)

4. Valitse **Tuo sähköisen raportoinnin konfiguraatioversioiden päivitykset** -valintaikkunan **Suoritustila** -kentässä **Näytä vain saatavilla olevat päivitykset**. Valitse sitten **OK**. 

    ![Suoritustila-kentän asetus on Näytä vain saatavilla olevat päivitykset](./media/er-download-updated-versions-global-repo2.png)

5. Tarkista saamasi sanomat. Nämä sanomat antavat seuraavia tietoja sähköisen raportoinnin konfiguraatioista nykyisessä Finance-esiintymässä ja vertaa niitä yleisen säilön sisältöön:

    - Sähköisen raportoinnin konfiguraatioiden kokonaismäärä
    - Sähköisen raportoinnin konfiguraatiot, joita ei ole yleisessä säilössä
    - Sähköisen raportoinnin konfiguraatiot, joiden viimeisin versio on jo saatavilla nykyisessä Finance-esiintymässä (katso täydellinen luettelo näistä sähköisen raportoinnin konfiguraatioista valitsemalla **Sanoman tiedot** -linkki.)

        ![Seuraavien konfiguraatioiden viimeisimmät versiot on jo tuotu -sanoma ja sanoman tiedot](./media/er-download-updated-versions-global-repo3.png)

    - Sähköisen raportoinnin konfiguraatiot, joiden viimeisin versio on saatavilla yleisessä säilössä ja voidaan tuoda nykyiseen Finance-esiintymään (katso täydellinen luettelo näistä sähköisen raportoinnin konfiguraatioista valitsemalla **Sanoman tiedot** -linkki.)

        ![Saatavilla olevat päivitykset -sanoma ja sanoman tiedot](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Päivitettyjen versioiden tuonti saatavilla

1. Kirjaudu Financeen yhdellä seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Tuo konfiguraatioversioiden päivitykset**-ruutu.
4. Valitse **Tuo sähköisen raportoinnin konfiguraatioversioiden päivitykset** -valintaikkunan **Suoritustila**-kentässä **Tuo viimeisimmät päivitykset** tuodaksesi sähköisen raportoinnin konfiguraatioiden viimeisimmät versiot yleisestä säilöstä nykyiseen Finance-esiintymään.
5. Voit ajastaa erätyön tuonnille **Suorita taustalla** -pikavälilehdessä määrittämällä **Eräkäsittely**-asetukseksi **Kyllä**. Jos haluat toistaa tuonnin säännöllisesti, määritä tarvittava toistuminen.

    ![Suoritustila-kentän asetukseksi on määritetty Tuo viimeisimmät päivitykset](./media/er-download-updated-versions-global-repo5.png)

6. Valitse **OK**.
7. Jos haluat tietää, mitä konfiguraatioversioita on tuotu, noudata jotakin näistä ohjeista:

    - Jos suoritat tuonnin interaktiivisesti erätyön käyttämisen sijaan, tarkista saamasi sanomat.

        ![Interaktiivisen tuonnin suorittamisen aikana saadut sanomat](./media/er-download-updated-versions-global-repo6.png)

    - Jos suoritat tuonnin erätilassa, noudata näitä ohjeita:

        1. Siirry kohtaan **Yleinen** \> **Kyselyt** \> **Erätyöt** \> **Omat erätyöt**.
        2. Etsi ja valitse **Tuo sähköisen raportoinnin konfiguraatioversioiden päivitykset** -työ ja valitse sitten toimintoruudun **Erätyö**-välilehdessä **Erätyöhistoria** nähdäksesi työhistorian.
        3. Valitse **Erätyöhistoria**-sivulla **Loki**. Valitse sitten saamassasi sanomassa **Sanoman tiedot** -linkki nähdäksesi työn lokin.

        ![Työloki](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Emme suosittele ajoittamaan toistuvaa erätyötä tuomaan sähköisen raportoinnin konfiguraatioiden päivitettyjä versioita suoraan yleisestä säilöstä tuotantoympäristöön, sillä tuodut versiot tulevat välittömästi saataville. Käytä sen sijaan tätä lähestymistapaa ottaaksesi sähköisen raportoinnin konfiguraatioiden versiot käyttöön eristysympäristössä. Tällöin ne voidaan arvioida eristysympäristössä ennen niiden käyttöönottoa tuotantoympäristössä.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
- [Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]