---
title: Ostoreskontran avaintiedot toimittajan laskua käyttämällä
description: Tämän tehtäväoppaan avulla voit luoda toimittajan laskun ostotilauksesta ja tarkastella ostotilauksen, vastaanoton ja laskun (kolmisuuntainen täsmäytys) täsmäytyksen tuloksia.
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f80c88b7fb3542f624d233f670cd7cd6ccd48b94
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143918"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a>Ostoreskontran avaintiedot toimittajan laskua käyttämällä

[!include [banner](../../includes/banner.md)]

Tämän tehtäväoppaan avulla voit luoda toimittajan laskun ostotilauksesta ja tarkastella ostotilauksen, vastaanoton ja laskun (kolmisuuntainen täsmäytys) täsmäytyksen tuloksia.


## <a name="create-a-purchase-order"></a>Ostotilauksen luominen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset**.
2. Valitse **Uusi**.
3. Avaa haku valitsemalla **Toimittajan tili** -kentässä avattavan valikon painike.
4. Etsi toimittaja ja valitse se. Voit esimerkiksi siirtyä kohtaan US-104.
5. Valitse toimittaja US-104.
6. Valitse **OK**.
7. Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.
8. Valitse varastonimike. Valitse tässä esimerkissä nimiketunnus 1000.
9. Laajenna **Rivin erittely** -pikavälilehti.
10. Valitse **Asetukset**-välilehti. Voit korvata täsmäytyskäytännön niin, että täsmäytystä ei käytetä tai että käytössä on kaksi- tai kolmisuuntainen täsmäytys.  
11. Valitse toimintoruudussa **Osto**.
12. Valitse **Vahvista**.

## <a name="receive-the-products"></a>Vastaanota tuotteet
1. Valitse toimintoruudussa **Vastaanota**.
2. Valitse **Tuotteen vastaanotto**.
3. Syötä **Tuotteen vastaanotto** -kenttään tuotteen vastaanottonumero. Syötä arvoksi esimerkiksi PR123.
4. Kirjaa tuotteen vastaanotto valitsemalla **OK**.
5. Sulje sivu.

## <a name="create-a-vendor-invoice"></a>Luo toimittajan lasku
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Vastaanotetut ostotilaukset, joita ei ole laskutettu**.
2. Valitse luomasi ostotilaus.
3. Valitse toimintoruudussa **Lasku**.
4. Valitse **Lasku**.
5. Syötä **Numero**-kenttään laskunumero.
6. Kirjoita arvo **Laskun kuvaus** -kenttään.
7. Syötä **Laskun päivämäärä** -kenttään päivämäärä.
8. Syötä **Yksikköhinta**-kentän arvoksi 1 200.
9. Valitse **Lisää rivi**.
10. Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.
11. Etsi asennuskulun nimiketunnus luettelosta. Syötä arvoksi esimerkiksi S0001
12. Valitse asennuskulun nimiketunnus. Huomaa, että täsmäytystä ei ole suoritettu, koska teit muutoksia.  
13. Valitse **Päivitä täsmäytyksen tila**.
14. Valitse toimintoruudussa **Tarkista**.
15. Valitse **Täsmäytyksen tiedot**. Uuden palveluita sisältävää riviä ei tarvitse täsmäyttää, joten tilana pysyy Ei suoritettu.  
16. Valitse tuotteen vastaanotto vastaanottamasi varastonimikkeelle. Tuotteen vastaanoton sisältävä rivi täsmäytettiin, mutta se sisälsi määrän tai hinnan ristiriidan, joten täsmäytys epäonnistui.  
17. Syötä **Yksikköhinta**-kenttään numero. Nyt, kun yksikköhinta täsmää, tilaksi päivitetään Hyväksytty. Jos käytäntö sallii ristiriidat tai jos täsmäytys on vain varoitus, voit kirjata laskun.  
18. Sulje sivu.
19. Valitse **Kirjaa**.
20. Sulje lomake. Huomaa, että ostotilaus on vastaanotettujen luettelon sijaan laskuttamattomien luettelossa.  

