--- 
title: "ER Muotomääritysten luominen (marraskuu 2016)"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda muotokonfiguraation sähköiselle raportoinnille (ER)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803ed4a1018d344f1b40fa1f2338fc066e784c3c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a>ER Muotomääritysten luominen (marraskuu 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda muotokonfiguraation sähköiselle raportoinnille (ER). Tämä muotokonfiguraatio määrittää maksujen käsittelyssä käytettävien sähköisten asiakirjojen muodon. Tässä esimerkissä luodaan muotokonfiguraatio Litware, Inc. -malliyritykselle. Voit suorittaa nämä vaiheet suoritettuasi ensin Mallin yhdistäminen valittuihin tietolähteisiin -menettelyn vaiheet.


## <a name="create-a-new-format-configuration"></a>Uuden muotokonfiguraation luominen
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Raportointikonfiguraatiot.
3. Valitse puussa solmu Payments (simplified model).
4. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
5. Syötä Uusi-kenttään Muoto perustuu tietomalliin PaymentModel.
6. Syötä Nimi-kenttään BACS (Iso-Britannia, kuvitteellinen).
    * BACS (Iso-Britannia, kuvitteellinen)  
7. Syötä kuvaus-kenttään BACS - toimittajan maksumuoto (Iso-Britannia, kuvitteellinen).
    * BACS - toimittajan maksumuoto (Iso-Britannia, kuvitteellinen)  
    * Aktiivinen konfiguraation lähde syötetään tässä automaattisesti. Tämä lähde voi ylläpitää tätä konfiguraatiota. Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.  
    * Voit määrittää sähköiselle asiakirjalle tietyn muodon. Jätä kenttä tyhjäksi, jos haluat valita muodon suorituksen aikana.  
8. Anna tai valitse Tietomallin määritelmä -kentän arvo.
9. Valitse Luo konfiguraatio.
    * Uusi konfiguraatio on luotu. Rakenteen muodon voi tallentaa luonnoksena sähköisten asiakirjojen hallintaa varten.  

## <a name="design-format-of-electronic-document"></a>Sähköisen asiakirjan muodon suunnitteleminen
1. Valitse Suunnittelutoiminto.
2. Avaa valintaikkuna valitsemalla Lisää juuri.
3. Valitse puussa solmu Common\File.
4. Syötä Nimi-kenttään Xml.
    * XML  
5. Syötä Koodaus-kenttään UTF-8.
    * UTF-8  
6. Valitse OK.
7. Avaa valintaikkuna valitsemalla Lisää.
8. Valitse puussa solmu XML\Element.
9. Syötä Nimi-kenttään Viesti.
    * Viesti  
10. Valitse OK.
11. Valitse puussa Xml\Sanoma.
12. Valitse Lisää elementti.
13. Syötä Nimi-kenttään ProcessingDate.
    * ProcessingDate  
14. Valitse OK.
15. Valitse Lisää elementti.
16. Syötä Nimi-kenttään MessageId.
    * MessageId  
17. Valitse OK.
18. Valitse Lisää elementti.
19. Syötä Nimi-kenttään Maksut.
    * Maksut  
20. Valitse OK.
21. Valitse puussa Xml\Sanoma\Maksut.
22. Valitse Lisää elementti.
23. Syötä Nimi-kenttään Nimike.
    * Nimike  
24. Valitse OK.
25. Valitse puussa Xml\Sanoma\Maksut\Nimike.
26. Avaa valintaikkuna valitsemalla Lisää.
27. Valitse puussa solmu XML\Attribute.
28. Syötä Nimi-kenttään Tunnus.
    * Tunnus  
29. Valitse OK.
30. Avaa valintaikkuna valitsemalla Lisää.
31. Valitse puussa solmu XML\Element.
32. Syötä Nimi-kenttään Toimittaja.
    * Toimittaja  
33. Valitse OK.
34. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja.
35. Valitse Lisää elementti.
36. Syötä Nimi-kenttään Nimi.
    * Nimi  
37. Valitse OK.
38. Valitse Lisää elementti.
39. Syötä Nimi-kenttään Pankki.
    * Pankki  
40. Valitse OK.
41. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki.
42. Valitse Lisää elementti.
43. Syötä Nimi-kenttään RoutingNumber.
    * RoutingNumber  
44. Valitse OK.
45. Valitse Lisää elementti.
46. Syötä Nimi-kenttään AccountNumber.
    * AccountNumber  
47. Valitse OK.
48. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja.
49. Valitse Kopioi.
50. Valitse puussa Xml\Sanoma\Maksut\Nimike.
51. Valitse Liitä.
52. Syötä Nimi-kenttään Maksaja.
    * Maksaja  
53. Valitse puussa Xml\Sanoma\Maksut\Nimike.
54. Valitse Lisää elementti.
55. Syötä Nimi-kenttään Valuutta.
    * Valuutta  
56. Valitse OK.
57. Valitse Lisää elementti.
58. Syötä Nimi-kenttään kuvaus.
    * kuvaus  
59. Valitse OK.
60. Valitse Lisää elementti.
61. Syötä Nimi-kenttään TransDate.
    * TransDate  
62. Valitse OK.
63. Valitse Lisää elementti.
64. Syötä Nimi-kenttään Summa.
    * Määrä  
65. Valitse OK.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Muotokomponenttien valmisteleminen tietomallielementtien yhdistämistä varten
1. Valitse puussa Xml\Sanoma\ProcessingDate.
2. Avaa valintaikkuna valitsemalla Lisää.
3. Valitse puussa Teksti\DateTime.
4. Syötä Muoto-kenttään vvvv-KK-pp.
    * yyyy-MM-dd  
5. Valitse OK.
6. Valitse puussa Xml\Sanoma\Maksut\Nimike\TransDate.
7. Valitse Lisää DateTime.
8. Syötä Muoto-kenttään vvvv-KK-pp.
    * yyyy-MM-dd  
9. Valitse DateTime-tyyppi-kentässä Date.
10. Valitse OK.
11. Valitse puussa Xml\Sanoma\MessageId.
12. Avaa valintaikkuna valitsemalla Lisää.
13. Valitse puussa solmu Text\String.
14. Valitse OK.
15. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi.
16. Valitse Lisää merkkijono.
17. Valitse OK.
18. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\RoutingNumber.
19. Valitse Lisää merkkijono.
20. Valitse OK.
21. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\AccountNumber.
22. Valitse Lisää merkkijono.
23. Valitse OK.
24. Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Nimi.
25. Valitse Lisää merkkijono.
26. Valitse OK.
27. Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\RoutingNumber.
28. Valitse Lisää merkkijono.
29. Valitse OK.
30. Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\AccountNumber.
31. Valitse Lisää merkkijono.
32. Valitse OK.
33. Valitse puussa Xml\Sanoma\Maksut\Nimike\Valuutta.
34. Valitse Lisää merkkijono.
35. Valitse OK.
36. Valitse puussa Xml\Sanoma\Maksut\Nimike\Kuvaus.
37. Valitse Lisää merkkijono.
38. Valitse OK.
39. Valitse puussa Xml\Sanoma\Maksut\Nimike\Summa.
40. Valitse Lisää merkkijono.
41. Valitse OK.
42. Valitse Tallenna.
43. Sulje sivu.


