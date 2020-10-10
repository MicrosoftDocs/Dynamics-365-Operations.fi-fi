---
title: ER-määritysten luominen RCS:ssä ja niiden lataaminen yleiseen säilöön
description: Tässä ohjeaiheessa käsitellään Microsoft Regulatory Configuration Servicesin (RCS) sähköisen raportoinnin (ER) määrityksen luomista ja lataamista yleiseen säilöön.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
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
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834230"
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

![Uusi RCS:n määritysversio](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Kun määrityksen tila on muuttuu, yhdistettyihin sovelluksiin liittyvä tarkistusvirhesanoma voi tulla näkyviin. Tarkistuksen voi poistaa käytöstä valitsemalla toimintoruudun **Konfiguraatiot**-välilehdessä **Käyttäjän parametrit** ja määrittämällä sitten **Ohita konfiguraation tilamuutoksen aikainen tarkistus ja perustaa uudelleen** -asetukseksi **Kyllä**. 

## <a name="upload-a-configuration-to-the-global-repository"></a>Määrityksen lataaminen yleiseen säilöön

Uusi tai johdettu määritys jaetaan organisaatiossa lataamalla se yleiseen säilöön.

1. Valitse ensin määrityksen valmis versio ja sitten **Lataa säilöön**.
2. Valitse ensin **Yleinen (Microsoft)** -vaihtoehto ja sitten **Lataa**.

    ![Säilöön lataamisen asetukset](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Valitse vahvistussanomaikkunassa **Kyllä**. 
4. Päivitä version kuvaus tarpeen mukaan ja valitse sitten **OK**. 

Määrityksen tilaksi päivitetään **Jako** ja määritys ladataan yleiseen säilöön. Määritystä voi käyttää säilössä seuraavasti:

- Tuonti Dynamics 365 -esiintymään. Lisätietoja on kohdassa [(ER) Konfiguraatioiden tuonti RCS:stä](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)
- Lisätietoja jakamisesta kolmannen osapuolen tai ulkoisen organisaation kanssa on kohdassa [RCS:n ulkoisten organisaatioiden kanssa jakamat sähköisen raportoinnin (ER) määritykset](rcs-global-repo-share-configuration.md)

    ![Johdettu Intrastat Contoso -määritysversio yleisessä säilössä.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Poista määritys yleisestä säilöstä
Suorita seuraavat vaiheet poistaaksesi määrityksen, jonka organisaatiosi on luonut.

1. Varmista **Sähköinen raportointi** -työtilassa, että määrityspalvelusi on **Aktiivinen**. Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Valitse aktiivisessa määrityspalvelussa **säilö**.
3. Valitse säilötyyppi **Yleinen** ja sitten **Avaa**.
4. Etsi poistettava määritys **Suodatin**-pikavälilehdessä käyttämällä **Suodata**-toimintoa.
5. Valitse **Versio**-pikavälilehdessä määrityksen poistettava versio ja valitse sitten **Poista**.

    ![Määrityksen poistaminen yleisestä säilöstä](media/RCS_Delete_from_GlobalRepo.JPG)

6. Valitse vahvistussanomaikkunassa **Kyllä**.

    ![Määritysversion vahvistusviestin poistaminen](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Määritysversio poistetaan ja vahvistusviesti näytetään. 

> [!NOTE]
> Vain määritykset luonut määrityspalvelu voi poistaa niitä. Jos määritys on jaettu toisen organisaation kanssa, määrityksen jakaminen on peruutettava ennen poistamista.
 
