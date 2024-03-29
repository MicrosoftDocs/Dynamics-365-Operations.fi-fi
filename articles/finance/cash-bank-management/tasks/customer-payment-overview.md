---
title: Asiakkaan maksun yhteenveto
description: Tässä menettelyssä käsitellään erilaisia tapoja, joilla asiakkaan maksuja syötetään.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b90b7f200133cfb0d30b335aca20c328856fba5
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778119"
---
# <a name="customer-payment-overview"></a>Asiakkaan maksun yhteenveto

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään erilaisia tapoja, joilla asiakkaan maksuja syötetään. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra > Maksut > Maksukirjauskansio**.
2. Valitse **Uusi**.
3. Valitse maksukirjauskansio, johon asiakkaan maksut tallennetaan.
4. Valitse kirjauskansio tai syötä se manuaalisesti.
5. Valitse **toimintoruudussa** **Lisää asiakkaan maksuja**. Lisää asiakkaan maksuja -sivua käytetään tallennettaessa yksi asiakkaan maksu kerralla. Voit syöttää samalla sivulla maksun tiedot (sivun yläosassa) ja maksun yhteydessä maksetut laskut.  
6. Syötä asiakas, jolta vastaanotit maksun. Jos et tiedä asiakasta, mutta tiedät maksetun tapahtuman, voit syöttää maksun **Tapahtuma**-kenttään. Syötä tai valitse lasku **Tapahtuma**-kentässä. Asiakas haetaan automaattisesti tapahtuman valitsemisen jälkeen.
7. Anna **Maksuviite**-kentässä maksuviite. Maksuviite voi olla asiakkaan sekkinumero tai asiakkaan sähköisen maksun viite. Maksuviite vaaditaan vain, jos maksu on merkitty talletuskuittiin sisällytettäväksi.  
8. Valitse **Talletuskuitti**-kentässä, sisällytetäänkö maksu tallennuskuittiin. 
9. Anna **Summa**-kentässä asiakkaan maksun summa. Maksun summaa ei haeta automaattisesti. Se on syötettävä manuaalisesti. 
10. Merkitse asiakkaan maksamat laskut. Jos maksu ennakkomaksu, laskuja ei tarvitse merkitä selvitystä varten. Maksun voi silti tallentaa ja kirjata. Laskun selvitys voidaan tehdä myöhemmin.
11. Syötä sen maksun summa, joka selvitetään merkitylle laskulle. Tätä kenttää voi käyttää, kun maksu koskee osittaista maksua. Jos et syötä summaa, selvitettävä summa määritetään automaattisesti.
12. Valitse **Tallenna kirjauskansioon**. Ennen kuin tallennat maksun kirjauskansioon, varmista, että vastatili on määritetty. **Tallenna kirjauskansioon** -toimintoa käytettäessä maksu tallennetaan ja siirretään kirjauskansioon. Tämän jälkeen voit jatkaa seuraavan maksun syöttämistä.
13. Sulje sivu.
14. Valitse **toimintoruudussa** **Rivit**. Kun avaat **Rivit**-kohdan, näkyviin tulevat **Lisää asiakkaan maksuja** -sivulla tallennetut ja kirjauskansioon siirretyt maksut. Tällä sivuilla voi myös syöttää uusia asiakkaan maksuja tai muokata aiemmin luotuja asiakkaan maksuja, ennen kuin ne kirjataan.
15. Luo toinen maksu valitsemalla **Uusi**. 
16. Valitse asiakas, jolta vastaanotit maksun. Jos et tiedä asiakasta, mutta tiedät, että maksun lasku on maksettu, syötä lasku manuaalisesti **Lasku**-kenttään tai valitse lasku siellä. Asiakas määritetään, kun lasku on valittu.  
17. Merkitse maksetut laskut valitsemalla **Selvitä tapahtumat**. Yhdenkään laskun maksua ei tarvitse selvittää. Jos tämä on ennakkomaksu tai jos et tiedä maksettua laskua, voit syöttää ja kirjata maksun. Maksu voidaan tilittää laskulle myöhemmin.  
18. Merkitse maksussa maksetut laskut. 
19. Anna **Summa**-kenttään sen maksun summa, joka selvitetään laskulle.
20. Valitse **OK**.
21. Anna **Maksuviite**-kentässä maksuviite. Maksuviite vaaditaan vain, jos maksu on merkitty talletuskuittiin sisällytettäväksi.  
22. Kirjaa asiakkaan maksut valitsemalla **toimintoruudussa** **Kirjaa**. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
