---
title: Pakkausmateriaalit ja maksut
description: Tässä ohjeaiheessa on tietoja pakkausmateriaalimaksuista, jotka maksetaan kierrätysyrityksille tietyin väliajoin.
author: MarkusFogelberg
manager: AnnBe
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2351cce9dc6e1a554800817f75591c4a4e24d43
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076244"
---
# <a name="packing-materials-and-fees"></a>Pakkausmateriaalit ja maksut

[!include [banner](../includes/banner.md)]

Pakkausmateriaalimaksuja maksetaan kierrätysyritykselle tietyin väliajoin. Maksuna peritään tietty summa kunkin pakkausyksikköön kuuluvan materiaalin painoyksikköä kohden. Vaikka pakkausmateriaalimaksut lasketaan ja raportoidaan, niistä ei kirjata kirjanpitotapahtumia, koska niitä ei käsitellä viranomaiselle maksettavana verona.

Pakkausmateriaalin painot ja maksut lasketaan sekä osto- että myyntitilausriveille.

Yhdelle nimikkeelle, nimikeryhmälle (pakkausryhmä) tai kaikille nimikkeille määritetään vähintään yksi pakkausyksikkö. Pakkausyksikköön kuuluvat pakkausmateriaalit, niiden paino ja pakkausyksikköön pakattavien nimikkeiden määrä. Pakkausmateriaalikoodi määritetään kullekin määritetylle pakkausmateriaalityypille. Voit määrittää pakkausmateriaalikoodin perusteella hinnan tietyksi ajaksi. Pakkausmateriaalimaksu lasketaan näiden tietojen perusteella.

> [!NOTE]
> Vaikka yritys ei maksaisi pakkausmateriaalimaksuja, toimintoa voi käyttää pakkausmateriaalien painoon perustuvien tilastojen laskemiseen.

## <a name="allocations"></a>Pakkausmateriaalin kohdistuksen määrittäminen

Ennen pakkausmateriaalipainojen, pakkausmateriaalimaksujen tai kummankin laskemista on otettava käyttöön laskenta ja määritettävä kutakin nimikettä koskevat materiaalit ja maksut.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto ja varastonhallinnan parametrit**.
1. Määritä **Yleistä**-välilehden **Pakkausmateriaali**-osassa **Laske pakkausmateriaalimaksut** -kohdan arvoksi **Kyllä**.
1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Pakkausmateriaali \> Pakkausryhmät** ja luo kaikki käytettävät pakkausryhmät. Kaikki pakkausryhmän nimikkeet käyttävät samaa pakkausmateriaalin kohdistusta. Jos et käytä pakkausryhmiä, voit ohittaa tämän vaiheen.

    > [!TIP]
    > Kun olet luonut pakkausryhmät, voit määrittää ryhmän kullekin tuotteelle tarpeen mukaan. Siirry kohtaan **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**, valitse tuote ja valitse sitten **Varastonhallinta**-pikavälilehdessä **Pakkausryhmä**-kentässä soveltuva pakkausryhmä.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Pakkausmateriaali \> Pakkausmateriaalikoodit**, määritä kunkin käytettävän pakkausmateriaalin tyyppi ja määritä sitten yksikkö, jota pakkausmateriaali käyttää lähetysten valmistelussa.
1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Pakkausmateriaali \> Pakkausmateriaalimaksut** ja määritä kullekin juuri määritetylle pakkausmateriaalityypille maksu. Maksut lasketaan kulutetun yksikkökohtaisen hinnan perusteella.
1. Jos haluat kohdistaa pakkausmateriaaleja nimikkeisiin, siirry kohtaan **Varastonhallinta \> Asetukset \> Pakkausmateriaali \> Pakkausmateriaalin kohdistus**. Luo kohdistukset. Voit luoda tarvitsemasi määrän kohdistuksia. Voit kohdistaa pakkausmateriaaleja yksittäisille nimikkeille, nimikeryhmille (pakkausryhmät) tai kaikille nimikkeille sen mukaan, miten yksityiskohtaisia kohdistukset ovat.

    Seuraa näitä ohjeita jokaiselle luodulle kohdistukselle.

    1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

        - **Nimikekoodi** – Valitse kohdistuksen laajuus seuraavasti:

            - **Taulukko** – Luo kohdistus yhdelle tietylle nimikkeelle.
            - **Ryhmä** – Luo kohdistus kaikille nimikkeille, jotka kuuluvat **Pakkausryhmät**-sivulla määritettyyn pakkausryhmään.
            - **Kaikki** – Luo kohdistus kaikille nimikkeille.

            > [!NOTE]
            > Yleensä kaikki kohdistukset on tehtävä samalla tasolla (**Taulukko**, **Ryhmä** tai **Kaikki**). Jos käytät useampaa kuin yhtä tasoa, kussakin nimikkeessä käytetään kohdistusta, joka vastaa nimikettä parhaiten. (**Taulukko**-tasoa käytetään ennen **Ryhmä**-tasoa. Kumpikin näistä tasoista on käytössä ennen **Kaikki**-tasoa.)

        - **Nimikkeen suhde** – Jos teet kohdistuksen yhdelle nimikkeelle, valitse nimike. Jos teet kohdistuksen nimikeryhmälle, valitse pakkausryhmä. Jos teet kohdistuksen kaikille nimikkeille, jätä tämä kenttä tyhjäksi.
        - **Määritys**, **Koko**, **Väri** ja **Tyyli** – Anna arvot näille dimensioille haluamallasi tavalla. Näin määrität nimikettä, jolle kohdistusta tehdään.
        - **Pakkausyksikkö** – Valitse yksikkö, johon nimike on pakattu, kun pakkausmateriaalia käytetään. Tämä yksikkö voi poiketa yksiköstä, jossa nimike ostetaan ja varastoidaan.
        - **Pakkausyksikkökerroin** – Anna muunto kerroin, jota käytetään muunnettaessa varastoyksikkö pakkausyksiköksi. (Muunnoksessa käytetään kaavaa *Pakkausyksiköt* = *Nimikeyksiköt* × *Pakkausyksikkökerroin*.)

    1. Lisää **Pakkausmateriaali**-pikavälilehdessä rivi kullekin pakkausmateriaalille, jota tarvitaan nykyisessä kohdistuksessa. Määritä kullakin rivillä materiaalin tyyppi (määritetty **Pakkausmateriaalikoodit**-sivulla) ja määrä, jota sitä kulutetaan kussakin nykyisen nimikkeen lähetysyksikössä.

## <a name="packing-units-on-sales-order-lines"></a>Myyntitilausrivien pakkausyksiköt

Kun olet [ottanut käyttöön pakkausmateriaalimaksujen laskennan ja määrittänyt kohdistukset](#allocations), järjestelmä tarkistaa, että pakkausyksiköt on määritetty jokaiselle myyntitilaukseen lisätylle nimikkeelle. Sen jälkeen lasketaan kaikki tarvittavat maksut. Kun nimike lisätään myyntitilaukseen, suoritetaan jokin seuraavista vaiheista:

- **Jos pakkauksen kohdistus koskee nimikettä**: Järjestelmä päivittää määritetyn pakkausyksikön ja pakkausyksikön määrän myyntitilausrivillä. (Pakkausyksikön määrä lasketaan käyttämällä kaavaa *Pakkausyksikön määrä* = *Tilattu määrä* ÷ *Valitun pakkausyksikön nimikkeiden määrä*.)
- **Jos pakkauksen kohdistus ei koske nimikettä:** Voit lisätä pakkausyksikön ja pakkausyksikön määrän myyntitilausriville manuaalisesti.

Pakkausyksikköä ja pakkausyksikön määrää voi muuttaa myös myyntitilausrivin kirjauksen yhteydessä. Tämä ominaisuus voi olla tarpeen, jos myyntitilausrivi toimitetaan tai laskutetaan vain osittain.

Järjestelmä luo pakkausmateriaalitapahtumat, kun myyntitilaus laskutetaan. Pakkausmateriaalitapahtumat sisältävät myyntirivin pakkausmateriaalien painon. Voit muokata tapahtumia niiden laskutuksen jälkeen. Voit sitten luoda uudet tapahtumat.

## <a name="packing-units-on-purchase-order-lines"></a>Ostotilausrivien pakkausyksiköt

Järjestelmä ei luo ostotilausriveille pakkausmateriaalitapahtumia. Sen sijaan voit luoda laskutettuja ostontilausrivien tapahtumia manuaalisesti **Pakkausmateriaalitapahtumat**-sivulla.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Niiden asiakkaiden lisenssinumeroiden määrittäminen, joilta pakkausmateriaalimaksut veloitetaan

Jos tietyn asiakkaan myyntitilausten tulee sisältää kuhunkin tilaukseen käytettävät pakkausmateriaalikulut, toimi seuraavasti.

1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse asiakas, jolta pakkausmateriaalit veloitetaan.
1. Valitse **Lasku ja toimitus** -pikavälilehdellä seuraavat lisäkentät:

    - Anna **Arvonlisävero**-osan **Pakkausmaksun lisenssinumero** -kenttään yrityksen lisenssinumero.
    - Anna **Pakkausmateriaalimaksu**-osan **Lisenssinumero**-kenttään yrityksen lisenssinumero.

Kun tämän jälkeen luot ja laskutat myyntitilauksen, joka sisältää vähintään yhden pakkausmateriaaleja käyttävän nimikkeen, lasku näyttää pakkausmateriaalimaksut.

Jos asiakas ei halua maksaa pakkausmateriaalimaksuja, noudata näitä samoja vaiheita, mutta tyhjennä lisenssinumerot **Pakkausmaksun lisenssinumero**- ja **Lisenssinumero**-kentistä. Sellaisten asiakkaiden laskut, jotka eivät maksa pakkausmateriaalimaksuja, näyttävät pakkausmateriaalien painot, mutta ne eivät näytä maksuja.

Jos haluat luoda raportin, jossa näkyvät kaikki pakkausmateriaalimaksut, jotka yritys on velkaa tietyltä kaudelta, siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Pakkausmateriaaliraportit \> Pakkausmateriaalimaksun laskeminen**, määritä päivämääräalue ja valitse **OK**.

## <a name="print-packing-material-weights-on-invoices"></a>Pakkausmateriaalin painon tulostaminen laskuihin

Voit tulostaa pakkausmateriaalien painon laskuun ja osoittaa, kuka maksaa liittyvät maksut. Painojen yhteenlaskeminen tapahtuu pakkauskoodeittain.

1. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
1. Määritä **Päivitykset**-välilehden **Lasku**-pikavälilehdessä **Tulosta pakkausmateriaalin paino** -asetuksen arvoksi **Kyllä**.
