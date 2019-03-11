---
title: Aja muotoja tiedostonhallinnan tiedostojen käyttämiseksi ER-tuotoksissa
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e87dbb0fa890f4d554c3e2ff09566fb2b1f3206b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "364784"
---
# <a name="run-formats-to-use-document-management-files-in-er-output"></a>Aja muotoja tiedostonhallinnan tiedostojen käyttämiseksi ER-tuotoksissa

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa. Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.

Jotta voit suorittaa nämä vaiheet, suorita ensin "ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 3: muodon luominen)" -ohjeen vaiheet.

Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Lisää tarpeelliset liitteet yhden laskun myyntitilaukseen.
1. Siirry kohtaan Myyntireskontra > Laskut > Avoimet myyntilaskut.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Lasku-kenttää arvolla CIV-000148.
    * CIV-000148  
3. Napsauta valitun laskun linkkiä avataksesi sen.
    * CIV-000148  
4. Siirry eteenpäin napsauttamalla Myyntitilaus-kentän linkkiä.
    * 000148  
5. Valitse Rivit vai otsikko -kentästä vaihtoehto Otsikko.
    * Valitse Otsikko osoittamaan, että tämä on liitteiden lisäämisen kohde.  
6. Valitse Liitä.
    * Lisää joitakin liitetiedostoja tälle myyntitilaukselle. Käytä Tiedostonhallinnassa tuettuja tiedostotyyppejä (tiedostopäätteet DOCX, PDF, XML, JPG jne.). Etsi ja valitse liitettävät tiedostot, jotka käsitellään liittyvän laskun kanssa sähköisessä ER-viestissä.  
7. Valitse Uusi.
8. Napsauta Tiedosto.
9. Valitse Uusi.
10. Napsauta Tiedosto.
11. Sulje sivu.
12. Sulje sivu.
13. Sulje sivu.
14. Sulje sivu.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Aja valitun laskun suunniteltu raportti
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa solmu "Customer invoice model".
3. Laajenna puussa "Customer invoice model\Customer invoice model (custom)".
4. Valitse puussa "Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message".
5. Valitse Suorita.
6. Laajenna Tietueet-kohta ja sisällytä () -osa.
7. Valitse Suodatin.
8. Valitse asiakkaan laskun kirjauskansion rivi sekä Myyntitilaus-kenttä.
9. Kirjoita Ehdot-kenttään 000148.
    * Kirjoita ehdoksi "Sales order" -kenttään tilausnumero 000148.  
10. Valitse OK.
11. Valitse OK.
    * Tarkista aikaansaatu tuotos. Huomaa, että kullekin liitetiedostolle on luotu yksi XML-solmu. Liitteen sisältö lisätään XML-tuotteeseen MIME (base64) -tekstimuodossa.  

