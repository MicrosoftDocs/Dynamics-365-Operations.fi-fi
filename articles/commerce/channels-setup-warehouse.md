---
title: Varaston määrittäminen
description: Tässä artikkelissa käsitellään uuden kanavan kanssa käytettävän varaston määrittämistä Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 476f78d7fe1bc61c2c9b783ed1f82bc660248b02
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273636"
---
# <a name="warehouse-set-up"></a>Varaston määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään uuden kanavan kanssa käytettävän varaston määrittämistä Microsoft Dynamics 365 Commercessa.

Jokaiseen Commerce-kanavaan on liitettävä määritetty varasto. Seuraavilla menetelmillä tehdään määritykset, jotka vähintään tarvitaan Commerce-kanavan varaston määrittämiseen. Lisätietoja varaston määrittämisestä on kohdassa [Varastonhallinnan yleiskatsaus](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).

## <a name="configure-a-warehouse-site"></a>Varaston toimipaikan määrittäminen

Ennen varaston määrittämistä on määritettävä varaston toimipaikka.

Varaston toimipaikka määritetään noudattamalla seuraavia ohjeita.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Toimipaikat**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna **Toimipaikka**-kentässä arvo.
1. Anna **Nimi**-kenttään arvo.
1. Määritä **Yleiset**-osassa sopiva **Aikavyöhyke**.
1. Anna osoite **Osoitteet**-osassa.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa on esimerkki varaston toimipaikasta.

![Esimerkki varaston toimipaikasta.](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Varaston määrittäminen

Voit määrittää varaston seuraavien ohjeiden mukaisesti.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna **Varasto**-kentässä arvo.  Jos tämä on myymälän 1:1-vastaavuus, voit käyttää myymälän nimeä tai alueellisen jakelukeskuksen nimeä.
1. Anna **Nimi**-kenttään arvo.
1. Valitse avattavassa **Toimipaikka**-luettelossa aiemmin luotu varaston toimipaikka.
1. Valitse **Tyyppi**-kentässä **Oletus**.
    - Jos haluat määrittää **karanteenivaraston**, ensin on luotava näiden ohjeiden mukaan lisävarasto, jossa **Tyyppi**-asetuksena on **Karanteeni**.
    - Jos haluat määrittää **siirtovaraston**, ensin on luotava näiden ohjeiden mukaan lisävarasto, jossa **Tyyppi**-asetuksena on **Siirto**.
1. Valitse toimintoruudussa **Tallenna**.

## <a name="set-up-inventory-aisles"></a>Määritä varastokäytävät

Voit määrittää varastokäytävät noudattamalla seuraavia ohjeita.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan asetukset \> Sijainnin asetukset \> Varastokäytävät**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse avattavassa **Varasto**-luettelossa aiemmin luotu varasto.
1. Anna **Käytävä**-kentässä nimi (kuten Olet).
1. Anna **Nimi**-kentässä nimi (kuten Oletuskäytävä).
1. Valitse toimintoruudussa **Tallenna**.

## <a name="set-up-warehouse-inventory-locations"></a>Määritä varaston varastosijainnit

Voit määrittää varaston varastosijainnit standardivarastolle, vaurioituneelle varastolle ja palautetulle varastolle seuraavien ohjeiden mukaisesti.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.
1. Valitse aiemmin luotu varasto.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse toimintoruudussa **Varasto** ja valitse sitten **Varastosijainti**.
1. Valitse toimintoruudussa **Uusi**. Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.
    1. Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi. 
    1. Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**
    1. Anna **Sijainti**-ruudussa varaston nimi.
    1. Valitse toimintoruudussa **Tallenna**.
 1. Valitse toimintoruudussa **Uusi**.  Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.
    1. Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.  
    1. Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**
    1. Kirjoita **Sijainti**-ruutuun Vaurioitunut.
    1. Valitse toimintoruudussa **Tallenna**.
 1. Valitse toimintoruudussa **Uusi**.  Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.
    1. Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi. 
    1. Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**
    1. Kirjoita **Sijainti**-ruutuun Palautukset.
    1. Valitse toimintoruudussa **Tallenna**.
    
Seuraavassa kuvassa on San Franciscon varaston varastosijaintiasetukset.

![Esimerkki varastosijainnin asetuksista.](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Varaston määrityksen viimeistely

Viimeiste varaston määritys noudattamalla seuraavia ohjeita.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.
1. Valitse aiemmin luotu varasto.
1. Valitse toimintoruudussa **Muokkaa**.
1. **Varastonhallinta**-kohdassa:
    1. Määritä **Oletusvastaanottosijainti**-asetukseksi edellä luotu oletussijainti.
    1. Määritä **Oletusvarasto-ottosijainti**-asetukseksi edellä luotu oletussijainti.
1. Anna varaston osoite **Osoitteet**-osassa.
1. **Vähittäismyynti**-kohdassa: 
    1. Anna **Oletuspalautussijainti**-ruudussa aiemmin luotu palautussijainti.
    1. Määritä **Myymälä**-asetukseksi **Kyllä**.
    1. Määritä **Paino**-asetukseksi **1,00**. 
    1. Anna **Varastodimensiot**-ruudussa aiemmin luotu oletussijainti.
1. Määritä **Varasto**-osassa **Fyysinen negatiivinen varasto** -asetukseksi **Kyllä**.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa on määritetyn varaston tiedot.

![Esimerkki määritetystä varastosta.](media/warehouse-sample.png)

## <a name="additional-resources"></a>Lisäresurssit

[Varastohallinnan yleiskatsaus](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Kanavien yleiskatsaus](channels-overview.md)

[Kanava-asetusten edellytykset](channels-prerequisites.md)

[Vähittäismyyntikanavan määrittäminen](channel-setup-retail.md)
    
[Verkkokanavan määrittäminen](channel-setup-online.md)

[Puhelinkeskuskanavan määrittäminen](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
