---
title: Käyttöomaisuuserän jakaminen
description: Tässä aiheessa kerrotaan miten jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da2dd4889a5f4722ff60a76a4a023c63fb59ad55
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514323"
---
# <a name="split-a-fixed-asset"></a>Käyttöomaisuuserän jakaminen

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kerrotaan miten jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan. Käytössä ovat kirjanpitäjän rooli ja USMF:n esittelytiedot.

## <a name="create-a-new-fixed-asset"></a>Luo uusi käyttöomaisuuserä

1. Valitse siirtymisruudussa **Moduulit \> Käyttöomaisuuserät \> Käyttöomaisuuserät \> Käyttöomaisuuserät**.
2. Valitse **Uusi**.
3. Syötä tai valitse arvo **Käyttöomaisuusryhmä**-kentässä. Huomaa, että käyttöomaisuusnumeroa käytetään jakoprosessissa myöhemmin.
4. Anna **Nimi**-kenttään arvo.
5. Sulje lomake.

## <a name="split-a-fixed-asset"></a>Käyttöomaisuuserän jakaminen

Ennen kokonaan poistetun käyttöomaisuuden jakamista käyttöomaisuuskirjan tila **Suljettu** on vaihdettava manuaalisesti tilaan **Avoin**. Tämä vaihe on pakollinen, koska kirjan tilan on oltava **Avoin**, jos käyttöomaisuuteen on kirjattava tapahtumia (kuten poistomyynti). Ota myös **Salli useita tapahtumia yhdessä tositteessa** -parametri käyttöön **Yleistiedot**-välilehdessä **Kirjanpidon parametrit** -sivulla. Kun käyttöomaisuuskirjan tila on muutettu ja yhden tositteen useita tapahtumia on sallittu, jaa käyttöomaisuuserä suorittamalla seuraavat vaiheet.

1. Etsi ja valitse luettelosta jaettavan käyttöomaisuuden linkki.
2. Valitse **Kirjat**. Valitse kirja, joka jaetaan uudeksi käyttöomaisuuseräksi.
3. Valitse **Toiminnot**.
4. Valitse **Jaa käyttöomaisuus**.
5. Syötä tai valitse arvo **Käyttöomaisuuserään**-kentässä.
6. Avaa haku napsauttamalla **Kirjaan**-kentässä avattavan valikon painiketta.
7. Syötä **Tapahtumapäivä**-kenttään päivämäärä.
8. Kirjoita numero **Prosentti**-kenttään.
9. Syötä tai valitse arvo **Kirjauskansion nimi** -kentässä.
10. Valitse **OK**.

## <a name="post-the-journal-transaction"></a>Kirjauskansiotapahtuman kirjaaminen

1. Valitse siirtymisruudussa **Moduulit \> Käyttöomaisuuserät \> Kirjauskansioviennit \> Käyttöomaisuuden kirjauskansio**.
2. Valitse luettelosta jakoprosessissa luotu kirjauskansio.
3. Valitse **Rivit**.

    - Tarkista luodut kirjauskansiorivit.
    - Alkuperäisen käyttöomaisuuserän hankinnan oikaisutapahtuma luodaan, kun arvoa halutaan nostaa määritetyn prosenttiosuuden verran jakoprosentin aikana.
    - Uudelle käyttöomaisuuserälle luodaan hankintatapahtuma samalle summalle.

4. Valitse **Kirjaa**.
