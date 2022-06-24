---
title: Konsernin sisäisen myyntitilauksen luominen ja laskuttaminen ulkoiselle asiakkaalle
description: Tässä artikkelissa käsitellään ulkoisen asiakkaan konsernin sisäisen myyntitilauksen luomista ja laskuttamista
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: cd42551730ab0123813a3b5a0b5a4b1c334e9d30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852154"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Konsernin sisäisen myyntitilauksen luominen ja laskuttaminen ulkoiselle asiakkaalle

[!include [banner](../../includes/banner.md)]

Konsernin sisäisen kaupan avulla voi kirjata tuotteen myynnin yrityksessä toiselle samassa organisaatiossa sijaitsevalle yritykselle.

Alkuperäistä myyntitilausta luotaessa konsernitoimittajalle voidaan luoda automaattisesti konsernin sisäinen ostotilaus. Näin luodaan automaattisesti konsernin sisäinen myyntitilaus konsernitoimittajan yrityksessä.

Seuraava kuva näyttää tapahtumien kulun, kun myyntitilaus luodaan ulkoiselle asiakkaalle mutta tilattu tuote on tilattava toiselta organisaation yritykseltä ennen tuotteen toimitusta asiakkaalle. Tässä tapauksessa konsernin sisäinen ostotilaus luodaan toimittajatilille, joka ilmaisee toisen yrityksen. Vastaavasti konsernin sisäinen myyntitilaus luodaan toisessa yrityksessä asiakastilille, joka ilmaisee oman yrityksen. Kun konsernin sisäinen ostotilaus laskutetaan, alkuperäisen myyntitilauksen lasku kirjataan automaattisesti, jos kyseessä on suoratoimitus.

![Konsernin sisäinen ulkoinen myyntiprosessi](media/intercompanyexternalsalesprocess.png)

Jos käytössä on suoratoimitus ja **Laskun kirjaus** -sivun **Määrä**-kentässä valitaan **Pakkausluettelo**, konsernin sisäinen toimittajan lasku perustuu aiemmin kirjattuun konsernin sisäiseen tuotteen vastaanottoon.

## <a name="prerequisites"></a>Edellytykset

Ennen aloittamista on varmistettava, että seuraavat konsernin sisäisten laskujen automaattisen kirjauksen ja tulostamisen edellytykset täyttyvät.

1. Valitse **Myynti ja markkinointi \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse toimintoruudun **Yleiset**-välilehdessä **Konsernin sisäinen**.
1. Valitse **Hankinta \> Toimittajat \> Kaikki toimittajat**.
1. Valitse toimintoruudun **Yleiset**-välilehdessä **Konsernin sisäinen**.
1. Valitse joko toimittajan tai asiakkaan **Konsernin sisäinen** -sivun **Ostotilauskäytännöt**-alueen **Konsernin sisäinen ostotilaus (suoratoimitus)** -kenttäryhmässä **Kirjaa lasku automaattisesti** -valintaruutu.
1. Valitse **Ostotilauskäytännöt**-alueen **Alkuperäinen myyntitilaus (suoratoimitus)** -kenttäryhmässä **Kirjaa lasku automaattisesti** -valintaruutu. Valitse tämä valintaruutu, jos haluat, että alkuperäisen myyntitilauksen lasku tulostetaan automaattisesti, kun konsernin sisäinen toimittajan lasku kirjataan.

> [!NOTE]
> Laskun tulostusasetukset määräytyvät **Tulostuksenhallinta-asetukset** -sivulla tehtyjen moduuli-, asiakirja- tai tapahtumamäärityksen perusteella.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Alkuperäisen myyntitilauksen luominen ulkoiselle asiakkaalle

Suorita nämä vaiheet yrityksessä A. Tämä toimenpide vastaa kuvan kenttää 1.

1. Valitse **Myyntireskontra \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo alkuperäinen myyntitilaus **Kaikki myyntitilaukset** -luettelosivulla. Kentän arvot kopioidaan asiakastililtä myyntitilaukseen.
1. Valitse toimintoruudun **Myyntitilaus**-sivulla **Otsikkonäkymä**.
1. Valitse **Konsernin sisäiset asetukset** -pikavälilehdessä **Luo konsernin sisäiset tilaukset automaattisesti** -valintaruutu.
1. Jos konsernitoimittajan halutaan toimittavan nimikkeen suoraan ulkoiselle asiakkaalle, valitse **Suoratoimitus**-valintaruutu.
1. Kun myyntitilaus on annettu, sulje **Myyntitilaus**-sivu.

Konsernin sisäinen ostotilaus luodaan automaattisesti kaikille nimikkeille, joihin on määritetty konsernitoimittaja, ja tämän jälkeen luodaan konsernin sisäinen myyntitilaus. Tietosanoma ilmaisee, että konsernin sisäinen ostotilaus ja myyntitilaus on luotu. Viesti sisältää myös linkit näihin tilauksiin. Jos nimikettä ei löydy, näkyviin tulee punainen varoitus, joka ilmaisee, että tilauksen luontiprosessia ei suoritettu loppuun.

> [!NOTE]
> Jos useita tilauksia luodaan eri yrityksissä ja jos nimikkeitä ei löydy yhdessä yrityksessä, tilauksen luontiprosessi keskeytyy myös niissä yrityksissä, joissa tilaukset voitaisiin täyttää.

## <a name="invoice-an-intercompany-sales-order"></a>Konsernin sisäinen myyntitilauksen laskuttaminen

Kun konsernin sisäinen myyntitilaus laskutetaan, vastaava konsernin sisäinen ostotilaus laskutetaan automaattisesti. Jos alkuperäinen myyntitilaus on suoratoimitustilaus, myös alkuperäinen myyntitilaus laskutetaan automaattisesti.

Suorita nämä vaiheet yrityksessä B. Tämä toimenpide vastaa kuvan kenttää 2.

1. Valitse **Myyntireskontra \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse konsernin sisäinen myyntitilaus **Kaikki myyntitilaukset** -luettelosivulla.
1. Valitse toimintoruudussa **Lasku**-välilehti ja valitse sitten **Lasku**.
1. Valitse **Kirjaus**-valintaruutu.
1. Valitse ensin myyntitilaus ja sitten **OK**.

Konsernin sisäisen myyntitilauksen asiakkaan lasku kirjataan automaattisesti yrityksessä B. Tämän jälkeen yrityksessä A luodaan ja kirjataan konsernin sisäinen ostolasku. Jos alkuperäinen myyntitilaus määritetään suoratoimitukseksi, myyntilasku luodaan alkuperäiselle myyntitilaukselle yrityksessä A.

> [!NOTE]
> Aiemmin konsernin sisäisen myynnin skenaariossa, jos toimittajan laskun työnkulku konfiguroitiin konsernin sisäisessä ostoyhtiössä, konsernin sisäisen myyntitilauksen laskutus ei onnistunut. Siksi toimittajan laskutyönkulku piti ottaa pois käytöstä konsernin sisäisessä ostoyrityksessä. 
> 
> Tämä rajoitus on korjattu viimeisimmässä versiossa 10.0.25. Konsernin sisäiset myyntitilaukset voidaan nyt laskuttaa, kun toimittajan laskun työnkulku on konfiguroitu konsernin sisäisessä ostoyhtiössä.
> 
> Ominaisuus otetaan käyttöön seuraavasti.
>
> 1. Valitse konsernin sisäisen myynnin yritys.  
> 2. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
> 3. Valitse konsernin sisäisen ostoyrityksen asiakas.
> 4. Siirry kohtaan **Yleiset \> Määritys \> Konsernin sisäinen**.
> 5. Valitse **Ostotilauskäytännöt**-välilehdestä **Ohita toimittajan laskun työnkulku konsernin sisäisissä ostolaskuissa** -parametri.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
