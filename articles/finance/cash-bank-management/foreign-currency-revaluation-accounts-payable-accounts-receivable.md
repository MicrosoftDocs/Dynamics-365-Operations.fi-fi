---
title: Valuutan uudelleenarvostus osto- ja myyntireskontrassa
description: Tässä artikkelissa on tietoja ulkomaanvaluutan uudelleenarvostusprosessista, jonka avulla voidaan päivittää osto- ja myyntireskontran avoimien tapahtumien arvo.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: kfend
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73f20323ff2eb36c89f4fb2848a056c2cb24ec30
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715718"
---
# <a name="currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Valuutan uudelleenarvostus osto- ja myyntireskontrassa

[!include [banner](../includes/banner.md)]

Valuuttakurssien vaihdellessa avoimien tapahtumien teoreettinen arvo (kirjanpitoarvo) ulkomaan valuuttana vaihtelee ajan myötä. Tässä artikkelissa on tietoja ulkomaanvaluutan uudelleenarvostusprosessista, jonka avulla voidaan päivittää osto- ja myyntireskontran avoimien tapahtumien arvo. 

Avoimien toimittajatapahtumien teoreettinen arvo, eli kirjanpitoarvo ulkomaan valuuttana vaihtelee ajan myötä, kun valuuttakurssit vaihtelevat. Voit päivittää osto- ja myyntireskontran avoimien tapahtumien arvon suorittamalla ulkomaanvaluutan uudelleenarvostusprosessin. Ulkomaanvaluutan uudelleenarvostuksen voi ajaa sekä osto- että myyntireskontrassa. Prosessi uudelleenarvostaa avoimet summat, eli selvittämättömät summat uudella vaihtokurssilla tiettynä päivänä. Alkuperäisten kirjattujen summien ja uudelleenarvostettujen summien väliset erot aiheuttavat toteutumattoman voiton tai tappion jokaiselle avoimelle tapahtumalle. Osto- ja myyntireskontran alareskontrat päivitetään sitten vastaamaan toteutumatonta voittoa tai tappiota, ja kirjanpidon tapahtuma kirjataan kirjanpitoon.

## <a name="simulate-a-foreign-currency-revaluation"></a>Ulkomaanvaluutan uudelleenarvostuksen stimuloiminen
Voit ajaa simulaatioraportin ulkomaanvaluutan uudelleenarvostukselle samalla päivämäärällä ja menetelmällä ennen ulkomaanvaluutan uudelleenarvostusta avoimille tapahtumille. Simulointiraportin voit ajaa napsauttamalla **Ulkomaanvaluutan uudelleenarvostus** -sivulla **Simulaatio**-painiketta. Raportti tarjoaa yhteenvedon toteutumattomasta voitosta tai tappiosta simulaatiolle määritettyjen parametrien mukaan.

## <a name="process-a-foreign-currency-revaluation"></a>Ulkomaanvaluutan uudelleenarvostuksen käsittely
Uudelleenarvosta avoimet tapahtumat **Kausittaiset tehtävät** -kohdan alta löytyvän **Ulkomaanvaluutan uudelleenarvostus** -sivun avulla. Voit suorittaa prosessin reaaliaikaisena tai ajoittaa sen erän avulla. Kun määrität uudelleenarvostusprosessin asetuksia, varmista, haluatko tulostaa tulosraportin. Uudelleenarvostusraporttia ei voi tulostaa uudelleen prosessin valmistuttua. Jos luot ulkomaanvaluutan uudelleenarvostusraportin, raportissa näytetään useita saldoja asiakas-/toimittajatasolla sekä valuuttatasolla:

-   Niiden asiakkaiden tai toimittajien saldot, joilla on uudelleenarvostettuja valuuttatapahtumia. Seuraavat saldot näytetään:
    -   Alkuperäinen loppusaldo ulkomaan valuuttana.
    -   Ulkomaanvaluutan uudelleenarvostuksen kokonaissumma kirjanpitovaluuttana, edellisestä uudelleenarvostuksesta lähtien.
    -   Ulkomaanvaluutan uudelleenarvostuksen kokonaissumma kirjanpitovaluuttana, nykyisestä uudelleenarvostuksesta lähtien.
    -   Edellisen ja nykyisen uudelleenarvostuksen erotus. Tämä erotus on toteutumaton lisävoitto- tai tappio.
-   Toteutumaton kokonaisvoitto- tai tappio jokaiselle valuutalle.

Ulkomaanvaluutan uudelleenarvostusprosessin ajosta säilytetään aina tietue. Valitse **Tapahtumat** **Ulkomaanvaluutan uudelleenarvostus** -sivulla, jos haluat tarkastella uudelleenarvostuksessa luotujen tapahtumien luetteloa. Jokainen tositetapahtuma vastaa uudelleenarvostettua avointa tapahtumaa. Jos avoin tapahtuma on uudelleenarvostettu useammin kuin kerran, näet kaksi tietuetta, joilla on sama tosite. Yksi tietue vastaa edellisen toteutumattoman voiton tai tappion peruutusta, ja toinen vastaa uutta toteutumatonta voittoa tai tappiota. Voit suorittaa uudelleenarvostusprosessi napsauttamalla **Ulkomaanvaluutan uudelleenarvostus** -painiketta. Määritä seuraaville parametreille asianmukaiset asetukset:

-   **Menetelmä** – Menetelmä, jota käytetään valitussa ulkomaanvaluutan uudelleenarvostustyössä:
    -   **Vakio** – Ulkomaanvaluutan uudelleenarvostustyöt kirjataan riippumatta siitä, onko tuloksena voitto vai tappio.
    -   **Vähintään** – Ulkomaanvaluutan uudelleenarvostustyöt kirjataan vain, jos tuloksena on tappio.
    -   **Laskun päivämäärä** Ulkomaanvaluutan uudelleenarvostustöissä käytetään niiden tapahtumien alkuperäistä vaihtokurssia, jotka arvostetaan uudelleen alkuperäiseen arvoonsa kirjanpitovaluutassa. Kaikkien aiempien ulkomaanvaluutan uudelleenarvostusten vaikutukset peruutetaan.
-   **Tarkastelupäivämäärä** – Päivä, jolloin havaitsee kaikki sellaiset tapahtumat, joissa on kyseisenä päivänä avoimia (selvittämättömiä) summia. Ulkomaan valuuttasummat arvostetaan uudelleen vaihtokursseilla, jotka on kirjattu **Vaihtokurssit**-sivulle tarkastelupäivänä. Kun ulkomaan valuuttasummat arvostetaan tarkastelupäivämääränä, tästä päivästä tulee ulkomaan valuutan uudelleenarvostuksen viimeinen tapahtumien hyväksymispäivä oikaistuille tapahtumille. Jos suoritat ulkomaanvaluutan uudelleenarvostuksen tarkastelupäivämääränä, joka on ennen jo oikaistujen tapahtumien viimeistä ulkomaanvaluutan uudelleenarvostusta, kausittainen työ ei oikaise sellaisia tapahtumia, jotka ovat aiempana tarkastelupäivämääränä avoimia, mutta joilla on myöhempi ulkomaanvaluutan uudelleenarvostus.
-   **Kurssin päivämäärä** – Päivämäärä, jonka mukaan ulkomaanvaluutan uudelleenarvostustapahtumassa käytetty vaihtokurssi määräytyy.
-   **Käytettävä kirjausprofiili** – Kirjausprofiili, jota käytetään oletusarvoisen osto- tai myyntireskontran päätilin kirjanpitokirjausten suorittamiseen ulkomaanvaluutan uudelleenarvostustapahtumille:
    -   **Kirjaus** – Käytetään asiakastapahtuman kirjausprofiilia.
    -   **Valitse** – Syötä kirjausprofiili **Kirjausprofiili**-kenttään.
-   **Kirjausprofiili** – Jos **Käytettävä kirjausprofiili** -kentän arvoksi on valittu **Valitse**, ulkomaanvaluutan uudelleenarvostustapahtumien kirjausprofiili määräytyy tämän kentän kirjausprofiilin mukaan.
-   **Taloushallinnon dimensiot** – Ulkomaanvaluutan uudelleenarvostustapahtumien kirjanpitomerkintöihin kirjattavat taloushallinnon dimensiot. Taloushallinnon dimensioita ei ole vahvistettu tilirakenteen sääntöjen perusteella. Tilirakenne, joka oli käytössä laskujen kirjausaikana, ei ehkä ole sama kuin säännöt, jotka olivat käytössä, kun uudelleenarvostus suoritettiin. Uudelleenarvostusprosessissa ei voi valita tiettyjä taloushallinnon dimensioita, joten tilirakenteen vahvistus ohitetaan.  
    -   **Ei mitään** – Kirjanpitodimensioita ei kirjata. Jos tilirakenteessasi on pakollinen taloushallinnon dimensio, uudelleenarvostusprosessi ajetaan siitä huolimatta ja prosessi luo kirjanpitomerkinnät, joissa ei ole taloushallinnon dimensioita. Näyttöön tulee ensin varoitussanoma voidaksesi peruuttaa uudelleenarvostuksen.
    -   **Taulu** – Ulkomaanvaluutan uudelleenarvostustapahtumiin kirjataan asiakas- tai toimittajan tilin taloushallinnon dimensioita.
    -   **Kirjaus** – Ulkomaanvaluutan uudelleenarvostustapahtumiin kirjataan uudelleenarvostettavana olevan tapahtuman taloushallinnon dimensioita. Oletusarvoisesti uudelleenarvostustapahtuman osto-/myyntireskontran päätilissä käytetään alkuperäisen tapahtuman osto-/myyntireskontran kirjanpitotilin taloushallinnon dimensioita, ja alkuperäisen tapahtuman kulu/vara/voitto-kirjanpitotilin taloushallinnon dimensioita käytetään uudelleenarvostustapahtuman toteutumaton voitto/tappio -päätilillä.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
