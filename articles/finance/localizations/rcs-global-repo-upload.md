---
title: ER-määritysten luominen RCS:ssä ja niiden lataaminen yleiseen säilöön
description: Tässä ohjeaiheessa käsitellään Microsoft Regulatory Configuration Servicesin (RCS) sähköisen raportoinnin (ER) määrityksen luomista ja lataamista yleiseen säilöön.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371243"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER-määritysten luominen Regulatory Configuration Servicesissä (RCS) ja niiden lataaminen yleiseen säilöön

[!include [banner](../includes/banner.md)]

Microsoft Regulatory Configuration Servicesiä (RCS) voi käyttää sähköisen raportoinnin (ER) määritysten suunnitteluun ja niiden julkaisemiseen organisaatiossa käytettäväksi.

Seuraavissa menettelyissä käsitellään tapaa, jolla järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda johdetun version RCS-esiintymässä määritetystä ER-määrityksestä ja jolla johdettu määritys sitten ladataan yleiseen säilöön. 

Seuraavat ennakkoedellytykset on oltava suoritettuna, ennen kuin kyseiset menetelmät voidaan suorittaa.

- RCS-esiintymän käyttäminen.
- Aktiivisen määrityspalvelun luonti. Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Lisäksi on varmistettava, että RCS-ympäristö on valmisteltu yritykseen.

1. Valitse Finance and Operations -sovelluksessa **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Jos yritykseen ei ole valmisteltu RCS-ympäristöä, valitse **Regulatory Services – ulkoinen määritys** -linkki ja valmistele sitten sellainen ohjeiden mukaisesti.

Jos yritykseen on valmisteltu RCS-ympäristö, siirry siihen sivun URL-osoitteen avulla valitsemalla kirjautumisvaihtoehto.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Määrityksen johdetun version luominen RCS:ssä

1. Varmista **Sähköinen raportointi** -työtilassa, että organisaatiossa on aktiviinen määrityspalvelu. 
2. Valitse **Raportointikonfiguraatiot**.
3. Valitse määritys, josta haluat johtaa uuden version. Voit tarkentaa hakua käyttämällä puun yläpuolella olevaa suodatinkenttää.
4. Valitse **Luo konfiguraatio** \> **Johda nimestä**.
5. Anna nimi ja kuvaus ja luo sitten uusi johdettu versio valitsemalla **Luo konfiguraatio**.
6. Valitse juuri johdettu konfiguraatio, lisää version kuvaus ja valitse **OK**. Konfiguraation tila muuttuu ja uusi tila on **Valmis**.

![Uusi RCS:n määritysversio](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Kun määrityksen tila on muuttuu, yhdistettyihin sovelluksiin liittyvä tarkistusvirhesanoma voi tulla näkyviin. Tarkistuksen voi poistaa käytöstä valitsemalla toimintoruudun **Konfiguraatiot**-välilehdessä **Käyttäjän parametrit** ja määrittämällä sitten **Ohita konfiguraation tilamuutoksen aikainen tarkistus ja perustaa uudelleen** -asetukseksi **Kyllä**. 

## <a name="upload-a-configuration-to-the-global-repository"></a>Määrityksen lataaminen yleiseen säilöön

Uusi tai johdettu määritys jaetaan organisaatiossa lataamalla se yleiseen säilöön.

1. Valitse ensin määrityksen valmis versio ja sitten **Lataa säilöön**.
2. Valitse ensin **Yleinen (Microsoft)** -vaihtoehto ja sitten **Lataa**.

    ![Säilöön lataamisen asetukset](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Valitse vahvistussanomaikkunassa **Kyllä**. 
4. Päivitä version kuvaus tarpeen mukaan ja valitse sitten **OK**. 

Määrityksen tilaksi päivitetään **Jako** ja määritys ladataan yleiseen säilöön. Määritystä voi käyttää säilössä seuraavasti:

- Tuonti Dynamics 365 -esiintymään. Lisätietoja on kohdassa [(ER) Konfiguraatioiden tuonti RCS:stä](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)
- Lisätietoja jakamisesta kolmannen osapuolen tai ulkoisen organisaation kanssa on kohdassa [RCS:n ulkoisten organisaatioiden kanssa jakamat sähköisen raportoinnin (ER) määritykset](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)

![Johdettu Intrastat Contoso -määritysversio yleisessä säilössä.](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
