---
title: Työntekijän vahvistus i9-lomakkeen tarkistaminen
description: Yhdysvaltojen IRCA (Immigration Reform and Control Act) -laki edellyttää, että työnantajat varmistavat uusien työntekijöiden oikeuden työskennellä.
author: ShielaSogge
ms.date: 01/10/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, HcmPersonIdentificationNumber, Hcmi9Document
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea77f112413a5b7d5c96768ad46fdb361023bd84
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964880"
---
# <a name="employment-verification-i9-verification"></a>Työntekijän vahvistus i9-lomakkeen tarkistaminen

[!include [banner](../../../includes/banner.md)]

Yhdysvaltojen IRCA (Immigration Reform and Control Act) -laki edellyttää, että työnantajat varmistavat uusien työntekijöiden oikeuden työskennellä. Tässä menettelyssä käydään läpi I-9-lomakkeen tarkistuksessa tarvittavien asiakirjojen tallentaminen. Menettelyssä käytetään USMF-yritystä.

1. Siirry kohtaan **Henkilöstöhallinto \> Työntekijät \> Työntekijät**.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Nimi**-kenttää arvolla **Vince**.
3. Valitse työntekijä. Valitse esimerkiksi **Vince Prado**.
4. Valitse **Henkilökohtaiset tiedot** -pikavälilehti.
5. Valitse **Tunnusnumerot**.
6. Valitse **Uusi**.
7. Valitse tallennettava tunnustyyppi. Valitse esimerkiksi **Passi**.
8. Syötä arvo **Numero**-kenttään.
9. Valitse **Ensisijainen**-kentässä **Kyllä**.
10. Määritä **Kuvaus**-kenttään tunnistetietueen nimi ja lyhyt kuvaus.
11. Valitse **Myöntäjätaho**-kentässä taho, joka on myöntänyt työntekijän henkilöllisyyden osoittavan asiakirjan. Valitse esimerkiksi **Hallitus**.
12. Syötä päivämäärä, jolloin työntekijän henkilöllisyyden osoittava asiakirja on myönnetty. Syötä esimerkiksi päivämäärä **15.02.2011** (Helmikuun 15. 2011).
13. Syötä päivämäärä, jolloin asiakirja vanhenee. Syötä esimerkiksi päivämäärä **15.2.2021** (Helmikuun 15. 2021).
14. Valitse **Tallenna**.
15. Sulje sivu.
16. Valitse **Työllisyys**-välilehti.
17. Valitse **I–9**.
18. Valitse **Uusi**.
19. Valitse **Työlupa**-kentässä vaihtoehto.

    Jos työntekijä ei ole Yhdysvaltain kansalainen, lisää myös työntekijän valtuutus- tai käyttöoikeusnumero.

20. Valitse **GroupListA**-vaihtoehto.

    Valitsemasi luettelo riippuu siitä, miten työntekijä todistaa henkilöllisyytensä. Työntekijän on toimitettava joko yksi tiedosto luettelosta A tai yksi tiedosto sekä luettelosta B että luettelosta C. Jos työntekijä on esimerkiksi antanut passin, voit valita luettelon A. Jos työntekijä on kuitenkin antanut vain ajokortin ja henkilökortin, on valittava luettelo B ja C.

21. Valitse **I-9-asiakirjan tyyppi** -kentässä työntekijän toimittaman asiakirjan tyyppi.
22. Anna tai valitse arvo **Asiakirjan numero** -kenttään.
23. Valitse **Tallenna**.

[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
