---
title: Luo päätuote
description: Luo ennalta määritetyille varianteille päätuotteen.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e76c367d4aa6c08332371374a26dd6fdbbdb4eb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577333"
---
# <a name="create-a-product-master"></a>Luo päätuote

[!include [banner](../../includes/banner.md)]

Luo ennalta määritetyille varianteille päätuotteen. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu tuotesuunnittelijalle.


## <a name="create-a-new-product-master"></a>Luo uusi päätuote
1. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Päätuotteet**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Tuotenumero**-kenttään. Numeron tulee olla yksilöivä. **Tuotetunnus**-kenttään voidaan määrittää numerojärjestys. Tällöin käyttäjän ei tarvitse syöttää arvoa.
4. Kirjoita arvo **Tuotteen nimi**-kenttään. Syötä kuvaava tuotteen nimi. Arvo saa oletusarvon haun nimestä, mutta käyttäjä voi muuttaa arvon.
5. Avaa haku valitsemalla **Tuotedimensioryhmä**-kentässä avattavan valikon painike. Tuotedimensioryhmä määrittää, mitä neljää tuotedimensiota tuotevarianttien luomisessa voidaan käyttää. Tässä esimerkissä käytetään ryhmää, joka sisältää värin ja koon.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä. Oletusmääritysmenetelmä on **Ennalta määritetty variantti**. Tässä esimerkissä käytetään sitä.
8. Valitse **OK**.

## <a name="select-product-dimension-groups"></a>Tuotedimensioryhmien valitseminen
1. Avaa haku valitsemalla **Väriryhmä**-kentässä avattavan valikon painike.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Avaa haku valitsemalla **Kokoryhmä**-kentässä avattavan valikon painike.
5. Etsi haluamasi tietue luettelosta ja valitse se.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="add-dimension-groups"></a>Lisää dimensioryhmät
1. Valitse **toimintoruudusta** **Tuote**.
2. Avaa valintaikkuna valitsemalla **Dimensioryhmät**.
3. Avaa haku valitsemalla **Varastodimensioryhmä**-kentässä avattavan valikon painike. Varastodimensioilla hallitaan nimikkeiden tallentamista varastoon ja ottamista sieltä. Varastodimensio voi sisältää esimerkiksi toimipisteen ja varaston.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Avaa haku valitsemalla **Seurantadimensioryhmä**-kentässä avattavan valikon painike. Seurantadimensioryhmä määrittää, mitkä seurantadimensiot voit tuotteelle määrittää. Esimerkiksi eränumeroa ja sarjanumeroa voidaan käyttää varastonimikkeiden seurantaan.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse **OK**.
10. Valitse **Tallenna**.
11. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]