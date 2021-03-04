---
title: Kenttien kuvausten tarkasteleminen ja vieminen
description: Tässä artikkelissa käsitellään kenttien kuvauksien näyttämistä ja kuvauksien tuomista Kenttien kuvaus -sivun avulla.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7a9e12eae7065bb37fc0ddbb579a0437120c165
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693518"
---
# <a name="view-and-export-field-descriptions"></a>Kenttien kuvausten tarkasteleminen ja vieminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään kenttien kuvauksien näyttämistä ja kuvauksien tuomista Kenttien kuvaus -sivun avulla.

Joillakin monimutkaisimmilla kentillä on kuvaukset. Nämä kuvaukset tulevat näkyviin, kun pidät hiiren osoitinta kentän päällä. Voit myös tarkastella ja viedä kuvauksia **Kentän kuvaukset** -sivulla.

Kaikilla sivuilla ei ole kentän kuvauksia. Vain monimutkaisilla kentillä on kuvaukset; kuvauksia ei ole kentillä, joiden käyttö on selkeää. Tämän vuoksi joillakin sivuilla ei ole lainkaan kenttäkuvauksia, joillakin sivuilla on muutamia kuvauksia ja joillakin monimutkaisilla sivuilla, kuten monilla parametrisivulla, on useita kuvauksia.

Voit lisätä halutessasi uusia kenttien kuvauksia ja mukauttaa valmiita kuvauksia, jos sinulla on kehitysympäristön käyttöoikeus. Voit esimerkiksi lisätä yrityskohtaiset tiedot kentän kuvaukseen. Lisätietoja on kohdassa [Kenttien kuvausten mukauttaminen](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Lisätietoja on käyttöliittymän kenttien kuvauksissa.

Voit tarkastella kentän kuvauksia asettamalla hiiren osoittimen kentän päälle. Jos kuvausta ei ole, kentän nimi tulee näkyviin, kun pidät hiiren osoitinta kentän päällä.

> [!NOTE]
> Kenttien kuvauksia voidaan tarkastella Dynamics AX 7.0:ssa (helmikuu 2016) vain **Kenttien kuvaukset** -sivulla.

Seuraavassa kuvassa on kentän kuvaus, joka tulee näkyviin, kun pidät hiiren osoitinta **Lukitse nimikkeet inventoinnin ajaksi** -kentän päällä.

[![Esimerkki kentän kuvauksesta](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Tarkastele kentän ohjetta ja vie ohje Kenttien kuvaukset -sivulla

Voit tarkastella ja viedä **Kenttien kuvaukset** -sivulla kenttien kuvauksia. Voit tarkastella kuvauksia, jotka ovat käytettävissä yhdelle sivulle kerrallaan.

### <a name="view-the-descriptions-for-a-page"></a>Näytä sivun kuvaukset

Tarkastele sivun kuvauksia seuraavasti.

- Kirjoita sivun nimi **Valitse sivu** -kenttään. Voit vaihtoehtoisesti avata kaikkien sivujen luettelon napsauttamalla nuolta ja selaamalla tai suodattamalla sitten luetteloa.

Voit käyttää joko käyttöliittymässä näkyvää nimeä (kuten **Asiakkaat**) tai koodinimeä, (AOT-nimeä), joka on käytettävissä, kun napsautat sivua hiiren kakkospainikkeella (kuten **CustTable**).

Lisätietoja sivuluettelon suodattimesta on myöhemmin tässä artikkelissa kohdassa Sivun haku.

Jos valitset **Sisällytä kenttiä ilman kuvaus** -asetukseksi **Kyllä**, kaikki sivun kentät näytetään, vaikka niillä ei olisi kuvausta.

### <a name="export-the-descriptions-for-a-page"></a>Tuo sivun kuvaukset

Voit viedä sivun kuvauksia toimimalla seuraavasti.

1. Valitse sivu **Valitse sivu** -kentässä.
2. Napsauta **Avaa Microsoft Officessa** -painiketta oikeassa yläkulmassa ja valitse sitten **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Hakemassa sivua

Voit etsiä sivua usealla eri tavalla **Valitse sivu** -kentässä. Usein avattava luettelo on avattava napsauttamalla **Valitse sivu** -kentässä nuolta ja tehtävä sitten valinta suodatetusta sivuluettelosta.

- Voit kirjoittaa nimen osittain ja tehdä sitten valinnan avattavassa luettelossa suodatetusta sivuluettelosta.
- Avaa avattava luettelo ja valitse sitten joko **Sivun nimi** -otsikko luettelon alussa tai **Sivu AOT-nimi** -otsikko. Voit käyttää avattavassa valintaikkunassa suodatuksen lisäasetuksia, kuten asetusta **Sivun nimi alkaa**.
- Kirjoita sivun kokonainen nimi. Jos käytät tätä asetusta, avattava luettelo kannattaa avata ja katsoa, mitä muuta luettelossa on, vaikka kenttien kuvaukset ovat näkyvissä.

    - Jos on yksi nimi tarkka vastine, kyseisen sivun kenttien kuvaukset näkyvät.
    - Jos tarkkoja vastineita on useita, kuvauksia ei näytetä. Avaa avattava luettelo ja valitse sopiva sivu.
    - Jos kirjoittamasi nimi on toisen sivun nimen osa, näet sivun kuvaukset. Jos kuitenkin avaat avattavan luettelon, näkyvissä on lisää nimen sisältäviä sivuja.

Kuvauksia ei esimerkiksi näytetä, jos kirjoitat **Inventointi** **Valitse sivu** -kenttään. Kun avaat luettelon näet, että kahdella sivulla on nimi **Inventointi** ja inventointi-sana on useiden sivujen nimessä. Jos valitset sivun, jonka AOT-nimi on **InventJournalCount**, kyseisen sivun kenttien kuvaukset näytetään. Jos kuitenkin avaat avattavan luettelon uudelleen, näet, että luettelo sisältää nyt kaikki sivut, joiden AOT-nimeen InventJournalCount sisältyy.

## <a name="troubleshooting"></a>Vianmääritys

Tässä osassa on tietoja, jotka on sellaisten ongelmien vianmäärityksessä, joita voi tulla esiin kenttien kuvauksia käytettäessä.

### <a name="i-cant-find-a-field-description"></a>Kentän kuvausta ei löydy.

Monimutkaisempia kenttiä varten lisätään parhaillaan kuvauksia. Jos tarvitset tiettyä kenttää koskevaa apua, ilmoita siitä meille lisäämällä kommentti tähän aiheeseen.

### <a name="the-field-description-isnt-helpful"></a>Kuvauksen kentästä ei ole apua

Ilmoita meille lisäämällä kommentti tähän aiheeseen. Jos mahdollista, kerro, mitä lisätietoja tarvitset.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>En löydä kenttää Kenttien kuvaukset -sivulla

Voit näyttää kaikki kentät sivulla, kun määrität **Sisällytä kentät, joihin ei liity kuvausta** -asetuksen arvoksi **Kyllä**. Varmista, että olet valinnut oikean sivun valitsemalla **Valitse sivu** -kenttä. Jos kirjoittamasi nimi on toisen kentän nimeä, olet ehkä valinnut sivun, jonka nimi on pidempi.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>En löydä sivua Kenttien kuvaukset -sivulla

Lisätietoja erilaisista sivujen etsimistavoista on aiemmin tässä artikkelissa kohdassa Sivujen etsiminen. Jos kirjoitit sivun tarkan nimen, kentän kuvauksia ei ehkä näytetä, jos usealla sivulla on sama nimi. Avaa suodatettu luettelo käytettävissä olevista sivuista napsauttamalla **Valitse sivu** -kentän nuolta.

## <a name="additional-resources"></a>Lisäresurssit

[Kenttien kuvausten mukauttaminen](../../dev-itpro/user-interface/customize-field-help.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]