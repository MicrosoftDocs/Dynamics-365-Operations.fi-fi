---
title: Määritä yrityksen pankkitilit ISO20022-suoraveloituksia varten
description: Tässä tehtävässä kerrotaan, miten asiakkaan maksutiedostojen luomisessa vaadittavat yrityskohtaisen pankkitilin tiedot määritetään.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 652d8aa8f78d9a12ee390d23904f2c94d9bcf684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442690"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Määritä yrityksen pankkitilit ISO20022-suoraveloituksia varten

[!include [banner](../../includes/banner.md)]

Tässä tehtävässä kerrotaan, miten asiakkaan maksutiedostojen luomisessa vaadittavat yrityskohtaisen pankkitilin tiedot määritetään. Näissä ohjeissa käytetään esimerkkinä ISO 20022 -suoraveloitusmuotoa. Muissa muodoissa voidaan vaatia lisämäärityksiä, kuten yrityksen tunnus tai lajittelukoodi.



Tämän tehtävän luomisessa käytettiin esittelytietojen DEMF-yritystä.



Tämä on toinen viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.


## <a name="set-up-the-iban-and-swift-codes"></a>IBAN- ja SWIFT-koodin määrittäminen
1. Siirry kohtaan Maksuliikenteen hallinta > Pankkitilit.
2. Pikasuodattimen avulla voit suodattaa Pankkitili-kentän DEMF OPER -arvon mukaan.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Esimerkki: valitse DEMF OPER, kun haluat avata pankkitilin tiedot.  
4. Valitse Muokkaa.
5. Laajenna tai tiivistä Lisätunnus-osa.
6. Syötä arvon IBAN-kenttään.
    * Kirjoita esimerkiksi 'DE89370400440532013000'.  
7. Syötä arvo SWIFT-koodi-kenttään.
    * Esimerkki: kirjoita "DEUTDEFF".    Huomaa, ettei SWIFT\BIC ole pakollinen monissa maksumuodoissa; se on kuitenkin suositeltavaa rekisteröidä pankkitilille.  
8. Valitse Tallenna.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Yrityksen pankkitilin määrittäminen
1. Siirry kohtaan Organisaation hallinto > Organisaatiot > Yritykset.
2. Valitse Muokkaa.
3. Laajenna tai tiivistä Pankkitilin tiedot -osa.
4. Avaa haku valitsemalla Pankkitili-kentässä avattavan valikon painike.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Esimerkki: valitse pankkitili "DEMF OPER".  
6. Valitse Tallenna.

