---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 2 – Tietomallin laajentaminen)
description: Tässä artikkelissa käsitellään sähköisen raportoinnin (ER) muodon määrittämisestä käyttämään tiedostonhallinnan tiedostoja (liitteitä) ER-tuotoksissa. (Osa 2)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 9d0d87d23bcdf537d638502fb5217f32fd1b328e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290991"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 2 – Tietomallin laajentaminen)

[!include [banner](../../includes/banner.md)]

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

## <a name="map-new-data-model-elements-to-data-sources"></a>Yhdistä uudet tietomallielementit tietolähteisiin
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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
