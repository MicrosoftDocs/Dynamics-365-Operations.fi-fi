--- 
title: "Maksukehotusjärjestyksen määrittäminen"
description: "Tämän tehtävän ohjauksen avulla luodaan maksukehotussarja."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 3b050d47910c146b9691e7aae5b4a1a847ce716e
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-collection-letter-sequence"></a>Maksukehotusjärjestyksen määrittäminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tämän tehtävän ohjauksen avulla luodaan maksukehotussarja. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan Luotonvalvonta > Asetukset > Määritä maksukehotusjärjestys.
2. Valitse Uusi.
3. Syötä Maksukehotussarja-kenttään sarjaa kuvaavan järjestyksen tunnus. Sitä käytetään kirjausprofiilin määrittämisessä.
4. Kirjoita arvo Kuvaus-kenttään.
    * Maksuehdot ovat valinnaisia. Jos syötät tähän arvon, maksukehotuksen perintälaskussa käytetään näitä maksuehtoja asiakkaan tietoihin tallennettujen maksuehtojen sijaan.  
5. Valitse Maksukehotuskoodi-kenttään ensimmäisenä lähetettävän maksukehotuksen koodi.
    * Ensimmäinen maksukehotus luodaan laskun eräpäivän, tämän rivin Päivät-kenttään syöttämäsi lisäajan ja muiden tälle riville syöttämiesi tietojen perusteella.  
6. Kirjoita arvo Kuvaus-kenttään.
    * Lisämaksun valuutan oletusarvo on asiakkaan valuutta. Tämä valuuttakoodi voi olla eri kuin laskun valuutta.  
7. Lisää järjestyksessä seuraavana lähetettävä maksukehotus valitsemalla Lisää.
    * Usein ensimmäinen maksukehotus toimii vain varoituksena. Voit lisätä lisämaksuja tarvittaessa.  
8. Valitse Maksukehotuskoodi-kentässä järjestyksessä seuraavana lähetettävä maksukehotus.
9. Kirjoita Kuvaus-kenttään arvo.
10. Valitse Päätili-kentässä lisämaksuissa käytettävä tuottotili.
11. Syötä lisämaksu, joka veloitetaan tämän maksukehotuksen kirjaamisen yhteydessä.
12. Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.
    * Valitse nimikkeen arvonlisäveroryhmä, jos lisämaksulle on laskettava arvonlisävero.  
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
14. Syötä maksukehotuksen lähettämiseksi vaadittava erääntynyt vähimmäissaldo.
15. Syötä sallittujen eräpäivän jälkeisten maksupäivien määrä.
    * Tämä on niiden eräpäivän jälkeisten päivien lukumäärä, joille maksukehotus voidaan luoda. Laskennassa käytettävä eräpäivä riippuu maksukehotuksen sijainnista maksukehotussarjassa: ⦁ Maksukehotuksen 1 lisäaika määritetään suhteessa laskun eräpäivään.  ⦁ Maksukehotuksen 2 ja sen jälkeisten maksukehotusten lisäaika määritetään suhteessa edellisen maksukehotuksen kirjaus- tai tulostuspäivämäärään. Tämä riippuu Myyntireskontran parametrit -sivun Päivitä maksukehotuskoodi -kentässä tehdystä valinnasta.  
16. Lisää sarjan viimeinen maksukehotus valitsemalla Lisää.
    * Voit lisätä maksukehotussarjaan enintään viisi maksukehotuskoodia.  
17. Valitse Maksukehotuskoodi-kentässä järjestyksessä seuraavana lähetettävä maksukehotus.
18. Kirjoita Kuvaus-kenttään arvo.
19. Määritä Päätili-kenttään haluamasi arvot.
20. Syötä Lisämaksu valuuttana -kenttään numero.
21. Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.
22. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
23. Syötä Erääntynyt vähimmäissaldo -kenttään numero.
24. Syötä Päivät-kenttään numero.
25. Lopeta asiakkaan lisätoimitukset ja laskutus valitsemalla tämä valintaruutu.
    * Voit poistaa tilin eston valitsemalla Asiakkaat-sivun Pidossa oleva laskutus ja toimitus -kenttään arvon Ei.  
26. Laajenna Huomautukset-pikavälilehti.
27. Kirjoita valitun maksukehotuskoodin maksukehotuksessa näkyvä teksti.
    * Huomautusruudun yläpuolella olevan Käännökset-valikon avulla voit kääntää tämän tekstin useille eri kielille.  

