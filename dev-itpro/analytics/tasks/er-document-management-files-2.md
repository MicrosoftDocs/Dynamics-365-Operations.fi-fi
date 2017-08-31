--- 
title: "Tietomallin laajentaminen tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 92177f4653325f6a43c704097d8d5d54d0e15ba9
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Tietomallin laajentaminen tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 1: valmistele tietomalli)" -tehtäväoppaan vaiheet.

Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Laajentaa tietomallia niin, sen sisältämät tiedostonhallinnan tiedostot voi esittää
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Raportointikonfiguraatiot.
3. Laajenna puussa solmu "Customer invoice model".
4. Valitse puusta "Customer invoice model\Customer invoice model (custom)".
5. Valitse Suunnittelutoiminto.
6. Valitse puussa "Customer invoice(InvoiceCustomer)".
    * Tätä tietomallia laajennetaan, jotta sitä voi käyttää kaikissa tiedostoissa, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.  
7. Avaa valintaikkuna valitsemalla Uusi.
8. Kirjoita Nimi-kenttään "Laskun liitteet".
    * Laskujen liitteet  
9. Valitse Nimiketyyppi-kentässä Tietueluettelo.
10. ValitseLisää.
11. Avaa valintaikkuna valitsemalla Uusi.
12. Kirjoita Nimi-kenttään "Tiedostosisältö".
    * Tiedoston sisältö  
13. Valitse Nimiketyyppi-kenttään "Säilö".
14. ValitseLisää.
15. Avaa valintaikkuna valitsemalla Uusi.
16. Kirjoita Nimi-kenttään "Tiedoston nimi".
    * Tiedostonimi  
17. Valitse Nimiketyyppi-kentässä Merkkijono.
18. ValitseLisää.

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a>Uusien tietomallielementtien yhdistäminen Dynamics 365 for Finance and Operations, Enterprise editionin tietolähteisiin
1. Valitse Yhdistä malli tietolähteeseen.
2. Pikasuodattimen avulla voit suodattaa Määritys-kentän arvolla "InvoiceCustomer".
    * InvoiceCustomer  
    * Yhdistä uuden mallin elementit asianmukaisiin tietolähteisiin.  
3. Valitse Suunnittelutoiminto.
4. Valitse puussa solmu "Invoice attachments".
5. Laajenna puussa solmu "Invoice attachments".
6. Valitse puussa solmu "Invoice attachments\File name".
7. Valitse Muokkaa.
8. Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Valitse Tallenna.
10. Sulje sivu.
11. Valitse puussa solmu "Invoice attachments\File content".
12. Valitse Muokkaa.
13. Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Valitse Tallenna.
15. Sulje sivu.
16. Valitse puussa solmu "Invoice attachments".
17. Valitse Muokkaa.
18. Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Valitse Tallenna.
20. Sulje sivu.
21. Valitse Tallenna.
22. Sulje sivu.
23. Sulje sivu.
24. Sulje sivu.
25. Voit muuttaa tilaa valitsemalla Muuta.
26. Valitse Valmis.
27. Valitse OK.


