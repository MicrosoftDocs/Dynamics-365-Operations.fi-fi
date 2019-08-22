---
title: Jaa käyttöomaisuuserä
description: Tässä tehtävän ohjauksessa jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: d8e5fdc8a7b326daca1fc0f0962c69bb8fb1ff64
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839710"
---
# <a name="split-a-fixed-asset"></a>Jaa käyttöomaisuuserä

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.  Käytössä ovat kirjanpitäjän rooli ja USMF:n esittelytiedot.


## <a name="create-a-new-fixed-asset"></a>Luo uusi käyttöomaisuuserä
1. Siirry kohtaan Käyttöomaisuudet > Käyttöomaisuudet > Käyttöomaisuudet.
2. Valitse Uusi.
3. Syötä tai valitse arvo Käyttöomaisuusryhmä-kentässä.
4. Huomaa, että käyttöomaisuusnumeroa käytetään jakoprosessissa myöhemmin.
5. Kirjoita arvo Nimi-kenttään.
6. Sulje lomake.

## <a name="split-a-fixed-asset"></a>Jaa käyttöomaisuuserä
1. Etsi ja valitse luettelosta jaettava käyttöomaisuus.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
3. Valitse Kirjat.
    * Valitse kirja, joka jaetaan uudeksi käyttöomaisuuseräksi.  
4. Valitse Toiminnot.
5. Valitse Jaa käyttöomaisuus.
6. Syötä tai valitse arvo Käyttöomaisuuserään-kentässä.
7. Avaa haku napsauttamalla Kirjaan-kentässä avattavan valikon painiketta.
8. Syötä Tapahtumapäivä-kenttään päivämäärä.
9. Kirjoita numero Prosentti-kenttään.
10. Syötä tai valitse arvo Kirjauskansion nimi -kentässä.
11. Valitse OK.

## <a name="post-the-journal-transaction"></a>Kirjauskansiotapahtuman kirjaaminen
1. Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.
2. Valitse luettelosta jakoprosessissa luotu kirjauskansio.
3. Valitse Rivit.
    * Tarkista luodut kirjauskansiorivit.  Alkuperäisen käyttöomaisuuserän hankinnan oikaisutapahtuma luodaan, kun arvoa halutaan nostaa määritetyn prosenttiosuuden verran jakoprosentin aikana.  Uudelle käyttöomaisuuserälle luodaan hankintatapahtuma samalle summalle.  
4. Valitse Kirjaa.

