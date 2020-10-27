---
title: Tuoterakenteen luominen dimensioperustaiselle päätuotteelle
description: Tätä menettelyä varten sinun tulisi olla suorittanut edelliset 4 opasta tässä neljän tallenteen sarjassa.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7961cfb4ad0e20c49d327d83f56c08811598ac1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986284"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Tuoterakenteen luominen dimensioperustaiselle päätuotteelle

[!include [banner](../../includes/banner.md)]

Tätä menettelyä varten sinun tulisi olla suorittanut edelliset 4 opasta tässä neljän tallenteen sarjassa. Ensimmäiset 4 tallennetta määrittävät tiedot, jotka tarvitaan tämän menettelyn suorittamiseen. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tästä tehtävästä vastaa yleensä tuotesuunnittelija.


## <a name="select-the-product"></a>Valitse tuote
1. Valitse Vapautetun tuotteen ylläpito.
2. Valitse Vapautetut tuotteet.
3. Merkitse valittu rivi luettelossa.
    * Paikanna tämän tehtäväoppaan ensimmäisessä vaiheessa luomasi julkaistu päätuote, jolla on dimensioihin perustuva konfiguraatio.  
4. Valitse toimintoruudussa Suunnittele.
5. Valitse Tuoterakenneversiot.

## <a name="create-new-bom-and-bom-version"></a>Luo uusi tuoterakenne ja tuoterakenneversio
1. Valitse Uusi.
2. Napsauta kohtia Tuoterakenne ja Tuoterakenneversio.
3. Kirjoita arvo Nimi-kenttään.
    * Toimipaikan määrittäminen  
    * Näissä toimintaohjeissa ei määritetä tuoterakenteelle tiettyä toimipaikkaa.  
4. Valitse OK.
5. Valitse Uusi.
    * Näissä toimintaohjeissa lisätään neljä riviä tuoterakenteeseen. Kaksi riviä edustavat kaapelivaihtoehtoja ja toisen kaksi riviä kabinettivaihtoehtoja.  
6. Merkitse valittu rivi luettelossa.
7. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Valitse nimiketunnus A0001, HDMI 6' kaapelit.  
8. Anna tai valitse arvo Konfiguraatioryhmä-kenttään.
    * Valitse kaapelin konfiguraatioryhmä, joka luotiin oppaan vaiheessa 4.  
9. Valitse Uusi.
    * Valitse nimiketunnus A0002, HDMI 12' kaapelit.  
10. Merkitse valittu rivi luettelossa.
11. Syötä tai valitse arvo Nimiketunnus-kentässä.
12. Anna tai valitse arvo Konfiguraatioryhmä-kenttään.
    * Valitse kaapelin konfiguraatioryhmä uudelleen.  
13. Valitse Uusi.
14. Merkitse valittu rivi luettelossa.
15. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Valitse nimiketunnus D0002 Kabinetti.  
16. Anna tai valitse arvo Konfiguraatioryhmä-kenttään.
    * Valitse kabinetin konfiguraatioryhmä tälle tuoterakenteen riville.  
17. Valitse Uusi.
18. Merkitse valittu rivi luettelossa.
19. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Valitse nimiketunnus M0007 Vakiokabinetti viimeiseksi tuoterakenteen riviksi.  
20. Anna tai valitse arvo Konfiguraatioryhmä-kenttään.
    * Valitse kabinetin konfiguraatioryhmä viimeiselle tuoterakenteen riville.  

## <a name="approve-and-activate"></a>Hyväksy ja aktivoi
1. Sulje sivu.
2. Valitse Hyväksy.
3. Anna tai valitse Hyväksyjä-kentässä arvo.
4. Vastaa kyllä kysymykseen "Haluatko myös hyväksyä tuoterakenteen?" avulla.
5. Valitse OK.
6. Valitse Aktivoi.

