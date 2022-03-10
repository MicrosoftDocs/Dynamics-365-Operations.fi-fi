---
title: Asiakkaan omistamien resurssien ylläpidon laskuttaminen
description: Tässä aiheessa käsitellään asiakkaiden omistamien resurssien ylläpitotyön luontia, käsittelyä ja laskuttamista.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a48e681da1801ef3c0d1c9c03cebaa5eecd37d76349a7b1c3cfe53e892fae489
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774942"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Asiakkaan omistamien resurssien ylläpidon laskuttaminen

[!include [banner](../../includes/banner.md)]

*Työtilauksen laskutus* -toiminnolla voi luoda, käsitellä ja laskuttaa asiakkaan omistamia resursseja koskevan ylläpitotyön. Toiminnolla voi suorittaa seuraavia tehtäviä:

- Asiakkaiden yhdistäminen asiakkaan omistamiin resursseihin.
- Asiakkaan valitseminen ja asiakkaan omistamien resurssien tarkasteleminen työtilausta luotaessa.
- Pääprojektin määrittäminen kullekin asiakkaalle.
- Työtilaukseen perustuvien tuntien, nimikkeiden, kulujen ja maksujen kirjaaminen sekä laskuehdotuksen luominen asiakkaalle myöhemmin.

Toiminnossa on lisäksi seuraavat toiminnot:

- Projektisopimus kopioidaan automaattisesti asiakkaan pääprojektista asianmukaiseen työtilauksenprojektiin.
- Resurssien hallinta voi nyt käyttää *lisämaksu*-projektitapahtumatyyppiä sekä työtilauksen ennusteissa että työtilauksen kirjauskansioissa.

## <a name="turn-on-the-customer-billing-feature"></a>Asiakkaan laskutustoiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Projektinhallinta ja kirjanpito*
- **Toiminnon nimi:** *Työtilauksen laskutus*

## <a name="example-scenario"></a>Esimerkkiskenaario

Seuraavan esimerkkiskenaarion toteuttaminen auttaa hahmottamaan toiminnon käyttöä.

Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Lisäksi **USMF**-yritys on valittava ennen aloittamista.

Voit hyödyntää tätä skenaariota myös ohjeena, kun työskentelet tuotantojärjestelmän parissa ja käytät toimintoa. Tässä tapauksessa sinun on kuitenkin korvattava omat arvosi, ja sinulta saattaa puuttua joitakin pakollisia tietoja, joita vakiodemotiedot sisältävät.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>Vaihe 1: Uuden projektisopimuksen luominen asiakkaalle

1. Valitse **Projektinhallinta ja kirjanpito \> Projektit \> Projektisopimukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä **Uusi projektisopimus** -valintaikkunassa seuraavat arvot:

    - **Nimi:** *Pelican Wholesales*
    - **Rahoitustyyppi:** *Asiakas*
    - **Rahoituslähde:** *US-013* (*Pelican Wholesales*)

1. Valitse **OK**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>Vaihe 2: Uuden pääprojektin luominen asiakkaalle

Tässä luotavaa pääprojektia käytetään, kun asiakkaalle luodaan työtilauksia.

1. Valitse **Projektinhallinta ja kirjanpito \> Projektit \> Kaikki projektit**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä **Uusi projekti** -valintaikkunassa seuraavat arvot:

    - **Projektityyppi:** *Aika ja materiaali*
    - **Projektiin nimi:** *Pelican Wholesalesin työtilaukset*
    - **Projektiryhmä:** *TM*
    - **Projektisopimuksen tunnus:** *Pelican Wholesales* (aiemmin luotu sopimus)
    - **Alkamispäivä:** valitse kuluva päivä.

1. Valitse **Luo projekti**.
1. Uusi projekti avataan. Kirjoita **Projektitunnus**-arvo muistiin. Se on annettava myöhemmin.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>Vaihe 3: Uuden työtilaustyypin luominen resurssien hallinnassa

1. Valitse **Resurssien hallinta \> Asetukset \> Työtilaus \> Työtilaustyypit**.
1. Valitse toimintoruudussa **Uusi**.
1. Uusi tietue lisätään luetteloon. Määritä sille seuraavat arvot:

    - **Työtilaustyyppi:** *Palvelu*
    - **Nimi:** *Palvelun työtilaukset*
    - **Työtilauksen elinkaaren tila:** *Vakio*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>Vaihe 4: Asiakastilin linkittäminen pääprojektiin

Asiakastili on nyt linkitettävä pääprojektiin resurssien hallinnan projektiasetuksissa.

1. Valitse **Resurssien hallinta \> Asetukset \> Työtilaukset \> Projektiasetukset**.
1. Lisää rivi valitsemalla **Pääprojekti**-välilehdessä **Lisää**.
1. Määritä uudelle riville seuraavat arvot:

    - **Asiakastili:** *US-013* (*Pelican Wholesales*)
    - **Projektitunnus:** anna aiemmin muistiin kirjoitettu projektitunnus.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>Vaihe 5: Projektiryhmän ja tyypin linkittäminen työtilausprojektiin

**Projektin määritys** -sivun (**Resurssien hallinta \> Asetukset \> Työtilaukset \> Projektin määritys**) pitäisi olla edelleen avoinna.

1. Lisää rivi valitsemalla **Projektiryhmä**-välilehdessä **Lisää**.
1. Määritä uudelle riville seuraavat arvot:

    - **Työtilaustyyppi:** *Palvelu* (aiemmin luotu työtilaustyyppi)
    - **Projektiryhmä:** *TM*

> [!NOTE]
> Työtilausprojektin projektisopimus periytyy aina pääprojektista.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>Vaihe 6: Resurssin linkittäminen asiakastunnukseen

1. Valitse **Resurssien hallinta \> Resurssit \> Aktiiviset resurssit**.
1. Anna **Suodatus**-kentässä *VE-102* ja valitse suodatusperusteeksi **Resurssi**.
1. Avaa resurssin asetukset valitsemalla se.
1. Määritä **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-013* (*Pelican Wholesales*).

    *Pelican Wholesales* päivittyy automaattisesti **Nimi**-kentän arvoksi.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>Vaihe 7: Uuden työtilaustyypin luominen resurssille

1. Valitse **Resurssien hallinta \> Työtilaukset \> Aktiiviset työtilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä **Luo työtilaus** -valintaikkunassa seuraavat arvot:

    - **Työtilaustyyppi:** *Palvelu*
    - **Kuvaus:** *Kuorma-auton korjaus*
    - **Asiakastili:** *US-013* (*Pelican Wholesales*)
    - **Resurssi:** *VE-102*

        > [!NOTE]
        > Haku näyttää vain valittuun asiakastiliin linkitetyt resurssit.

    - **Ylläpitotyön tyyppi:** *Korjaus*
    - **Ammatti:** *Mekaanikko*
    - **Palvelutaso:** *4*

1. Valitse **OK**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>Vaihe 8: Työtilauksen tarkistaminen ja sen käytön aloittaminen

Tässä osassa käytetään edellisessä osassa luotua työtilausta.

1. Seuraavien ohjeiden avulla tarkistetaan, että pääprojekti on *Pelican wholesalesin työtilaus* -projekti:

    1. Valitse rivi **Työtilauksen ylläpitotyöt** -kohdassa.
    1. Tarkista **Rivin tiedot** -pikavälilehdessä **Projektitunnus**-arvo. Sen pitäisi olla seuraavanlainen tavuviivalla yhdistetty luku: *\<Parent-Project-ID\>-\<Project-ID\>*. Tämä arvo on linkki.
    1. Valitse projektitunnuksen linkki. Se avaa sivun, jossa on näkyvissä pääprojektin ja projektin nimet.

1. Valitse toimintoruudun **Työtilaus**-välilehden **Elinkaaren tila** -ryhmässä **Päivitä työtilauksen tila**.
1. Valitse **Päivitä työtilauksen tila** -valintaikkunan **Valitse**-sarakkeessa sen rivin valintaruutu, jonka **Elinkaaren tila** -kentän asetuksena on *Käsittelyssä*.
1. Valitse **OK**.
1. Valitse **Elinkaaren tila: Käynnissä** -valintaikkunassa **OK**.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>Vaihe 9: Työtilaukseen kuluneiden tuntien kirjaaminen ja uuden laskuehdotuksen luominen

Tässä osassa jatketaan edellisessä osassa luodun työtilauksen käyttämistä.

1. Valitse toimintoruudun **Työtilaus**-välilehden **Projekti**-ryhmässä **Kirjauskansiot**.

    **Työtilauksen kirjauskansiot** -sivu avautuu. Tällä sivulla voi kirjata työtilaukseen kuluneen ajan.

1. Valitse **Tunnit**-pikavälilehdessä **Lisää rivi**.
1. Määritä uuden rivin **Tunnin**-kentän arvoksi *4*.
1. Valitse toimintoruudussa **Kirjaa kirjauskansiot**.
1. Palaa työtilaukseen sulkemalla **Työtilauksen kirjauskansiot** -sivu.
1. Valitse toimintoruudun **Laskutus**-välilehdessä **Uusi laskuehdotus**.
1. Valitse **Luo laskuehdotus** -valintaikkunan **Projektitapahtumat**-osassa jokaisen laskutettavan rivin kohdalla **Valitse**-valintaruutu.
1. Sulje valintaikkuna ja tarkastele uutta laskuehdotusta valitsemalla **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]