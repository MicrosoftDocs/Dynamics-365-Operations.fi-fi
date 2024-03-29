---
title: Myyntitilausten lähettäminen ilman varastointia
description: Tässä artikkelissa kerrotaan, miten myyntitilaus päivitetään, kun tuotteet on lähetetty asiakkaalle.
author: Henrikan
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bb4115a486fbfe7287c9b183224699de4dfd456
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335522"
---
# <a name="ship-sales-orders-without-warehousing"></a>Myyntitilausten lähettäminen ilman varastointia

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten myyntitilaus päivitetään, kun tuotteet on lähetetty asiakkaalle. Opastus koskee toteutustyönkulkua, jota ei ole määritetty varastonhallintaa varten (ei perus- eikä varastonhallintaprosesseihin (WMS)), joten se ei edellytä tuotteen keräilyn rekisteröintiä ennen lähetystä. Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja. Molemmissa tapauksissa ennen tehtävän aloittamista varastoidulle tuotteelle on luotava myyntitilaus, jonka määrä on suurempi kuin 1. Kirjausvirheen välttämiseksi sinun on tarkistettava, että tuotteen varastossa oleva määrä tilaukseen valitussa toimipaikassa ja varastossa riittää kattamaan tilausmäärän.

## <a name="post-packing-slip-for-an-order"></a>Kirjaa tilauksen pakkausluettelo
1. Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.
2. Etsi ja valitse luettelossa tehtävää varten luotu tilaus.
3. Valitse toimintoruudussa **Kerää ja pakkaa**.
4. Valitse **Kirjaa pakkausluettelo**.
5. Laajenna tai tiivistä **Parametrit**-osa.
6. Valitse **Määrä**-kentässä **Kaikki**.
    - Vaihtoehtoja ovat lisäksi **Toimita nyt** ja **Keräilty**. Jos tilausrivi toimitetaan osittain ja tilausrivin **Toimita nyt** -kentässä on määrä, valitaan **Toimita nyt**. Jos organisaation toteuttamistyönkulku sisältää keräilyn erillisenä, keräysluettelon hallitsemana ja rekisteröimänä prosessina, valitaan **Keräilty**.  
    - Tarkista, että **Kirjaus**-asetukseksi on valittu **Kyllä**.  
7. Valitse **Tulosta pakkausluettelo** -asetukseksi **Kyllä**. Tälle kirjaukselle luotavat pakkausluettelot ovat **Yhteenveto**-välilehdessä. Jos toimitat yksittäisen tilauksen, pakkausluetteloita on yleensä yksi. Jos kyseiseen tilauksen rivit kuitenkin toimitetaan eri toimipaikoista, kirjaus jaetaan automaattisesti niin, että asiakirjoja on tarvittava määrä. Tämä on pakollinen ehto, jota ei voi muuttaa. Kirjaus jaetaan vastaavasti useisiin asiakirjoihin myös silloin, jos tilauksen rivit lähetetään eri toimitusosoitteisiin ja lähetyskäytäntö määrittää jaon pakolliseksi.  
8. Valitse **Rivit**-välilehdessä lähetettävän tilausrivin rivi.
9. Lisää **Päivitä**-kenttään luku, joka on pienempi kuin alkuperäinen määrä.
10. Valitse **OK**.
11. Valitse **Kyllä**.
12. Sulje sivu.
13. Valitse toimintoruudussa **Asetukset**.
14. Valitse **Vaihda näyttö**.
15. Valitse **Otsikkonäkymä**.
    - Jos kaikki tilauksen rivit on lähetetty kokonaisuudessa, tilauksen tila muuttuu avoimesta toimitetuksi.  
    - Tässä esimerkissä tilausrivi on toimitettu osittain. Tämän vuoksi vielä tilaus on edelleen avoinna.     
    - **Asiakirjan tila** -kentän asetuksena on Pakkausluettelo, koska vähintään yksi tilausriveistä on lähetetty.  
16. Valitse toimintoruudussa **Yleiset**.
17. Valitse **Rivin määrä**.
18. Sulje sivu.
19. Valitse toimintoruudussa **Kerää ja pakkaa**.
20. Valitse **Pakkausluettelo**. Kaikki tilausta varten luodut pakkausluetteloasiakirjat ovat **Pakkausluettelo-kirjauskansio**-sivulla. Voit tarvittaessa tarkastella kunkin asiakirjan tietoja ja tulostaa ne.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]