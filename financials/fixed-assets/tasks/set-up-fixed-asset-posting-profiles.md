--- 
title: "Käyttöomaisuuden kirjausprofiilien määrittäminen"
description: "Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f2fd3c8cfa63e11a0bf4e5e095375d024c9d45ce
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a>Käyttöomaisuuden kirjausprofiilien määrittäminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot.  Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.  Tehtävän ohjauksen esimerkeissä käsitellään peruskirjausprofiileja. Kirjausprofiileja on luotava myös erityisiä tilikartan ja taloushallinnon raportoinnin tarpeita varten.

1. Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden kirjausprofiilit.
2. Valitse Uusi.
3. Kirjoita arvo Kirjausprofiili-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
    * Jokaiselle käyttöomaisuuserien käsittelyssä käytettävälle käyttöomaisuuden tapahtumalajille on luotava kirjausprofiili.  Tämä tehtävä ohjaus alkaa hankintatapahtumalajin käsittelyllä.  
5. ValitseLisää.
6. Syötä tai valitse arvo kentässä Kirja.
    * Ryhmittelyt-kentän avulla voit määrittää taulun (määritetään yksi tili jokaiselle käyttöomaisuuserälle) tai ryhmän (määritetään yksi tili jokaiselle käyttöomaisuusryhmälle) kirjausprofiilin.  Tässä tehtäväoppaassa arvojoukoksi jätetään Kaikki, jolloin kaikissa käyttöomaisuuserissä käytetään määritettyä kirjaa.  
7. Määritä Päätili-kenttään haluamasi arvot.
    * Hankinnoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.    
8. Valitse Tapahtumalaji-kentässä Hankintaoikaisu.
    * Hankinnan oikaisutapahtumissa käytetään samoja tilejä kuin hankintatapahtumissa.  
9. ValitseLisää.
10. Syötä tai valitse arvo kentässä Kirja.
11. Määritä Päätili-kenttään haluamasi arvot.
    * Hankintaoikaisuille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.    
12. Valitse Tapahtumalaji-kentässä Poisto.
13. ValitseLisää.
14. Syötä tai valitse arvo kentässä Kirja.
15. Määritä Päätili-kenttään haluamasi arvot.
16. Määritä Vastatili-kenttään haluamasi arvot.
17. Valitse Tapahtumalaji-kentässä Poiston oikaisu.
    * Poiston oikaisutapahtumissa käytetään samoja tilejä kuin poistotapahtumissa.  
18. ValitseLisää.
19. Syötä tai valitse arvo kentässä Kirja.
20. Määritä Päätili-kenttään haluamasi arvot.
21. Määritä Vastatili-kenttään haluamasi arvot.
22. Valitse Tapahtumalaji-kentässä Poisto - myynti.
23. ValitseLisää.
24. Syötä tai valitse arvo kentässä Kirja.
25. Määritä Päätili-kenttään haluamasi arvot.
    * Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.  
26. Valitse Tapahtumalaji-kentässä Poisto - hävikki.
    * Poistomyynnissä ja -hävikissä käytetään samoja tilejä.  
27. ValitseLisää.
28. Syötä tai valitse arvo kentässä Kirja.
29. Määritä Päätili-kenttään haluamasi arvot.
    * Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.  
30. Laajenna Luovutus-osa.
    * Määritä poiston kirjausprofiilit sekä myynnille että hävikille.  Aloitetaan poistomyyntitapahtumilla.  
31. ValitseLisää.
32. Syötä tai valitse arvo kentässä Kirja.
33. Valitse Kirjausarvo-kentässä Hankinnan arvo.
    * Hankinta-arvo koskee kaikkien vuosien hankinta-arvoja ja hankinnan oikaisun arvoja.  Voit myös määrittää tilit erikseen näille tapahtumalajeille.  
    * Voit määrittää poistoprosessin käyttämään eri tilejä sen mukaan, onko poiston tuloksena voitto vai tappio.  Määritetään myynnin arvon tyypiksi Kaikki. Tällöin samoja tilejä käytetään kaikissa poistotyypeissä.  
34. Määritä Päätili-kenttään haluamasi arvot.
35. Määritä Vastatili-kenttään haluamasi arvot.
36. ValitseLisää.
37. Syötä tai valitse arvo kentässä Kirja.
    * Valitse Kirjausarvo-kentässä Poisto (edeltävät vuodet).  
38. Määritä Päätili-kenttään haluamasi arvot.
39. Määritä Vastatili-kenttään haluamasi arvot.
40. ValitseLisää.
41. Syötä tai valitse arvo kentässä Kirja.
42. Valitse Kirjausarvo-kentässä Poisto (tämä vuosi).
43. Määritä Päätili-kenttään haluamasi arvot.
44. Määritä Vastatili-kenttään haluamasi arvot.
45. ValitseLisää.
46. Syötä tai valitse arvo kentässä Kirja.
47. Valitse Kirjausarvo-kentässä Poiston oikaisut (edeltävät vuodet).
48. Määritä Päätili-kenttään haluamasi arvot.
49. Määritä Vastatili-kenttään haluamasi arvot.
50. ValitseLisää.
51. Syötä tai valitse arvo kentässä Kirja.
52. Valitse Kirjausarvo-kentässä Poiston oikaisut (tämä vuosi).
53. Määritä Päätili-kenttään haluamasi arvot.
54. Määritä Vastatili-kenttään haluamasi arvot.
55. ValitseLisää.
56. Syötä tai valitse arvo kentässä Kirja.
57. Valitse Kirjausarvo-kentässä Nettokirjanpitoarvo.
58. Määritä Päätili-kenttään haluamasi arvot.
59. Määritä Vastatili-kenttään haluamasi arvot.
60. Valitse Myynti tai hävikki -kentässä Hävikki.
61. ValitseLisää.
62. Syötä tai valitse arvo kentässä Kirja.
63. Valitse Kirjausarvo-kentässä Hankinnan arvo.
64. Määritä Päätili-kenttään haluamasi arvot.
65. Määritä Vastatili-kenttään haluamasi arvot.
66. ValitseLisää.
67. Syötä tai valitse arvo kentässä Kirja.
    * Valitse Kirjausarvo-kentässä Poisto (edeltävät vuodet).  
68. Määritä Päätili-kenttään haluamasi arvot.
69. Määritä Vastatili-kenttään haluamasi arvot.
70. ValitseLisää.
71. Syötä tai valitse arvo kentässä Kirja.
72. Valitse Kirjausarvo-kentässä Poisto (tämä vuosi).
73. Määritä Päätili-kenttään haluamasi arvot.
74. Määritä Vastatili-kenttään haluamasi arvot.
75. ValitseLisää.
76. Syötä tai valitse arvo kentässä Kirja.
77. Valitse Kirjausarvo-kentässä Poiston oikaisut (edeltävät vuodet).
78. Määritä Päätili-kenttään haluamasi arvot.
79. Määritä Vastatili-kenttään haluamasi arvot.
80. ValitseLisää.
81. Syötä tai valitse arvo kentässä Kirja.
82. Valitse Kirjausarvo-kentässä Poiston oikaisut (tämä vuosi).
83. Määritä Päätili-kenttään haluamasi arvot.
84. Määritä Vastatili-kenttään haluamasi arvot.
85. ValitseLisää.
86. Syötä tai valitse arvo kentässä Kirja.
87. Valitse Kirjausarvo-kentässä Nettokirjanpitoarvo.
88. Määritä Päätili-kenttään haluamasi arvot.
89. Määritä Vastatili-kenttään haluamasi arvot.


