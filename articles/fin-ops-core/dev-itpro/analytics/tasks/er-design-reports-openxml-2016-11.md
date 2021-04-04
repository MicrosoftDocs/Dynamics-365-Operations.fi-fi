---
title: ER OPENXML-muodossa luotavien raporttien määritysten suunnittelu (marraskuu 2016)
description: Tässä aiheessa käsitellään sellaisen uuden sähköisen raportoinnin määrityksen luontia, joka sisältää OPENXML-muotoisen sähköisten asiakirjojen luontimallin.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fac102f760de9c3e99bd69863570e6503620567
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567783"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER OPENXML-muodossa luotavien raporttien määritysten suunnittelu (marraskuu 2016)

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation, joka sisältää sähköisen asiakirjojen OPENXML-muodon luontimallin. Tätä konfiguraatiota käytetään toimittajamaksujen käsittelyyn.

Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.

Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista. Sinulla on myös oltava Excel-tiedosto, joka tuodaan mallia luotaessa. Tätä tiedostoa voi käyttää kohdasta [Maksuilmoituksen malli](https://go.microsoft.com/fwlink/?linkid=862266).


## <a name="upload-the-payments-data-model-configuration"></a>Lataa maksujen tietomallin konfiguraatio
1. Siirry kohtaan **siirtymisruutu > Moduulit > organisaation hallinto > Työtilat > Sähköinen raportointi**.
2. Valitse luettelossa malliyrityksen määrityksen lähde Litware, Inc. Jos lähde ei ole näkyvissä, suorita ensin kohdan [Konfiguraation lähteiden luominen ja sen merkitseminen aktiiviseksi](er-configuration-provider-mark-it-active-2016-11.md) vaiheet.
3. Valitse **Määritä aktiivinen**.
4. Valitse **Säilöt**. Jos operatiivisen resurssityypin säilö on käytettävissä, valitse se. Jos säilö on käytettävissä, ohita seuraavat, uuden säilön luomista koskevat vaiheet.  
5. Avaa valintaikkuna valitsemalla **Lisää**.
6. Syötä **Konfiguraatiosäilön tyyppi** -kentän arvoksi `Operations resourcesdd`.
7. Valitse **Luo säilö**.
8. Valitse **OK**.
9. Valitse **Avaa**.
10. Valitse puussa solmu **Maksumalli**.
11. Valitse **Tuo**. Tuo tämä tietomalli. Sitä käytetään uuden muotokonfiguraation tietolähteenä. Ohita tämä vaihe, jos tämä konfiguraatio on tuotu aiemmin.  
12. Valitse **Kyllä**.
13. Sulje sivut, kunnes palaat Sähköinen raportointi -sivulle.

## <a name="create-a-new-format-configuration"></a>Uuden muotokonfiguraation luominen
1. Valitse **Raportointikonfiguraatiot**.
2. Valitse puussa solmu **Maksumalli**.
3. Avaa valintaikkuna valitsemalla **Luo konfigurointi**.
4. Kirjoita **Uusi**- kenttään arvo `Format based on data model PaymentModel`. Luo muoto, joka perustuu PaymentModel-tietomalliin.
5. Syötä **Nimi**-kenttään `Sample worksheet report`. Laskentataulukkoraportin esimerkki  
6. Kirjoita **Kuvaus**-kenttään `Sample worksheet report for vendors' payments`. Toimittajamaksujen laskentataulukkoraportin esimerkki.  
7. Anna tai valitse **Tietomallin määritelmä** -kentän arvo. Valitse **CustomerCreditTransferInitiation**-määritelmä.  
8. Valitse **Luo konfiguraatio**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Suunnittele uusi asiakirja OPENXML-laskentataulukkomuodossa
1. Valitse puusta **Maksumalli\Laskentataulukkoraportin esimerkki**.
2. Valitse **Suunnittelu**.
3. Valitse toimintoruudussa **Tuo**.
4. Valitse **Tuo Excelistä**.
5. Valitse **Liitteet**. Liitä aiemmin luotu Excel-asiakirja mallina.  
6. Valitse **Uusi**.
7. Valitse **Tiedosto**. Osoita aiemmin luotu Excel-tiedosto.  
8. Sulje sivu.
9. Syötä tai valitse **Malli**-kentän arvo. Valitse liitetty Excel-tiedosto käytettäväksi mallina.  
10. Valitse **OK**. Huomaa, ER-muodon osat on luotu suunnittelumuodossa, joka perustuu viittaavan MS Excel -tiedoston rakenteeseen (nimetyt alueet).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Luo uusi tietolähde kokonaissummien laskentaan valuuttakoodien perusteella
1. Valitse **Yhdistämismääritys**-välilehti.
2. Avaa valintaikkuna valitsemalla **Lisää juuri**.
3. Valitse valikkopuussa **Toiminnot\Ryhmittely**.
4. Syötä **Nimi**-kenttään `PaymentByCurrency`.
5. Napsauta **Muokkaa ryhmittelyä**.
6. Laajenna puurakenteessa **model** ja valitse sitten **model\payments**.
7. Valitse **Lisää kenttä kohteeseen**.
8. Napsauta **Mitä ryhmään**.
9. Laajenna puurakenteessa **model\Payments** ja valitse sitten **model\Payments\Currency**.
10. Valitse **Lisää kenttä kohteeseen**.
11. Valitse **Ryhmitellyt kentät**.
12. Valitse puussa solmu **model\Payments\Instructed Amount(InstructedAmount)**.
13. Valitse **Lisää kenttä kohteeseen** ja valitse sitten **Koostekentät**.
14. Valitse vaihtoehto **Menetelmä**-kentässä. Valitse koostefunktioksi **SUMMA**.  
15. Syötä **Nimi**-kenttään `TotalInstructuredAmount`.
16. Valitse **Tallenna**.
17. Sulje sivu.
18. Valitse **OK**.

## <a name="map-format-components-to-data-sources"></a>Määritä muodon komponentit tietolähteisiin
1. Valitse puussa **model\Payments\Initiating Party(InitiatingParty)\Name** ja **Excel\ReportHeader\CompanyName**.
2. Valitse **Sido**.
3. Valitse puussa **model\Payments\Creditor\Identification\Source ID(SourceID)** ja **Excel\PaymLines\VendAccountName**.
4. Valitse **Sido**.
5. Valitse puussa **model\Payments\Creditor\Name** ja **Excel\PaymLines\VendName**.
6. Valitse **Sido**.
7. Valitse puussa **model\Payments\Creditor Agent(CreditorAgent)\Name** ja **Excel\PaymLines\Bank**.
8. Valitse **Sido**.
9. Valitse puussa **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** ja **Excel\PaymLines\RoutingNumber**.
10. Valitse **Sido**.
11. Valitse puussa **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** ja **Excel\PaymLines\AccountNumber**.
12. Valitse **Sido**.
13. Valitse puussa **model\Payments\Instructed Amount(InstructedAmount)** ja **Excel\PaymLines\Debit**.
14. Valitse **Sido**.
15. Valitse puussa **model\Payments\Currency** ja **Excel\PaymLines\Currency**.
16. Valitse **Sido**.
17. Valitse puussa **PaymentByCurrency\grouped\Currency** ja **Excel\SummaryLines\SummaryCurrency**.
18. Valitse **Sido**.
19. Valitse puussa **PaymentByCurrency\aggregated\TotalInstructuredAmount** ja **Excel\SummaryLines\SummaryAmount**.
20. Valitse **Sido**.
21. Valitse puussa **PaymentByCurrency** ja **Excel\SummaryLines**.
22. Valitse **Sido**.
23. Valitse puussa **model\Payments** ja **Excel\PaymLines**.
24. Valitse **Sido**.
25. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="use-the-created-configuration-for-payments-processing"></a>Käytä luotua määritystä maksujen käsittelyssä
1. Valitse **Muutoksen tila**.
2. Valitse **Valmis**.
3. Valitse **OK**.
4. Siirry kohtaan **Siirtymisruutu > Moduulit > Ostoreskontra >Maksujen asetukset > Maksutavat**.
5. Voit suodattaa **Maksutapa**-kentän pikasuodattimella käyttämällä **Sähköinen**-arvoa.
6. Valitse **Muokkaa**.
7. Laajenna **Tiedostomuodot**-osa.
8. Valitse **Yleinen sähköinen raportointi** -kentässä **Kyllä**.
9. Syötä **Vie muotokonfiguraatio** -kenttään arvo tai valitse arvo. Valitse **Laskentataulukkoraportin esimerkki** -konfiguraatio.  
10. Valitse **Tallenna**.
11. Sulje sivu.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Käytä luotua konfiguraatiota maksukirjauskansioiden käsittelemisen testaamiseen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Maksut > Maksukirjauskansio**.
2. Luo uusi maksukirjauskansio valitsemalla **Uusi**.
3. Kirjoita **Nimi**-kenttään **VendPay**.
4. Valitse **Rivit**.
5. Määritä **Tili**-kentässä arvo `GB_SI_000001`.
6. Aseta **Debet**-kentän arvoksi `1000`.
7. Valitse **Uusi**.
8. Määritä **Tili**-kentässä arvo `GB_SI_000005`.
9. Aseta **Debet**-kentän arvoksi `2000`.
10. Anna **Valuutta**-kentän arvoksi `EUR`.
11. Määritä **Vastatili**-kenttään arvo `GBSI OPER`.
12. Kirjoita **Maksutapa**-kenttään `Electronic`.
13. Valitse **Tallenna**.
14. Valitse **Muodosta maksut**.
15. Kirjoita **Maksutapa**-kenttään `Electronic`.
16. Kirjoita **Tiedoston nimi** -kenttään `Payments`.
17. Anna **Pankkitili**-kentän arvoksi `GBSI OPER`.
18. Valitse ensin **OK** ja sitten uudelleen **OK**. Tarkista luotu taulukko, mukaan lukien maksutietorivit sekä jokaisen tässä maksusanomassa käytetyn valuuttakoodin kokonaissummat.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]