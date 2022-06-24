---
title: ER Muotomääritysten luominen (marraskuu 2016)
description: Tässä artikkelissa käsitellään sähköisen raportoinnin (ER) muotomäärityksen luontia.
author: NickSelin
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2617f33293c38b7f1aaa61fda7d8de06711c6727
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902651"
---
# <a name="er-create-a-format-configuration-november-2016"></a>ER Muotomääritysten luominen (marraskuu 2016)

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda muotokonfiguraation sähköiselle raportoinnille (ER). Tämä muotokonfiguraatio määrittää maksujen käsittelyssä käytettävien sähköisten asiakirjojen muodon. Tässä esimerkissä luodaan muotokonfiguraatio Litware, Inc. -malliyritykselle. Voit suorittaa nämä vaiheet suoritettuasi ensin Mallin yhdistäminen valittuihin tietolähteisiin -menettelyn vaiheet.


## <a name="create-a-new-format-configuration"></a>Uuden muotokonfiguraation luominen
1. Valitse **Organisaation hallinto > Työtilat > Sähköinen raportointi**.
2. Valitse **Raportointikonfiguraatiot**.
3. Valitse puussa **Maksut (yksinkertaistettu malli)**.
4. Avaa valintaikkuna valitsemalla **Luo konfigurointi**.

 > [!NOTE]
 > Jos **Luo konfigurointi** ei ole näkyvissä, suunnittelutila on otettava käyttöön **Sähköisen raportoinnin parametrit** -sivulla. 
 
5. Anna **Uusi**-kentässä **Muoto perustuu tietomalliin PaymentModel**.
6. Anna **Nimi**-kentässä **BACS (Iso-Britannia, kuvitteellinen)**.
7. Anna **Kuvaus**-kenttään **BACS - toimittajan maksumuoto (Iso-Britannia, kuvitteellinen)**.
    * Aktiivinen konfiguraation lähde syötetään tässä automaattisesti. Tämä lähde voi ylläpitää tätä konfiguraatiota. Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.  
    * Voit määrittää sähköiselle asiakirjalle tietyn muodon. Jätä kenttä tyhjäksi, jos haluat valita muodon suorituksen aikana.  
8. Anna tai valitse **Tietomallin määritelmä** -kentän arvo.
9. Valitse **Luo konfiguraatio**. Uusi konfiguraatio on luotu. Rakenteen muodon voi tallentaa luonnoksena sähköisten asiakirjojen hallintaa varten.  

## <a name="design-the-format-of-an-electronic-document"></a>Sähköisen asiakirjan muodon suunnitteleminen
1. Valitse **Suunnittelutoiminto**.
2. Avaa valintaikkuna valitsemalla **Lisää juuri**.
3. Valitse puussa **Common\File**.
4. Anna **Nimi**-kentässä **Xml**.
5. Anna **Koodaus**-kentässä **UTF-8**.
6. Napsauta **OK**.
7. Valitse **Lisää**.
8. Valitse puussa **XML\Elementti**.
9. Kirjoita **Nimi**-kenttään **Viesti**.
10. Napsauta **OK**.
11. Valitse puussa **Xml\Sanoma**.
12. Valitse **Lisää elementti**.
13. Kirjoita **Nimi**-kenttään **ProcessingDate**.
14. Napsauta **OK**.
15. Valitse **Lisää elementti**.
16. Kirjoita Nimi-kenttään **MessageId**.
17. Napsauta **OK**.
18. Valitse **Lisää elementti**.
19. Kirjoita **Nimi**-kenttään **Maksut**.
20. Napsauta **OK**.
21. Valitse puussa **Xml\Sanoma\Maksut**.
22. Valitse **Lisää elementti**.
23. Kirjoita **Nimi**-kenttään **Nimike**.
24. Napsauta **OK**.
25. Valitse puussa **Xml\Sanoma\Maksut\Nimike**.
26. Valitse **Lisää**.
27. Valitse puussa **XML\Määrite**.
28. Kirjoita Nimi-kenttään **Tunnus**.
29. Napsauta **OK**.
30. Valitse **Lisää**.
31. Valitse puussa **XML\Elementti**.
32. Kirjoita Nimi-kenttään **Toimittaja**.
33. Napsauta **OK**.
34. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja**.
35. Valitse **Lisää elementti**.
36. Kirjoita Nimi-kenttään **Nimi**.
37. Napsauta **OK**.
38. Valitse **Lisää elementti**.
39. Kirjoita **Nimi**-kenttään **Pankki**.
40. Napsauta **OK**.
41. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki**.
42. Valitse **Lisää elementti**.
43. Kirjoita **Nimi**-kenttään **RoutingNumber**.
44. Napsauta **OK**.
45. Valitse **Lisää elementti**.
46. Kirjoita **Nimi**-kenttään **AccountNumber**.
47. Napsauta **OK**.
48. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja**.
49. Valitse **Kopioi**.
50. Valitse puussa **Xml\Sanoma\Maksut\Nimike**.
51. Valitse **Liitä**.
52. Kirjoita **Nimi**-kenttään **Maksaja**.
53. Valitse puussa **Xml\Sanoma\Maksut\Nimike**.
54. Valitse **Lisää elementti**.
55. Kirjoita **Nimi**-kenttään **Valuutta**.
56. Napsauta **OK**.
57. Valitse **Lisää elementti**.
58. Kirjoita **Nimi**-kenttään **Kuvaus**.
59. Napsauta **OK**.
60. Valitse **Lisää elementti**.
61. Kirjoita Nimi-kenttään **TransDate**.
62. Napsauta **OK**.
63. Valitse **Lisää elementti**.
64. Kirjoita Nimi-kenttään **Summa**.
65. Napsauta **OK**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Muotokomponenttien valmisteleminen tietomallielementtien yhdistämistä varten
1. Valitse puussa **Xml\Sanoma\ProcessingDate**.
2. Avaa valintaikkuna valitsemalla **Lisää**.
3. Valitse puussa **Teksti\DateTime**.
4. Kirjoita **Muoto**-kenttään **vvvv-KK-pp**.
5. Napsauta **OK**.
6. Valitse puussa **Xml\Sanoma\Maksut\Nimike\TransDate**.
7. Valitse **Lisää DateTime**.
8. Kirjoita **Muoto**-kenttään **vvvv-KK-pp**.
9. Valitse **DateTime**-tyyppikentässä **Päivämäärä**.
10. Napsauta **OK**.
11. Valitse puussa **Xml\Sanoma\MessageId**.
12. Avaa valintaikkuna valitsemalla **Lisää**.
13. Valitse puussa **Teksti\Merkkijono**.
14. Napsauta **OK**.
15. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi**.
16. Valitse **Lisää merkkijono**.
17. Napsauta **OK**.
18. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\RoutingNumber**.
19. Valitse **Lisää merkkijono**.
20. Napsauta **OK**.
21. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\AccountNumber**.
22. Valitse **Lisää merkkijono**.
23. Napsauta **OK**.
24. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Maksaja\Nimi**.
25. Valitse **Lisää merkkijono**.
26. Napsauta **OK**.
27. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\RoutingNumber**.
28. Valitse **Lisää merkkijono**.
29. Napsauta **OK**.
30. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\AccountNumber**.
31. Valitse **Lisää merkkijono**.
32. Napsauta **OK**.
33. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Valuutta**.
34. Valitse **Lisää merkkijono**.
35. Napsauta **OK**.
36. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Kuvaus**.
37. Valitse **Lisää merkkijono**.
38. Napsauta **OK**.
39. Valitse puussa **Xml\Sanoma\Maksut\Nimike\Summa**.
40. Valitse **Lisää merkkijono**.
41. Napsauta **OK**.
42. Valitse **Tallenna**.
43. Sulje sivu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]