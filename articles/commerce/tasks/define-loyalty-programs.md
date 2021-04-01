---
title: Määritä kanta-asiakasohjelmat
description: Seuraavassa kerrotaan, miten kaksi tasoa sisältävä kanta-asiakasohjelma määritetään.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69424cdaae84ffe5ca8157f061ba5876b9eeeff9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256898"
---
# <a name="define-loyalty-programs"></a>Määritä kanta-asiakasohjelmat

[!include [banner](../includes/banner.md)]

Seuraavassa kerrotaan, miten kaksi tasoa sisältävä kanta-asiakasohjelma määritetään. Menettely käyttää esittelytietojen USRT-yritystä.

1. Valitse Retail ja Commerce > .. > Kanta-asiakasohjelmat.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Lisää rivi.
6. Syötä numero Taso-kenttään.
7. Syötä Taso-kenttään kanta-asiakkuustaso.
8. Kirjoita Kuvaus-kenttään arvo.
9. Avaa haku valitsemalla Päivämääräväli-kentässä avattavan valikon painike.
    * Tämän päivämäärävälin tulee jatkua tulevaisuuteen. Jos kultatasolle on valittu päivämääräväliksi yhden vuoden jakso, jokainen asiakas, joka pätevöityy kultatasolle voi vastaanottaa yhden vuoden ajan kultatasolle määritettäviä palkkioita. Jos asiakas saavuttaa uudelleen kultatason, kun hän on kyseisellä tasolla, päivämäärää, jona hänen tasonsa vanhenee, lykätään vuodella eteenpäin siitä päivästä, jona asiakas saavuttaa tason uudelleen.  
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Valitse Lisää rivi.
12. Syötä numero Taso-kenttään.
13. Syötä Taso-kenttään kanta-asiakkuustaso.
14. Kirjoita Kuvaus-kenttään arvo.
15. Avaa haku valitsemalla Päivämääräväli-kentässä avattavan valikon painike.
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
17. Valitse Tallenna.
18. Etsi haluamasi tietue luettelosta ja valitse se.
    * Tasosäännöt määrittävät niiden palkkiopisteiden vähimmäismäärän, jotka tiettynä ajanjaksona on ansaittava ollakseen oikeutettu tasoon.  
19. Ota käyttöön Tasosäännöt-osan laajennus.
20. Valitse Uusi.
    * Yksi taso voi sisältää useita tasosääntöjä. Tason ansaitsemiselle on voitu määrittää esimerkiksi kolme ehtoa, jotka ovat 500 euron suuruiset ostot kuukauden aikana, 1 000 euron suuruiset ostot vuoden aikana ja 20 tapahtuman tekeminen vuoden aikana. Tätä varten on luotava kolme tasosääntöä.  
21. Avaa haku valitsemalla Palkkiopiste-kentässä avattavan valikon painike.
    * Tämän on oltava ei-lunastettava kanta-asiakasohjelman palkkiopiste.  
22. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
23. Syötä Myönnetyt pisteet vähintään -kenttään numero.
    * Jos haluat asiakkaiden olevat oikeutettuja alimmalle tasolle yksinkertaisesti osallistumalla ohjelmaan, syötä 0.  
24. Avaa haku valitsemalla Arviointipäivän aikaväli -kentässä avattavan valikon painike.
    * Tämän päivämäärävälin tulee jatkua menneisyyteen. Vain tämän päivämäärävälin aikana ansaitut pisteet lasketaan mukaan, kun tavoitellaan myönnettyjen vähimmäispisteiden arvoa.  
25. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
26. Valitse Tallenna.
27. Etsi haluamasi tietue luettelosta ja valitse se.
28. Valitse Uusi.
29. Avaa haku valitsemalla Palkkiopiste-kentässä avattavan valikon painike.
30. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
31. Syötä Myönnetyt pisteet vähintään -kenttään numero.
32. Avaa haku valitsemalla Arviointipäivän aikaväli -kentässä avattavan valikon painike.
    * Tämän päivämäärävälin tulee jatkua menneisyyteen.  
33. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
34. Valitse Tallenna.
35. Valitse Hintaryhmät.
    * Jos haluat antaa kanta-asiakkaille alennuksia, määritä kanta-asiakasohjelmaan vähintään yksi hintaryhmä ja liitä hintaryhmä(t) alennuksiin. Hintaryhmiä ja erityyppisiä alennusentiteettejä ei kannata yhdistää keskenään.  Älä käytä esimerkiksi samaa hintaryhmää kanta-asiakas- ja kanava-alennuksessa.  
36. Avaa haku valitsemalla Hintaryhmä-kentässä avattavan valikon painike.
    * Sivun yläosassa oleva Hintaryhmät-linkki koskee kanta-asiakasohjelmaa. Ohjelman tasot -pikavälilehden Hintaryhmät-linkki koskee vain tiettyä kanta-asiakkuustasoa.  
37. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
38. Valitse Tallenna.
39. Sulje sivu.
40. Valitse Tallenna.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]