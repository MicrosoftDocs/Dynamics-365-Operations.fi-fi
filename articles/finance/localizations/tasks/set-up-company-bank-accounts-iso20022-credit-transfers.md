---
title: Määritä yrityksen pankkitilit ISO20022-tilisiirtoja varten
description: Näiden ohjeiden avulla voit määrittää SEPA-maksutiedoston luomisessa vaadittavat yrityskohtaiset pankkitilin tiedot.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3b3b5ce9d7e24b2b7d3f76e4d770968df897b546df507ba9e3bde5aeac91715
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780767"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Määritä yrityksen pankkitilit ISO20022-tilisiirtoja varten

[!include [banner](../../includes/banner.md)]

Näiden ohjeiden avulla voit määrittää SEPA-maksutiedoston luomisessa vaadittavat yrityskohtaiset pankkitilin tiedot. Voit määrittää ISO 20022 -pankkisiirtomuodon luomiseen vaadittavat tiedot, mutta muodosta riippuen voit joutua määrittämään muita tietoja, kuten yrityksen tunnuksen tai lajittelukoodin. 

Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.

Tämä on toinen viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]