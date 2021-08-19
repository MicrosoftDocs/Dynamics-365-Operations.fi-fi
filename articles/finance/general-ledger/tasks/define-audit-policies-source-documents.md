---
title: Tarkistuskäytäntöjen määrittäminen lähdeasiakirjoille
description: Tässä aiheessa kuvataan, miten tarkistuskäytännön säännöt määritetään ja suoritetaan.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0779589a3583909984e35014a2ec0e86455cd30a3833110556f095241e7172ca
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722668"
---
# <a name="define-audit-policies-for-source-documents"></a>Tarkistuskäytäntöjen määrittäminen lähdeasiakirjoille

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten tarkistuskäytännön säännöt määritetään ja suoritetaan. Tässä esimerkissä käytetään hotellin kululajin kuluraportteja. Näissä toimintaohjeissa käytetään esittely-yritystä USMF. Tilintarkistajan rooli sisältää näiden tehtävien suorittamisessa vaadittavat käyttöoikeudet.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Tarkastustyötila > Asetukset > Käytäntösäännön tyyppi**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Säännön nimi**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Kyselyn nimi** -kentässä **Kuluraportin rivi**
6. Valitse **Kyselytyyppi**-kentässä **Yhdistä**
7. Valitse **Yritys**-kentässä **Yritys**
8. Valitse **Asiakirjan päivämääräviite** -kentässä **Muokkauksen päivämäärä ja aika**
9. Valitse **Tallenna**.
10. Siirry siirtymisruudussa kohtaan **Moduulit > Tarkastustyötila > Asetukset > Tarkistuskäytännöt**.
11. Valitse **Uusi**.
12. Kirjoita arvo **Nimi**-kenttään.
13. Laajenna **Käytäntöorganisaatiot**-osa.
14. Valitse puussa **Contoso Entertainment System USA** ja sitten **Lisää**.
15. Valitse puussa **Contoso Consulting USA** ja sitten **Lisää**.
16. Valitse puussa **Contoso Retail USA** ja sitten **Lisää**.
17. Tiivistä **Käytäntöorganisaatiot**-osa.
18. Laajenna **Käytäntösäännöt**-osa.
19. Etsi ja valitse luettelosta aiemmin luotu käytäntösääntö.
20. Valitse **Luo käytäntösääntö**.
21. Syötä päivämäärä ja kellonaika **Voimaantulopäivä**-kenttään.
22. Valitse **Suodata**.
23. Valitse luettelosta **kululuokan** rivi ja määritä **hotellin** tiedot.
24. Anna tai valitse arvo **Ehdot**-kentässä.
25. Valitse **Yhdistelmä**-välilehti.
26. Valitse **Lisää**.
27. Valitse luettelosta **Tapahtumasumma**-kentän arvo.
28. Syötä tai valitse arvo **Kenttä**-kentässä.
29. Valitse **AggregateFunction**-kentässä **Summa**.
30. Valitse **Ryhmittely**-välilehti.
31. Valitse **Lisää**.
32. Valitse luettelosta **Työntekijä**-kentän arvo.
33. Valitse **Lisää**.
34. Valitse luettelosta **Kululuokka**-kentän arvo
35. Syötä tai valitse arvo **Kenttä**-kentässä.
36. Valitse **On**-välilehti.
37. Valitse **Lisää**.
38. Valitse **Tapahtumasumma**.
39. Syötä tai valitse arvo **Kenttä**-kentässä.
40. Valitse **AggregateFunction**-kentässä **Summa**.
41. Kirjoita **Ehdot**-kenttään `>2000`.
42. Valitse **OK**.
43. Valitse **Testi**.
44. Syötä **Asiakirjan valinnan aloituspäivämäärä** -kenttään päivämäärä ja aika.
45. Syötä **Asiakirjan valinnan lopetuspäivämäärä** -kenttään päivämäärä ja aika.
46. Valitse **Suorita testi**.
47. Valitse toimintoruudussa **Tarkistuskäytäntö**.
48. Valitse **Lisäasetukset**.
49. Määritä päivämäärä ja kellonaika **Aloituspäivämäärä**-kenttään.
50. Syötä päivämäärä ja kellonaika **Päättymispäivämäärä**-kenttään.
51. Valitse **Erä**.
52. Laajenna **Suorita taustalla** -osa.
53. Valitse **Eräkäsittely**-kentässä **Kyllä**.
54. Valitse **OK**.
55. Siirry siirtymisruudussa kohtaan **Moduulit > Tarkastustyötila > Tarkistusasiat**.
56. Etsi haluamasi tietue luettelosta ja valitse se.
57. Laajenna **Liitokset**-osa.
58. Etsi haluamasi tietue luettelosta ja valitse se.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]