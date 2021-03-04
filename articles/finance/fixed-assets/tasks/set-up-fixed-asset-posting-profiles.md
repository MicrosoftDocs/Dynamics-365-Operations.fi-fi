---
title: Käyttöomaisuuden kirjausprofiilien määrittäminen
description: Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07961d8613b6b5e0e1c5dc6a91b554305dcb17f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442832"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>Käyttöomaisuuden kirjausprofiilien määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot.  Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.  Tehtävän ohjauksen esimerkeissä käsitellään peruskirjausprofiileja. Kirjausprofiileja on luotava myös erityisiä tilikartan ja taloushallinnon raportoinnin tarpeita varten.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Asetukset > Käyttöomaisuuserän kirjausprofiili**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Kirjausprofiili**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo. Jokaiselle käyttöomaisuuserien käsittelyssä käytettävälle käyttöomaisuuden tapahtumalajille on luotava kirjausprofiili. Tämä tehtävä ohjaus alkaa hankintatapahtumalajin käsittelyllä.  
5. Napsauta **Lisää** valikkorivillä.
6. Syötä tai valitse arvo kentässä **Kirja**. **Ryhmittelyt**-kentän avulla voit määrittää taulun (määritetään yksi tili jokaiselle käyttöomaisuuserälle) tai ryhmän (määritetään yksi tili jokaiselle käyttöomaisuusryhmälle) kirjausprofiilin. Tässä tehtäväoppaassa arvojoukoksi jätetään Kaikki, jolloin kaikissa käyttöomaisuuserissä käytetään määritettyä kirjaa.  
7. Määritä **Päätili**-kenttään haluamasi arvot. Hankinnoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.    
8. Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Hankintaoikaisu. Hankinnan oikaisutapahtumissa käytetään samoja tilejä kuin hankintatapahtumissa.  
9. Valitse **Lisää**.
10. Syötä tai valitse arvo kentässä **Kirja**.
11. Määritä **Päätili**-kenttään haluamasi arvot. Hankintaoikaisuille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.    
12. Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Poisto.
13. Valitse **Lisää**.
14. Syötä tai valitse arvo kentässä **Kirja**.
15. Määritä **Päätili**-kenttään haluamasi arvot.
16. Määritä **Vastatili**-kenttään haluamasi arvot.
17. Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Poistojen oikaisu. Poiston oikaisutapahtumissa käytetään samoja tilejä kuin poistotapahtumissa.  
18. Valitse **Lisää**.
19. Syötä tai valitse arvo kentässä **Kirja**.
20. Määritä **Päätili**-kenttään haluamasi arvot.
21. Määritä **Vastatili**-kenttään haluamasi arvot.
22. Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Poistomyynti.
23. Valitse **Lisää**.
24. Syötä tai valitse arvo kentässä **Kirja**.
25. Määritä **Päätili**-kenttään haluamasi arvot. Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.  
26. Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Poistohävikki. Poistomyynnissä ja -hävikissä käytetään samoja tilejä.  
27. Valitse **Lisää**.
28. Syötä tai valitse arvo kentässä **Kirja**.
29. Määritä **Päätili**-kenttään haluamasi arvot. Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.  
30. Laajenna **Poisto**-pikavälilehti. Määritä poiston kirjausprofiilit sekä myynnille että hävikille.  Aloitetaan poistomyyntitapahtumilla.  
31. Valitse **Lisää**.
32. Syötä tai valitse arvo kentässä **Kirja**.
33. Valitse **Kirjausarvo**-kentässä Hankinnan arvo.
    * Hankinta-arvo koskee kaikkien vuosien hankinta-arvoja ja hankinnan oikaisun arvoja. Voit myös määrittää tilit erikseen näille tapahtumalajeille.  
    * Voit määrittää poistoprosessin käyttämään eri tilejä sen mukaan, onko poiston tuloksena voitto vai tappio. Määritetään myynnin arvon tyypiksi Kaikki. Tällöin samoja tilejä käytetään kaikissa poistotyypeissä.  
34. Määritä **Päätili**-kenttään haluamasi arvot.
35. Määritä **Vastatili**-kenttään haluamasi arvot.
36. Valitse **Lisää**.
37. Syötä tai valitse arvo kentässä **Kirja**.
38. Valitse **Kirjausarvo**-kentässä Poisto (edeltävät vuodet).  
38. Määritä **Päätili**-kenttään haluamasi arvot.
39. Määritä **Vastatili**-kenttään haluamasi arvot.
40. Valitse **Lisää**.
41. Syötä tai valitse arvo kentässä **Kirja**.
42. Valitse **Kirjausarvo**-kentässä Poisto (tämä vuosi).
43. Määritä **Päätili**-kenttään haluamasi arvot.
44. Määritä **Vastatili**-kenttään haluamasi arvot.
45. Valitse **Lisää**.
46. Syötä tai valitse arvo kentässä **Kirja**.
47. Valitse **Kirjausarvo**-kentässä Poiston oikaisut (edeltävät vuodet).
48. Määritä **Päätili**-kenttään haluamasi arvot.
49. Määritä **Vastatili**-kenttään haluamasi arvot.
50. Valitse **Lisää**.
51. Syötä tai valitse arvo kentässä **Kirja**.
52. Valitse **Kirjausarvo**-kentässä Poiston oikaisut (tämä vuosi).
53. Määritä **Päätili**-kenttään haluamasi arvot.
54. Määritä **Vastatili**-kenttään haluamasi arvot.
55. Valitse **Lisää**.
56. Syötä tai valitse arvo kentässä **Kirja**.
57. Valitse **Kirjausarvo**-kentässä Nettokirjanpitoarvo.
58. Määritä **Päätili**-kenttään haluamasi arvot.
59. Määritä **Vastatili**-kenttään haluamasi arvot.
60. Valitse **Myynti tai hävikki** -kentässä Hävikki.
61. Valitse **Lisää**.
62. Syötä tai valitse arvo kentässä **Kirja**.
63. Valitse **Kirjausarvo**-kentässä Hankinnan arvo.
64. Määritä **Päätili**-kenttään haluamasi arvot.
65. Määritä **Vastatili**-kenttään haluamasi arvot.
66. Valitse **Lisää**.
67. Syötä tai valitse arvo kentässä **Kirja**.
67. Valitse **Kirjausarvo**-kentässä Poisto (edeltävät vuodet).  
68. Määritä **Päätili**-kenttään haluamasi arvot.
69. Määritä **Vastatili**-kenttään haluamasi arvot.
70. Valitse **Lisää**.
71. Syötä tai valitse arvo kentässä **Kirja**.
72. Valitse **Kirjausarvo**-kentässä Poisto (tämä vuosi).
73. Määritä **Päätili**-kenttään haluamasi arvot.
74. Määritä **Vastatili**-kenttään haluamasi arvot.
75. Valitse **Lisää**.
76. Syötä tai valitse arvo kentässä **Kirja**.
77. Valitse **Kirjausarvo**-kentässä Poiston oikaisut (edeltävät vuodet).
78. Määritä **Päätili**-kenttään haluamasi arvot.
79. Määritä **Vastatili**-kenttään haluamasi arvot.
80. Valitse **Lisää**.
81. Syötä tai valitse arvo kentässä **Kirja**.
82. Valitse **Kirjausarvo**-kentässä Poiston oikaisut (tämä vuosi).
83. Määritä **Päätili**-kenttään haluamasi arvot.
84. Määritä **Vastatili**-kenttään haluamasi arvot.
85. Valitse **Lisää**.
86. Syötä tai valitse arvo kentässä **Kirja**.
87. Valitse **Kirjausarvo**-kentässä Nettokirjanpitoarvo.
88. Määritä **Päätili**-kenttään haluamasi arvot.
89. Määritä **Vastatili**-kenttään haluamasi arvot.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]