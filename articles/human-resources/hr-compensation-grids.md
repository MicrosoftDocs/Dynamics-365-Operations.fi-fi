---
title: Kompensaatioruudukoiden määrittäminen
description: Kompensaatioruudukoiden avulla voidaan määrittää ja ylläpitää kiinteiden kompensaatiosuunnitelmien palkkarakenteita.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51b98320eac539e49787d352f32683efadc11f41
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071448"
---
# <a name="set-up-compensation-grids"></a>Kompensaatioruudukoiden määrittäminen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensaatioruudukoiden avulla voidaan määrittää ja ylläpitää kiinteiden kompensaatiosuunnitelmien palkkarakenteita. Kompensaatioruudukoita voidaan jakaa useiden suunnitelmien välillä tai ne voidaan kopioida uutta kompensaatiosuunnitelmaa luotaessa.  Tasot ja viitepisteet on määritettävä ennen kompensaatioruudukon luontia. Tässä esimerkissä luodaan uusi Palkkaluokka-tyyppinen kompensaatioruudukko käyttämällä esittelytiedot tasoissa ja viitepisteissä demotietoja. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Määritä kompensaatioruudukkoa koskevat tiedot
1. Siirry kohteeseen **Henkilöstöhallinto** > **Kompensaatio** > **Kiinteä kompensaatio** > **Kompensaatioruudukot**.
2. Valitse **Uusi**.
3. Kirjoita **Ruudukko**-kenttään arvo.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse vaihtoehto **Tyyppi**-kentässä.
6. Syötä tai valitse arvo **Viitemääritykset**-kentässä.
7. Anna tai valitse **Valuutta**-kentässä arvo.
8. Syötä päivämäärä **Voimaantulopäivä**-kenttään.

## <a name="add-levels-to-the-compensation-structure"></a>Lisää tasoja kompensaatiorakenteeseen
1. Napsauta **Kompensaatiorakenne**.
2. Merkitse valittu rivi luettelossa.
3. Anna tai valitse **Taso**-kentässä arvo.
4. Valitse **Uusi**.
5. Merkitse valittu rivi luettelossa.
6. Anna tai valitse **Taso**-kentässä arvo.
7. Valitse **Uusi**.
8. Merkitse valittu rivi luettelossa.
9. Anna tai valitse **Taso**-kentässä arvo.
10. Valitse **Uusi**.
11. Merkitse valittu rivi luettelossa.
12. Anna tai valitse **Taso**-kentässä arvo.
13. Valitse **Uusi**.
14. Merkitse valittu rivi luettelossa.
15. Anna tai valitse **Taso**-kentässä arvo.

## <a name="fill-in-the-compensation-structure-with-values"></a>Täytä kompensaatiorakenteen arvot
1. Merkitse valittu rivi luettelossa.
    * Kompensaatioarvot voidaan lisätä tässä vaiheessa taulun kenttiin. Joukkomuutos-toiminnolla voidaan vaihtoehtoisesti täyttää kätevästi useita kenttiä ja suorittaa peruslaskutoimituksia.  
2. Valitse **Joukkomuutos**.
    * Tässä ruudukossa käytetään ensiksi ensimmäisen tason keskipisteen arvoa kaikkiin taulun kenttiin. Kompensaatiomatriisi tulee perustumaan siihen.  
3. Valitse **Oikaisulaji**-kentässä vaihtoehto.
4. Anna **Oikaisusumma**-kenttään arvo.
5. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
6. Valitse **Käytä ruudukossa**.
    * Seuraavaksi kasvatetaan joukkomuutostoiminnolla kunkin seuraavan tason summia tietyllä prosentilla tai summalla. Tässä esimerkissä jokaisella luokalla on 12,5 prosentin hajonta keskipisteiden välillä.  
7. Valitse **Oikaisulaji**-kentässä vaihtoehto.
8. Anna **Oikaisusumma**-kenttään arvo.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Valitse **Käytä ruudukossa**.
    * Nyt joukkomuutostoiminnolla muutetaan kunkin tason pienintä ja suurinta viitepistettä. Tässä esimerkissä käytetään 50 prosentin hajontaa, joten pienintä viitepistettä vähennetään 20 prosentilla ja suurinta suurennetaan 20 prosentilla.  
11. Anna **Oikaisusumma**-kenttään arvo.
12. Syötä tai valitse arvo **Viitepiste**-kentässä.
13. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
14. Valitse **Käytä ruudukossa**.
15. Anna **Oikaisusumma**-kenttään arvo.
16. Syötä tai valitse arvo **Viitepiste**-kentässä.
17. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
18. Valitse **Käytä ruudukossa**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
