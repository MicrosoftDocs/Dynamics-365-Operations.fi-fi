---
title: Konfiguraatioiden tarkistaminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia
description: Tässä aiheessa käsitellään raportoinnin määritysten suunnittelua luomaan upotettuja kuvia sisältäviä sähköisiä asiakirjoja. (Osa 1 – Parametrien määrittäminen).
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de815b363daa9135b50a2f5c9c4ac19e87b6b7ee
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751579"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Konfiguraatioiden tarkistaminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia

[!include [banner](../../includes/banner.md)]

Voit suorittaa nämä vaiheet, kun suoritat ensin ER Upotettuja kuvia sisältävien raporttien tekeminen MS Office -muodoissa (Osa 1: parametrien määrittäminen) -tehtäväoppaan vaiheet.

Näissä ohjeissa kerrotaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan, kun tavoitteena on luoda sähköisiä Microsoft Excel- ja Microsoft Word -asiakirjoja, jotka sisältävät upotettuja kuvia. Tässä esimerkissä tarkistetaan ER-konfiguraatiot malliyritykselle Litware Inc. 

Nämä ohjeet on tarkoitettu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Vaiheet voidaan suorittaa USMF-tietojoukon avulla.


## <a name="review-the-imported-data-model"></a>Tuodun tietomallin tarkistaminen
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Valitse puussa Sekkien malli.
3. Valitse Suunnittelutoiminto.
    * Tämä malli on suunniteltu maksusekkien esittämiseen yrityksen näkökulmasta ja tämän mallin yhdistämiseen sovelluksen tietolähteisiin. Tarkista tämä malli ER-toimintojen suunnitteluohjelman avulla. Ota huomioon esillä olevat mallielementtien määritteet, joita ovat esimerkiksi rakenne, nimi, kuvaus ja tietotyyppi.   
4. Laajenna puussa root.
5. Laajenna puussa root\cheques.
6. Laajenna puussa root\cheques.
7. Laajenna puussa root\cheques\attributes.
8. Laajenna puussa root\payer.
9. Valitse puussa root\istestrun.
10. Valitse puussa root\layout.
    * Tämän mallin asetteluelementti edustaa valitun pankkitilin tulostetun sekin lomakkeen asettelun tietoja. Se sisältää myös kaksi Säilö-tietotyypin solmua kuvien tallentamista varten.   
11. Laajenna puussa root\layout.
12. Valitse puussa root\layout\company logo.
13. Laajenna puussa root\layout\company logo.
14. Valitse puussa root\layout\company logo\image.
15. Valitse puussa root\layout\company logo\isprinted.
16. Valitse puussa root\layout\signature.
17. Laajenna puussa root\layout\signature.
18. Valitse puussa root\layout\signature\image.
19. Valitse puussa root\layout\signature\isprinted.
    * Ota huomioon, että kaksi kuvan tietomallielementtiä on sidottu sellaisen taulun kenttiin, jotka sisältävät yrityksen logon ja valtuutetun henkilön allekirjoituksen kuvat binaarisessa muodossa.  
20. Laajenna puussa root\layout\watermark.
21. Valitse Yhdistä malli tietolähteeseen.
22. Valitse Suunnittelutoiminto.
23. Laajenna puussa chequesselected.
24. Laajenna puussa layout.
25. Laajenna puussa layout\company logo.
26. Laajenna puussa layout\signature.
27. Laajenna puussa layout\watermark.
28. Vaihda Näytä tiedot käyttöön
    * Ota huomioon, että sekkien tietomallielementti on sidottu TmpChequePrintout-tauluun, joka sisältää suorituksen aikana käyttäjän tulostettavaksi valitsemien sekkien tietueita.   
29. Sulje sivu.
30. Sulje sivu.
31. Sulje sivu.

## <a name="review-the-imported-format"></a>Tuodun muodon tarkistaminen
1. Valitse puussa Model for cheques.
2. Valitse puussa Model for cheques\Cheques printing format.
3. Valitse Suunnittelutoiminto.
4. Napsauta Liitteet.
5. Valitse Avaa.
    * Avaa Excelissä liitetyn raportin malli.  
    * Tarkista sekkien tulostamisessa käytettävä liitetyn raportin Excel-malli. Mallissa on kaksi sekkiä sivulla. Se on suunniteltu tulostamaan sekit esitäytettyyn lomakkeeseen. Ota huomioon kaksi tyhjää upotettua kuvaa. Nämä tyhjät kuvat on tarkoitettu yrityksen logoa ja maksun hyväksyvän henkilön allekirjoitusta varten. Varmista, että kuvien nimet ovat Excelissä CompLogo ja SignatureImage.   
6. Sulje sivu.
7. Laajenna puussa Report.
8. Laajenna puussa Report\ChequeLines.
9. Valitse puussa Report\ChequeLines\CompLogo.
10. Vaihda Näytä tiedot käyttöön
    * Ota huomioon, että CompLogo-muodon solun elementti edustaa Excel-kohdetta, jonka avulla yrityksen logon kuvan täytetään raporttiin. Tämä muotoelementti on sidottu kuvan tietomallielementtiin, joka sisältää suorituksen aikana yrityksen logon kuvan binaarisessa muodossa.   
11. Valitse Yhdistämismääritys-välilehti.
12. Valitse Muokkaus on käytössä.
    * Ota huomioon, että voit ottaa CompLogo-muodon solun elementin pois käytöstä. Tällöin liitetty Excel-kuvaelementti piilottaa yrityksen logon luodussa raportissa. Jos käytössä oleva lauseke palauttaa TRUE-arvon ja määritetty sidonta ei tuo kuvaa, liitetty Excel-kuvaelementti näyttää Excel-malliin tallennetun kuvan.   
13. Sulje sivu.
14. Laajenna puussa labels: Container.
    * Jotkin esitäytetyn sekin lomakkeessa olevat nimiöt sisällytetään raporttiin, kun se luodaan testausta varten. Näitä nimiöitä ei kuitenkaan tulosteta todellisen tulostuksen aikana, koska ne ovat jo esitäytetyssä lomakkeessa.  
15. Sulje sivu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]