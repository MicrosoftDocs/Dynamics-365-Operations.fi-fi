--- 
title: "Lähetä myyntitilaukset ilman varastointia"
description: "Tässä opastuksessa käsitellään, miten myyntitilaus päivitetään, kun tuotteet on lähetetty asiakkaalle."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: a98e58b26432ee01e62d60f81a768f14568e34e4
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---
# <a name="ship-sales-orders-without-warehousing"></a>Lähetä myyntitilaukset ilman varastointia

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä opastuksessa käsitellään, miten myyntitilaus päivitetään, kun tuotteet on lähetetty asiakkaalle. Opastus koskee toteutustyönkulkua, jota ei ole määritetty varastonhallintaa varten (ei perus- eikä lisätason varastointiin), joten se ei edellytä tuotteen keräilyn rekisteröintiä ennen lähetystä. Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja. Molemmissa tapauksissa ennen tehtävän aloittamista varastoidulle tuotteelle on luotava myyntitilaus, jonka määrä on suurempi kuin 1. Kirjausvirheen välttämiseksi sinun on tarkistettava, että tuotteen varastossa oleva määrä tilaukseen valitussa toimipaikassa ja varastossa riittää kattamaan tilausmäärän.


## <a name="post-packing-slip-for-an-order"></a>Kirjaa tilauksen pakkausluettelo
1. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
2. Etsi ja valitse luettelossa tehtävää varten luotu tilaus.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse toimintoruudussa Kerää ja pakkaa.
5. Valitse Kirjaa pakkausluettelo.
6. Laajenna tai tiivistä Parametrit-osa.
7. Valitse Määrä-kentässä Kaikki.
    * Vaihtoehtoja ovat lisäksi Toimita nyt ja Keräilty. Jos tilausrivi toimitetaan osittain ja tilausrivin Toimita nyt -kentässä on määrä, valitaan Toimita nyt. Jos organisaation toteuttamistyönkulku sisältää keräilyn erillisenä, keräysluettelon hallitsemana ja rekisteröimänä prosessina, valitaan Keräilty.  
    * Tarkista, että Kirjaus-asetukseksi on valittu Kyllä.  
8. Valitse Tulosta pakkausluettelo -asetukseksi Kyllä.
    * Tälle kirjaukselle luotavat pakkausluettelot ovat Yhteenveto-välilehdessä. Jos toimitat yksittäisen tilauksen, pakkausluetteloita on yleensä yksi. Jos kyseiseen tilauksen rivit kuitenkin toimitetaan eri toimipaikoista, kirjaus jaetaan automaattisesti niin, että asiakirjoja on tarvittava määrä. Tämä on pakollinen ehto, jota ei voi muuttaa. Kirjaus jaetaan vastaavasti useisiin asiakirjoihin myös silloin, jos tilauksen rivit lähetetään eri toimitusosoitteisiin ja lähetyskäytäntö määrittää jaon pakolliseksi.  
9. Valitse Rivit-välilehdessä lähetettävän tilausrivin rivi.
10. Lisää Päivitä-kenttään luku, joka on pienempi kuin alkuperäinen määrä.
11. Valitse OK.
12. Valitse Kyllä.
13. Sulje sivu.
14. Valitse toimintoruudussa Asetukset.
15. Valitse Vaihda näkymä.
16. Valitse Otsikkonäkymä.
    * Jos kaikki tilauksen rivit on lähetetty kokonaisuudessa, tilauksen tila muuttuu avoimesta toimitetuksi.  
    * Tässä esimerkissä tilausrivi on toimitettu osittain. Tämän vuoksi vielä tilaus on edelleen avoinna.     
    * Asiakirjan tila -kentän asetuksena on Pakkausluettelo, koska vähintään yksi tilausriveistä on lähetetty.  
17. Valitse toimintoruudussa Yleiset.
18. Valitse Rivin määrä.
19. Sulje sivu.
20. Valitse toimintoruudussa Kerää ja pakkaa.
21. Valitse Pakkausluettelo.
    * Kaikki tilausta varten luodut pakkausluetteloasiakirjat ovat Pakkausluettelo-kirjauskansio-sivulla. Voit tarvittaessa tarkastella kunkin asiakirjan tietoja ja tulostaa ne.  


