--- 
title: "Määritä tarkistuskäytännöt lähdeasiakirjoille"
description: "Tässä menettelyssä kuvataan, miten tarkistuskäytännön säännöt määritetään ja suoritetaan."
author: ryansandness
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
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ca4c8735258170c41dc907ed0ef8afca250ea9dd
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="define-audit-policies-for-source-documents"></a>Määritä tarkistuskäytännöt lähdeasiakirjoille

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten tarkistuskäytännön säännöt määritetään ja suoritetaan. Tässä esimerkissä käytetään hotellin kululajin kuluraportteja. Näissä toimintaohjeissa käytetään esittely-yritystä USMF. Tilintarkistajan rooli sisältää näiden tehtävien suorittamisessa vaadittavat käyttöoikeudet.

1. Siirry kohtaan Tarkastustyötila > Asetukset > Käytäntösäännön tyyppi.
2. Valitse Uusi.
3. Kirjoita arvo Säännön nimi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse kuluraportin rivillä Kyselyn nimi -kenttä
6. Valitse Kyselytyyppi-kentässä Yhdistä
7. Valitse Yritys-kentässä Yritys
8. Valitse Asiakirjan päivämääräviite -kentässä Muokkauksen päivämäärä ja aika
9. Valitse Tallenna.
10. Siirry kohtaan Tarkastustyötila > Asetukset > Tarkistuskäytännöt.
11. Valitse Uusi.
12. Kirjoita arvo Nimi-kenttään.
13. Laajenna Käytäntöorganisaatiot-osa.
14. Valitse puussa solmu Contoso Entertainment System USA.
15. ValitseLisää.
16. Valitse puussa solmu Contoso Consulting USA.
17. ValitseLisää.
18. Valitse puussa solmu Contoso Retail USA.
19. ValitseLisää.
20. Tiivistä Käytäntöorganisaatiot-osa.
21. Laajenna Käytäntösäännöt-osa.
22. Etsi ja valitse luettelosta aiemmin luotu käytäntösääntö.
23. Valitse Luo käytäntösääntö.
24. Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.
25. Valitse Suodatin.
26. Valitse luettelosta kululuokan rivi ja määritä hotellin tiedot
27. Syötä tai valitse arvo Ehdot-kenttään.
28. Valitse Yhdistä-välilehti.
29. ValitseLisää.
30. Valitse luettelosta tapahtumasumman kentän arvo.
31. Syötä tai valitse arvo Kenttä-kentässä.
32. Valitse AggregateFunction-kentässä Summa.
33. Valitse Ryhmittely-välilehti.
34. ValitseLisää.
35. Valitse luettelosta työntekijän arvo  
36. ValitseLisää.
37. Valitse luettelosta työntekijäluokan arvo
38. Syötä tai valitse arvo Kenttä-kentässä.
39. Valitse On-välilehti.
40. ValitseLisää.
41. Valitse tapahtumasumma
42. Syötä tai valitse arvo Kenttä-kentässä.
43. Valitse AggregateFunction-kentässä Summa.
44. Kirjoita Ehdot-kenttään > 2 000.
45. Valitse OK.
46. Valitse Testi.
47. Syötä Asiakirjan valinnan aloituspäivämäärä -kenttään päivämäärä ja aika.
48. Syötä Asiakirjan valinnan lopetuspäivämäärä -kenttään päivämäärä ja aika.
49. Valitse Suorita testi.
50. Valitse toimintoruudussa Tarkistuskäytäntö.
51. Valitse Lisäasetukset.
52. Määritä päivämäärä ja kellonaika Aloituspäivämäärä-kenttään.
53. Syötä päivämäärä ja kellonaika Päättymispäivämäärä-kenttään.
54. Valitse erä.
55. Laajenna Suorita taustalla -osa.
56. Valitse Eräkäsittely-kentässä Kyllä.
57. Valitse OK.
58. Siirry kohtaan Tarkastustyötila > Tarkistustapaukset
59. Etsi haluamasi tietue luettelosta ja valitse se.
60. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
61. Laajenna Liitokset-osa.
62. Etsi haluamasi tietue luettelosta ja valitse se.
63. Napsauta luettelossa valitulla rivillä olevaa linkkiä.


