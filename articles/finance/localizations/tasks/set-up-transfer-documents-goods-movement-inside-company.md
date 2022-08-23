---
title: Siirtoasiakirjojen määrittäminen tavaroiden siirrolle yrityksen sisällä
description: Tässä menettelyssä kuvataan, miten yrityksen sisäisen tavaroidensiirron siirtoasiakirjat määritetään.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
ms.openlocfilehash: 333c5b5e5cfa25e705c9864542517f8ec5532dfe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282331"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a>Siirtoasiakirjojen määrittäminen tavaroiden siirrolle yrityksen sisällä

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kuvataan, miten yrityksen sisäisen tavaroidensiirron siirtoasiakirjat luodaan. Tämä menettely on käytettävissä vain yrityksille, joiden ensisijainen osoite on Liettuassa. Tämä menettely luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Liettuassa. "Yrityksen sisäisten tavaransiirtojen siirtoasiakirjojen määrittäminen" -menettely on suoritettava ennen, kuin suoritat tämän menettelyn. Menettely on tarkoitettu varastokirjanpitäjille. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
