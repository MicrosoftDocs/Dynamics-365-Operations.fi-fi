---
title: Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla
description: Tässä ohjeaiheessa kerrotaan, miten luodaan laskuja laskurekisterin avulla ja käytetään hyväksymiskirjauskansiota kulutilien päivittämisessä.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb690769a33f88e63ab8f54cec69a5e927fd324c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177599"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten luodaan laskuja laskurekisterin avulla ja käytetään hyväksymiskirjauskansiota kulutilien päivittämisessä.

## <a name="create-and-post-and-invoice"></a>Luominen, kirjaaminen ja laskuttaminen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskurekisteri**.
2. Valitse **Uusi**.
3. Valitse sen laskurekisterin nimi, jota haluat käyttää.
4. Valitse **Rivit**, kun haluat avata rekisterin ja syöttää kulurivejä.
5. Valitse toimittaja. Voit esimerkiksi syöttää tai valita arvoksi `US-104`.
6. Kirjoita **Lasku**-kenttään arvo.
7. Kirjoita **Kuvaus**-kenttään arvo.
8. Syötä **Kredit**-kenttään numero.
9. Valitse **Hyväksynyt**-kentästä hyväksyjä avattavasta valikosta.
10. Valitse **Kirjaa**.

## <a name="approve-an-invoice"></a>Laskun hyväksyminen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskun hyväksyntä**.
2. Valitse **Uusi**.
3. Valitse sen laskun hyväksymiskirjauskansion nimi, jota haluat käyttää.
4. Valitse sivulla näytettävät **Rivit**. Sivulla voit valita hyväksyttäviä laskuja.
5. Valitse **Etsi tositteet**, kun haluat näyttää kaikki laskut, jotka ovat valmiita hyväksyttäväksi.
6. Merkitse luomasi lasku ja valitse sitten **Valitse.** Yllä valitut tositteet siirretään tähän luetteloon sen jälkeen, kun tositteet on valittu.  
7. Valitse **OK**.
8. Valitse **Tilinumero**-kenttä, kun haluat lisätä laskuun kulutilin.
9. Syötä tilinumero ja siirry pois kentästä sarkainnäppäimellä. Syötä arvoksi esimerkiksi `600120`.
10. Valitse **Kirjaa**.
11. Valitse **Tosite**, kun haluat tarkastella kirjattuja syöttöjä. Hyväksyntää odottavien laskujen tili peruutetaan ja korvataan toteutuneella kulutilillä.  
