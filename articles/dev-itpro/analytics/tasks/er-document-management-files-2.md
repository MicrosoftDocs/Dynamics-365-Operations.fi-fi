---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 2 – Tietomallin laajentaminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb4c58dc86a159a70634c05408a8db471ebcae4c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544799"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a>ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 2: tietomallin laajennus)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 1: valmistele tietomalli)" -tehtäväoppaan vaiheet.

Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


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

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a>Yhdistä uuden tietomallin elementit Dynamics 365 for Finance and Operations, Enterprise Editionin tietolähteisiin.
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

