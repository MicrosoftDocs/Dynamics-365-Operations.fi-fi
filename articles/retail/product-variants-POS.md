---
title: Varastohaku myyntipisteessä (POS)
description: Tässä ohjeaiheessa käsitellään asetuksia, joilla voi tarkastella varastotietoja myyntipisteessä.
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: cd2dc460c9e862503ebbf1942dcf998d67829d86
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572046"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Varastohaku myyntipisteessä (POS)

[!include [banner](includes/banner.md)]

Myyntipisteen varastohaku auttaa jälleenmyyjiä tehostamaan toimintaa reaaliaikaisesti. Samalla myymälöiden, myyntipisteen ja taustatoimintojen yhdistäminen antaa analyysitietoja. Tällä toiminnolla saa tarkan reaaliaikaisen näkymän eri myymälöiden ja jakelukeskusten tuotevarastoon. Sen avulla jälleenmyyjät voivat myös tehostaa toimintaa ja kustannussäästöjä, sillä reaaliaikainen varastosuunnittelu paranee.

Tarkka reaaliaikainen koko organisaation kattava varastonäkymä auttaa myyntiedustajia tarjoamaan nopeaa ja erinomaista asiakaspalvelua. Tärkein hetki on se hetki, jolloin asiakas on valmis tekemään ostopäätöksen. On tärkeää, että myymälän kassojen käytettävissä on reaaliaikaiset varastotiedot, jotta he voivat luvata tuotteen toimituksen ja noudon tarkasti.

Voit avata **Varastohaku**-sivun **Retail Modern POS**- tai **Retail Cloud POS** -työtilasta.

![Myyntipisteen aloitussivun varastohakuruutu](media/POSHomepage.png)

Voit antaa tuotteen numeron **Varastohaku**-sivulla numeronäppäimistöllä. Voit sitten tarkastella useiden myymälöiden ja varastojen käytettävissä olevaa määrää.

![Vakiovarastohaku-sivu](media/InventoryLookUp.png)

Kullekin sijainnille näytetään myös **Varattu**- ja **Tilattu**-määrät.

- **Varattu** – tämä määrä viittaa sijainnissa tietyn tuotenumeron taustatoimintojen**Fyysiset varatut** -arvoon.
- **Tilattu** – tämä määrä viittaa sijainnissa tietyn tuotenumeron taustatoimintojen**Tilattu yhteensä** -arvoon.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Sijainnit, joiden varastosaatavuustiedot näytetään

Sijaintiluettelossa on kahden tyyppisiä yksiköitä:

- **Vähittäismyymälät** – luettelo sisältää myymälät, jotka on määritetty käyttämällä nykyisen myymälän myymälän paikanninryhmää Retail Headquartersissa.
- **Jakelukeskukset** – Microsoft Dynamics 365 for Retailissa voidaan määrittää erilaisia jakelukeskuksen (kuten varastoja). Luettelossa näkyy kuitenkin vain **Vakio**-oletustyyppisten jakelukeskusten varaston saatavuustiedot.

    > [!NOTE]
    > Varaston saatavuustietoja ei näytetä myyntipisteellä seuraaville varastotyypeille: **Kuljetus**, **Karanteeni** ja **Tavarat matkalla**.

Voit tarkastella **Varastohaku**-sivulla kunkin myymälän luvattavissa olevaa määrää (ATP) nykyisten käytettävissä olevan määrän, varattujen määrien ja tilattujen määrien lisäksi. Valitse myymälä, jonka ATP-tietoja haluat tarkastella, ja valitse sitten myymälä **Näytä myymälän käytettävyys**.

![ATP-määrät](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>Kaikkien varianttien näyttäminen avaamalla dimensioon perustuva matriisi

Valitse päätuotteen **Tuotteen tiedot** -sivulla tai **Varastohaku**-sivulla **Näytä kaikki variantit** sivun alaosassa olevasta sovelluspalkista. Näillä sivulla aluksi avautuva **Dimensioon perustuva matriisi** -näkymä näyttää nykyisen myymälän kaikkien tuotevarianttien varaston saatavuustiedot.

> [!NOTE]
> **Näytä kaikki variantit** -painike on käytettävissä niillä nimikkeen päätuotteilla, joilla on tuotevariantteja. Se ei ole käytettävissä erillisissä tuotteissa tai myyntirakenteissa.

![Näytä kaikki variantit -painike Varastohaku-sivulla](media/StandardToMatrix.png)

Valitse **Näytä kaikki variantit** päätuotteen **Tuotteen tiedot** -sivulla tai **Varastohaku**-sivulla sijaintia valitsematta. Siirry sitten **Dimensioon perustuva matriisi** -näkymään, jossa voit tarkastella nykyisen myymälän kaikkien tuotevarianttien varaston saatavuustietoja.

![Varastohaku-sivun Dimensioon perustuva matriisi -näkymä](media/Matrix.png)

> [!NOTE]
> Edellisessä kuvassa dimensioiden näytetään aakkosjärjestyksessä, koska valitun tuotteen dimensioiden näyttöjärjestystä ei ole määritetty.

**Dimensioon perustuva matriisi** -näkymässä tuotevarianttien solujen oikeassa alakulmassa on käytettävissä oleva arvo. Seuraavassa taulukossa selitetään eri arvojen merkitykset.

| Käytettävissä olevan varaston arvo                            | kuvaus |
|------------------------------------------|-------------|
| Numeerinen arvo, joka on suurempi kuin 0 (nolla) | Variantti on vapautettu valittuun sijaintiin, ja voit tehdä solussa lisätoimintoja. (Näitä toimintoja käsitellään tarkemmin jäljempänä tässä ohjeaiheessa.) |
| **0** (nolla)                             | Variantti on vapautettu valittuun sijaintiin mutta nimike ei käytettävissä valitussa sijainnissa. Voit kuitenkin tehdä solussa muita toimia. (Näitä toimintoja käsitellään tarkemmin jäljempänä tässä ohjeaiheessa.) |
| **–** tai passiivinen solu              | Varianttia ei ole vapautettu valittuun sijaintiin etkä voi tehdä solussa lisätoimintoja. |

Voit myös muuttaa pivot-dimensiota valitsemalla uuden käytettävän dimension.

![Pivot-dimension muuttaminen](media/ChangePivot.png)

![Pivot-dimensio muutettu](media/PivotChanged.png)

> [!NOTE]
> Edellisissä kuvissa valitun tuotteen dimensioiden näyttöjärjestys on mukautettu (ei aakkosellinen). Se perustuu taustatoiminnossa määritettyyn dimension näyttöjärjestykseen.

**Dimensioon perustuva matriisi** -näkymässä voidaan suorittaa myös muita toimintoja, jotka tehostavat myymälän myyjien tuottavuutta. Seuraavassa on muutamia esimerkkejä:

- Muuttamalla myymälän sijaintia voit hakea kaikkien tuotevarianttien varastosaatavuuden muissa sijainnissa. Näitä sijainteja ovat muut myymälän paikannin ryhmät myymälät ja **Vakio**-oletustyypin jakelukeskukset.
- Myy yksittäinen tuotevariantti asiakkaalle käyttämällä itsepalvelutukkua, noutoa myymälästä tai lähetystä osoitteeseen.
- Anna asiakkaalle yksittäisen tuotevariantin ATP-tiedot tietyssä sijainnissa.

![Varianttiruutujen muut toiminnot](media/VariantActions.png)

> [!NOTE]
> Edellisessä kuvassa dimensioiden näytetään aakkosjärjestyksessä, koska valitun tuotteen dimensioiden näyttöjärjestystä ei ole määritetty.

Seuraavassa taulukossa on lisätietoja käytettävissä olevista toiminnoista.

| Toimenpide               | kuvaus |
|----------------------|-------------|
| Myy nyt             | Lisää tapahtumaan valittu nimikevariantti ja ohjaa käyttäjä tapahtumanäyttöön. (Tämä toiminto ei ole käytettävissä, kun valittu sijainti on jakelukeskus.) |
| Nouto myymälästä     | Luo tuotevariantille asiakastilaus, joka noudetaan valitusta sijainnista, ja ohjaa käyttäjä tapahtumanäyttöön. (Tämä toiminto ei ole käytettävissä, kun valittu sijainti on jakelukeskus.) |
| Lähetä tuote         | Luo tuotevariantille asiakastilaus, joka lähetetään valitusta sijainnista, ja ohjaa käyttäjä tapahtumanäyttöön. |
| Käytettävyys         | Näytä valitun sijainnin valitun varianttiyhdistelmän ATP-tiedot. |
| Näytä kaikki sijainnit   | Vaihda varastohaun vakionäkymään ja korosta nimikevariantiin varaston saatavuustiedot kaikissa myymälän paikanninryhmän myymälöissä sekä **vakio- tai oletustyypin** jakelukeskuksissa. |
| Näytä tuotteen tiedot | Ohjaa käyttäjä liitetyn päätuotteen **Tuotteen tiedot** -sivulle. |
