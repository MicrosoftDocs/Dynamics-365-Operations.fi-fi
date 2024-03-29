---
title: Haitarivalikkomoduuli
description: Tässä artikkelissa on tietoja haitarivalikkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: ec895476770f297825d6c88d0b0a5fef43a5c6ef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279153"
---
# <a name="accordion-module"></a>Haitarivalikkomoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja haitarivalikkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Haitarimoduulit ovat konttimoduulin kaltaisia ja niitä käytetään tietojen tai moduulien järjestämiseen sivulla tarjoamalla tiivistettävän laatikon kaltaisen ominaisuuden. Haitarimoduulia voidaan käyttää millä tahansa sivulla.

Jokaisen haitarimoduulin sisällä voidaan lisätä yksi tai useampia haitarinimikemoduuleja. Jokainen haitarinimikemoduuli edustaa tiivistettävää laatikkoa. Jokaisen haitarinimikemoduulin sisällä voidaan lisätä yksi tai useampia moduuleja. Haitarinimikemoduuleihin lisättävien moduulien tyyppiä ei ole rajoitettu.

Seuraavassa kuvassa on esimerkki haitarimoduulista, jota käytetään myymälän usein kysyttyjen kysymysten (FAQ) tietojen järjestämiseen.

![Esimerkki haitarimoduulista.](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Haitarimoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Otsikko | Teksti | Tämä ominaisuus määrittää valinnaisen tekstiotsikon haitarimoduulille. |
| Laajenna kaikki | **Tosi** vai **Epätosi** | Jos arvoksi on määritetty **Tosi**, laajenna/tiivistä-toiminto on käytössä, jotta kaikki haitarimoduulin kohteet voidaan laajentaa ja tiivistää. |
| Vuorovaikutustyyli | **Itsenäinen** tai **Laajenna vain yksi nimike** | Tämä ominaisuus määrittää haitarinimikkeiden vuorovaikutuksen tyylin. Jos arvoksi on määritetty **Itsenäinen**, jokainen haitarikohde voidaan laajentaa tai tiivistää itsenäisesti. Jos arvo on määritetty niin, että **vain yksi nimike laajennetaan**, vain yksi nimike voidaan laajentaa kerrallaan. Kun nimikkeitä laajennetaan, aiemmin laajennetut nimikkeet tiivistetään. |

## <a name="accordion-item-module-properties"></a>Haitarinimikemoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|----------------|--------|-------------|
| Tehtävänimike | Teksti | Tämä ominaisuus määrittää otsikkotekstin haitarinimikemoduulille. Kun valitset otsikkoalueen, käyttäjät voivat laajentaa tai tiivistää osan. |
| Laajenna oletusarvoisesti | **Tosi** vai **Epätosi** | Jos arvoksi on määritetty **Tosi**, haitarikohde laajennetaan oletuksena, kun sivu ladataan. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>Haitarimoduulin lisääminen Usein kysyttyjä kysymyksiä -sivulle

Voit lisätä haitarimoduulin Usein kysyttyjä kysymyksiä -sivulle ja määrittää sen ominaisuudet sivuston luontityökalussa seuraavasti.

1. Siirry kohteeseen **Sivut** ja käytä Fabrikam-markkinointimallia (tai mitä tahansa mallia, jolla ei ole rajoituksia) luodaksesi uuden sivun nimeltä **Myymälän usein kysytyt kysymykset**.
1. Valitse **Oletussivulla** **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Haitari**-moduuli ja valitse sitten **OK**.
1. Valitse haitarimoduulin ominaisuusruudussa kynäsymbolin vieressä oleva **Otsikko**.
1. Lisää **Usein kysyttyjä kysymyksiä** **Otsikko**-valintaikkunan **Otsikon teksti** -kohtaan. Valitse sitten **OK**.
1. Valitse haitarimoduulin ominaisuusruudussa **Näytä Laajenna kaikki** -valintaruutu ja valitse sitten **Vuorovaikutustyyli**-kentästä **Itsenäinen**.
1. Valitse kolme pistettä (**...**) **Haitari**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Haitarinimike**-moduuli ja valitse sitten **OK**.
1. Kirjoita haitarinimikemoduulin ominaisuusruudussa **Otsikon** kohdalle otsikkoteksti (esimerkiksi **Miten palautus toimii?**).
1. Valitse kolme pistettä (**...**) **Haitarinimike**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**.
1. Kirjoita tekstilohkomoduulin ominaisuusruutuun tekstikappale (esimerkiksi **Palautus on käsiteltävä Call Centerin kautta. Ota yhteyttä 1-800-FABRIKAM palautuksiin liittyen. Tuotteilla on 30 päivän palautuskäytäntö. Palautus on aloitettava tämän aikavälin sisällä.**).
1. Lisää **Haitari**-paikassa muutama haitarinimikemoduuli. Lisää kuhunkin haitarinimikemoduuliin tekstilohkomoduuli, jossa on sisältöä.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Sivulla näkyy haitarimoduuli, jossa on lisäämäsi sisältö.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Välilehtimoduuli](add-tab.md)

[Tekstilohkomoduuli](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
