---
title: Luo online-kanava ja määritä kanavamääritteet
description: Tässä menettelyssä kerrotaan, miten uusi online-kanava luodaan ja lisätään organisaatiohierarkiaan.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4547731d7e3bc56b1ba5e0a35ff4746c6c0e9863
ms.sourcegitcommit: 901ec3b360303bb8b4d9a9dcfecc6d75d7f844a0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/05/2019
ms.locfileid: "1618293"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Luo online-kanava ja määritä kanavamääritteet

[!include[task guide banner](../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten uusi online-kanava luodaan ja lisätään organisaatiohierarkiaan. Organisaatiohierarkia on luotava ennen uuden online-kanavan luomista. Menettely käyttää esittelytietojen USRT-yritystä.


## <a name="create-a-new-online-channel"></a>Uuden online-kanavan luominen
1. Valitse Vähittäismyynti ja kauppa > Kanavat > Verkkokaupat.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Anna tai valitse Varasto-kentässä arvo.
5. Valitse vaihtoehto Varaston aikavyöhyke -kentässä.
6. Syötä tai valitse arvo Oletusasiakas-kentässä.
7. Syötä tai valitse arvo Asiakkaan osoitekirja -kentässä.
8. Syötä tai valitse arvo Maksuehdot-kenttään.
9. Anna tai valitse arvo Maksutapa-kentässä.
10. Syötä tai valitse arvo Sähköposti-ilmoitusprofiili-kenttään.
11. Laajenna Taloushallinnon dimensiot -osa.
12. Syötä tai valitse arvo BusinessUnit-kentässä.
    * Määritä samalla tavalla kaikkien muiden oletusdimensioiden arvot.  
13. Valitse Tallenna.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Verkkokaupan lisääminen organisaatiohierarkiaan
1. Sulje sivu.
2. Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkiat.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Valitse Näytä.
5. Valitse Muokkaa.
    * Voit valita minkä tahansa hierarkiasolmun, josta haluat lisätä uuden kanavan.  
6. Valitse Lisää.
7. Valitse Vähittäismyyntikanava.
8. Valitse OK.
9. Valitse Julkaise, jolloin valintaikkuna avautuu.
10. Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.
11. Valitse Julkaise.

## <a name="configure-orders-for-near-realtime-notification"></a>Tilausten määrittäminen lähes reaaliaikaista ilmoitusta varten
1. Valitse Vähittäismyynti > Pääkonttorin asetukset > Parametrit > Vähittäismyyntiparametrit.
2. Määritä Käytä reaaliaikaista palvelua verkkokauppatilausten luontiin asetukseksi "kyllä".
3. Suorita 1070-jakeluaikataulu, kun synkronoit muutokset kanavatietokannan kanssa. 


