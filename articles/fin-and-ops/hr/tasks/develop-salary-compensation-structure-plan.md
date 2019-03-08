---
title: Palkka- ja kompensaatiorakenteen ja -suunnitelman kehittäminen
description: Tässä tehtävän ohjauksessa kerrotaan kiinteän kompensaatiosuunnitelman luontiprosessista ja siitä, miten työntekijöille annetaan mahdollisuus rekisteröityä suunnitelmaan oikeutussääntöjen avulla.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 28d044cedbcc9f483a4deb7739aef0f8e3abf9ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "332768"
---
# <a name="develop-salarycompensation-structure-and-plan"></a>Palkka- ja kompensaatiorakenteen ja -suunnitelman kehittäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa kerrotaan kiinteän kompensaatiosuunnitelman luontiprosessista ja siitä, miten työntekijöille annetaan mahdollisuus rekisteröityä suunnitelmaan oikeutussääntöjen avulla. Tämän tehtävän luomisessa käytetään esittely-tietojen yritystä USMF. Tehtävä on tarkoitettu etuuspäällikölle.


## <a name="create-fixed-compensation-plan"></a>Kiinteän kompensaatiosuunnitelman luominen
1. Valitse Kompensaation hallinta.
2. Valitse Kiinteät kompensaatiosuunnitelmat.
3. Valitse Uusi.
4. Kirjoita arvo Suunnitelma-kenttään.
5. Kirjoita arvo Kuvaus-kenttään.
6. Syötä päivämäärä Voimaantulopäivä-kenttään.
7. Määritä Tyyppi-kentässä, onko kiinteä kompensaatiosuunnitelma kompensaatioluokka, palkkaluokka vai vaihesuunnitelma.
8. Suositus sallitaan -valintaruutu toimii minkä tahansa käsittelytapahtumassa tähän suunnitelmaan lisätyn toiminnon oletusarvona.  Jos suositukset ovat käytössä, voit korvata lasketun ohjeellisen summan kompensaation käsittelyn yhteydessä.
9. Alueen ulkopuolisuuden toleranssin avulla voit määrittää, miten annetun tason määritetyn kompensaatiorakenteen alueen ulkopuolella olevia kompensaatiosummia käsitellään.  Jos Alueen ulkopuolisuuden toleranssi -kohdan arvo on Ei mitään, mitä tahansa kompensaatiosummaa voidaan käyttää.  Alustava toleranssi varoittaa käyttäjää, jos kompensaatiosumma on pienempi kuin kyseisen tason vähimmäisviitepisteen summa tai suurempi kuin tason enimmäissumma. Käyttäjä voi ohittaa varoituksen ja jatkaa.  Kiinteä toleranssi luo virheen, jos työntekijän kompensaatio on määritetty tason vähimmäis- ja enimmäisviitepisteen ulkopuolelle. Se muokkaa työntekijän kompensaatiota automaattisesti niin, että se kuuluu alueeseen.
10. Työhönottosääntö-kenttää käytetään suoritettaessa kompensaatioprosessitapahtuma työntekijän kompensaation laskemista varten.  Prosentin työhönottosääntö laskee nousun, joka jaetaan sille ajalle, jonka työntekijä on työskennellyt syklissä.
11. Kirjoita arvo Valuutta-kenttään.
12. Syötä tai valitse arvo Palkkion muunnos -kenttään.
13. Laajenna Palkka-alueen käyttöastematriisi -osa.
    * Vaihtoehtoisesti voit lisätä alueen käyttöasteen tietueita, jos haluat työntekijöiden saavuttavan alueen keskipisteen nopeammin ja maksimin hitaammin.  
14. Tässä vaiheessa kiinteä kompensaatiosuunnitelma on tallennettava, jotta Määritä kompensaatio -painike tulee käyttöön. Tämän jälkeen voit jatkaa suunnitelman kompensaatiorakenteen määrittämistä.  Valitse Tallenna.
15. Valitse Määritä kompensaatio.
    * Kompensaatiorakenteen voi luoda kolmella eri tavalla. 1: Luo kokonaan uusi rakenne valitsemalla viitepisteet ja lisäämällä tasot, joiden avulla oma rakenne luodaan. 2: Kopioi aiemmin luodun suunnitelman kompensaatiorakenne aloituskohdaksi ja muokkaa uusi suunnitelma sen avulla. 3: Valitse aiemmin luotu kompensaatioruudukko. Jos toinen suunnitelma jo käyttää kompensaatioruudukkoa, ruudukkoon tehdyt muutokset vaikuttavat myös tähän suunnitelmaan.  
16. Valitse Luo aiemmin luodusta kompensaatiomatriisista uusi matriisi -asetus.
17. Anna tai valitse Kopioi ruudukosta -kentän arvo.
    * Vaihtoehtoisesti voit muuttaa valitun ruudukon kopioksi luotavan uuden kompensaatioruudukon nimen.  
18. Valitse OK.
19. Valitse Joukkomuutos.
    * Joukkomuutostoiminnon avulla voit ylläpitää kompensaatiomatriisin summia kohdistamalla prosentin tai kiinteän summan lisäyksen vähintään yhteen tasoon ja/tai viitepisteeseen.  
20. Syötä Oikaisusumma-kenttään numero.
21. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
22. Valitse Sovella ruudukkoon.
23. Sulje sivu.
    * Kun kompensaatiorakenne on luotu tai valittu, voit valita kiinteän kompensaatiosuunnitelman tarkistuspisteinä käytettävät viitepisteet.  Tarkistuspistettä käytetään laskettaessa työntekijän kompensaatioastetta.  
24. Anna tai valitse arvo Tarkistuspiste-kenttään.
25. Sulje sivu.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Oikeutussäännön luominen uudelle kiinteälle kompensaatiosuunnitelmalle
    * Uutta kiinteää kompensaatiosuunnitelmaa ei voi liittää työntekijään, ennen kuin suunnitelmalle on määritetty oikeutussäännöt.  
1. Valitse Oikeutussäännöt.
2. Valitse Uusi.
3. Kirjoita arvo Oikeutus-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Syötä päivämäärä Voimaantulopäivä-kenttään.
    * Oikeutussääntöjä käytetään sekä kiinteissä että muuttuvissa kompensaatiosuunnitelmissa.  Valitse Tyyppi-kentässä se suunnitelman tyyppi, jossa näitä oikeutussääntöjä käytetään.  
6. Anna tai valitse Suunnitelma-kentässä arvo.
    * Valitse ehdot, jotka työntekijän on täytettävä, ennen kuin hän on oikeutettu kompensaatiosuunnitelmaan. Ehdot voivat koskea osastoa, ammattijärjestöä, sijaintia (kompensaatioalue), työtä, toimintoa, työn tyyppiä tai kompensaatiotasoa. Työntekijän on täytettävä kaikki määritetyt ehdot, jotta hän on oikeutettu kompensaatiosuunnitelmaan. Jos ehtoja ei ole määritetty, kaikki työntekijät ovat oikeutettuja kompensaatiosuunnitelmaan. Jos työntekijä ei täytä oikeutussäännön määrittämiä ehtoja tai jos kompensaatiosuunnitelmalle ei ole määritetty oikeutussääntöä, kompensaatiosuunnitelma ei ole valittavissa, kun työntekijälle luodaan kiinteää kompensaatiotietuetta.  
7. Sulje sivu.
8. Sulje sivu.

