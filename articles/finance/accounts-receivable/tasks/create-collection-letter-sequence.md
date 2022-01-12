---
title: Maksukehotusjärjestyksen määrittäminen
description: Tällä menettelyllä luodaan maksukehotusjärjestys.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adeae6e20a799165e086df28b92a1357e8f2f0d3
ms.sourcegitcommit: f82372b1e9bf67d055fd265b68ee6d0d2f10d533
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921196"
---
# <a name="create-a-collection-letter-sequence"></a>Maksukehotusjärjestyksen määrittäminen

[!include [banner](../../includes/banner.md)]

Tällä menettelyllä luodaan maksukehotusjärjestys. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Valitse siirtymisruudussa **Moduulit > Luotonvalvonta > Asetukset > Määritä maksukehotusjärjestys**.
2. Valitse **Uusi**.
3. Syötä **Maksukehotusjärjestys**-kenttään sarjaa kuvaavan järjestyksen tunnus. Sitä käytetään kirjausprofiilin määrittämisessä.
4. Kirjoita **Kuvaus**-kenttään arvo.  Maksuehdot ovat valinnaisia. Jos syötät tähän arvon, maksukehotuksen perintälaskussa käytetään näitä maksuehtoja asiakkaan tietoihin tallennettujen maksuehtojen sijaan.  
5. Valitse **Maksukehotuskoodi**-kenttään ensimmäisenä lähetettävän maksukehotuksen koodi. Ensimmäinen maksukehotus luodaan laskun eräpäivän, tämän rivin Päivät-kenttään syöttämäsi lisäajan ja muiden tälle riville syöttämiesi tietojen perusteella.  
6. Kirjoita **Kuvaus**-kenttään arvo. 
7. Maksun oletusvaluutta on yrityksen valuutta. Tämä valuuttakoodi voi olla eri kuin laskun valuutta.   
8. Lisää järjestyksessä seuraavana lähetettävä maksukehotus valitsemalla **Lisää**. Usein ensimmäinen maksukehotus toimii vain varoituksena. Voit lisätä lisämaksuja tarvittaessa.  
9. Valitse **Maksukehotuskoodi**-kentässä järjestyksessä seuraavana lähetettävä maksukehotus.
10. Valitse **Päätili**-kentässä lisämaksuissa käytettävä tuottotili.
11. Syötä lisämaksu, joka veloitetaan tämän maksukehotuksen kirjaamisen yhteydessä.
12. Avaa haku valitsemalla **Nimikkeen arvonlisäveroryhmä** -kentässä avattavan valikon painike. Valitse nimikkeen arvonlisäveroryhmä, jos lisämaksulle on laskettava arvonlisävero.  
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
14. Syötä **Erääntynyt vähimmäissaldo** -kenttään erääntynyt vähimmäissaldo, joka tarvitaan ennen maksukehotuksen lähettämistä.
15. Syötä sallittujen eräpäivän jälkeisten maksupäivien määrä **Päivää**-kenttään. Tämä on niiden eräpäivän jälkeisten päivien lukumäärä, joille maksukehotus voidaan luoda. Laskennassa käytettävä eräpäivä riippuu maksukehotuksen sijainnista maksukehotussarjassa:
    - Maksukehotuksen 1 lisäaika määritetään suhteessa laskun eräpäivään.
    - Maksukehotuksen 2 ja sen jälkeisten maksukehotusten lisäaika määritetään suhteessa edellisen maksukehotuksen kirjaus- tai tulostuspäivämäärään. Tämä riippuu Myyntireskontran parametrit -sivun Päivitä maksukehotuskoodi -kentässä tehdystä valinnasta.  
16. Lisää sarjan viimeinen maksukehotus valitsemalla **Lisää**. Voit lisätä maksukehotussarjaan enintään viisi maksukehotuskoodia.  
17. Valitse **Maksukehotuskoodi**-kentässä järjestyksessä seuraavana lähetettävä maksukehotus.
18. Kirjoita **Kuvaus**-kenttään arvo.
19. Määritä **Päätili**-kenttään haluamasi arvot.
20. Syötä **Lisämaksu valuuttana** -kenttään numero.
21. Avaa haku valitsemalla **Nimikkeen arvonlisäveroryhmä** -kentässä avattavan valikon painike.
22. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
23. Syötä **Erääntynyt vähimmäissaldo** -kenttään numero.
24. Syötä **Päivää**-kenttään numero.
25. Lopeta asiakkaan lisätoimitukset ja laskutus valitsemalla **Esto**-valintaruutu. Voit poistaa tilin eston valitsemalla Asiakkaat-sivun Pidossa oleva laskutus ja toimitus -kenttään arvon **Ei**.  
26. Laajenna **Huomautukset**-pikavälilehti.
27. Kirjoita valitun maksukehotuskoodin maksukehotuksessa näkyvä teksti. Huomautusruudun yläpuolella olevan Käännökset-valikon avulla voit kääntää tämän tekstin useille eri kielille.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
