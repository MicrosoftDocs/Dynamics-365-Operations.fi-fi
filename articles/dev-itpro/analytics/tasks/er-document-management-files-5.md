--- 
title: "Tiedostonhallinnan tiedostojen käyttäminen muodon tuotoksissa muokkaamalla muotoa ja suorittamalla se"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b38f69fc169367aa56468b2c8f06b65fd1291c79
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs"></a>Tiedostonhallinnan tiedostojen käyttäminen muodon tuotoksissa muokkaamalla muotoa ja suorittamalla se

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa. Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.

Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 4: Aja muoto)" -menettelyn vaiheet.

Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Muokkaa muotoa täyttämään liitteet tuottaviin viesteihin binäärimuodossa.
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa solmu "Customer invoice model".
3. Laajenna puussa "Customer invoice model\Customer invoice model (custom)".
4. Valitse puussa "Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message".
5. Valitse Suunnittelutoiminto.
    * Laskuviesti täytetään Unicode-koodatulla XML-tiedoston tulosteella.  
6. Avaa valintaikkuna valitsemalla Lisää juuri.
7. Valitse puussa solmu Common\File.
8. Syötä Nimi-kenttään Xml-sanoma.
    * Xml-sanoma  
9. Syötä Koodaus-kenttään UTF-8.
    * UTF-8  
10. Valitse OK.
    * Konfiguroi tulosten luominen zip-tiedostona.  
11. Avaa valintaikkuna valitsemalla Lisää juuri.
12. Valitse puussa solmu Common\Folder.
13. Syötä Nimi-kenttään Zip-tulos.
    * Zip-tulos  
14. Valitse OK.
15. Valitse puussa Zip-tulos.
    * Lisää liitteet luonnin zip-tiedostoon tiedostoina, joilla on niiden alkuperäiset nimet ja tiedostopäätteet.  
16. Avaa valintaikkuna valitsemalla Lisää.
17. Valitse puussa solmu Common\File.
18. Kirjoita Nimi-kenttään Liitetiedosto.
    * Liitetiedosto  
19. Valitse OK.
20. Valitse puusta 'Zip output\Attached file'.
21. Avaa valintaikkuna valitsemalla Lisää.
22. Valitse puussa "Text\Base64".
23. Valitse OK.

## <a name="map-new-format-elements-to-data-model"></a>Uusien muotoelementtien yhdistäminen tietomalliin
1. Valitse Yhdistämismääritys-välilehti.
2. Laajenna puussa solmu model.
3. Laajenna puussa "model\Invoice attachments".
4. Valitse puusta 'Zip output\Attached file\Base64'.
5. Valitse puussa "model\Invoice attachments\File content".
6. Valitse Sido.
7. Valitse puusta 'Zip output\Attached file'.
8. Valitse Muokkaa tiedostonimeä.
9. Laajenna puussa solmu model.
10. Laajenna puussa "model\Invoice attachments".
11. Valitse puussa "model\Invoice attachments\File name".
12. Valitse Lisää tietolähde.
13. Valitse Tallenna.
14. Sulje sivu.
15. Valitse puussa solmu "model\Invoice attachments".
16. Valitse Sido.
17. Valitse Tallenna.
18. Sulje sivu.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Aja valitun laskun suunniteltu raportti
1. Valitse Suorita.
2. Laajenna Tietueet-kohta ja sisällytä () -osa.
3. Valitse Suodatin.
4. Valitse asiakkaan laskun kirjauskansion rivi sekä Myyntitilaus-kenttä.
5. Kirjoita Myyntitilaus-ehtokenttään tilausnumero 000148.
    * 000148  
6. Valitse OK.
7. Valitse OK.
    * Tarkista aikaansaatu tuotos. Huomaa, että XML-muotoisen laskuviestin lisäksi jokaiselle liitteelle on luotu yksi tiedosto. Liitetiedostot täytetään pakatulla, binäärimuotoisella tulosteella.  


