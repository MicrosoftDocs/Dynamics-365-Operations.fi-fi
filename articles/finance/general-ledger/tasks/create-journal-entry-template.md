---
title: Kirjauskansioviennin luonti mallin avulla
description: Kirjatut kirjauskansion tositteet voidaan tallentaa tositemalleina. Ne voidaan kohdistaa uuteen kirjauskansion tositteeseen.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05cb878b570c45a2f7358ad60e6e01c7af17dc90
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716479"
---
# <a name="create-a-journal-entry-using-template"></a>Kirjauskansioviennin luonti mallin avulla

[!include [banner](../../includes/banner.md)]

Kirjatut kirjauskansion tositteet voidaan tallentaa tositemalleina. Ne voidaan kohdistaa uuteen kirjauskansion tositteeseen. Näissä toimintaohjeissa käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > kirjanpito > kirjauskansioviennit > Yleiset kirjauskansiot**.
2. Napsauta **Toimintoruudussa** **Uusi**. Tämä menettely käynnistyy kirjauskansion tositteen luomisella ja kirjaamisella. Myös aiemmin kirjattu kirjauskansion tosite voidaan tallentaa mallina.  
3. Avaa haku valitsemalla **Nimi**-kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse **Rivit**.
7. Kirjoita arvo **Tilityyppi** -kenttään.
8. Kirjoita **Kuvaus**-kenttään arvo.
9. Kirjoita arvo kenttään **Debet**.
10. Valitse **Uusi**.
11. Kirjoita arvo **Tilityyppi** -kenttään.
12. Kirjoita **Kuvaus**-kenttään arvo.
13. Kirjoita arvo kenttään **Debet**.
14. Valitse **Uusi**.
14. Määritä **Tili**-kenttään haluamasi arvot.
15. Kirjoita **Kuvaus**-kenttään arvo.
16. Oikaise tositteen saldo syöttämällä arvo **Kredit**-kenttään.
17. Valitse **toimintoruudussa** **Kirjaa**.
18. Valitse **Toiminnot**.
19. Valitse **Tallenna tosite** -malli.
20. Tässä menettelyssä oletetaan, että tyyppi on **Prosenttimalli**. Valitse OK.
    - Prosentti: Tositteen summat muunnetaan prosenttikertoimiksi. Näin mikä tahansa summa voidaan kohdistaa, kun tositemalli valitaan.
    - Summa: Toteutuneet summat tallennetaan ja kohdistetaan.  
21. Valitse **Yleiset kirjauskansiot**.
22. Valitse **Uusi**.
23. Avaa haku valitsemalla **Nimi**-kentässä avattavan valikon painike.
24. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
25. Valitse **Rivit**.
26. Valitse **Toiminnot**.
27. Valitse **Valitse tositemalli**.
28. Etsi aiemmin luomasi malli. Valitse **OK**. Sinun on ehkä valittava **Edellinen vaihe** ja valittava sitten oikea malli, jos muita malleja on olemassa.  
29. Syötä **Summa**-kenttään tositteeseen kohdistettava summa. **Summa**-kenttä näytetään vain, jos tositemallin tyyppi on Prosentti.  
30. Valitse **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
