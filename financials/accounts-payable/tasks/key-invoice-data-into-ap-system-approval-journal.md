--- 
title: "Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla"
description: "Tässä ohjauksessa opastetaan luomaan laskuja laskurekisterin avulla ja käyttämään hyväksymiskirjauskansiota kulutilien päivittämisessä."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d7cf810f1d8eabb9989fdd858585afcdf2e9574b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

