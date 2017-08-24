--- 
title: "Konfiguraation suunnitteleminen raporttien luomiseksi OpenXML-muodossa sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation, joka sisältää sähköisen asiakirjojen OPENXML-muodon luontimallin."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d552dbcf932813de4d060b4f2190cf388eddb1bf
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>Konfiguraation suunnitteleminen raporttien luomiseksi OpenXML-muodossa sähköistä raportointia (ER) varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation, joka sisältää sähköisen asiakirjojen OPENXML-muodon luontimallin. Tätä konfiguraatiota käytetään toimittajamaksujen käsittelyyn.



Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.



Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista. Sinulla on myös oltava Excel-tiedosto, joka tuodaan mallia luotaessa. Tiedosto on saatavilla sijainnissa https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx


## <a name="upload-the-payments-data-model-configuration"></a>Lataa maksujen tietomallin konfiguraatio
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Merkitse valittu rivi luettelossa.
    * Valitse malliyrityksen konfiguraation lähde Litware, Inc. Jos lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.  
3. Valitse Aseta aktiiviseksi.
4. Valitse Säilöt.
    * Jos operatiivisen resurssityypin säilö on käytettävissä, valitse se. Jos säilö on käytettävissä, ohita seuraavat, uuden säilön luomista koskevat vaiheet.  
5. Avaa valintaikkuna valitsemalla Lisää.
6. Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi Operatiiviset resurssit.
7. Valitse Luo säilö.
8. Valitse OK.
9. Valitse Avaa.
10. Valitse puussa solmu Maksumalli.
11. Valitse Tuo.
    * Tuo tämä tietomalli. Sitä käytetään uuden muotokonfiguraation tietolähteenä. Ohita tämä vaihe, jos tämä konfiguraatio on tuotu aiemmin.  
12. Valitse Kyllä.
13. Sulje sivu.
14. Sulje sivu.

## <a name="create-a-new-format-configuration"></a>Uuden muotokonfiguraation luominen
1. Valitse Raportointikonfiguraatiot.
2. Valitse puussa solmu Maksumalli.
3. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
4. Syötä Uusi-kenttään Muoto perustuu tietomalliin PaymentModel.
    * Luo muoto, joka perustuu PaymentModel-tietomalliin.  
5. Kirjoita Nimi-kentän arvoksi Laskentataulukkoraportin esimerkki.
    * Laskentataulukkoraportin esimerkki  
6. Kirjoita Kuvaus-kentän arvoksi Toimittajamaksujen laskentataulukkoraportin esimerkki.
    * Toimittajamaksujen laskentataulukkoraportin esimerkki  
7. Anna tai valitse Tietomallin määritelmä -kentän arvo.
    * Valitse CustomerCreditTransferInitiation-määritelmä.  
8. Valitse Luo konfiguraatio.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Suunnittele uusi asiakirja OPENXML-laskentataulukkomuodossa
1. Valitse puusta Maksumalli\Laskentataulukkoraportin esimerkki.
2. Valitse Suunnittelutoiminto.
3. Valitse toimintoruudussa Tuo.
4. Napsauta Tuo Microsoft Excelissä.
5. Napsauta Liitteet.
    * Liitä aiemmin luotu Excel-asiakirja mallina.  
6. Valitse Uusi.
7. Napsauta Tiedosto.
    * Osoita aiemmin luotu Excel-tiedosto.  
8. Sulje sivu.
9. Syötä tai valitse Malli-kentän arvo.
    * Valitse liitetty Excel-tiedosto käytettäväksi mallina.  
10. Valitse OK.
    * Huomaa, ER-muodon osat on luotu suunnittelumuodossa, joka perustuu viittaavan MS Excel -tiedoston rakenteeseen (nimetyt alueet).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Luo uusi tietolähde kokonaissummien laskentaan valuuttakoodien perusteella
1. Valitse Yhdistämismääritys-välilehti.
2. Avaa valintaikkuna valitsemalla Lisää juuri.
3. Valitse valikkopuussa Toiminnot\Ryhmittely.
4. Kirjoita Nimi-kenttään PaymentByCurrency.
    * PaymentByCurrency  
5. Napsauta Muokkaa ryhmittelyä.
6. Laajenna puussa solmu model.
7. Laajenna puussa solmu model\Payments.
8. Napsauta Lisää kenttä kohteeseen.
9. Napsauta Mitä ryhmään.
10. Laajenna puussa solmu model\Payments.
11. Valitse puussa solmu Malli\Maksut\Kuvaus.
12. Napsauta Lisää kenttä kohteeseen.
13. Napsauta Ryhmitellyt kentät.
14. Valitse puussa solmu Malli\Maksut\Ohjattu summa(InstructedAmount).
15. Napsauta Lisää kenttä kohteeseen.
16. Napsauta Koostekentät.
17. Valitse vaihtoehto Menetelmä-kentässä.
    * Valitse koostefunktioksi SUMMA.  
18. Kirjoita Nimi-kenttään TotalInstructuredAmount.
    * TotalInstructuredAmount  
19. Valitse Tallenna.
20. Sulje sivu.
21. Valitse OK.

## <a name="map-format-components-to-data-sources"></a>Määritä muodon komponentit tietolähteisiin
1. Laajenna puussa solmu model.
2. Laajenna puussa solmu model\Payments.
3. Laajenna puussa solmu Malli\Maksut\Aloittava osapuoli(InitiatingParty).
4. Valitse puussa solmu Malli\Maksut\Aloittava osapuoli(InitiatingParty)\Nimi.
5. Valitse puussa Excel\ReportHeader.
6. Valitse puussa Excel\ReportHeader\CompanyName.
7. Valitse Sido.
8. Laajenna puussa solmu model\Payments\Creditor.
9. Laajenna puussa solmu Malli\Maksut\Laskuttaja\Tunnus.
10. Laajenna puussa Malli\Maksut\Laskuttaja\Tunnus\Lähdetunnus(SourceID).
11. Valitse puussa Excel\PaymLines.
12. Valitse puussa Excel\PaymLines\VendAccountName.
13. Valitse Sido.
14. Valitse puussa solmu model\Payments\Creditor\Name.
15. Valitse puussa Excel\PaymLines\VendName.
16. Valitse Sido.
17. Laajenna puussa Malli\Maksut\Laskuttajan edustaja(CreditorAgent).
18. Valitse puussa solmu Malli\Maksut\Laskuttajan edustaja(CreditorAgent)\Nimi.
19. Valitse puussa Excel\PaymLines\Pankki.
20. Valitse Sido.
21. Valitse puussa solmu Malli\Maksut\Laskuttajan edustaja(CreditorAgent)\Reititysnumero(RoutingNumber).
22. Valitse puussa Excel\PaymLines\RoutingNumber.
23. Valitse Sido.
24. Laajenna puussa model\Payments\Creditor Account(CreditorAccount).
25. Laajenna puussa model\Payments\Creditor Account(CreditorAccount)\Identification.
26. Valitse puussa Malli\Maksut\Laskuttajan tili(CreditorAccount)\Tunnus\Numero.
27. Valitse puussa Excel\PaymLines\AccountNumber.
28. Valitse Sido.
29. Valitse puussa solmu Malli\Maksut\Ohjattu summa(InstructedAmount).
30. Valitse puussa Excel\PaymLines\Veloitus.
31. Valitse Sido.
32. Laajenna puussa solmu model\Payments\Creditor.
33. Laajenna puussa model\Payments\Creditor Account(CreditorAccount).
34. Laajenna puussa Malli\Maksut\Laskuttajan edustaja(CreditorAgent).
35. Valitse puussa solmu Malli\Maksut\Kuvaus.
36. Valitse puussa Excel\PaymLines\Valuutta.
37. Valitse Sido.
38. Laajenna puussa PaymentByCurrency.
39. Laajenna puussa PaymentByCurrency\ryhmitelty.
40. Valitse puussa PaymentByCurrency\ryhmitelty\Valuutta.
41. Laajenna puussa Excel\SummaryLines.
42. Valitse puussa Excel\SummaryLines\SummaryCurrency.
43. Valitse Sido.
44. Laajenna puussa PaymentByCurrency\koottu.
45. Valitse puussa PaymentByCurrency\koottu\TotalInstructuredAmount.
46. Valitse puussa Excel\SummaryLines\SummaryAmount.
47. Valitse Sido.
48. Valitse puussa solmu PaymentByCurrency.
49. Valitse puussa Excel\SummaryLines.
50. Valitse Sido.
51. Laajenna puussa solmu model\Payments.
52. Valitse puussa Excel\PaymLines.
53. Valitse Sido.
54. Valitse Tallenna.
55. Sulje sivu.

## <a name="use-the-created-configuration-for-payments-processing"></a>Käytä luotua määritystä maksujen käsittelyssä
1. Voit muuttaa tilaa valitsemalla Muuta.
2. Valitse Valmis.
3. Valitse OK.
4. Sulje sivu.
5. Sulje sivu.
6. Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.
7. Voit suodattaa Maksutapa-kentän pikasuodattimella käyttämällä Sähköinen-arvoa.
    * Sähköinen  
8. Valitse Muokkaa.
9. Laajenna Tiedostomuodot-osa.
10. Valitse Yleinen sähköinen raportointi -kentässä Kyllä.
11. Syötä Vie muotokonfiguraatio -kenttään arvo tai valitse arvo.
    * Valitse Laskentataulukkoraportin esimerkki -konfiguraatio.  
12. Valitse Tallenna.
13. Sulje sivu.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Käytä luotua konfiguraatiota maksukirjauskansioiden käsittelemisen testaamiseen
1. Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.
2. Valitse Uusi.
    * Luo uusi maksukirjauskansio.  
3. Kirjoita Nimi-kenttään VendPay.
    * VendPay  
4. Valitse Rivit.
5. Määritä Tili-kenttään arvo GB_SI_000001.
    * GB_SI_000001  
6. Aseta veloitusarvoksi 1000.
7. Valitse Uusi.
8. Määritä Tili-kenttään arvo GB_SI_000005.
    * GB_SI_000005  
9. Aseta veloitusarvoksi 2000.
10. Anna Valuutta-kentän arvoksi EUR.
    * Euro  
11. Määritä Vastatili-kenttään arvo GBSI OPER.
    * GBSI OPER  
12. Syötä Maksutapa-kentän arvoksi Sähköinen.
    * Sähköinen  
13. Valitse Tallenna.
14. Valitse Muodosta maksut.
15. Syötä Maksutapa-kentän arvoksi Sähköinen.
    * Sähköinen  
16. Kirjoita Tiedostonimi-kenttään Maksut.
    * Kirjoita esimerkiksi Maksut.  
17. Anna Pankkitili-kentän arvoksi GBSI OPER.
    * GBSI OPER  
18. Valitse OK.
19. Valitse OK.
    * Tarkista luotu taulukko, mukaan lukien maksutietorivit sekä jokaisen tässä maksusanomassa käytetyn valuuttakoodin kokonaissummat.  


