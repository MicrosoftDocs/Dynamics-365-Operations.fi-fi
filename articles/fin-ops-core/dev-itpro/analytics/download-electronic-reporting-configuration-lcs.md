---
title: Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta
description: Tässä artikkelissa neuvotaan, miten sähköisen raportoinnin (ER) konfiguraatiot ladataan Microsoft Dynamics Lifecycle Services -palvelusta (LCS).
author: kfend
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace
ms.openlocfilehash: f48dd14bc3009550d78bd71db030c172d2ef6450
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277813"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten [sähköisen raportoinnin konfiguraatioiden](general-electronic-reporting.md#Configuration) uusin versio ladataan [jaetusta resurssikirjastosta](../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.

> [!IMPORTANT]
> Lifecycle Services (LCS) -palveluiden käyttö sähköisen raportoinnin (ER) konfiguraatioiden tallennusvarastona on [vanhentunut](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Lue lisätietoja kohdasta [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) -tallennustilan vanhentuminen](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

1. Kirjaudu sovellukseen yhdellä seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

2. Valitse **Organisaation hallinto** &gt; **Työtilat** &gt; **Sähköinen raportointi**.
3. Valitse **Konfiguraation lähteet** -osassa **Microsoft**-ruutu.
4. Valitse **Microsoft**-ruudusta **Säilöt**.

    [![Microsoft-ruutu lokalisointien konfiguraatioiden sivulla.](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **LCS**. Jos säilöä ei ole ruudukossa, noudata seuraavia ohjeita:

    1. Valitse säilö valitsemalla **Lisää**.
    2. Valitse säilön tyypiksi **LCS**.
    3. Valitse **Luo säilö**.
    4. Jos järjestelmä pyytää lupaa, noudata näyttöön tulevia ohjeita.
    5. Kirjoita säilön nimi ja kuvaus.
    6. Valitse **OK**, jos haluat vahvistaa uuden säilön luonnin.
    7. Valitse ruudukossa uusi **LCS**-tyypin säilö.

6. Valitsemalla **Avaa** voit tarkastella valitun säilön ER-konfiguraatioita.

    [![Konfiguraatiosäilöjen sivu.](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Jos et voi käyttää LCS-säilöä ja ladata konfiguraatioita LCS:n jaetusta resurssikirjastosta, voit ladata ne sen sijaan [yleisestä säilöstä](er-download-configurations-global-repo.md).

7. Valitse vasemman ruudun konfiguraatioiden puurakenteessa vaadittu sähköisen raportoinnin konfiguraatio.
8. Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation tarvittava versio.
9. Valitse **Tuo** ja lataa valittu versio LCS-palvelusta nykyiseen esiintymään.

    > [!NOTE]
    > **Tuo**-painike ei ole käytettävissä ER-määritysversioille, jotka on jo ladattu nykyiseen esiintymään.

    [![Konfiguraatiosäilön sivu.](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> ER-asetusten mukaan määritykset tarkistetaan tuonnin jälkeen. Voit saada ilmoituksia havaituista epäyhtenäisyysongelmista. Kyseiset ongelmat on ratkaistava, ennen kuin voit käyttää tuotua konfiguraatioversiota. Lisätietoja saat tähän artikkeliin liittyvistä aiheista.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
