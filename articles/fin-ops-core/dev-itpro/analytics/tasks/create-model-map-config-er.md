---
title: Luo mallin määrityksen konfiguraatioita sähköistä raportointia (ER) varten
description: Tämän toiminnon avulla voit suunnitella uuden sähköisen raportoinnin (ER) mallin yhdistämismäärityksen konfiguraation ja käyttää sisäänrakennettuja ER-toimintoja laskelmien tehokkaassa koostamisessa.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6ba23af5f7eb517cc58994e54e918b2a305da17
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142157"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Luo mallin määrityksen konfiguraatioita sähköistä raportointia (ER) varten

[!include [banner](../../includes/banner.md)]

Tämän toiminnon avulla voit suunnitella uuden sähköisen raportoinnin (ER) mallin yhdistämismäärityksen konfiguraation ja käyttää sisäänrakennettuja ER-toimintoja laskelmien tehokkaassa koostamisessa. Tässä menettelyssä luodaan konfiguraatio malliyritykselle Litware, Inc. 

Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.

Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla. Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.  
2. Valitse Raportointikonfiguraatiot.
3. Valitse Näytä suodattimet.
4. Syötä Nimi-kenttään suodattimen arvo Intrastat ja käytä alkaa-suodatinoperaattoria.
    * Käytä tätä suodatinta, kun haluat löytää Intrastat-tietomallin konfiguraation. Tämä malli voi jo olla konfiguraatioiden puurakenteessa. Jos se on puurakenteessa, ohita seuraava alitehtävä.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Hae Microsoftin Intrastat-mallikonfiguraatio
1. Sulje sivu.
2. Sulje sivu.
3. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
4. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse Microsoft-toimittaja-ruutu.  
5. Valitse Säilöt.
    * Valitse Microsoft-toimittaja-ruudussa Säilöt.  
6. Valitse Näytä suodattimet.
7. Syötä Tyypin nimi -kenttään suodattimen arvo resources ja käytä sisältää-suodatinoperaattoria. 
8. Valitse Avaa.
9. Valitse puussa 'Intrastat model'.
10. Valitse Tuo.
11. Valitse Kyllä.
    * Toit ER-muotokonfiguraation, joka tietomallin. Tämän tietomallin avulla voit tutustua uuteen ER-toimintoon.  
12. Sulje sivu.
13. Sulje sivu.
14. Valitse Raportointikonfiguraatiot.

## <a name="add-a-new-model-mapping-configuration"></a>Uuden mallin yhdistämismäärityksen konfiguraation lisääminen
1. Valitse puussa 'Intrastat model'.
2. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
3. Syötä Uusi-kenttään Mallin yhdistämismääritys perustuu tietomalliin Intrastat.
4. Syötä Nimi-kenttään Intrastat-esimerkkiyhdistämismääritys.
    * Intrastat-esimerkkiyhdistämismääritys  
5. Valitse Luo konfiguraatio.

