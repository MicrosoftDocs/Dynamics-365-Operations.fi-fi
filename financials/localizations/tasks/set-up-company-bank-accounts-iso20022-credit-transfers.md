--- 
title: "Määritä yrityksen pankkitilit ISO20022-tilisiirtoja varten"
description: "Näiden ohjeiden avulla voit määrittää SEPA-maksutiedoston luomisessa vaadittavat yrityskohtaiset pankkitilin tiedot."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4e55a4727555f781b6880103abb1a38c5d0d5b78
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Määritä yrityksen pankkitilit ISO20022-tilisiirtoja varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Näiden ohjeiden avulla voit määrittää SEPA-maksutiedoston luomisessa vaadittavat yrityskohtaiset pankkitilin tiedot. Voit määrittää ISO 20022 -pankkisiirtomuodon luomiseen vaadittavat tiedot, mutta muodosta riippuen voit joutua määrittämään muita tietoja, kuten yrityksen tunnuksen tai lajittelukoodin. 

Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.

Tämä on toinen viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="set-up-iban-and-swift-code"></a>IBAN- ja SWIFT-koodin määrittäminen
1. Siirry kohtaan Maksuliikenteen hallinta > Pankkitilit.
2. Pikasuodattimen avulla voit suodattaa Pankkitili-kentän DEMF OPER -arvon mukaan.
3. Avaa pankkitilin tiedot valitsemalla DEMF OPER.
4. Valitse Muokkaa.
5. Laajenna Lisätunnus-osa.
6. Kirjoita IBAN-kenttään DE89370400440532013000.
7. Syötä SWIFT-koodi-kenttään DEUTDEFF.
    * Huomaa, ettei SWIFT\BIC ole pakollinen monissa maksumuodoissa; se on kuitenkin suositeltavaa rekisteröidä pankkitilille.  
8. Valitse Tallenna.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Yrityksen pankkitilin määrittäminen
1. Siirry kohtaan Organisaation hallinto > Organisaatiot > Yritykset.
2. Valitse Muokkaa.
3. Laajenna Pankkitilitiedot-osa.
4. Syötä tai valitse arvo Pankkitili-kentässä.
5. Valitse Tallenna.


