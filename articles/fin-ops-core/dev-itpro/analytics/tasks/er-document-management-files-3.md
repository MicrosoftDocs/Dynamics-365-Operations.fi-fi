---
title: ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 3 – muodon luominen)
description: Tässä artikkelissa käsitellään sähköisen raportoinnin muodon määrittämisestä käyttämään tiedostonhallinnan tiedostoja ER-tuotoksissa. (Osa 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6957b314f8120f3cd240336f93dd6fbb43132759
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908323"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 3 – muodon luominen)

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 2: laajenna tietomallia)" -menettelyn vaiheet.

Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


## <a name="create-a-format-to-process-invoices"></a>Uuden muodon luonti laskujen käsittelyä varten
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Raportointikonfiguraatiot.
3. Laajenna puussa solmu "Customer invoice model".
4. Valitse puusta "Customer invoice model\Customer invoice model (custom)".
    * Luot muodon, jolla luodaan sähköisiä viestejä tiedostoista, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.  
5. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
6. Syötä Uusi-kenttään Muoto perustuu tietomalliin Myyntilaskumalli (mukautettu).
7. Kirjoita Nimi-kenttään "Sähköisen laskun malliviesti".
    * Sähköisen laskun esimerkkisanoma  
8. Anna tai valitse Tietomallin määritelmä -kentän arvo.
    * InvoiceCustomer  
9. Valitse Luo konfiguraatio.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Muodon suunnittelu, joka täyttää liitteet viestiin MIME-muodossa
1. Valitse Suunnittelutoiminto.
2. Avaa valintaikkuna valitsemalla Lisää juuri.
3. Valitse puussa solmu XML\Element.
4. Kirjoita Nimi-kenttään "Lasku".
    * Lasku  
5. Valitse OK.
6. Avaa valintaikkuna valitsemalla Lisää.
7. Valitse puussa solmu XML\Attribute.
8. Syötä Nimi-kenttään "SalesOrder".
    * SalesOrder  
9. Valitse OK.
10. Valitse Lisää määrite.
11. Syötä Nimi-kenttään "InvoiceNumber".
    * InvoiceNumber  
12. Valitse OK.
13. Valitse Lisää määrite.
14. Kirjoita Nimi-kenttään "InvoiceAmount".
    * InvoiceAmount  
15. Valitse OK.
16. Avaa valintaikkuna valitsemalla Lisää.
17. Valitse puussa solmu XML\Element.
18. Kirjoita Nimi-kenttään "EnclosedDocs".
    * EnclosedDocs  
19. Valitse OK.
20. Valitse puusta 'Invoice\EnclosedDocs'.
21. Valitse Lisää elementti.
22. Kirjoita Nimi-kenttään "Document".
    * Asiakirja  
23. Valitse OK.
24. Valitse puusta "Invoice\EnclosedDocs\Document".
25. Avaa valintaikkuna valitsemalla Lisää.
26. Valitse puussa solmu XML\Attribute.
27. Kirjoita Nimi-kenttään "FileName".
    * FileName  
28. Valitse OK.
29. Avaa valintaikkuna valitsemalla Lisää.
30. Valitse puussa solmu XML\Element.
31. Kirjoita Nimi-kenttään "FileContent".
    * FileContent  
32. Valitse OK.
33. Valitse puusta "Invoice\EnclosedDocs\Document\FileContent".
34. Avaa valintaikkuna valitsemalla Lisää.
35. Valitse puussa "Text\Base64".
36. Valitse OK.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Yhdistä muodon elementit tietomalliin tietolähteenä
1. Valitse puusta "Invoice\SalesOrder".
2. Valitse Yhdistämismääritys-välilehti.
3. Laajenna puussa solmu model.
4. Valitse puussa "model\Sales order number(SalesId)".
5. Valitse Sido.
6. Valitse puusta "Invoice\InvoiceNumber".
7. Laajenna puussa "model\Base invoice(InvoiceBase)".
8. Valitse puusta "model\Base invoice(InvoiceBase)\Invoice number(Id)".
9. Valitse Sido.
10. Valitse puusta "Invoice\InvoiceAmount".
11. Valitse puusta "model\Base invoice(InvoiceBase)\Invoice amount(Amount)".
12. Valitse Sido.
13. Laajenna puussa "model\Invoice attachments".
14. Valitse puussa "model\Invoice attachments\File content".
15. Valitse puusta "Invoice\EnclosedDocs\Document\FileContent\Base64".
16. Valitse Sido.
17. Valitse puussa "model\Invoice attachments\File name".
18. Valitse puusta "Invoice\EnclosedDocs\Document\FileName".
19. Valitse Sido.
20. Valitse puussa solmu "model\Invoice attachments".
21. Valitse puusta "Invoice\EnclosedDocs\Document".
22. Valitse Sido.
23. Valitse Tallenna.
24. Sulje sivu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]