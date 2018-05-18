--- 
title: "Muodon muokkaaminen käyttämällä uudelleen Microsoft Excel -mallia sähköistä raportointia (ER) varten"
description: "Tämän menettelyn vaiheiden suorittaminen edellyttää, että ER Määrityksen suunnittelu OPENXML-muotoisten raporttien luomiseksi -menettelyn vaiheet on suoritettu ensin."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: 2f35727376812b0de428ce929ebe0d33bc497984
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a>Muodon muokkaaminen käyttämällä uudelleen Microsoft Excel -mallia sähköistä raportointia (ER) varten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämän menettelyn vaiheiden suorittaminen edellyttää, että ER Määrityksen suunnittelu OPENXML-muotoisten raporttien luomiseksi -menettelyn vaiheet on suoritettu ensin.

Menettelyssä kerrotaan, miten sähköisen raportoinnin (ER) muodon määrityksiä muokataan käyttämällä uudelleen muokattua Microsoft Excel -mallia. Tässä menettelyssä tuodaan muokattu Excel-malli ER-muotokonfiguraatioihin, jotka on luotu malliyritykselle Litware Inc. ja joita käytetään sähköisten asiakirjojen luomisessa. Nämä ohjeet on tarkoitettu käyttäjille, joilla on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa GBSI-tietojoukon avulla. Lataa ja tallenna ennen aloittamista SampleVendPaymWsReport2.xlsx-tiedosto, joka on mainittu ohjeaiheessa Sähköisen raportoinnin muodon muokkaaminen käyttämällä uudelleen Excel-mallia (modify-electronic-reporting-format-reapply-excel-template/).

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.  

## <a name="select-the-er-format"></a>Valitse ER-muoto
1. Valitse Raportointikonfiguraatiot.
2. Laajenna puussa solmu Payment model.
3. Valitse puusta Maksumalli\Laskentataulukkoraportin esimerkki.
4. Napsauta Liitteet.
    * Ota huomioon, että Excel-tiedostoa SampleVendPaymWsReport.xlsx käytetään tällä hetkellä maksukirjauskansion käsittelyn mallina.   
5. Valitse Avaa.
    * Valitse Avaa, kun haluat katsoa Excel-mallin asettelua.  
    * Tarkista malli. Ota huomioon, että se sisältää tällä hetkellä seuraavat tiedot kunkin maksurivin osalta: toimittajan tilinumero, toimittajan nimi, pankki, reititysnumero, tilinumero, hyvitys, veloitus ja valuutta. Tässä esimerkissä halutaan laajentaa luetteloa lisäämällä maksupäivämäärän tiedot.   
6. Sulje sivu.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Käytä uutta Excel-mallia uudelleen ER-muodossa
1. Valitse Suunnittelutoiminto.
    * Avaa valitun ER-muodon luonnosversio muokkausta varten.  
2. Valitse toimintoruudussa Tuo.
3. Valitse Päivitä Excelistä.
    * Valitse Päivitä malli ja valitse sitten tiedosto (SampleVendPaymWsReport2.xlsx).  
    * Valitse Päivitä malli ja siirry aiemmin ladattuun SampleVendPaymWsReport2.xlsx-tiedostoon.  
4. Valitse OK.
    * SampleVendPaymWsReport2.xlsx-malli on otettu käyttöön. ER-muodon rakenne on synkronoitu sen mallin sisällön kanssa, jonka elementit on lisätty ER-muotoon. Kaikki ER-muodot, jotka eivät sisälly malliin, poistetaan muodon määrityksestä.  
5. Valitse puussa Excel.
    * Ota huomioon, että Malli-kenttä sisältää nyt uuden mallin viitteen.   
6. Napsauta Liitteet.
7. Valitse Avaa.
    * Valitse Avaa, kun haluat katsoa muokatun Excel-mallin asettelua.  
    * Tarkista malli. Ota huomioon, että se sisältää maksupäivämäärän rivin.   
8. Sulje sivu.
9. Laajenna puussa Excel.
10. Valitse puussa Excel\PaymLines.
11. Valitse puussa Excel\PaymLines\PaymDate.
    * Ota huomioon, että ER-muoto sisältää nyt yhden lisänimikkeen. PaymDate-solu on lisätty Excel-malliin.  
12. Valitse Yhdistämismääritys-välilehti.
13. Laajenna puussa solmu model.
14. Laajenna puussa solmu model\Payments.
15. Valitse puussa solmu model\Payments\Transaction date(TransactionDate).
16. Valitse Sido.
    * Määritä, mitkä tiedot lisätään uuteen soluun suorituksen aikana.  
17. Valitse Tallenna.
18. Sulje sivu.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Ota käyttöön ER-muodon muokattu luonnosversio maksukirjauskansion käsittelyssä
1. Valitse toimintoruudussa Konfiguroinnit.
2. Valitse Käyttäjän parametrit.
3. Valitse Suorita asetukset -kentässä Kyllä.
4. Valitse OK.
5. Valitse Muokkaa.
6. Valitse Suorita luonnos -kentässä Kyllä.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Käytä ER-muodon muokattua luonnosversiota maksukirjauskansion käsittelyssä
    * Tarkista luotu laskentataulukko ja maksurivien uudet maksupäivämäärien tiedot.  


