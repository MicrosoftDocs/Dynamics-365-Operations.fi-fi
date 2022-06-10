---
title: Tilausmoduuli
description: Tässä ohjeaiheessa on tietoja tilausmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: efc9150ea5ddeb7051f82fb07c4d566ac8a48dfa
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780586"
---
# <a name="subscribe-module"></a>Tilausmoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja tilausmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Tilausmoduuleita voidaan käyttää sivuston sivuilla asiakastietojen keräämiseksi uutiskirjeitä ja kampanjoita varten.

Seuraavassa kuvassa on esimerkki tilausmoduulista Adventure Works -sivuston sivun alatunnisteessa.

![Esimerkki tilausmoduulista Adventure Works -sivuston sivun alatunnisteessa](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Tilausmoduuli on käytettävissä Commerce-moduulikirjastossa Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin.
> - Tilausmoduuli on esillä Adventure Works -teemassa.
> - Tilausmoduuli edellyttää tietotoiminnon laajennusta toimiakseen joidenkin markkinointisähköpostien tarjoajien kanssa, jotta uutiskirjeitä tai kampanjasähköposteja voidaan lähettää, kun asiakastiedot on kerätty.

## <a name="subscribe-module-properties"></a>Tilausmoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Otsikko       | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Tilausmoduulin tekstiotsikko, kuten **Tilaa uutiskirje** tai **Rekisteröidy saadaksesi 10 % alennuksen**. |
| Kappale     | Kappaleen teksti | Tilausmoduuli tukee kappaletekstissä muotoiltua tekstiä, jotta otsikko voi tarjota lisätietoja toimintokutsusta. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Tilausmoduulin lisääminen uudelle sivulle

Voit lisätä tilausmoduulin uudelle sivulle ja määrittää sen vaaditut ominaisuudet Commerce-sivuston luontiohjelmassa noudattamalla seuraavia ohjeita.

1. Valitse **Mallit** ja avaa sivustosi aloitussivun markkinointimalli (tai luo uusi markkinointimalli).
1. Valitse oletussivun **pääpaikassa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Tilaa**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Valitse **Sivut** ja avaa sivuston aloitussivu (tai luo uusi aloitussivu käyttämällä markkinointimallia).
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Tilaa**-moduuli ja valitse sitten **OK**.
1. Lisää tilausmoduulin ominaisuusruudussa otsikko, kuten **Tilaa**.
1. Lisää kappaleteksti, kuten **Uusimmat trendit, tyylit ja tarjoukset. Oletko jo listalla? Tilaa nyt nähdäksesi uusimmat huipputarjoukset!**
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Adventure Works -teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
