---
title: Määritä työntekijän vamma- ja sairaustiedot
description: Tässä tehtävässä käsitellään tapaturma- tai sairaustapausta.
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06307331db4d420e99de21c0eb0b3cf1c233f0d5
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066647"
---
# <a name="maintain-employee-injury-and-illness-information"></a>Määritä työntekijän vamma- ja sairaustiedot


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tapaturmien ja sairauksien asetukset -tehtävän opastus kannattaa suorittaa ensin, sillä joitakin asetustietoja käytetään tässä tehtävässä. 



Tässä tehtävätallenteessa käsitellään tapaturma- tai sairaustapauksen luonnin perusvaiheita. Tapaturman tai sairauden tietojen lisäksi seurataan palvelupyynnön tilaa. Palvelupyyntöjen tila on oletusarvoisesti **Avoin**. Tilaa voi hallita sivun yläosan **Palvelupyynnön tila** -valikkovaihtoehdolla.

1. Valitse **Henkilöstöhallinto \> Työntekijät \> Tapaturma ja sairaus \> Tapaturma- tai sairastapaukset**.
2. Valitse **Uusi**.
3. Anna **Palvelupyynnön kuvaus**-kenttään arvo (kuten **Rannevamma**).
4. Anna tai valitse **Työntekijä**-kentässä arvo (kuten **Ana Bowman**).
5. Anna **Tapauksen päivämäärä ja aika** -kentässä päivämäärä ja aika (kuten 20.1.2016 kello 10.00).
6. Anna tai valitse **Tapaturma- tai sairaustyyppi** -kentässä arvo (kuten **Murtuma**).
7. Anna tai valitse **Kehon osa** -kentässä arvo (kuten **Ranne**).
8. Anna tai valitse **Seuraustyyppi**-kentässä arvo (kuten **Terapia**).
9. Anna **Raportoitu päivämäärä ja aika** -kentässä päivämäärä ja aika.

    Raportointipäivämäärän ja -ajan on oltava myöhemmin kuin tapauksen päivämäärä ja aika.

10. Anna tai valitse **Ilmoittaja**-kentässä arvo (kuten **Ana Bowman**).

    Määritetty henkilö voi olla työntekijä tai joku muu tapahtuman todistaja.

11. Anna **Tapaus**-osan **Tapahtumapaikka**-kentässä arvo (kuten **Varasto**).
12. Valitse **Työpaikalla**-kentässä **Kyllä**, jos tapaus tapahtui työpaikalla.
13. Anna **Työn aloituspäivä ja -aika** -kentässä päivämäärä ja aika, jolloin kyseinen henkilö aloitti työskentelyn ennen tapausta.
14. Anna **Työntekijän työ tai tehtävä** -kentässä työ tai tehtävä, jota työntekijä oli tekemässä, kun tapaus tapahtui (kuten **Laatikoiden lastaaminen**). 
15. Anna **Tapauksen syy** -kentässä tapauksen syy (kuten **Liukastuminen kostealla lattialla**).
16. Anna tai valitse **Vakavuustaso**-kentässä arvo.
17. Anna **Suoritettava toimenpide** -kentässä arvo (kuten **Kaatuneen nesteen siivoaminen heti**).
18. Anna **Poissaolon odotettu kesto päivinä** -kentässä niiden päivien määrä, jonka henkilön odotetaan olevan pois töistä.

    Kun henkilö palaa töihin, päivitä **Poissaolopäivät**-kenttään niiden päivien määrä, jonka henkilö oli pois töistä.

19. Valitse **Tapaturman tai sairauden kustannukset** -osassa **Lisää**.
20. Syötä **Päivämäärä**-kenttään päivämäärä.
21. Anna tai valitse **Kustannustyyppi**-kentässä arvo (kuten **Terapia**).

    Voit antaa myös summan ja liittää tukidokumentaation kustannukseen (esimerkkejä ovat laskut tai lääkärin muistiinpanot).

22. Valitse **Lisää**.
23. Syötä **Päivämäärä**-kenttään päivämäärä.
24. Anna tai valitse **Kustannustyyppi**-kentässä arvo (kuten **Lääkäri**).
25. Valitse **Vamman tai sairauden hoito** -osassa **Lisää**.
26. Anna **Hoitopäivämäärä**-kentässä päivämäärä ja aika.
27. Anna tai valitse **Hoitotyyppi**-kentässä arvo (kuten **Lasta**).
28. Valinnainen: määritä **Sairaalan päivystyspoliklinikka** -osassa asetukseksi **Kyllä**.
29. Anna **Hoitokommentit**-kentässä arvo (kuten **Lasta 2 viikkoa**).
30. Anna nimi **Lääkärin nimi** -kentässä arvo (esimerkiksi **Anderson**).
31. Anna **Hoitopaikka ja sijainti** -kentässä arvo (kuten **Elm St. Emergency**).
32. Anna **Hoidon lisätiedot** -kentässä arvo (kuten **Röntgenkuva vahvistaa murtuman, lastan käyttö**).
33. Valitse **Tallenna**.

Tapaustilan voi päivittää milloin tahansa. Jos tapaturman tai sairauden käsittely on kesken, määritä sen tilaksi **Keskeneräinen**. Kun tapaus on suljettu, siihen voi lisätä vain tapaukseen liittyviä kustannuksia, hoitoja tai ilmoituksia tai poistaa niitä. Muiden tietojen muuttaminen edellyttää tapauksen uudelleenavaamista.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
