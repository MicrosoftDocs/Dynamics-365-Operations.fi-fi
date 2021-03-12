---
title: Varastotapahtumien tuotesuodattimien määrittäminen
description: Tässä aiheessa käsitellään tuotesuodattimien ja suodatinkoodien määrittämistä luokittelemaan varastonimikkeitä varastossa. Suodattimilla voidaan myös määrittää asiakkaat, jotka voivat tilata tietyn nimikkeen, ja määrittää nimikkeet, joita voidaan ostaa tietyltä toimittajalta.
author: Mirzaab
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 922ff818e069f41c139cc00db9161dc6e113888b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973732"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Varastotapahtumien tuotesuodattimien määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään tuotesuodattimien ja suodatinkoodien määrittämistä luokittelemaan varastonimikkeitä varastossa. Suodattimilla voidaan myös määrittää asiakkaat, jotka voivat tilata tietyn nimikkeen, ja määrittää nimikkeet, joita voidaan ostaa tietyltä toimittajalta.

Lisäksi voidaan määrittää ja käyttää tuotesuodattimia varastonimikkeiden automaattiseen järjestämiseen ja suodatettujen nimikkeiden yhdistämiseen suodatusryhmiksi. Suodattimien avulla nimikkeitä voidaan sijoittaa luokkiin käsittely-, osto- ja myyntiprosesseja varten. Nimikkeitä halutaan ehkä ryhmitellä tai erottaa toisistaan silloin, kun niiden käsittelytapa perustuu painoon tai käsittelyrajoituksiin. Lisäksi voidaan määrittää asiakkaat tai toimittajat, joille nimike voidaan myydä tai joilta se voidaan ostaa.

## <a name="prerequisites"></a>Edellytykset

Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.

| Edellytys | Ohjeet |
|---|---|
| Varastokäsittely on otettava käyttöön tuotteen varastodimensioryhmässä, ennen kuin tuotteiden määrittäminen **Vapautetun tuotteen tiedot** -sivulla voidaan aloittaa. | Valitse **Tuotetietojen hallinta \> Asetukset \> Dimensio- ja varianttiryhmät \> Varastodimensioryhmät**. Valitse tai luo sitten varastodimensioryhmä, jossa **Käytä varastonhallintaprosesseja** -asetukseksi on määritetty *Kyllä*. |
| Jos käytössä on asiakkaan suodattamia ja/tai toimittajan suodattimia, ne on otettava käyttöön varastonhallinnan parametreissa. | Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**. Määritä **Tuotesuodattimet**-välilehdessä **Ota asiakkaan suodattimet käyttöön**- ja/tai **Ota toimittajan suodattimet käyttöön** -asetukseksi *Kyllä*. |

## <a name="set-up-product-filters"></a>Tuotesuodattimien määrittäminen

Tuotesuodattimessa voi olla enintään 10 **Suodattimen otsikko** -ominaisuutta, jotka ovat luetteloinnin (valintalistan) arvoja. Valintalistan arvot ovat valittavissa, kun tuotesuodatin luodaan. Valintalistan arvot *Koodi 1*–*Koodi 10* ovat järjestelmän määrittämiä arvoja, ja ne ilmaisevat nimikkeen erikoisominaisuuden tai määritteen. *Koodi 1* voi esimerkiksi ilmaista nimikkeet, jotka on luokiteltu vaaralliseksi aineeksi. *Koodi 2* voisi taas ilmaista nimikkeitä, joita vain toimittajat voivat ostaa. Tuotesuodattimet määrittävät sitten tietyn **suodatinkoodin** arvon, joka liitetään **suodattimen otsikon** arvoon.

1. Valitse **Varastonhallinta \> Asetukset \> Tuotesuodattimet \> Tuotesuodattimet**.
1. Lisää tuotesuodatin ruudukkoon valitsemalla toimintoruudussa **Uusi**.
1. Valitse **Suodattimen otsikko** -kenttään arvo.
1. Anna **Suodatinkoodi**-kenttään arvo.

    ![Tuotesuodattimen määrittäminen](media/Product_Filters10.png "Tuotesuodattimen määrittäminen")

1. Anna koodi nimi **Kuvaus**-kentässä. Esimerkiksi *Koodi 2* voi viitata toimittajiin. Tämän jälkeen tietylle toimittajalle tai toimittajaryhmällä voidaan luoda tuotesuodatin. Lisätietoja on jäljempänä tämän aiheen kohdassa [Toimittajan suodatinkoodien määrittäminen](#vendor-product-filters).

    ![Tuotesuodattimien joukko](media/Product_Filters.png "Tuotesuodattimien joukko")

## <a name="set-up-product-filter-groups"></a>Tuotesuodatinryhmien määrittäminen

Suodatinkoodeja voi ryhmitellä suodatinryhmien avulla. Tämä ominaisuus on kätevä, kun ryhmää käytetään sijaintidirektiivissä tehtävässä kyselyssä, ja haku halutaan kohdistaa ryhmää eikä koodisarjoihin. Kukin suodatinryhmä liitetään nimikeryhmään.

> [!IMPORTANT]
> Kaikki tuotesuodatinryhmät eivät ole käytettävissä suodatinkoodeille, jotka on suurempia kuin *Koodi 4* (eli koodit *Koodi 5*–*Koodi 10*). Vaikka esimerkiksi vapautettuihin tuotteisiin voidaan lisätä kaikki tuotteen suodatinkoodit, suodatinkoodien ryhmittelyä ei päivitetä. Tämä toiminto saatetaan päivittää myöhemmissä julkaisuissa.

Suodatinryhmät määritetään seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Tuotesuodattimet \> Tuotesuodatinryhmät**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna **Ryhmä 1**- ja **Ryhmä 2** -kentissä nimet, joilla nimikkeitä luokitellaan.
1. Lisää rivi valitsemalla **Tiedot**-pikavälilehdessä **Uusi**.
1. Anna suodatinryhmät alkamis- ja päättymispäivät **Alkamispäivämäärä ja -aika**- ja **Päättymispäivämäärä ja -aika** -kentissä.
1. Valitse **Nimikeryhmä**-kentässä nimikeryhmä, jossa tuotesuodatinta käytetään.
1. Valitse ryhmässä käytettävät suodatinkoodit tarpeen mukaan kentissä **Koodi 1**–**Koodi 10**.

    ![Nimikeryhmä](media/ProdFilterGroup.png "Nimikeryhmä")

> [!NOTE]
> Jos virhesanoma avautuu, kun sivu suljetaan, koodimääritys saattaa puuttua. Nimikeryhmän koodeista voidaan tehdä pakollisia valitsemalla **Nimikeryhmät**-sivulla valintaruudut **Määritä nimikeryhmälle suodatinkoodi 1**, **Määritä nimikeryhmälle suodatinkoodi 2** ja niin edelleen.

## <a name="set-up-filter-codes-on-item-groups"></a>Nimikeryhmien suodatinkoodien määrittäminen

Nimikeryhmään määritettyjen suodatinkoodien avulla koodeista tulee pakollisia kyseiseen nimikeryhmään liitetyissä tuotteissa.

Suodatinkoodit määritetään nimikeryhmissä seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Nimikeryhmät**.
1. Luo nimikeryhmä valitse toimintoruudussa **Uusi**.
1. Anna **Nimikeryhmä**-kentässä nimi.
1. Anna kuvaus **nimi**-kenttään.
1. Valitse **Varasto**-pikavälilehden **Pakollinen suodatin** -osassa niiden suodatinkoodien valintaruudut, jotka on määritettävä nimikeryhmään liitetyille tuotteille.

    Päivitä vapautettu tuote avaamalla tuotteen **Vapautetun tuotteen tiedot** -sivu ja valitsemalla sitten toimintoruudussa **Muokkaa**. Koodeihin liitetyt suodattimet ovat tämän jälkeen käytettävissä **Varasto**-pikavälilehdessä.

    ![Nimikeryhmät](media/ItemGroup10.png "Nimikeryhmät")

1. Valitse **Nimikeryhmän suodatin** -osassa niiden suodattimien valintaruudut, joiden on vastattava, jotta suodatinryhmä voi olla nimikkeen oletussuodatinryhmä.

    Jos esimerkiksi **Käytä suodatinkoodia 1** ja **Käytä suodatinkoodia 2** -valintaruudut on valittu, nimikkeen suodatinkoodin 1 ja suodatinkoodin 2 on vastattava nimikeryhmän suodatinryhmän määritystä, ennen kuin suodatinryhmä voidaan valita. Uutta nimikettä luotaessa valittu suodatinryhmä on **Vapautetun tuotteen tiedot** -sivun **Varasto**-pikavälilehden **Ryhmä 1**- ja **Ryhmä 2** -kenttien oletussuodatinryhmä.

> [!IMPORTANT]
> Tuotteen suodatinkoodit ovat käytössä vain nimikkeissä, joissa käytetään edistynyttä varastonhallintaa.

## <a name="specify-filter-codes-for-released-products"></a>Vapautettujen tuotteiden suodatinkoodien määrittäminen

Vapautettujen tuotteiden suodatinkoodit määritetään seuraavien ohjeiden avulla. Suodatinkoodeilla voi ryhmitellä esimerkiksi vaaralliset aineet, joita tietyt toimittajat ostavat.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Luo tuote valitsemalla toimintoruudussa **Uusi**.
1. Anna **Uusi vapautettu tuote** -valintaikkunassa tiedot, joita tarvitaan uuden tuotteen perustan luontiin, ja valitse sitten **OK**.

    Tuotteen suodatinkoodeja ei ole otettu käyttöön, ellei suodatinkoodeja ole määritetty nimikeryhmään, joka on liitetty tuotteeseen.

    Lisätietoja on kohdassa [Uuden tuotteen luominen](../pim/tasks/create-new-product.md).

1. Määritä tuotteen suodatinkoodit valitsemalla **Varasto**-pikavälilehden **Tuotteen suodatinkoodit**-osassa tarvittaessa kenttien **Koodi 1**–**Koodi 10** suodatinkoodit.

## <a name="set-up-generally-available-items"></a>Yleisesti saatavana olevien nimikkeiden määrittäminen

Tietyt varastonimikkeet voidaan määrittää käytettäviksi vain asiakkaille, vain toimittajille tai asiakkaille ja toimittajille.

> [!NOTE]
> Asiakkaan ja toimittajan suodattimia ei käytetä nimikkeissä, jotka on määritetty yleisesti saataville.

Yleisesti saatavana olevat nimikkeet määritetään seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Tuotesuodattimet \> Yleisesti saatavana olevat tuotteet**.
1. Luo tietue valitsemalla toimintoruudussa **Uusi**.
1. Tuo nimikkeet asiakkaiden, toimittajien tai molempien käyttöön valitsemalla **Asiakas tai toimittaja** -kentässä *Asiakas*, *Toimittaja* tai *Kaikki*.
1. Anna **Alkamispäivämäärä ja -aika** -kentässä päivämäärä ja kellonaika, jolloin nimike on saatavana.
1. Valitse **Nimikeryhmä**-kentässä nimikeryhmä.
1. Rajoita yleisesti saatavana olevia nimikkeitä valitsemalla suodatuskoodit kentissä **Koodi 1**–**Koodi 10**.

    Kun nimikeryhmä valitaan, kyseinen nimikeryhmä määritetään yleisesti saatavilla. Suodatinkoodien valitseminen näissä kentissä rajoittaa saatavana olevia nimikkeitä.

## <a name="set-up-customer-product-filters"></a>Asiakkaan tuotesuodattimien määrittäminen

Tällä valinnaisella menetelmällä voidaan määrittää nimikkeet, joiden on oltava asiakkaiden käytettävissä niiden nimikkeiden ohella, jotka saadaan käytettäviksi **Yleisesti saatavana olevat nimikkeet** -sivun suodatinmääritysten perusteella. Yhdelle asiakkaalle voi määrittää useita suodattimia.

Asiakkaan suodatinkoodit määritetään seuraavasti:

1. Valitse **Myynti ja markkinointi \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse asiakas.
1. Valitse toimintoruudun **Asiakas**-välilehden **Asetukset**-ryhmässä **Tuotesuodattimet**.
1. Valitse **Tuotteen suodatinkoodit** -sivun toimintoruudussa **Uusi**.
1. Anna valitun nimikeryhmän alkamis- ja päättymispäivät **Alkamispäivämäärä ja -aika**- ja **Päättymispäivämäärä ja -aika** -kentissä.
1. Valitse **Nimikeryhmä**-kentässä nimikeryhmä.
1. Valitse kentissä **Koodi 1**–**Koodi 10** suodatinkoodit, joiden perusteella rajoitetaan asiakkaan saatavilla olevia nimikkeitä valitussa nimikeryhmässä. Valinta on tehtävä jokaisen nimikeryhmässä määritetyn suodatinkoodin osalta.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Toimittajan tuotesuodattimien määrittäminen

Tällä valinnaisella menetelmällä voidaan määrittää nimikkeet, joiden on oltava toimittajien käytettävissä niiden nimikkeiden ohella, jotka saadaan käytettäviksi **Yleisesti saatavana olevat nimikkeet** -sivun suodatinmääritysten perusteella. Yhdelle toimittajalle voidaan määrittää useita suodattimia.

Toimittajan suodatinkoodit määritetään seuraavasti:

1. Valitse **Hankinta \> Toimittajat \> Kaikki toimittajat**.
1. Valitse toimittaja.
1. Valitse toimintoruudun **Toimittaja**-välilehden **Asetukset**-ryhmässä **Tuotesuodattimet**.
1. Valitse **Suodatinkoodit** -sivun toimintoruudussa **Uusi**.
1. Anna valitun nimikeryhmän alkamis- ja päättymispäivät **Alkamispäivämäärä ja -aika**- ja **Päättymispäivämäärä ja -aika** -kentissä.
1. Valitse **Nimikeryhmä**-kentässä nimikeryhmä.
1. Valitse kentissä **Koodi 1**–**Koodi 10** suodatinkoodit, joiden perusteella rajoitetaan toimittajan saatavilla olevia nimikkeitä valitussa nimikeryhmässä. Valinta on tehtävä jokaisen nimikeryhmässä määritetyn suodatinkoodin osalta.

> [!NOTE]
> Toimittajan tuotesuodattimien määritykset koskeva sellaisia vapautettuja tuotteita, joissa varastonhallintaprosessit on otettu käyttöön liitetyssä varastodimensioryhmässä. Suodatinkoodien avulla määritetään ostotilausrivejä luotaessa, antaako järjestelmä käyttäjien ostaa tietyn toimittajan tietyn nimikkeen. Microsoft Dynamics 365 Supply Chain Managementissa on kaksi tapaa käsitellä toimittajan hyväksyntää. Jos vähintään yhdessä vapautetussa tuotteessa **Hyväksytyn toimittajan tarkistusmenetelmä** -kentän määrityksenä on *Vain varoitus* tai *Ei sallittu*, kumpikin toimittajan hyväksyntämenetelmä voidaan ottaa käyttöön kyseisissä nimikkeissä. Tämä tilanne voi aiheuttaa ongelmia, kun käyttäjät luovat ostotilausrivejä.

## <a name="see-also"></a>Lisätietoja

[Lisätietoja on blogikirjoituksessa WMS-varaston suodatinkoodit](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)
