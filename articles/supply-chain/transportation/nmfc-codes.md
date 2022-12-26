---
title: National Motor Freight Classification (NMFC) -koodit
description: Tässä artikkelissa kuvataan, miten National Motor Freight Classification (NMFC) -koodeja käsitellään Microsoft Dynamics 365 Supply Chain Managementissa
author: Weijiesa
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c173057b8e1357790e780469c5806afb857be62a
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838314"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>National Motor Freight Classification (NMFC) -koodit

[!include [banner](../includes/banner.md)]

National Motor Freight Classification (NMFC) -koodit auttavat sinua luokittelemaan toimitettavat nimikkeet. NMFC-koodi on merkintä, jota käytetään kauppatavaran ryhmittelemisessä. Kuljetusyritysten on sen avulla mahdollista arvioida toimitettavat tavarat luokittelemalla nimikkeet eri näkökohdat, kuten kuorma-autoon sopivat, lastausongelmat, käsittelyongelmat ja käytettävyys huomioon ottaen. Kauppatavarat ryhmitellään yhteen 18 rahtiluokasta käyttämällä lukuja 50–500. Luokka, jonne kauppatavara on ryhmitelty, perustuu neljään kuljetusominaisuudesta, jotka ovat tiheys, säilytettävyys, käsittely ja velka. Yhdessä nämä ominaisuudet muodostavat kauppatavaran kuljetettavuuden.

NMFC-koodi on liitetty kuorma-autokuormaa pienempiin (LTL) lähetysnimikkeisiin. Esimerkiksi kannettavalle tietokoneelle voidaan määrittää NMFC-luokka 2.5, kun taas sähköjohdoille määritetään NMFC-luokka 65.

Tämän ominaisuuden avulla työntekijät voivat luokitella LTL-lähetysnimikkeet NMFC-koodien avulla. Seuraavassa on muutamia esimerkkejä:

- Jos yrityksesi sisällyttää rahtikirjaan rahtikuvauksen, operaattori saa käsityksen rahdista. Rahti on tärkeä luokitus, koska monet kuljetusyritykset perustavat koko liiketoimintamallinsa rahtityyppeihin.
- Luokitus voi olla tärkeä yrityksellesi, koska sitä käytetään tietyn kuormituksen kustannusten määrittämiseen.
- Yrityksesi voi tunnistaa LTL-logistiikka- ja kuljetusyrityksen kannattavuuden.

Tässä artikkelissa käsitellään NMFC-koodien käsittelemistä Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit luoda NMFC-koodit, sinun on määritettävä kaikki LTL-rahtiluokat, jotka on määritettävä niihin. LTL-rahtiluokat edustavat nimikeluokkia, kun taas NMFC-koodit liittyvät kunkin 18 rahtiluokan tiettyihin kauppatavaroihin. Lisätietoja LTL-luokkien kanssa työskentelystä on kohdassa [Kuorma-autokuormaa pienemmät (LTL) luokat](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Luo NMFC-koodi

Luo NMFC-koodi seuraavien ohjeiden avulla.

1. Noudata seuraavia ohjeita:

    - Valitse **Varastonhallinta \> Asetukset \> Varasto \> NMFC-koodit**.
    - Valitse **Kuljetustenhallinta \> Asetukset \> Kuljetusstandardit \> NMFC-koodit**.

1. Luo uusi NMFC-koodi valitsemalla **Uusi**. Määritä sitten seuraavat kentät:

    - **NMFC-koodi** – Kirjoita kauppatavaran tyypin NMFC-koodi.
    - **Nimi** – Kirjoita NMFC-koodin nimi.
    - **LTL-luokka** – Valitse LTL-luokka, joka on liitetty NMFC-koodiin.
    - **BOL materiaalin käsittely-yksikkö** – Määritä lähetyksen oletuskäsittelytyyppi.

## <a name="example-set-up-nmfc-codes"></a>Esimerkki: NMFC-koodien määrittäminen

Seuraavassa esimerkissä kerrotaan, miten määritetään kaksi erilaista NMFC-koodia, joita voit käyttää erityyppisten tuotteiden kanssa.

1. Valitse **Varastonhallinta \> Määritykset \> Varasto \> NMFC-koodit** tai **Kuljetustenhallinta \> Määritykset \> Kuljetusstandardit \> NMFC-koodit**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **NMFC-koodi:** *92.5*
    - **Nimi:** *Tietokoneet*
    - **LTL-luokka:** *92.5*
    - **BOL materiaalin käsittely-yksikkö:** *Yksikkö*

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **NMFC-koodi:** *125*
    - **Nimi:** *Puhelimet*
    - **LTL-luokka:** *125*
    - **BOL materiaalin käsittely-yksikkö:** *Yksikkö*

1. Valitse toimintoruudussa **Tallenna**.

## <a name="additional-resources"></a>Lisäresurssit

- [Kuorma-autokuormaa pienemmät (LTL) luokat](ltl-class.md)
- [Rahtikirjan luominen](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
