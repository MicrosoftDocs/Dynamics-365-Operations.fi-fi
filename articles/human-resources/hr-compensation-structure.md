---
title: Kompensaatiorakenteen kehittäminen
description: Tässä artikkelissa kerrotaan kiinteän kompensaatiosuunnitelman luomisesta ja siitä, miten työntekijät voivat rekisteröityä suunnitelmaan oikeutussääntöjen avulla.
author: andreabichsel
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2649a392b5c8bb2482622eba22b0b2f458058314dce25a8b9032eb2ef518240c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732366"
---
# <a name="develop-a-compensation-structure"></a>Kompensaatiorakenteen kehittäminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kerrotaan kiinteän kompensaatiosuunnitelman luomisesta ja siitä, miten työntekijät voivat rekisteröityä suunnitelmaan oikeutussääntöjen avulla. Tässä artikkelissa käytetään USMF-esittelytietoja. Artikkeli on tarkoitettu kompensaatio- ja etuuspäälliköille.

## <a name="create-a-fixed-compensation-plan"></a>Luo kiinteä kompensaatiosuunnitelma

1. Valitse **Kompensaation hallinta**.

2. Valitse **Kiinteät kompensaatiosuunnitelmat**.

3. Valitse **Uusi**.

4. Anna **Suunnitelma**-kenttään arvo.

5. Anna arvo **Kuvaus**-kentässä.

6. Syötä päivämäärä **Voimaantulopäivä**-kenttään.

7. Määritä **Tyyppi**-kentässä, onko kiinteä kompensaatiosuunnitelma **kompensaatioluokka**-, **palkkaluokka**- vai **vaihesuunnitelma**.

8. **Suositus sallitaan** -valintaruutu toimii minkä tahansa käsittelytapahtumassa tähän suunnitelmaan lisätyn toiminnon oletusarvona. Jos suositukset ovat käytössä, voit korvata lasketun ohjeellisen summan kompensaation käsittelyn yhteydessä.

9. **Alueen ulkopuolisuuden toleranssi** -kentän avulla voit määrittää, miten annetun tason määritetyn kompensaatiorakenteen alueen ulkopuolella olevia kompensaatiosummia käsitellään. Kun määrität **Alueen ulkopuolisuuden toleranssi** -kentän arvoksi **Ei mitään**, voit käyttää mitä tahansa kompensaatiosummaa. **Alustava toleranssi** varoittaa käyttäjää, jos kompensaatiosumma on pienempi kuin vähimmäisviitepisteen summa tai suurempi kuin tason enimmäissumma. Käyttäjät voivat ohittaa varoituksen ja jatkaa. **Kiinteä toleranssi** luo virheen, jos työntekijän kompensaatio on tason vähimmäis- ja enimmäisviitepisteen ulkopuolella. Se muokkaa työntekijän kompensaatiota automaattisesti niin, että se kuuluu alueeseen.

10. **Työhönottosääntö**-kenttä laskee työntekijän kompensaation tapahtuman käsittelyn aikana. **Työhönottosääntö**, joka on **Prosentti**,  laskee nousun, joka jaetaan sille ajalle, jonka työntekijä on työskennellyt syklissä.

11. Kirjoita arvo **Valuutta**-kenttään.

12. Syötä tai valitse arvo **Palkkion muunnos** -kenttään.

13. Laajenna **Palkka-alueen käyttöastematriisi** -osa. Vaihtoehtoisesti voit lisätä alueen käyttöasteen tietueita, jos haluat työntekijöiden saavuttavan alueen keskipisteen nopeammin ja maksimin hitaammin.

14. Valitse **Tallenna**. **Määritä kompensaatio** -painike tulee käyttöön. Tämän jälkeen voit jatkaa suunnitelman kompensaatiorakenteen määrittämistä.

15. Valitse **Määritä kompensaatio**. Voit luoda kompensaatiorakenteen jollakin seuraavista kolmesta tavasta:

    - Luo kokonaan uusi rakenne valitsemalla viitepisteet ja lisäämällä tasot, joiden avulla oma rakenne luodaan.
    - Kopioi aiemmin luodun suunnitelman kompensaatiorakenne aloituskohdaksi ja muokkaa uusi suunnitelma sen avulla.
    - Valitse aiemmin luotu kompensaatioruudukko. Jos toinen suunnitelma jo käyttää kompensaatioruudukkoa, ruudukkoon tehdyt muutokset vaikuttavat myös tähän suunnitelmaan.

16. Valitse **Luo aiemmin luodusta kompensaatiomatriisista uusi matriisi**.

17. Anna arvo **Kopioi ruudukosta** -kenttään tai valitse siihen arvo. Vaihtoehtoisesti voit muuttaa valitun ruudukon kopioksi luotavan uuden kompensaatioruudukon nimen.

18. Valitse **OK**.

19. Valitse **Joukkomuutos**. **Joukkomuutostoiminnon** avulla voit ylläpitää kompensaatiomatriisin summia kohdistamalla prosentin tai kiinteän summan lisäyksen vähintään yhteen tasoon tai viitepisteeseen.

20. Anna **Oikaisusumma**-kenttään arvo.

21. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.

22. Valitse **Käytä ruudukossa**.

23. Sulje sivu. Kun kompensaatiorakenne on luotu, voit valita kiinteän kompensaatiosuunnitelman tarkistuspisteinä käytettävät viitepisteet. Tarkistuspistettä käytetään laskettaessa työntekijän kompensaatioastetta.

24. Anna arvo **Tarkistuspiste**-kenttään tai valitse siinä arvo.

25. Sulje sivu.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Oikeutussäännön luominen kiinteälle kompensaatiosuunnitelmalle

Uutta kiinteää kompensaatiosuunnitelmaa ei voi liittää työntekijään, ennen kuin suunnitelmalle on määritetty oikeutussäännöt.  

1. Valitse **Oikeutussäännöt**.

2. Valitse **Uusi**.

3. Anna arvo **Oikeutus**-kenttään.

4. Anna arvo **Kuvaus**-kentässä.

5. Syötä päivämäärä **Voimaantulopäivä**-kenttään. Oikeutussääntöjä käytetään sekä kiinteissä että muuttuvissa kompensaatiosuunnitelmissa. Valitse **Tyyppi**-kentässä suunnitelman tyyppi.

6. Anna tai valitse **Suunnitelma**-kentässä arvo. Valitse ehdot, jotka työntekijän on täytettävä, ennen kuin hän on oikeutettu kompensaatiosuunnitelmaan. Ehtoja voivat olla seuraavat:

    - **Osasto**
    - **Ammattijärjestö**
    - **Sijainti** (**kompensaation alue**)
    - **Työ**
    - **Toiminto**
    - **Työlaji**
    - **Kompensaatiotaso**
    
    Työntekijän on täytettävä kaikki määritetyt ehdot, jotta hän on oikeutettu kompensaatiosuunnitelmaan. Jos et määritä ehtoja, kaikki työntekijät ovat oikeutettuja kompensaatiosuunnitelmaan. Jos työntekijä ei täytä oikeutussäännön määrittämiä ehtoja tai jos kompensaatiosuunnitelmalle ei ole määritetty oikeutussääntöä, kompensaatiosuunnitelma ei ole valittavissa, kun työntekijälle luodaan kiinteää kompensaatiotietuetta.

7. Sulje sivu.

8. Sulje sivu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]