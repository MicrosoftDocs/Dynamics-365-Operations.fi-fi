--- 
title: "Jaa käyttöomaisuuserä"
description: "Tässä tehtävän ohjauksessa jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5aea1aab9f6b084bd0c5bd2119639bff3555bb8a
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="split-a-fixed-asset"></a>Jaa käyttöomaisuuserä

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


