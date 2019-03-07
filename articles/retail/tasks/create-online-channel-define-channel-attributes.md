---
title: Luo online-kanava ja määritä kanavamääritteet
description: Tässä menettelyssä kerrotaan, miten uusi online-kanava luodaan ja lisätään organisaatiohierarkiaan.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "312367"
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

