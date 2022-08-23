---
title: Sähköisen raportoinnin konfiguraatioiden luominen RCS:ssä ja niiden lataaminen yleiseen säilöön
description: Tässä artikkelissa käsitellään Microsoft Regulatory Configuration Servicesin (RCS) sähköisen raportoinnin (ER) määrityksen luomista ja lataamista yleiseen säilöön.
author: kfend
ms.date: 01/11/2021
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
ms.openlocfilehash: 21e6ab3a7066fda23f1f5672f6f74bc6bd1ff1f6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282990"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER-määritysten luominen Regulatory Configuration Servicesissä (RCS) ja niiden lataaminen yleiseen säilöön

[!include [banner](../includes/banner.md)]

Microsoft Regulatory Configuration Servicesiä (RCS) voi käyttää sähköisen raportoinnin (ER) määritysten suunnitteluun ja niiden julkaisemiseen organisaatiossa käytettäväksi.

Seuraavissa menettelyissä käsitellään tapaa, jolla järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda johdetun version RCS-esiintymässä määritetystä ER-määrityksestä ja jolla johdettu määritys sitten ladataan yleiseen säilöön. 

Seuraavat ennakkoedellytykset on oltava suoritettuna, ennen kuin kyseiset menetelmät voidaan suorittaa.

- Voit käyttää organisaatiosi RCS-ympäristöä.
- Aktiivisen konfiguraation lähteen luominen ja sen muuttaminen aktiiviseksi. Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

On varmistettava, että RCS-ympäristö on valmisteltu organisaatioon. Jos organisaatiollesi ei ole varattu RCS-esiintymää, voit tehdä sen noudattamalla seuraavia ohjeita:

1. Valitse talous- ja toimintosovelluksessa **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Liittyvät linkit/ulkoiset linkit** -kohdasta **Säännöspalvelut – Konfigurointi** ja noudata sitten **rekisteröintiin** liittyviä ohjeita varataksesi yhden.

Jos organisaatioon on valmisteltu RCS-ympäristö, siirry siihen sivun URL-osoitteen avulla ja valitse **Kirjaudu**-vaihtoehto.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Määrityksen johdetun version luominen RCS:ssä

> [!NOTE]
> Jos käytät RCS:tä ensimmäistä kertaa, käytettävissäsi ei ole konfiguraatiota, jonka perusteella käyttäjä voi tehdä määrityksiä. Konfiguraatio on tuotava yleisvarastosta. Lisätietoja on kohdassa [ER-määritysten lataaminen määrityspalvelun yleisestä varastosta](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Kirjaudu** RCS:ään ja valitse **Sähköinen raportointi** -työtila.
2. Varmista, että organisaatiossasi on aktiivinen konfigurointitoimittaja, joka on asetettu aktiiviseksi (katso edellytykset). 
3. Valitse **Raportointikonfiguraatiot**.
4. Valitse määritys, josta haluat johtaa uuden version. Voit tarkentaa hakua käyttämällä puun yläpuolella olevaa suodatinkenttää.
5. Valitse **Luo konfiguraatio** \> **Johda nimestä**.
6. Anna nimi ja kuvaus ja luo sitten uusi johdettu versio luonnostilassa valitsemalla **Luo konfiguraatio**.
7. Valitse uusi johdettu konfiguraatio ja tee tarvittaessa lisämuutoksia konfiguraatiomuotoon. 
8. Kun muutokset on tehty, sinun on asetettava **Muuta tila** asetukseksi **Valmis**, jotta voit julkaista sen arkistoon. Valitse **OK**.

![Uusi RCS:n määritysversio.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Kun määrityksen tila on muuttuu, yhdistettyihin sovelluksiin liittyvä tarkistusvirhesanoma voi tulla näkyviin. Tarkistuksen voi poistaa käytöstä valitsemalla toimintoruudun **Konfiguraatiot**-välilehdessä **Käyttäjän parametrit** ja määrittämällä sitten **Ohita konfiguraation tilamuutoksen aikainen tarkistus ja perustaa uudelleen** -asetukseksi **Kyllä**. 

## <a name="upload-a-configuration-to-the-global-repository"></a>Määrityksen lataaminen yleiseen säilöön

Uusi tai johdettu määritys jaetaan organisaatiossa lataamalla se yleiseen säilöön seuraamalla näitä ohjeita:

1. Valitse ensin määrityksen valmis versio ja sitten **Lataa säilöön**.
2. Valitse ensin **Yleinen (Microsoft)** -vaihtoehto ja sitten **Lataa**.

    ![Säilöön lataamisen asetukset.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Valitse vahvistussanomaikkunassa **Kyllä**. 
4. Päivitä version kuvaus tarpeen mukaan ja valitse sitten **OK**. Voit myös halutessasi ladata version liitettyyn sovellukseen tai GIT-tietovarastoon.  

Määrityksen tilaksi päivitetään **Jaettu** ja määritys ladataan yleiseen säilöön. Myös lataamistasi konfiguraatioversioista luodaan luonnosversio, ja sitä voidaan käyttää, jos muutoksia tarvitaan.

Kun konfiguraatio on ladattu yleistietovarastoon, voit käyttää sitä seuraavilla tavoilla:

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

    ![Määrityksen poistaminen yleisestä säilöstä.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Valitse vahvistussanomaikkunassa **Kyllä**.

    ![Määritysversion vahvistusviestin poistaminen.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Määritysversio poistetaan ja vahvistusviesti näytetään. 

> [!NOTE]
> Vain määritykset luonut määrityspalvelu voi poistaa niitä. Jos määritys on jaettu toisen organisaation kanssa, määrityksen jakaminen on peruutettava ennen poistamista.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

