---
title: RSC:n tai yleisen säilön ER-määritysten jakaminen ulkoisten organisaatioiden kanssa
description: Tässä artikkelissa käsitellään Microsoft Regulatory Configuration Servicesin tai yleisen säilön sähköisen raportoinnin (ER) määritysten jakamista suoraan ulkoisten organisaatioiden kanssa.
author: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
ms.openlocfilehash: d9400ffcede9924a01391a433b570651d3f0c5e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284812"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>Microsoft Regulatory Configuration Servicesin yleisen säilön sähköisen raportoinnin (ER) määritysten jakaminen ulkoisten organisaatioiden kanssa

[!include [banner](../includes/banner.md)]

Microsoft Regulatory Configuration Servicesiä (RCS) voi käyttää sähköisen raportoinnin (ER) määritysten jakamiseen ja niiden julkaisemiseen ulkoisille organisaatioille.

Seuraavissa menettelyissä selitetään, miten RCS-käyttäjä voi jakaa RCS-esiintymässä määritetyn ER-määrityksen version ulkoisen organisaation kanssa. Seuraavat ennakkoedellytykset on oltava suoritettuna, ennen kuin kyseiset menetelmät voidaan suorittaa.

- RCS-esiintymän käyttäminen.
- Aktiivisen määrityspalvelun luonti. Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- Luo ja lataa ER-määrityksen uusi versio. Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) määrityksen uuden version luominen ja lataaminen](rcs-global-repo-upload.md).

Lisäksi on varmistettava, että RCS-ympäristö on valmisteltu yritykseen.

1. Valitse talous- ja toimintosovelluksessa **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Jos yritykseen ei ole valmisteltu RCS-ympäristöä, valitse **Regulatory Services – ulkoinen määritys** -linkki ja valmistele sitten sellainen ohjeiden mukaisesti.

Jos yritykseen on valmisteltu RCS-ympäristö, siirry siihen sivun URL-osoitteen avulla valitsemalla kirjautumisvaihtoehto.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Jaettavan määrityksen tarkistaminen

Tarkista seuraavien ohjeiden avulla, että jaettava määritys on jo ladattu yleiseen säilöön.

1. Valitse **Sähköinen raportointi** -työtilassa oman määrityspalvelun **Säilöt**.

    ![Konfiguraation tarjoajat.](media/1_RCS_Repo_for_config_provider.JPG)

2. Valitse **Yleinen säilö** \> **Avaa**.
3. Hae jaettava määritys. Voit tarkentaa hakua suodatinkentän avulla. Jos määritystä ei löydy yleisestä säilöstä, noudata ohjeita kohdassa [Sähköisen raportoinnin (ER) määrityksen uuden version luominen ja lataaminen](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>ER-määritysten jakaminen ulkoisten organisaatioiden kanssa

Kun määritys on luotu määrityspalvelussa, voit jakaa sen suoraan ulkoisten organisaatioiden kanssa käyttämällä **Yleinen määrityssäilö** -sivun **Jaettu**-pikavälilehteä.

1. Valitse **Sähköinen raportointi** -työtilassa oman määrityspalvelun **Säilöt**.
2. Valitse **Yleinen säilö** \> **Avaa**. 
3. Valitse jaettava määritys.
4. Valitse **Jaettu**-pikavälilehdessä **Organisaatio**.

    ![Jaettu-pikavälilehti.](media/1_RCS_Repo_for_Share_with_org.JPG)

5. Anna valintaikkunassa ulkoisen organisaation toimialueen nimi ja valitse sitten **OK**.

    ![Jaa määritysversio ulkoisen organisaation kanssa -valintaikkuna.](media/1_RCS_Repo_for_Share_with_form.JPG)

Määritys jaetaan ulkoisen organisaation kanssa, ja se on kyseisen organisaation käytettävissä yleisessä säilössä. Se voidaan tuoda sieltä organisaation RCS-esiintymään tai talous- ja toimintosovellusten esiintymiin.

6. Ulkoisen organisaation kanssa aiemmin jaetun määrityksen jakaminen poistetaan valitsemalla ensin määritys, sitten **Poista jako** ja lopuksi **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
