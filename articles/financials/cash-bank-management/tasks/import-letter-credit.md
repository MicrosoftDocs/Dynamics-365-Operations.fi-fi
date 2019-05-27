---
title: Tuo remburssi
description: Tässä menettelyssä käsitellään tuontiremburssiprosessi.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d5539fbd17c880d8bbadd47444c9cc53fce039c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566291"
---
# <a name="import-letter-of-credit"></a>Tuo remburssi

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään tuontiremburssiprosessi. Seuraavat on määritettävä ennen menettelyn suorittamista: pankkilimiitit, kirjausprofiilit, pankin limiittisopimus ja toimittajan pankkitiedot.

Näissä toimintaohjeissa käytetään esittely-yritystä USMF.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Luo myyntitilaus, jossa on remburssi
1. Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.
2. Valitse Uusi.
3. Anna tai valitse arvo Toimittajatili-kentässä.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Laajenna Yleinen-osa.
7. Syötä tai valitse arvo Toimipaikka-kenttään.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Anna tai valitse Varasto-kentässä arvo.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Kirjoita päivämäärä Kirjauspäivä-kenttään.
12. Kirjoita päivämäärä Toimituspäivämäärä-kenttään.
    * Huomautus: Pankkitositteen tyyppi -kenttään on valittava arvo Remburssi.  
13. Valitse OK.
14. Syötä tai valitse arvo Nimiketunnus-kentässä.
15. Etsi haluamasi tietue luettelosta ja valitse se.
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
17. Laajenna Rivin erittely -osa.
18. Valitse Toimitus-välilehti.
19. Kirjoita päivämäärä Toimituspäivämäärä-kenttään.
20. Kirjoita päivämäärä Vahvistettu toimituspäivämäärä-kenttään.
21. Syötä Yksikköhinta-kenttään numero.
    * Määritä remburssin tiedot.  
22. Valitse toimintoruudussa Hallitse.
23. Valitse Remburssi/tuontiperintä.
24. Anna päivämäärä ja kellonaika Hakemuksen päivämäärä -kenttään.
    * Tarkista, että Pankkitili-kentässä on aktiivinen, käyttöpäivämäärään perustuva oletuspankkitili.  
25. Kirjoita arvo Pankkitositteen numero -kenttään.
26. Anna päivämäärä ja kellonaika Vastaanottopäivä -kenttään.
27. Laajenna Pankkitosite-osa.
28. Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.
29. Laajenna Pankin tiedot -osa.
30. Anna tai valitse Neuvova pankki -kentässä arvo.
31. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
32. Valitse Tallenna.
33. Valitse Hae ostotilauksen lähetykset.
34. Sulje sivu.
35. Valitse toimintoruudussa Osta.
36. Valitse Vahvista.
37. Valitse toimintoruudussa Hallitse.
38. Valitse Remburssi/tuontiperintä.
39. Valitse Prosessi.
40. Valitse Vahvista.
    * Tarkista, että limiittisaldo pienentää ostotilauksen summaa.  Tässä esimerkissä ostosumma = 500,00, tositteen limiitti = 10 000,00, joten limiittisaldo = 9 500,00.  
41. Sulje sivu.
42. Syötä Yksikköhinta-kenttään numero.
43. Valitse Tallenna.
44. Valitse toimintoruudussa Osta.
45. Valitse Vahvista.
    * Muuta remburssia yksikköhinnan muutoksen takia.  
46. Valitse toimintoruudussa Hallitse.
47. Valitse Remburssi/tuontiperintä.
    * Muuta remburssia ostoyksikön hinnan muutoksen takia.  
48. Valitse Prosessi.
49. Valitse Muuta.
50. Valitse Poista.
51. Valitse Kyllä.
52. Valitse Hae ostotilauksen lähetykset.
53. Valitse Prosessi.
54. Valitse Vahvista.
    * Tarkista, että limiittisaldo pienentää ostotilauksen summaa.  Tässä esimerkissä muokattu ostosumma = 600,00, tositteen limiitti = 10 000,00, joten limiittisaldo = 9 400,00.  
55. Sulje sivu.

## <a name="post-packing-slip"></a>Kirjaa pakkausluettelo
1. Valitse toimintoruudussa Vastaanota.
2. Valitse Tuotteen vastaanotto.
3. Kirjoita PurchParmTable_Num-kenttään arvo.
    * Valitse remburssiviittauksen avulla luotu lähetyksen numero.  
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Kirjoita päivämäärä Tuotteen vastaanottopäivämäärä -kenttään.
6. Valitse OK.
7. Sulje sivu.
8. Sulje sivu.

## <a name="verify-import-letter-of-credit-status"></a>Tarkista Tuo remburssitapahtuma -tila
1. Valitse Maksuliikenteen hallinta > Luottokirjeet > Tuontiremburssi ja tuontiperintä.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Tarkista Tuo remburssitapahtuma -tila.     
4. Sulje sivu.
5. Sulje sivu.

## <a name="post-purchase-invoice"></a>Kirjaa ostolasku
1. Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.
    * Valitse remburssin avulla luotu ostotilaus.  
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse toimintoruudussa Lasku.
5. Valitse lasku.
6. Kirjoita arvo Numero-kenttään.
7. Anna tai valitse arvo Lähetyksen numero -kentässä.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Kirjoita päivämäärä Laskun päivämäärä -kenttään.
10. Valitse Päivitä täsmäytyksen tila.
11. Valitse Kirjaa.
12. Sulje sivu.
13. Sulje sivu.

## <a name="verify-import-letter-of-credit-status"></a>Tarkista Tuo remburssitapahtuma -tila
1. Valitse Maksuliikenteen hallinta > Luottokirjeet > Tuontiremburssi ja tuontiperintä.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Tarkista Tuo remburssi2.  
    * Varmista: Lähetyksen tila = laskutetun pankkilimiitin tiedot  
4. Valitse Näytä.
5. Valitse Tulosta hakemus.
6. Valitse OK.
    * Tarkista, että remburssianomus tulostetaan.  
7. Sulje sivu.
8. Sulje sivu.
9. Sulje sivu.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Kirjaa luodun remburssin sisältävän ostolaskun toimittajan maksukirjauskansio.
1. Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.
2. Valitse Uusi.
3. Syötä tai valitse arvo Nimi-kenttään.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Valitse Rivit.
6. Syötä Päivämäärään-kenttään päivämäärä.
7. Määritä Tili-kenttään haluamasi arvot.
8. Valitse Selvitä tapahtumat.
9. Laajenna Summat-osa.
10. Valitse vaihtoehto Näytä-kentässä.
    * Tarkista, että Pankkitositteen numero- ja Lähetyksen numero -kentät on päivitetty.  
11. Valitse Merkitse-valintaruutu.
12. Valitse OK.
13. Valitse Maksu-välilehti.
    * Tarkista, että Pankkitositteen numero- ja Lähetyksen numero -kentät on päivitetty.  
14. Valitse Kirjaa.
15. Sulje sivu.
16. Sulje sivu.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Tarkista Tuo remburssi -tila, kun lasku on maksettu
1. Valitse Maksuliikenteen hallinta > Luottokirjeet > Tuontiremburssi ja tuontiperintä.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Tarkista Tuo remburssitapahtuma -tila.   
4. Sulje sivu.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Tarkista pankkilimiitti ja käyttöraportti
1. Valitse Maksuliikenteen hallinta > Kyselyt ja raportit > Luottokirjeet tai takaukset > Pankkipalvelut ja käyttö -raportti.
2. Laajenna Tietueet-kohta ja sisällytä osaan.
3. Valitse Suodatin.
    * Määritä Ehdot-kenttä pakollisen pankkitilin avulla.  
4. Syötä tai valitse arvo Ehdot-kenttään.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse OK.
7. Valitse OK.
    * Tarkista tapahtumat sisältävä raportti.  
    * Tarkista, että raportin tapahtumissa on mainittu pankkitositteen numero, tositteen limiitti, käytetty summa ja limiittisaldo.  
8. Sulje sivu.

