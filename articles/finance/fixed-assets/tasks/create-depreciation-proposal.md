---
title: Luo poistoehdotus
description: Tässä ohjeaiheessa kuvataan, kuinka poiston eräehdotukset toimivat ja kuinka poisto ehdotetaan käyttöomaisuuserille.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07337063c01f146c72ca6d9e0f9096907cdc9638
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442859"
---
# <a name="create-a-depreciation-proposal"></a>Luo poistoehdotus

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka poiston eräehdotukset toimivat ja kuinka poisto ehdotetaan käyttöomaisuuserille. Tässä tehtävässä käytetään USMF-esittely-yritystä ja kirjanpitäjän roolia.


## <a name="create-a-depreciation-proposal"></a>Luo poistoehdotus
1. Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Kirjauskansioviennit > Luo poistoehdotus**.
2. Valitse **Kirjauskansion nimi**-kentästä vaihtoehto avattavasta valikosta.
3. Kirjoita päivämäärä **Päivämäärään**-kenttään.

    - Valitse **Tee yhteenveto poistoista** -valintaruutu kootaksesi kuukausittaiset poistot yhdelle kirjauskansioriville.  
    - Jos esimerkiksi Päivämäärään-arvo on 31. maaliskuuta 2015, seuraava kuvaus muodostetaan: Poistot alkaen 31. tammikuuta 2015. Ehdotettavien kirjauskansiorivien **Päivämäärä**-kenttään määritetään sitten 31. maaliskuuta 2015.  
    - Poistoehdotus voidaan suodattaa käyttöomaisuuserän, käyttöomaisuusryhmän tai muun ehdon avulla käyttämällä **Suodatus**-vaihtoehtoa.  
    - Kun käytössä on **Luo hankinta- tai poistoehdotus käyttöomaisuudelle** -lomake, voit ehdottaa erille poistoa. Tätä suositellaan suuremmille ehdotuksille, jotka käyttävät enemmän järjestelmäresursseja. Jos valitset erävaihtoehdon, voit edelleen suorittaa muita tehtäviä samaan aikaan. Kun näin poiston ehdottaa, poisto lasketaan käyttöomaisuuden arvomalleille.  

4. Valitse **Luo kirjauskansio**.

## <a name="review-depreciation-entries"></a>Poistotapahtumien tarkasteleminen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio**.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Valitse **Rivit**.
4. Valitse **Kirjaa**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]