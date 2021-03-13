---
title: Konfiguraatioiden suunnitteleminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia
description: Tässä aiheessa käsitellään määritysten suunnittelua luomaan upotettuja kuvia sisältäviä Excel- ja Word-muotoisia sähköisiä asiakirjoja.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b60ed6b07851c44ceb4b8f313bc65f04b802e646
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093667"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Konfiguraatioiden suunnitteleminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia

[!include [banner](../../includes/banner.md)]

ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista. Näissä ohjeissa kerrotaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan, kun tavoitteena on luoda Microsoft Excel- ja Word -asiakirjoja, jotka sisältävät upotettuja kuvia. Tässä menettelyssä luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa USMF-tietojoukon avulla. Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Ennen kuin aloitat, lataa ja tallenna kohdan [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](../electronic-reporting-embed-images-shapes.md) tiedostot. Tiedostot ovat seuraavat: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png ja Cheque template Word.docx.

## <a name="verify-prerequisites"></a>Edellytysten tarkistaminen  
 1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.  
 2. Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.   
 3. Valitse Raportointikonfiguraatiot.  
 
## <a name="add-a-new-er-model-configuration"></a>Uuden ER-mallimäärityksen lisääminen  
 1. Uuden mallin luomisen sijaan voit ladata ER-mallimääritystiedoston (Model for cheques.xml), jonka tallensit aiemmin. Tämä tiedosto sisältää maksusekkien tietomalliesimerkin ja tietomallin Dynamics 365 for Operations -sovelluksen vastaavuuden tieto-osiin.   
 2. Valitse Versiot-pikavälilehdessä Vaihda.   
 3. Valitse Lataa XML-tiedostosta.  
 4. Valitse Selaa ja valitse sitten Model for cheques.xml.   
 5. Valitse OK.  
 6. Ladattua mallia käytetään tietolähteenä luotaessa asiakirjoja, jotka sisältävät Excelin tai Wordin kuvia.  

## <a name="add-a-new-er-format-configuration"></a>Uuden ER-muotokonfiguraation lisääminen  
 1. Uuden muodon luomisen sijaan voit ladata ER-muotomääritystiedoston (Cheques printing format.xml), jonka tallensit aiemmin. Tämä tiedosto sisältää sekkien tulostamisen muodon malliasettelun. Se käyttää esitäytettyä lomaketta ja tämän muodon vastaavuutta Model for cheques -tiedoston tietomalliin.   
 2. Valitse Vaihto.  
 3. Valitse Lataa XML-tiedostosta.  
 4. Valitse Selaa ja valitse sitten tiedosto Cheques printing format.xml.   
 5. Valitse OK.  
 6. Valitse puussa Model for cheques.  
 7. Valitse puussa Model for cheques\Cheques printing format.  
 8. Ladattua muotoa käytetään luotaessa asiakirjoja, jotka sisältävät Excelin tai Wordin kuvia.   

## <a name="configure-er-user-parameters"></a>ER-käyttäjän parametrien määrittäminen  
 1. Valitse toimintoruudussa Konfiguroinnit.  
 2. Valitse Käyttäjän parametrit.  
 3. Valitse Suorita asetukset -kentässä Kyllä.  
  Ota käyttöön Suorita luonnos -osoitin, kun haluat aloittaa valitun mallin luonnosversiolla valmiin version sijaan.  
 4. Valitse OK.  

## <a name="configure-cash--bank-management-parameters"></a>Määritä Maksuliikennetiedot  
 1. Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.  
 2. Pikasuodattimen avulla voit suodattaa Pankkitili-kentän USMF OPER -arvon mukaan.  
 3. Valitse toimintoruudussa Määritä.  
 4. Valitse Tarkista.  
 5. Laajenna osa Asetukset.  
 6. Valitse Muokkaa.  
 7. Valitse Yrityksen logo -kentässä Kyllä.  
 8. Valitse Yrityksen logo.  
 9. Valitse Muuta.  
 10. Valitse Selaa ja valitse sitten aiemmin ladattu tiedosto Company logo.png.   
 11. Valitse Tallenna.  
 12. Sulje sivu.  
 13. Laajenna Allekirjoitus-osa.  
 14. Valitse Tulosta ensimmäinen allekirjoitus -kentässä Kyllä.  
 15. Valitse Muuta.  
 16. Valitse Selaa ja valitse sitten aiemmin ladattu tiedosto Signature image.png.   
 17. Laajenna Kopiot-osa.  
 18. Valitse vaihtoehto Vesileima-kentässä.  
 19. Valitse Yleinen sähköinen vientimuoto -kentässä Kyllä.  
 20. Valitse Sekkien tulostusmuoto -konfiguraatio.  
 21. Nyt valittua ER-muotoa käytetään sekkien tulostamisessa.  
 22. Valitse Liitä.  
 23. Valitse Uusi.  
 24. Napsauta Tiedosto.  
 25. Valitse Selaa ja valitse sitten aiemmin ladattu tiedosto Signature image 2.png.   
 26. Sulje sivu.  
 27. Sulje sivu.  
 28. Sulje sivu.  
 29. Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.  
 30. Valitse Kyllä kohdassa Salli esilaskun luonti käytöstä poistetuille pankkitileille: kenttä.  
 31. Valitse Tallenna.  
 32. Sulje sivu.  
