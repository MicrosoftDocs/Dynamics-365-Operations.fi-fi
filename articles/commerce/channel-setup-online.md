---
title: Online-kanavan määrittäminen
description: Tässä ohjeaiheessa käsitellään uuden verkkokanavan luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f0f1e0f3e7145c66b8f2b082b44ad7035c57d947
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936941"
---
# <a name="set-up-an-online-channel"></a>Online-kanavan määrittäminen


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään uuden verkkokanavan luontia Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Dynamics 365 Commerce tukee useita vähittäismyynnin kanavia. Vähittäismyyntikanavia ovat verkkokaupat, puhelinkeskukset ja vähittäismyymälät (eli kivijalkakaupat). Verkkokaupassa asiakkaat voivat ostaa tuotteita sekä verkkokaupasta että vähittäismyymälästä.

Verkkokaupan luonti Commercessa edellyttää, että verkkokanava on luotava ensin. Varmista, ennen uuden verkkokanavan luontia, että [kanava-asetusten edellytykset](channels-prerequisites.md) toteutuvat.

Ennen kuin voit luoda uuden sivuston, Commerce-sovellukseen on luotava vähintään yksi verkkokauppa. Katso lisätietoja kohdasta [Luo sähköisen kaupankäynnin sivusto](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Uuden verkkokanavan luominen ja määrittäminen

Voit luoda ja määrittää uuden verkkokanavan seuraavasti.

1. Valitse siirtymisruudussa **Moduulit \> Kanavat \> Verkkomyymälät**.
1. Valitse toimintoruudussa **Uusi**.
1. Kirjoita **Nimi**-kenttään uuden kanavan nimi.
1. Anna sopiva yritys avattavassa **Yritys**-luettelossa.
1. Anna sopiva varasto avattavassa **Varasto**-luettelossa.
1. Valitse sopiva aikavyöhyke **Myymälän aikavyöhyke** -kentässä.
1. Valitse sopiva valuutta **Valuutta**-kentässä.
1. Anna kelvollinen oletusasiakas **Oletusasiakas**-kentässä.
1. Anna kelvollinen osoitekirja **Asiakkaan osoitekirja** -kentässä.
1. Valitse toimintoprofiili tarvittaessa **Toimintoprofiili**-kentässä.
1. Anna kelvollinen sähköpostin ilmoitusprofiili **Sähköposti-ilmoitusprofiili**-kentässä.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näytetään, miten uusi verkkokanava luodaan.

![Uusi verkkokanava](media/channel-setup-online-1.png)

Seuraavassa kuvassa on esimerkki verkkokanavasta.

![Esimerkki verkkokanavasta](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a>Kielien määrittäminen

Jos sähköinen kaupankäyntisivusto tukee useita kieliä, laajenna **Kielet**-osa ja lisää uusia kieliä tarvittaessa.

## <a name="set-up-payment-account"></a>Maksutilin määrittäminen

Voit lisätä **Maksutili**-osassa kolmannen osapuolen maksupalvelun. Lisätietoja Adyen-maksuyhdistimen määrittämisestä on kohdassa [Dynamics 365:n Adyen-maksuyhdistin](./dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Lisäkanavan määrittäminen

Verkkokanavan asetuksia varten tarvittavia tehtäviä, kuten maksutapojen, toimitustapojen ja täytäntöönpanoryhmään määrityksen määrittäminen.

Seuraavassa kuvassa on **Asetukset**-välilehden **Toimitustavat**-, **Maksutavat**- ja **Täytäntöönpanoryhmän määritys** -asetusvaihtoehdot.

![Verkkokanavan lisämääritykset](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Maksutapojen määrittäminen

Voit määrittää maksutavan kullekin tässä kanavassa tuetulle maksutyypille seuraavien ohjeiden mukaisesti.

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Maksutavat**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse maksutapa siirtymisruudussa.
1. Anna **Yleiset**-osassa **Toiminnon nimi** ja määritä muut mahdolliset asetukset.
1. Määritä tarvittaessa maksutyypin mahdolliset lisäasetukset.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkki käteismaksutavasta.

![Esimerkki maksutavasta](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Määritä toimitustavat

Määritetyt toimitustavat saadaan näkyviin valitsemalla **Toimitustapa** **toimintoruudun** **Asetukset**-välilehdessä.  

Voit muuttaa toimitustapaa tai lisätä sen seuraavien ohjeiden mukaisesti.

1. Valitse siirtymisruudussa **Moduulit \> Varastonhallinta \> Toimitustavat**.
1. Luo uusi toimitustapa valitsemalla toimintoruudussa **Uusi** tai valitse aiemmin luotu tapa.
1. Lisää kanava valitsemalla **Vähittäismyyntikanava**-osassa **Lisää rivi**. Kanavien lisäämistä voi yksinkertaistaa käyttämällä organisaatiosolmua sen sijaan, että kukin kanava lisättäisiin erikseen.

Seuraavassa kuvassa on esimerkki toimitustavasta.

![Määritä toimitustavat](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Täytäntöönpanoryhmän määrityksen määrittäminen

Voit määrittää täytäntöönpanoryhmän määrityksen noudattamalla seuraavia ohjeita.

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Täytäntöönpanoryhmän määritys**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse täytäntöönpanoryhmä avattavassa **Täytäntöönpanoryhmä**-luettelossa.
1. Anna kuvaus avattavassa **Kuvaus**-luettelossa.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa on esimerkki täytäntöönpanoryhmän määrityksen määrittämisestä.

![Täytäntöönpanoryhmän määrityksen määrittäminen](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Lisäresurssit

[Kanavien yleiskatsaus](channels-overview.md)

[Kanava-asetusten edellytykset](channels-prerequisites.md)

[Vähittäismyyntikanavan määrittäminen](channel-setup-retail.md)

[Puhelinkeskuskanavan määrittäminen](channel-setup-callcenter.md)

[Dynamics 365 -maksuyhdistin Adyenia varten](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]