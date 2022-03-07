---
title: Tuoterakenteen luominen dimensioperustaiselle päätuotteelle
description: Tätä menettelyä varten sinun tulisi olla suorittanut edelliset 4 opasta tässä neljän tallenteen sarjassa.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920702"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Tuoterakenteen luominen dimensioperustaiselle päätuotteelle

[!include [banner](../../includes/banner.md)]

Tätä menettelyä varten sinun tulisi olla suorittanut edelliset 4 opasta tässä neljän tallenteen sarjassa. Ensimmäiset 4 tallennetta määrittävät tiedot, jotka tarvitaan tämän menettelyn suorittamiseen. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tästä tehtävästä vastaa yleensä tuotesuunnittelija.

## <a name="select-the-product"></a>Valitse tuote

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Merkitse valittu rivi luettelossa.
    * Paikanna tämän tehtäväoppaan ensimmäisessä vaiheessa luomasi julkaistu päätuote, jolla on dimensioihin perustuva konfiguraatio.  
1. Valitse toimintoruudussa **Kehittäjä**.
1. Valitse **Tuoterakenneversiot**.

## <a name="create-new-bom-and-bom-version"></a>Luo uusi tuoterakenne ja tuoterakenneversio

1. Valitse **Uusi**.
1. Valitse **Tuoterakenne ja tuoterakenneversio**.
1. Kirjoita arvo **Nimi**-kenttään.
    * Toimipaikan määrittäminen  
    * Näissä toimintaohjeissa ei määritetä tuoterakenteelle tiettyä toimipaikkaa.  
1. Valitse **OK**.
1. Valitse **Uusi**.
    * Näissä toimintaohjeissa lisätään neljä riviä tuoterakenteeseen. Kaksi riviä edustavat kaapelivaihtoehtoja ja toisen kaksi riviä kabinettivaihtoehtoja.  
1. Merkitse valittu rivi luettelossa.
1. Syötä tai valitse arvo **Nimiketunnus**-kentässä.
    * Valitse nimiketunnus A0001, HDMI 6' kaapelit.  
1. Anna tai valitse arvo **Konfiguraatioryhmä**-kenttään.
    * Valitse kaapelin konfiguraatioryhmä, joka luotiin oppaan vaiheessa 4.  
1. Valitse **Uusi**.
    * Valitse nimiketunnus A0002, HDMI 12' kaapelit.  
1. Merkitse valittu rivi luettelossa.
1. Syötä tai valitse arvo **Nimiketunnus**-kentässä.
1. Anna tai valitse arvo **Konfiguraatioryhmä**-kenttään.
    * Valitse kaapelin konfiguraatioryhmä uudelleen.  
1. Valitse **Uusi**.
1. Merkitse valittu rivi luettelossa.
1. Syötä tai valitse arvo **Nimiketunnus**-kentässä.
    * Valitse nimiketunnus D0002 Kabinetti.  
1. Anna tai valitse arvo **Konfiguraatioryhmä**-kenttään.
    * Valitse kabinetin konfiguraatioryhmä tälle tuoterakenteen riville.  
1. Valitse **Uusi**.
1. Merkitse valittu rivi luettelossa.
1. Syötä tai valitse arvo **Nimiketunnus**-kentässä.
    * Valitse nimiketunnus M0007 Vakiokabinetti viimeiseksi tuoterakenteen riviksi.  
1. Anna tai valitse arvo **Konfiguraatioryhmä**-kenttään.
    * Valitse kabinetin konfiguraatioryhmä viimeiselle tuoterakenteen riville.  

## <a name="approve-and-activate"></a>Hyväksy ja aktivoi

1. Sulje sivu.
1. Valitse **Hyväksy**.
1. Anna tai valitse **Hyväksyjä**-kentässä arvo.
1. Vastaa *Kyllä* **Haluatko myös hyväksyä tuoterakenteen?** -kentässä.
1. Valitse **OK**.
1. Valitse **Aktivoi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]