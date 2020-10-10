---
title: Välilehtimoduuli
description: Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c9d897113442f14b95539efb9fec9482be96447a
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817031"
---
# <a name="tab-module"></a>Välilehtimoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskuvaus

Välilehtimoduulit ovat kontin kaltaisia moduuleja, joita käytetään välilehtien sivujen tietojen järjestämiseen. Niitä voidaan käyttää millä tahansa sivulla, jolla tiedot on esitettävä välilehdissä.

Jokaisessa välilehtimoduulissa voidaan lisätä yksi tai useampia välilehtimoduuleja. Jokainen välilehtinimikemoduuli edustaa yhtä välilehteä. Jokaiseen välilehtinimikemoduuliin voidaan lisätä yksi tai useita moduuleja. Välilehtinimikemoduuleihin lisättävien moduulien tyyppiä ei ole rajoitettu.

Seuraavassa kuvassa on esimerkki välilehtimoduulista sivuston sivulla. Tässä esimerkissä valittu **Toimitus**-välilehti on valittuna.

![Esimerkki välilehtimoduulista](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Välilehtimoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Otsikko | Teksti | Tämä ominaisuus määrittää valinnaisen tekstiotsikon välilehtimoduulille. |
| Aktiivinen välilehden indeksi | Numero | Tämä ominaisuus määrittää välilehden, joka on oletusarvoisesti aktiivinen, kun sivu ladataan. Jos arvoa ei ole annettu, ensimmäinen välilehti on oletusarvon mukaan aktiivinen. |

## <a name="tab-item-module-properties"></a>Välilehtinimikemoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Tehtävänimike | Teksti | Tämä ominaisuus määrittää otsikkotekstin välilehtinimikemoduulille. |

## <a name="add-a-tab-module-to-a-page"></a>Välilehtimoduulin lisääminen sivulle

Voit lisätä välilehtimoduulin sivulle ja määrittää ominaisuudet seuraavasti.

1. Käytä Fabrikam-markkinointimallia (tai mitä tahansa mallia, jolla ei ole rajoituksia) luodaksesi uuden sivun nimeltä **Myymälän käytännöt**.
1. Valitse **Oletussivulla** **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Välilehti**-moduuli ja valitse sitten **OK**.
1. Valitse välilehtimoduulin ominaisuusruudussa kynäsymbolin vieressä oleva **Otsikko**.
1. Kirjoita **Otsikko**-valintaikkunan **Otsikkoteksti** -kohtaan otsikkoteksti (esimerkiksi **Käytännöt**). Valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Välilehti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Välilehtinimike**-moduuli ja valitse sitten **OK**.
1. Kirjoita välilehtinimikemoduulin ominaisuusruudussa **Otsikon** kohdalle otsikkoteksti (esimerkiksi **Toimitus**).
1. Valitse kolme pistettä (**...**) **Välilehtinimike**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**.
1. Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään tekstikappale.
1. Lisää **Välilehti**-paikkaan muutamia otsikoita sisältävän välilehtinimikkeen moduuleja. Lisää kuhunkin välilehtinimikemoduuliin tekstilohkomoduuli, jossa on sisältöä.
1. Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**. Sivulla näkyy välilehtimoduuli, joka sisältää välilehtinimikemoduulit, joissa on lisäämäsi sisältö.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Haitarivalikkomoduuli](add-accordion.md)

[Tekstilohkomoduuli](add-content-rich-block.md)
