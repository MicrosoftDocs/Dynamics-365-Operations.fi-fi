---
title: Varaston arvon varastoraportti
description: Tässä ohjeaiheessa kerrotaan, miten varaston arvon tallennusraportti suoritetaan ja miten tulos määritetään käytettäväksi digitaalisesti interaktiivisena sivuna Microsoft Dynamics 365 Supply Chain Management -sovelluksessa tai vietynä asiakirjana jossakin useista muodoista.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f50318e0a955d8244ba854aa1fd73ad7532b9198
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427047"
---
# <a name="inventory-value-storage-report"></a>Varaston arvon varastoraportti

Tässä ohjeaiheessa kerrotaan, miten **varaston arvon tallennusraportti** suoritetaan ja miten tulos määritetään käytettäväksi digitaalisesti interaktiivisena sivuna Microsoft Dynamics 365 Supply Chain Management -sovelluksessa tai vietynä asiakirjana jossakin useista muodoista.

Kun tarkastelet raporttia selaimessa, sarakkeita ja yhdistettyjä saldoja muutetaan dynaamisesti määrittämästäsi asettelusta riippuen. Voit esimerkiksi lajitella tulokset, suodattaa ne ja porautua tietoihin.

Raportin tulokset tallennetaan **Varastoarvon** tietoyksikköön. Näin voit suodattaa ja viedä tulokset muotoon, joka voi olla esimerkiksi pilkuilla eroteltu CSV tai Microsoft Excel -muoto.

**Varastoarvon varastointi** -raportti on hyödyllinen, kun tuloste sisältää useita rivejä. Sinulla on esimerkiksi 50 000 nimikettä, ja 300 myymälää on luotu varastoina. Tässä tapauksessa, jos pyydät varaston loppusaldoja nimikkeen, toimipaikan ja varaston mukaan, tuotos sisältää useita rivejä.

> [!NOTE]
> Raportti ei sisällä raporttiasettelussa määritettyjä välisummia. Se ei myöskään sisällä kirjanpidon saldoja, vaikka ne olisi määritetty raportin asettelussa. Täsmäytys kirjanpitoon on tehtävä käyttämällä pääkirjasaldoja.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Varastoarvon tallennusominaisuuden ottaminen käyttöön

Ennen kuin **Varastoarvon varastointi** -raportti voidaan luoda, toiminto on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli** – Kustannustenhallinta
- **Toiminnon nimi** – Varaston arvon tallennus

## <a name="generate-an-inventory-value-storage-report"></a>Luo varaston arvon tallennusraportti

Seuraavien vaiheiden avulla voit luoda ja tallentaa **Varaston arvon tallennus** -raportin.

1. Valitse **Kustannushintojen hallinta \> Kyselyt ja raportit \> Varaston arvoraportin tallennus**.
1. Valitse **Uusi**.
1. Määritä näyttöön tulevassa **Varaston arvo** -valintaikkunassa seuraavat arvot, jotka määrittävät raporttiin sisällytettävät tiedot:

    - Kirjoita **Parametrit**-pikavälilehdessä raportille yksilöivä nimi ja määritä **Päivämääräväli**-osan kenttien avulla, mitkä tiedot sisällytetään raporttiin. Voit määrittää päivämäärävälin joko valitsemalla esimääritetyn alueen (suhteessa raportin luontipäivämäärään) **Päivämäärävälin koodi** -kentässä tai valitsemalla tietyt päivämäärät **Alkamispäivä**- ja **Päättymispäivä**-kentistä.
    - Määritä **Sisällytettävät tietueet** -pikavälilehdessä suodattimet ja rajoitteet, joiden avulla määritetään raporttiin sisällytettävät tiedot.
    - Määritä **Suorita taustalla** -pikavälilehdessä, miten, milloin ja kuinka usein raportti luodaan.

    > [!NOTE]
    > Tämä raportti suoritetaan aina osana erätyötä.

1. Ota asetukset käyttöön valitsemalla **OK** ja sulje valintaikkuna.

Kun erätyö on valmis, raportti näkyy **Varaston arvon raportin tallennus** -sivulla. Sivu on ehkä päivitettävä, ennen kuin päivitetty raportti tulee näkyviin.

## <a name="explore-an-inventory-value-storage-report"></a>Tutki varaston arvon tallennusraportti

Kun olet luonut raportin, voit tarkastella sitä ja tutustua sen tietoihin milloin tahansa seuraavien ohjeiden mukaisesti.

1. Valitse **Kustannushintojen hallinta \> Kyselyt ja raportit \> Varaston arvoraportin tallennus**.
1. Valitse raportti luettelosta.
1. Valitse **Näytä tiedot**, jos haluat näyttää raportin sisällön.
1. Tutki raporttia noudattamalla seuraavia vaiheita:

    - Kuten useimmilla standardisivuilla Supply Chain Management -sovelluksessa voit valita melkein minkä tahansa sarakkeen otsikon lajitellaksesi tai suodattaaksesi ruudukon kyseisen sarakkeen arvojen perusteella.
    - **Suodatin**-kentän avulla voit suodattaa raportin minkä tahansa useiden käytettävissä olevan sarakkeen arvon mukaan.
    - Käytä näytä-valikkoa ( **Suodatin**-kentän yläpuolella) lajittelu- ja suodatusvaihtoehtojen suosikkiyhdistelmien tallentamiseen ja lataamiseen.

## <a name="export-an-inventory-value-storage-report"></a>Vie varaston arvon tallennusraportti

Jokainen luotu raportti tallennetaan **Varastoarvo**-tietoentiteettiin. Voit käyttää Supply Chain Management -sovelluksen vakiotiedonhallintatoimintoja, jos haluat viedä tämän entiteetin tiedot mihin tahansa tuettuun tietomuotoon, kuten CSV- tai Excel-muotoon.

Seuraavassa esimerkissä näytetään, miten **Varastoarvon raportti** -raportti viedään.

1. Valitse **Järjestelmänhallinta \> Työtilat \> Tietojen hallinta**.
1. Valitse **Vienti/Tuonti**-osassa **Vienti**-ruutu. 
1. Näkyviin tulevalla **Vie**-sivulla voit määrittää vientityön. Syötä ensin työlle ryhmänimi.
1. Valitse **Valitut yksiköt** -osassa **Lisää yksikkö**.
1. Näyttöön tulevassa valintaikkunassa kuvaillaan seuraavat kentät:

    - **Yksikön nimi** – Valitse **Varastoarvo**.
    - **Kohteen tietomuoto** – Valitse muoto, johon tiedot viedään.

1. Valitse **Lisää**, jos haluat lisätä uuden rivin. Valitse sitten **Sulje**, jolloin valintaikkuna suljetaan.
1. Tavallisesti viedään yksi raportti kerralla. Jos haluat viedä yksittäisen raportin, määritä suodattimen avulla **Kysely**-valintaikkunaan juuri lisäämäsi rivi. Näin voit määrittää, mikä **Varastoarvo**-kohteen raportti sisältyy vientiin. Määritä seuraavat suodatusasetukset seuraavien vaiheiden mukaisesti viedäksesi yhden raportin:

    1. Valitse **Väli**-välilehdessä **Lisää**, jos haluat lisätä rivin.
    2. Aseta **Taulu**-kentän arvoksi **Varastoarvo**.
    3. Aseta **Johdettu taulu** -kentän arvoksi **Varastoarvo**.
    4. Määritä **Kenttä**-kenttä sille kentälle, jonka mukaan haluat suodattaa. Yleensä käytetään **Suorituksen nimi** -kenttää ja/tai **Suoritusaika**-kenttää.
    5. Määritä **Ehto**-kentästä arvo, jonka haluat etsiä valitusta kentästä. (Jos valitsit **Suorituksen nimi** -kentän edellisessä vaiheessa, tämä arvo on raportin nimi. Jos valitsit **Suoritusaika**-kentän, se on aika, jolloin raportti luotiin.)
    6. Lisää tarvittaessa rivejä **Väli**-välilehteen, kunnes olet yksilöinyt etsittävän raportin.

1. Valitse **OK** tallentaaksesi asetukset ja sulje valintaikkuna.
1. Tallenna vientiasetukset valitsemalla **Tallenna**.
1. Valitse **Vientiasetukset**-välilehdellä **Vie nyt** luodaksesi vientitiedoston.
1. Näkyviin tulevalla **Suorituksen yhteenveto** -sivulla näkyy vientityön tila ja vietyjen entiteettien luettelo. Valitse **Entiteetin käsittelyn tila** -osassa listasta **Varaston arvo** -yksikkö. Lataa tästä yksiköstä viedyt tiedot valitsemalla **Lataa tiedosto**.

Lisätietoja tietojen hallinnan käyttämisestä tietojen viemisessä on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]