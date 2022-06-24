---
title: Luo ehdotus, joka käyttää tarjouspyyntöä
description: Tässä artikkelissa kerrotaan, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecde250e3517464611b68fe3c960bfbfdf06319
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846008"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Luo ehdotus, joka käyttää tarjouspyyntöä

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista. Tämän oppaan esimerkkiä voidaan käyttää USMF-yrityksen demotiedoilla, ja sinun on kirjauduttava järjestelmänvalvojana suorittaaksesi kaikki vaiheet. Tässä oppaassa tehtävät kuuluvat yleensä hankintojen asiantuntijoille.


## <a name="create-a-requisition"></a>Luo ehdotus
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostoehdotukset > Itse luodut ostoehdotukset**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Nimi**-kenttään.
4. Kirjoita päivämäärä **Vaadittu päivämäärä** -kenttään.
5. Kirjoita päivämäärä **Kirjauspäivä**-kenttään.
6. Valitse **OK**.
7. Anna tai valitse **Syy**-kentässä arvo.
8. Valitse **Lisää rivi**.
9. Valitse **Hankintaluokka**-kenttään puussa oleva luokka ja valitse sitten **OK**.
10. Kirjoita arvo **Tuotteen nimi**-kenttään.
11. Anna **Määrä**-kentässä numero.
12. Syötä tai valitse arvo **Yksikkö**-kenttään.
13. Valitse **Tallenna**.
14. Avaa valintaikkuna valitsemalla **Työnkulku**.
15. Valitse **Lähetä**.
16. Sulje sivu.
17. Valitse **Lähetä**.

## <a name="reassign-a-workflow-task"></a>Määritä työnkulkutehtävä uudelleen
Seuraava tehtävä on luoda tarjouspyyntö toimittajien tuotetarjouksia varten. USMF-esittelytiedoissa ostoehdotuksen työnkululle on määritetty sääntö, jos toimittajaa ei ole valittu tai rivin yksikköhinta on 0, tietylle työntekijälle määritetään tarjouspyynnön luomisen tehtävä. Voit jatkaa tämän oppaan seuraamista delegoimalla kyseisen tehtävän toiselle käyttäjälle (itsellesi). Voit tehdä tämän vain, jos olet kirjautunut sisään järjestelmänvalvojana  

1. Avaa valintaikkuna valitsemalla **Työnkulku**.
2. Valitse **Näytä historia**.
3. Päivitä sivu.
4. Laajenna **Seurantatiedot** -osa.
5. Valitse puusta rivi, joka alkaa "Rivin työnkulku käynnistetty".
6. Valitse **Näytä työnkulun tiedot**.
7. Laajenna **Työnimikkeet**-osa.
8. Valitse **Määritä uudelleen**.
9. Valitse **Järjestelmänvalvoja** **Käyttäjä**-kentässä.
10. Valitse **Määritä uudelleen**.
11. Sulje sivut.

## <a name="create-an-rfq"></a>Luo tarjouspyyntö

1. Päivitä sivu.
2. Valitse **Tarjouspyyntö**.
3. Valitse **Ostava yritys** -kenttään **USMF**. Valitse sama yritys, joka on ehdotusrivillä.  
4. Merkitse valittu rivi luettelossa. Jos ostoehdotuksessa on useita rivejä, valitse kaikki rivit, jotka haluat lisätä tarjouspyyntöön.  
5. Valitse **OK**.
6. Päivitä sivu.
7. Varmista, että tietoruutu on avoinna ja laajenna **Liittyvät asiakirjat** -osa.
8. Valitse **Tarjouspyyntö**-kentän linkkiä avataksesi juuri luodun tarjouspyynnön.
9. Valitse **Otsikko**.
10. Valitse **Lisää**.
11. Anna tai valitse arvo **Toimittajatili**-kentässä.
12. Valitse **Lisää**.
13. Anna tai valitse arvo **Toimittajatili**-kentässä.
14. Valitse **Lähetä**.
15. Valitse **OK**.
16. Valitse **Kirjoita vastaus**.
17. Valitse toimintoruudussa **Vastaa**.
18. Valitse **Kopioi tiedot vastaukseen**. Tämä kopioi tarjouspyynnön tiedot, kuten määrän ja päivämäärät, vastaukseen.  
19. Syötä **Yksikköhinta**-kenttään numero. Tämä on hinta, jonka olet saanut toimittajalta. Voit myös halutessasi kirjoittaa toimittajalta saamiasi lisätietoja.  
20. Valitse **Hyväksy**.
21. Valitse **OK**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Tarkista, että hinta ja toimittaja on siirretty ehdotukseen
1. Sulje sivu.
2. Valitse **Rivit**.
3. Valitse **Aiheeseen liittyviä tietoja**.
4. Valitse **Ostoehdotus**.
5. Valitse tarjouspyyntöön siirretty rivi. Tarkista, että hinta ja toimittaja on kopioitu ehdotukseen..  
6. Avaa valintaikkuna valitsemalla **Työnkulku**.
7. Valitse Valmis.
8. Valitse sivu.
9. Valitse Valmis.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]