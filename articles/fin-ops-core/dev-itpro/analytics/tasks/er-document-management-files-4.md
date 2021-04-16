---
title: ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 4 – muodon suorittaminen)
description: Tässä aiheessa käsitellään sähköisen raportoinnin muodon määrittämisestä käyttämään tiedostonhallinnan tiedostoja ER-tuotoksissa. (Osa 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a7c9705d8b53ef13cd3faf13290f3f1b1d1c43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749114"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a>ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 4 – muodon suorittaminen)

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]