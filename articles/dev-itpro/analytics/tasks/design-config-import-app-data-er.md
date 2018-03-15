--- 
title: "Saapuvien asiakirjojen jäsennysmääritysten suunnittelu sovellustietojen päivitystä varten (ER)"
description: "Tässä menettelyssä näytetään, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan saapuvan sähköisen asiakirjan jäsentämistä varten."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 96c9397c6a83d61b679492f66f4aa6661f1f8621
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="design-configurations-to-parse-incoming-documents-for-application-data-updates-er"></a>Saapuvien asiakirjojen jäsennysmääritysten suunnittelu sovellustietojen päivitystä varten (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan saapuvan sähköisen asiakirjan jäsentämistä varten. Tässä menettelyssä tuodaan pakollisia ER-konfiguraatioita, jotka on luotu malliyritykselle Litware Inc. ja joita käytetään saapuvien sähköisten asiakirjojen jäsentämistä varten. ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista.

Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. 

Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla. Ennen kuin aloitat, lataa ja tallenna ohjeaiheessa Saapuvien asiakirjojen jäsentäminen sovellustietojen päivittämistä varten mainitut tiedostot (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents). Tiedostot: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.  
2. Valitse Raportointikonfiguraatiot.
    * Seuraavaa skenaariota käytetään näytettäessä ominaisuudet, joiden avulla jäsennetään saapuvia sähköisiä asiakirjoja, jotka ovat XML-muodossa: ERP-sovellus (Dynamics 365 for Finance and Operations) pyytää tietoja verkkopalvelulta (kuten http://efsta.org/ EFSTA-tilipalvelu) ja jäsentää saapuvat vastaukset sekä päivittää sovellustiedot vastaavasti. Jotta jäsentäminen tapahtuu tehokkaasti, käytössä on yksi ER-muoto odotettujen XML-muotoisten saapuvien asiakirjojen eri rakenteesta huolimatta.   

## <a name="import-and-review-er-configurations"></a>ER-konfiguraatioiden tuominen ja tarkistaminen
Tuo se ER-mallikonfiguraatio, joka sisältää saapuvan tiedoston tiedot tallentavan tietomalliesimerkin.  
1. Valitse Vaihto.
2. Valitse Lataa XML-tiedostosta.
    * Valitse Selaa ja valitse sitten EFSTA model.xml-tiedosto.  
3. Valitse OK.
4. Valitse puussa 'EFSTA model'.
5. Valitse Suunnittelutoiminto.
    * Tarkista tuodun tietomallin rakenne. Huomaa, että enumType-luettelointi on määritetty tunnistamaan seuraavat palveluvastausten tyypit: tapahtuman lähettämisen vahvistuksen hakeminen, edellisen lähetetyn tapahtuman tietojen hakeminen ja ei-tuettujen vastaustyyppien tunnistaminen.   
6. Laajenna puussa 'Response'.
    * Huomaa, että Vastaus-juurinimike määrittää, minkä tyyppisiä tietoja tuetusta palveluvastauksesta on otettava, jotta sovelluksen tiedot voidaan päivittää vastaavasti.   
7. Sulje sivu.
    * Tuo ER-muotokonfiguraatio, joka määrittää, miten saapuvat asiakirjat jäsennetään ER-tietomallin tietojen tallentamista varten.   
8. Valitse Vaihto.
9. Valitse Lataa XML-tiedostosta.
    * Valitse Selaa ja valitse sitten EFSTA format.xml-tiedosto.  
10. Valitse OK.
11. Laajenna puussa 'EFSTA model'.
12. Valitse puussa EFSTA model\EFSTA format.
13. Valitse Suunnittelutoiminto.
14. Valitse Laajenna tai tiivistä.
    * Huomaa, ett' CASE-muotoelementtiä käytetään juurena. Se sisältää kolme sisäkkäistä FILE-elementtiä, eli tämä muoto on suunniteltu jäsentämään eri muotoisia saapuvia tiedostoja.  
15. Valitse puussa Responses\Transaction completion\TraC.
    * Huomaa, että lähetetyn tapahtuman vastaus alkaa TraC-juurielementistä.   
16. Valitse puussa Responses\Last transaction request\Tra.
    * Huomaa, että edellisen lähetetyn tapahtuman vastaus alkaa Tra-juurielementistä.   
17. Valitse puussa Responses\Unexpected response\Text.
    * Kolmas FILE-elementti ja sisäkkäinen TEXT-elementti auttavat tunnistamaan muun tyyppisiä vastauksia, jotka eroavat yllä mainituista.   
18. Valitse Yhdistä muoto malliin.
    * Tämä mallin yhdistämismääritys sisältää tietovirran määrityksen. Jäsennetyn saapuvan asiakirjan tiedot tallennetaan tietomallin nimikkeiden avulla.  
19. Valitse Suunnittelutoiminto.
20. Laajenna puussa format.
21. Laajenna puussa format\Responses: Case(Responses).
    * Tarkista muoto-tietomallin rakenne. Huomaa, että kaikki kolme vastaustyyppiä tarjotaan erikseen.   
22. Valitse puussa format\Responses: Case(Responses)\aType.
    * Tietolkähteen nimike aType on lisätty osoittamaan vastaustyyppiä. Se on sidottu tietomallin nimikkeeseen Type.  
23. Valitse Vahvistukset-välilehti.
24. Valitse puussa 'Type = format.Responses.aType'.
    * Huomaa, että ER-tarkistus on määritetty niin, että se ilmoittaa käyttäjälle, jos vastauksen rakenne ei vastaa tapahtuman lähetyksen vahvistusta tai edellisen lähetetyn tapahtuman tietoja (ei-tuetun vastauksen tapaus).   
25. Sulje sivu.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Saapuvien tiedostojen jäsennystä varten määritetyn ER-muodon mallin yhdistämismäärityksen suorittaminen
Suorita luotu mallin yhdistämismääritys testausta varten. Tällöin näet, miten konfiguroitu ER-malli jäsentää saapuvat palveluvastaukset. Tässä vaiheessa käytetään erilaisia XML-tiedostoja eri tyyppisten verkkopalveluvastausten simuloimista varten.   
1. Avaa Response1.xml-tiedosto XML-lukuohjelmassa, kuten WWW-selaimessa. Huomaa, että tämä tiedosto sisältää suoritetun tapahtuman vahvistustiedot (TraC on juurielementti).   
2. Valitse Suorita.
    * Valitse Selaa ja valitse sitten Response1.xml-tiedosto.  
3. Valitse OK.
    * Tarkista aikaansaatu tuotos. Huomaa, että vastaustyyppi on tunnistettu ja jäsennetty oikein (ERModelEnumDataSourceHandler#EFSTA model#enumType#C tarkoittaa, että tapahtuma on suoritettu).   
    * Avaa Response2.xml-tiedosto XML-lukuohjelmassa. Huomaa, että tämä tiedosto sisältää tietoja edellisestä lähetetystä tapahtumasta (Tra on juurielementti).   
4. Valitse Suorita.
    * Valitse Selaa ja valitse sitten Response2.xml-tiedosto.  
5. Valitse OK.
    * Tarkista aikaansaatu tuotos. Huomaa, että vastaustyyppi on tunnistettu ja jäsennetty oikein (ERModelEnumDataSourceHandler#EFSTA model#enumType#R tarkoittaa, että järjestelmä on käynnistetty uudelleen).   
    * Avaa Response3.xml-tiedosto XML-lukuohjelmassa. Huomaa, että tämä tiedosto alkaa TraZ-juurinimikkeestä ja että tätä rakennetta ei ole määritetty ER-muodon avulla.   
6. Valitse Suorita.
    * Valitse Selaa ja valitse sitten Response3.xml-tiedosto.  
7. Valitse OK.
    * Tarkista aikaansaatu tuotos. Huomaa, että vastaustyyppi on tunnistettu ei-tuetuksi (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Vastaava sanoma on asetettu infolokiin (ER-tarkistusasetuksen mukaan). Suurinta osaa tietomallista ei ole täytetty.    
    * Avaa Response4.xml-tiedosto XML-lukuohjelmassa. Huomaa, että tämän tiedoston rakenne on lähes sama kuin onnistuneesti jäsennetyn Response1.xml-tiedoston rakenne. Vain juurielementin TraC sisäkkäisten elementtien järjestys on eri.   
8. Valitse Suorita.
    * Valitse Selaa ja valitse sitten Response4.xml-tiedosto.  
9. Valitse OK.
    * Tarkista aikaansaatu tuotos. Huomaa, että vastaustyyppi on tunnistettu ei-tuetuksi (ERModelEnumDataSourceHandler#EFSTA model#enumType#U)). Vastaava sanoma on asetettu infolokiin. Suurinta osaa tietomallista ei ole täytetty. Tämä johtuu siitä, että ER-muodon nykyinen asetus olettaa saapuvan tiedoston juurinimikkeen sisäkkäisten elementtien järjestyksen.   
10. Sulje sivu.
11. Valitse puussa Responses\Transaction completion\TraC.
12. Valitse Sisäkkäisten elementtien jäsentelyjärjestys -kentässä Mikä tahansa.
    * Valitse Sisäkkäisten elementtien jäsentelyjärjestys -kentän arvoksi Mikä tahansa. Tällöin tällä XML-juurinimikkeellä voidaan käyttää mitä tahansa sisäkkäisten elementtien järjestystä.  
13. Valitse Tallenna.
14. Valitse Yhdistä muoto malliin.
15. Valitse Suorita.
    * Valitse Selaa ja valitse sitten Response4.xml-tiedosto.  
16. Valitse OK.
    * Tarkista aikaansaatu tuotos. Huomaa, että vastaustyyppi on nyt tunnistettu oikein samanlaiseksi kuin Response1.xml-tiedostolla.  


