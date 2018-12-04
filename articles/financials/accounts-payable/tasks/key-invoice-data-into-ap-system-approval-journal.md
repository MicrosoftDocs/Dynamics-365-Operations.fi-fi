--- 
title: "Avaintiedot ostoreskontrajärjestelmään hyväksymiskirjauskansiota käyttämällä"
description: "Tässä ohjauksessa opastetaan luomaan laskuja laskurekisterin avulla ja käyttämään hyväksymiskirjauskansiota kulutilien päivittämisessä."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>Avaintiedot ostoreskontrajärjestelmään hyväksymiskirjauskansiota käyttämällä

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjauksessa opastetaan luomaan laskuja laskurekisterin avulla ja käyttämään hyväksymiskirjauskansiota kulutilien päivittämisessä.


## <a name="create-and-post-and-invoice"></a>Luominen, kirjaaminen ja laskuttaminen
1. Siirry kohtaan Ostoreskontra > Laskut > Laskurekisteri.
2. Valitse Uusi.
3. Valitse sen laskurekisterin nimi, jota haluat käyttää.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Valitse Rivit, kun haluat avata rekisterin ja syöttää kulurivejä.
6. Valitse toimittaja. Voit esimerkiksi syöttää tai valita arvoksi US-104
7. Kirjoita Lasku-kenttään arvo.
8. Kirjoita Kuvaus-kenttään arvo.
9. Syötä Kredit-kenttään numero.
10. Avaa haku valitsemalla Hyväksynyt-kentässä avattavan valikon painike.
11. Korosta hyväksyjä ja valitse hyväksyjä valitsemalla Valitse.
12. Valitse Kirjaa.
13. Sulje sivu.
14. Sulje sivu.

## <a name="approve-an-invoice"></a>Laskun hyväksyminen
1. Siirry kohtaan Ostoreskontra > Laskut > Laskun hyväksyntä.
2. Valitse Uusi.
3. Valitse sen laskun hyväksymiskirjauskansion nimi, jota haluat käyttää.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Valitse sivulla näytettävät rivit. Sivulla voit valita hyväksyttäviä laskuja.
6. Valitse Etsi tositteet, kun haluat näyttää kaikki laskut, jotka ovat valmiita hyväksyttäväksi.
7. Merkitse luomasi lasku.
8. Klikkaa Valitse.
    * Yllä valitut tositteet siirretään tähän luetteloon sen jälkeen, kun tositteet on valittu.  
9. Valitse OK.
10. Valitse Tilinumero-kenttä, kun haluat lisätä laskuun kulutilin.
11. Syötä tilinumero ja siirry pois kentästä sarkainnäppäimellä. Syötä arvoksi esimerkiksi 600120.
12. Valitse Kirjaa.
13. Valitse Tosite, kun haluat tarkastella kirjattuja syöttöjä.
    * Hyväksyntää odottavien laskujen tili peruutetaan ja korvataan toteutuneella kulutilillä.  


