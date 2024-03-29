---
title: Varastohallintaprosessit käyttöönottaneiden nimikkeiden rekisteröinti nimikkeen saapumisen kirjauskansion avulla
description: Tässä artikkelissa käsitellään tilannetta, jossa nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallintaprosessit (WMS).
author: Mirzaab
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66fc9e21b79d70ec14750440c74d354bb8ec0695
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219595"
---
# <a name="register-items-enabled-for-warehouse-management-processes-using-an-item-arrival-journal"></a>Varastohallintaprosessit käyttöönottaneiden nimikkeiden rekisteröinti nimikkeen saapumisen kirjauskansion avulla

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa käsitellään tilannetta, jossa nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallintaprosessit (WMS). Vastaanottoassistentti tekee yleensä tämän tehtävän.

## <a name="enable-sample-data"></a>Mallitietojen ottaminen käyttöön

Jos haluat suorittaa tämän skenaarion käyttämällä tässä artikkelissa määritettyjä esimerkkitietueita ja -arvoja, sinun täytyy käyttää järjestelmää, johon vakiomuotoiset [demotiedot](../../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu, sekä valita *USMF*-yritys ennen aloittamista.

Voit myös käyttää tätä skenaariota korvaamalla arvot omista tiedoista, jos käytettävissäsi ovat seuraavat tiedot:

- Olet vahvistanut ostotilauksen, jossa on avoin ostotilausrivi.
- Rivin nimike on varastoitava. Se ei saa käyttää tuotevariantteja eikä sillä saa olla seurantadimensioita.
- Nimike on liitettävä varastodimensioryhmään, jossa varastonhallintaprosessi on otettu käyttöön.
- WMS on oltava otettuna käyttöön käytettävässä varastossa ja vastaanottoa on ohjattava käytettävässä toimipaikassa rekisterikilvillä.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Varastonhallintaa käyttävän nimikkeen saapumisen kirjauskansion otsikon luominen

Seuraavassa skenaariossa näytetään, miten varastonhallintaa käyttävä nimikkeen saapumisen kirjauskansion otsikko luodaan:

1. Varmista, että järjestelmässä on vahvistettu ostotilaus, joka täyttää edellisessä osassa kuvatut vaatimukset. Tässä skenaariossa käytetään ostotilausta yritykselle *USMF* toimittajatilille *1001*, varastolle *51* ja tilausriviä, jossa on *10 PL* (10 kuormalavaa) nimikenumeroa *M9200*.
1. Kirjoita käytettävä ostotilauksen numero muistiin.
1. Valitse **Inventoinnin- ja varastonhallinta \> Kirjauskansioviennit \> Nimikkeen saapuminen \> Nimikkeen saapuminen**.
1. Valitse toimintoruudussa **Uusi**.
1. Näyttöön avautuu **Luo varastonhallinnan kirjauskansio** -valintaikkuna. Valitse **Nimi**-kentästä kirjauskansion nimi.
    - Jos käytät *USMF*-yrityksen demotietoja, valitse *WHS*.
    - Jos käytät omia tietojasi, valitussa kirjauskansiossa **Tarkista keräilysijainti** -asetuksen on oltava *Ei* ja **Karanteeninhallinta**-arvoksi on määritettävä *Ei*.
1. Määritä **Viite**-arvoksi *Ostotilaus*.
1. Määritä **Tilinumero**-arvoksi *1001*.
1. Määritä **Numero** tätä harjoitusta varten tunnistamasi ostotilauksen numeroon.

    ![Nimikkeen saapumisen kirjauskansio.](../media/item-arrival-journal-header.png "Nimikkeen saapumisen kirjauskansio")

1. Luo kirjauskansion otsikko valitsemalla **OK**.
1. Valitse **Kirjauskansion rivit**  -osasta **Lisää rivi** ja kirjoita seuraavat tiedot:
    - **Nimikenumero** – määritä arvoksi *M9200*. **Toimipaikka**, **Varasto** ja **Määrä** asetetaan 10 kuormalavan (1 000 kpl) varastotapahtumatietojen perusteella.
    - **Sijainti** – Määritä arvoksi *001*. Tämä tietty sijainti ei seuraa rekisterikilpiä.

    ![Nimikkeen saapumisen kirjauskansion rivi.](../media/item-arrival-journal-line.png "Nimikkeen saapumisen kirjauskansion rivi")

    > [!NOTE]
    > **Päivämäärä**-kenttä määrittää päivämäärän, jolloin tämän nimikkeen käytettävissä oleva määrä rekisteröidään varastoon.  
    >
    > Järjestelmä lisää **erätunnuksen** tiedot, jos erä voidaan yksilöivästi tunnistaa annetuista tiedoista. Muussa tapauksessa tiedot on lisättävä manuaalisesti. Tämä on pakollinen kenttä, joka linkittää tämän rekisteröinnin tietylle lähdeasiakirjariville.  

1. Valitse toimintoruudussa **Vahvista**. Tämä tarkistaa, että kirjauskansio on valmis kirjattavaksi. Jos vahvistus epäonnistuu, virheet on korjattava ennen kirjausta kirjauskansioon.  
1. Näyttöön avautuu **Tarkista kirjauskansio** -valintaikkuna. Valitse **OK**.
1. Tarkista sanomapalkki. Sanoman pitäisi ilmoittaa, että toiminto on valmis.  
1. Valitse toimintoruudussa **Kirjaa**.
1. Näyttöön avautuu **Kirjaa kirjauskansio** -valintaikkuna. Valitse **OK**.
1. Tarkista sanomapalkki. Sanomien pitäisi ilmoittaa, että toiminto onnistui.
1. Päivitä ostotilausrivi ja kirjaa tuotteen vastaanotto valitsemalla toimintoruudusta **Toiminnot > Tuotteen vastaanotto**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
