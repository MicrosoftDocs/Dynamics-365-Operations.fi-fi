---
title: Online-tilausten verot on laskettu väärin
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun online-tilausten verot on laskettu väärin tai kun myyntirivin veroryhmää ei ole määritetty oikein.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585299"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Online-tilausten verot on laskettu väärin

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun online-tilausten verot on laskettu väärin tai kun myyntirivin veroryhmää ei ole määritetty oikein.

## <a name="description"></a>kuvaus

Kun sähköinen kaupankäyntitilaus on tehty, verot lasketaan väärin tai myyntirivin veroryhmä on määritetty väärin.

## <a name="resolution"></a>Ratkaisu

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Vähittäismyymälän arvonlisäveron konfiguroiminen Commerce headquarters -sovelluksessa

Voit konfiguroida vähittäismyymälän arvonlisäveron Commerce headquarters -sovelluksessa seuraavasti.

1. Valitse **Retail ja Commerce \> Kanavat \> Kaikki myymälät**.
1. Valitse myymälä, jolle arvonlisävero konfiguroitaan.
1. Määritä myymälän arvonlisäverotiedot **Yleiset**-pikavälilehden **Arvonlisävero**-osassa.

> [!NOTE]
> Jos tuote noudetaan myymälästä, veroryhmä tulee noutoa varten valitusta myymälästä. Lisätietoja on kohdassa [Muiden myymälän veroasetusten määrittäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Asiakkaan osoitteen arvonlisäveron konfiguroiminen Commerce headquarters -sovelluksessa

Voit konfiguroida asiakkaan osoitteen arvonlisäveron Commerce headquarters -sovelluksessa seuraavasti.

1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse asiakas, jolle arvonlisäverot määritetään.
1. Valitse **Osoitteet**-pikavälilehdestä osoite, jolle haluat määrittää arvonlisäverot, valitse **Lisää vaihtoehtoja** ja valitse sitten **Lisäasetukset**.
1. Valitse **Yleiset**-pikavälilehdessä **Veroryhmä**.
1. Valitse sopiva arvo **Arvonlisävero**-kenttään.

> [!NOTE]
> Lähetykselle, johon liittyy asiakkaan osoitteen arvonlisäveroa, rivin toimitusosoite määrittää rivin veroryhmän. Jos asiakkaalle toimitetaan olemassa olevaan osoitteeseen, jonka veroryhmä on jo konfiguroitu, käytetään aiemmin luotua veroryhmää. Osoitteilla ei oletusarvoisesti ole veroryhmää, kun ne luodaan.

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Yleisten arvonlisäveroryhmien konfiguroiminen Commerce headquarters -sovelluksessa

Voit konfiguroida yleiset arvonlisäveroryhmät Commerce headquarters -sovelluksessa seuraavasti.

1. Siirry kohtaan **Vero \> Välilliset verot \> Arvonlisävero \> Arvonlisäveroryhmä**.
1. Valitse määritettävä veroryhmä vasemmasta siirtymisruudusta.
1. Määritä arvonlisäveroryhmän verot **Vähittäismyyntikohteeseen perustuva vero** -pikavälilehdessä.

> [!NOTE]
> Jos lähetykseen ei liity arvonlisäveroa asiakkaan osoitteeseen, rivin toimitusosoite sekä veroryhmälle määritetyt kohteeseen perustuvat verot määrittävät veroryhmän. Lisätietoja on kohdassa [Määränpäähän perustuvien verojen määrittäminen online-myymälöille](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="additional-resources"></a>Lisäresurssit

[Arvonlisäveron laskeminen online-tilauksille](../sales-tax-config.md)