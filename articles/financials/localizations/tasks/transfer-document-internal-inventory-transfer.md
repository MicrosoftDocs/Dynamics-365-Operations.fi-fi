--- 
title: "Siirtoasiakirjan luominen sisäiselle varastosiirrolle"
description: "Tässä menettelyssä kuvataan, miten yrityksen sisäisen tavaroidensiirron siirtoasiakirjat luodaan."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 30e5f6ad184720d0e119f86fb703ed7211b27fab
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>Siirtoasiakirjan luominen sisäiselle varastosiirrolle

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten yrityksen sisäisen tavaroidensiirron siirtoasiakirjat luodaan. Tämä menettely on käytettävissä vain yrityksille, joiden ensisijainen osoite on Liettuassa. Tämä menettely luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Liettuassa. "Yrityksen sisäisten tavaransiirtojen siirtoasiakirjojen määrittäminen" -menettely on suoritettava ennen, kuin suoritat tämän menettelyn. Menettely on tarkoitettu varastokirjanpitäjille. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="create-a-transfer-order"></a>Siirtotilauksen luonti
1. Valitse Varastonhallinta > Saapuvat tilaukset > Siirtotilaus.
2. Valitse Uusi.
3. Anna tai valitse Varastosta-kentässä arvo.
4. Anna tai valitse Varastoon-kentässä arvo.
5. ValitseLisää.
6. Merkitse valittu rivi luettelossa.
7. Syötä tai valitse arvo Nimiketunnus-kentässä.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Täytä siirtotilauksen kuljetustiedot
1. Valitse Tallenna.
2. Valitse toimintoruudussa Lähetys.
3. Valitse Kuljetustiedot.
4. Valitse Tulosta kuljetustiedot -kentässä Kyllä.
5. Anna tai valitse Tuotteiden hyväksyjä -kentässä arvo.
6. Kirjoita arvo Paketti-kenttään.
7. Kirjoita arvo Lastin riskitaso -kenttään.
8. Syötä tai valitse arvo Rahdinkuljettaja-kenttään.
9. Syötä tai valitse arvo Malli-kentässä.
10. Kirjoita Rekisteröintinumero-kenttään arvo.
11. Kirjoita Perävaunun rekisterinumero -kenttään arvo.
12. Syötä tai valitse arvo Kuljettaja-kenttään.
13. Kirjoita arvo Kuljettajan nimi -kenttään.
14. Valitse Tallenna.
15. Sulje sivu.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Näytä kirjaamattoman siirtotilauksen pakkausluettelo
1. Valitse Pakkausluettelo.
2. Valitse OK.
3. Sulje sivu.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Näytä kirjatun siirtotilauksen pakkausluettelo
1. Valitse toimintoruudussa Siirtotilaus.
2. Valitse toimintoruudussa Lähetys.
3. Valitse Siirtotilauksen lähettäminen.
4. Valitse Yleiset-välilehti.
5. Valitse vaihtoehto Päivitä-kentässä.
6. Valitse Yhteenveto-välilehti.
7. Kirjoita arvo Pakkausluettelo-kenttään.
8. Valitse OK.
9. Valitse toimintoruudussa Lähetys.
10. Valitse Pakkausluettelo.
11. Valitse OK.


