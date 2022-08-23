---
title: Konfiguraatioiden suunnitteleminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia
description: Tässä artikkelissa käsitellään määritysten suunnittelua luomaan upotettuja kuvia sisältäviä Excel- ja Word-muotoisia sähköisiä asiakirjoja.
author: kfend
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13cb3cac7369bc68e8b33e4c01f0de0e43689ecb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290331"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Konfiguraatioiden suunnitteleminen raporttien luomiseksi Office-muodoissa, joissa on upotettuja kuvia

[!include [banner](../../includes/banner.md)]

ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista. Näissä ohjeissa kerrotaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan, kun tavoitteena on luoda Microsoft Excel- ja Word -asiakirjoja, jotka sisältävät upotettuja kuvia. Tässä menettelyssä luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa USMF-tietojoukon avulla. Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Ennen aloittamista seuraavat tiedostot täytyy ladata ja tallentaa: 

| kuvaus                                          | Tiedostonimi                   |
|------------------------------------------------------|-----------------------------|
| ER-tietomallin konfigurointi                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER-muodon konfigurointi                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Yrityksen logokuva                                   | [Yrityksen logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Allekirjoituksen kuva                                      | [Allekirjoituksen kuva.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Vaihtoehtoisen allekirjoituksen kuva                          | [Allekirjoituksen kuva 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word -malli sekkien tulostukseen  | [Sekkimalli Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
