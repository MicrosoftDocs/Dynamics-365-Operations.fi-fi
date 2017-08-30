---
title: "Materiaaliottosäännöt"
description: "Tässä ohjeaiheessa käsitellään neljää materiaalinottosääntöä, joita käytetään raaka-aineiden kulutuksessa."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 9eb39893bbb7fdcb11d6c1d0b73dc0278ff1f814
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

# <a name="controlling-raw-material-consumption-by-using-flushing-principles"></a>Raaka-aineiden kulutuksen hallinta materiaaliottosääntöjen avulla

[!include[banner](../includes/banner.md)]

Materiaalinottosäännöt vastaavat erilaisia tuotantoprosesseissa käytettäviä raaka-aineiden kulutusstrategioita. Kulutus on prosessi, jossa materiaali vähennetään käytettävissä olevasta varastosta ja joka määrittää kulutettujen materiaalien arvon tuotantotilausten ja erätilausten **keskeneräiselle työlle** (KET). Raaka-aineet kulutetaan yleensä sijainnista, joka on määritetty materiaalia kuluttavalle prosessille. Tätä sijaintia kutsutaan tuotannon varastosijainniksi.

Materiaalit siirretään varastosijaintiin ennen materiaalikulutusta. Prosessi on esitetty seuraavassa kuvassa.

[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)

1. Materiaalivarasto
2. Raaka-aineiden keräily
3. Tuotannon varastointisijainti
4. Raaka-aineen kulutus
5. Tuotantoprosessi

Materiaalikulutusta hallitaan neljän materiaaliottosääntöjen avulla:

- Manuaalinen
- Alku
- Valmis
- Käytettävissä sijainnissa

Materiaalinottosäännöt määritetään hierarkian oletusarvoissa. Hierarkia alkaa vapautetusta tuotteesta, jossa materiaaliottosäännön arvona on **Alku**. Tuotteen materiaaliottosääntö voidaan ohittaa tuoterakenne- tai kaavarivillä. Tuotannon tuoterakennerivien tai erätilauksen kaavarivien oletusmateriaalinottosääntö haetaan tuotteesta tai tuoterakenteen tai kaavojen ohitetusta arvosta.

## <a name="description-of-the-flushing-principles"></a>Materiaalinottosääntöjen kuvaus

### <a name="manual"></a>Manuaalinen
Manuaalinen materiaalinottosääntö ilmaisee, että materiaalikulutuksen rekisteröinti on manuaalinen toiminto. Tällä säännöllä on merkitystä, jos haluat esimerkiksi seurata aikaa, ja kulutettujen eränumeroiden tai sarjanumeroiden määrästä on oltava selvillä seurantaa varten. Manuaalinen kulutus rekisteröidään tuotannon keräysluettelon kirjauskansioon. Jos edistykselliset varastoprosessit on otettu käyttöön nimikkeissä, voidaan käyttää käsikäyttöistä työnkulkua.

### <a name="start"></a>Alku
Alku-materiaaliottosääntö ilmaisee, että materiaali kulutetaan automaattisesti, kun tuotantotilaus käynnistetään. Kulutetun materiaalin määrä on suhteessa käynnistettyyn määrään. Kun Alku-materiaaliottosääntöä käytetään yhdessä tuotannonohjausjärjestelmän kanssa, sitä voidaan käyttää materiaaliottoihin, kun toiminto tai prosessityö on aloitettu. Säännöllä on merkitystä, jos esimerkiksi kulutuksen varianssi on pieni, materiaalit ovat arvoiltaan vähäisiä, seurantaa ei tarvita tai toimenpiteen suoritusaika on lyhyt. 

### <a name="finish"></a>Valmis
Loppu-materiaaliottosääntö ilmaisee, että materiaali kulutetaan automaattisesti, kun tuotantotilaus on ilmoitettu valmiiksi tai kun materiaalia kuluttavaksi määritetty toiminto on rekisteröity valmiiksi. Kulutetun materiaalin määrä on suhteessa valmiiksi ilmoitettuun määrään. Kun Loppu-materiaaliottosääntöä käytetään yhdessä tuotannonohjausjärjestelmän kanssa, sitä voidaan käyttää materiaaliottoihin, kun toiminto tai prosessityö on valmis. Tällä säännöllä on merkitystä samoissa tilanteissa kuin Alku-säännöllä. Loppu-sääntö on kuitenkin tarkoitettu toiminnoille, joiden ajoaika pidempi ja joissa materiaaleja ei määritetä keskeneräisiksi töiksi ennen toiminnon valmistumista. 

### <a name="available-at-location"></a>Käytettävissä sijainnissa
Käytettävissä sijainnissa -materiaaliottosääntö ilmaisee, että materiaali kulutetaan automaattisesti, kun se on rekisteröity tuotantoon kerätyksi. Materiaali on rekisteröity sijainnista kerätyksi, kun raaka-aineen keräilytyö on valmis tai kun materiaali on käytettävissä tuotannon varastosijainnissa ja materiaalirivi on vapautettu varastoon. Prosessin aikana luotu keräystyö kirjataan erätyöhön. Tällä säännöllä on merkitystä, jos sinulla on esimerkiksi tuotantotilaus, jossa on useita keräystoimintoja. Tässä tapauksessa keräyslistaa ei tarvitse päivittää manuaalisesti ja saat KET-saldon ajantasaisen näkymän.
