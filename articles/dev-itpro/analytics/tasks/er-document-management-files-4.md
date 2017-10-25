--- 
title: "Muodon suorittaminen tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 419c3e305dfdd7d8612340b4a8e8e54e13c6362b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Muodon suorittaminen tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa. Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.

Jotta voit suorittaa nämä vaiheet, suorita ensin "ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 3: muodon luominen)" -ohjeen vaiheet.

Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


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

