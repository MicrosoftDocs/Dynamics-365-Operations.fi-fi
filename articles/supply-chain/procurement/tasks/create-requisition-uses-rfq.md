--- 
title: "Luo ehdotus, joka käyttää tarjouspyyntöä"
description: "Tässä oppaassa esitellään, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 14eed7982041b7af7dad5453b10f07f063ba1855
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Luo ehdotus, joka käyttää tarjouspyyntöä

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä oppaassa esitellään, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista. Tämän oppaan esimerkkiä voidaan käyttää USMF-yrityksen demotiedoilla, ja sinun on kirjauduttava järjestelmänvalvojana suorittaaksesi kaikki vaiheet. Tässä oppaassa tehtävät kuuluvat yleensä hankintojen asiantuntijoille.


## <a name="create-a-requisition"></a>Luo ehdotus
1. Valitse Hankinta > Ostoehdotukset > Itse luodut ostoehdotukset.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Kirjoita päivämäärä Vaadittu päivämäärä -kenttään.
5. Kirjoita päivämäärä Kirjauspäivä-kenttään.
6. Valitse OK.
7. Anna tai valitse Syy-kentässä arvo.
8. Valitse Lisää rivi.
9. Valitse Hankintaluokka-kenttään puussa oleva luokka ja valitse sitten OK.
10. Kirjoita arvo Tuotteen nimi-kenttään.
11. Kirjoita numero Määrä-kenttään.
12. Syötä tai valitse arvo Yksikkö-kenttään.
13. Valitse Tallenna.
14. Avaa valintaikkuna valitsemalla Työnkulku.
15. Valitse Lähetä.
16. Sulje sivu.
17. Valitse Lähetä.

## <a name="reassign-a-workflow-task"></a>Määritä työnkulkutehtävä uudelleen
    * Seuraava tehtävä on luoda tarjouspyyntö toimittajien tuotetarjouksia varten. USMF-esittelytiedoissa ostoehdotuksen työnkululle on määritetty sääntö, jos toimittajaa ei ole valittu tai rivin yksikköhinta on 0, tietylle työntekijälle määritetään tarjouspyynnön luomisen tehtävä. Voit jatkaa tämän oppaan seuraamista delegoimalla kyseisen tehtävän toiselle käyttäjälle (itsellesi). Voit tehdä tämän vain, jos olet kirjautunut sisään järjestelmänvalvojana  
1. Avaa valintaikkuna valitsemalla Työnkulku.
2. Valitse Näytä historia.
3. Päivitä sivu.
4. Laajenna Seurantatiedot -osa.
5. Valitse puusta "rivi, joka alkaa 'Rivin työnkulku käynnistetty'".
6. Valitse Näytä työnkulun tiedot.
7. Laajenna Työnimikkeet-osa.
8. Valitse Määritä uudelleen.
9. Valitse Järjestelmänvalvoja Käyttäjä-kentässä.
10. Valitse Määritä uudelleen.
11. Sulje sivu.
12. Sulje sivu.

## <a name="create-an-rfq"></a>Luo tarjouspyyntö
1. Päivitä sivu.
2. Valitse Tarjouspyynnön vastaus.
3. Valitse Ostava yritys -kenttään USMF.
    * Valitse sama yritys, joka on ehdotusrivillä.  
4. Merkitse valittu rivi luettelossa.
    * Jos ostoehdotuksessa on useita rivejä, valitse kaikki rivit, jotka haluat lisätä tarjouspyyntöön.  
5. Valitse OK.
6. Päivitä sivu.
7. Avaa tietoruutu ja laajenna liittyvien asiakirjojen osa.
    * Tietoruutu saattaa olla jo auki. Paikanna nuolikuvake, joka on Rivit-/Otsikko-vaihtopainikkeen oikealla puolella. Jos nuoli osoittaa oikealle, tietoruudun on jo avoinna. Vasemmalle osoittavasta nuolesta saat avattua tietoruudun.  
8. Napsauta Tarjouspyyntö-kentän linkkiä avataksesi juuri luodun tarjouspyynnön.
9. Napsauta otsikkoa.
10. ValitseLisää.
11. Anna tai valitse arvo Toimittajatili-kentässä.
12. ValitseLisää.
13. Anna tai valitse arvo Toimittajatili-kentässä.
14. Valitse Lähetä.
15. Valitse OK.
16. Napsauta Kirjoita vastaus -kohtaa.
17. Valitse toimintoruudussa Vastaa.
18. Napsauta Kopioi tiedot vastauskenttiin -kohtaa.
    * Tämä kopioi tarjouspyynnön tiedot, kuten määrän ja päivämäärät, vastaukseen.  
19. Syötä Yksikköhinta-kenttään numero.
    * Tämä on hinta, jonka olet saanut toimittajalta. Voit myös halutessasi kirjoittaa toimittajalta saamiasi lisätietoja.  
20. Valitse Hyväksy.
21. Valitse OK.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Tarkista, että hinta ja toimittaja on siirretty ehdotukseen
1. Sulje sivu.
2. Valitse Rivit.
3. Valitse Aiheeseen liittyviä tietoja.
4. Valitse Ostoehdotus.
5. Valitse tarjouspyyntöön siirretty rivi.
    * Tarkista, että hinta ja toimittaja on kopioitu ehdotukseen..  
6. Avaa valintaikkuna valitsemalla Työnkulku.
7. Valitse Valmis.
8. Sulje sivu.
9. Valitse Valmis.

