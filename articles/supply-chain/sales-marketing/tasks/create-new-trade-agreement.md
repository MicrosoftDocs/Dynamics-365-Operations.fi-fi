---
title: Luo uusi kauppasopimus
description: Tämä menetelmä selittää, miten luodaan kauppasopimus, johon rekisteröidään tuotteen tietyn asiakkaan kanssa sovittu uusi hinta.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1642da7b06363d1f704e51276b5cb36823707231
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383415"
---
# <a name="create-a-new-trade-agreement"></a>Luo uusi kauppasopimus

[!include [banner](../../includes/banner.md)]

Tämä menetelmä selittää, miten luodaan kauppasopimus, johon rekisteröidään tuotteen tietyn asiakkaan kanssa sovittu uusi hinta. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi. Jos käytät omia tietojasi, varmista ennen tämän ohjeen käyttöä, että kauppasopimuksen kirjauskansion nimi on kohteeseen, jossa Oletussuhde-arvoksi on valittu Hinta (myynti).


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Luo ja kirjaa uusi kauppasopimuksen kirjauskansi
1. Valitse **Siirtymisruutu > Moduulit >Myynti ja markkinointi > Hinnat ja alennukset > Kauppasopimuksen kirjauskansiot**.
2. Valitse **Uusi**.
3. Avaa haku valitsemalla **Nimi**-kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Valitse **toimintoruudussa** **Rivit**.
6. Valitse **Tilikoodi**-kentässä Taulu.
    
    Tässä esimerkissä päivitetään tietyn asiakkaan hinta, joten sinun on valittava Taulu. Jos päivittäisit tuotteen luettelohinnan, valitsisit Kaikki, jotta uusi hinta koskisi kaikkia asiakkaita. Jos eri asiakassegmenteillä olisi eri hinta, valitsisit Ryhmä. Ryhmä-vaihtoehdon käyttö edellyttää asiakkaan hintaryhmien määrittämistä.  

7. Avaa haku napsauttamalla **Tilin valinta** -kentässä avattavan valikon painiketta.
8. Etsi haluamasi tietue luettelosta ja valitse se.
9. Valitse **Nimikekoodi**-kentässä Taulu.
    
    Kun annat kauppasopimuksen tyypiksi Hinta (myynti), **Nimikekoodi**-kentässä valitaan vain Taulu. Tämä johtuu siitä, että hinta on absoluuttinen arvo eikä kaikilla tuotteilla tai tuoteryhmillä voi olla sama hinta.
    
10. Avaa haku napsauttamalla **Nimikkeen suhde**-kentässä avattavan valikon painiketta.
11. Valitse luettelossa sopimukseen sisällytettävä tuote. Kirjaa muistiin valitsemasi tuotteet.  
12. Anna **Mistä**-kenttään vähimmäismäärä.
    - Jos asiakkaalla on tietty määrä, joka on tilattava ennen uuden hinnan käyttöönottoa, määrä on ilmoitettava tässä.  
    - Määritä **Mihin**-kenttään arvo, jota suurempana sopimuksen hinta ei kelpaa. Jos hinnat ja alennukset perustuvat useisiin hintarajoihin, määritä kunkin hintahaarukan vähimmäis- ja enimmäismäärä **Mistä**- ja **Mihin**-kenttiin.
13. Anna **Summa valuuttana** -kenttään hinta.
14. Anna **Tiedot**-osan **Päivämäärästä**-kenttään päivämäärä, jolloin sopimus astuu voimaan.
15. Valitse **Tallenna**.
16. Valitse **Vahvista**.
17. Valitse **Tarkista valitut rivit**.
18. Valitse **OK**.
19. Valitse **Kirjaa**.
20. Valitse **OK**.

## <a name="view-trade-agreements-for-a-product"></a>Näytä tuotteen kauppasopimukset
1. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.
2. Etsi ja valitse luettelosta tuote, jonka hinnan päivitit.
3. Valitse **toimintoruudussa** **Myynti**.
4. Valitse **Näytä kauppasopimukset**.
    
    Tarkastele juuri luodun hinnan kauppasopimuksen tietoja.    

5. Sulje sivu.

## <a name="additional-resources"></a>Lisäresurssit
### <a name="community-blogs"></a>Yhteisöblogit
- [Dynamics 365 for Finance and Operationsin myyntihinnat](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
