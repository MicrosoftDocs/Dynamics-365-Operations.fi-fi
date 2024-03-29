---
title: Oletusasiakkaan luominen
description: Tässä artikkelissa esitellään, miten luodaan oletusasiakas käytettäväksi, kun Microsoft Dynamics 365 Commercessa luodaan kanavaa.
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
ms.openlocfilehash: 79e145c21be9178622b7c105afefecb78062e3b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273582"
---
# <a name="create-a-default-customer"></a>Oletusasiakkaan luominen

[!include [banner](includes/banner.md)]

Tässä artikkelissa esitellään, miten luodaan oletusasiakas käytettäväksi, kun Microsoft Dynamics 365 Commercessa luodaan kanavaa.

Kun luot kanavaa, sinun on määritettävä oletusasiakas. Oletusasiakas on helppo luoda, kun asiakasryhmä ja asiakasosoitekirja on luotu ensin.

## <a name="create-a-customer-group"></a>Asiakasryhmän luominen

Jos asiakasryhmiä ei vielä ole, voit luoda sellaisen. Esimerkkejä voivat olla eri asiakasryhmiä, kuten tukkukauppa, vähittäiskauppa, internet, työntekijät jne.

Luo asiakasryhmä noudattamalla seuraavia ohjeita.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Asiakkaat \> Asiakasryhmät**.
1. Valitse toimintoruudussa **Uusi**.
1. Kirjoita asiakkaan tunnus **Asiakasryhmä**-kenttään.
1. Kirjoita soveltuva kuvaus **Kuvaus**-ruutuun.
1. Kirjoita soveltuva arvo **Maksuehdot**-ruutuun.
1. Kirjoita soveltuva arvo **Laskun eräpäivän ja maksupäivän välinen aika** -ruutuun.
1. Kirjoita tarvittaessa veroryhmä **Oletusveroryhmä**-ruutuun.
1. Valitse tarvittaessa **Hinnat sisältävät arvonlisäveron** -valintaruutu.
1. Kirjoita **Poiskirjauksen oletussyy** -ruutuun tarvittaessa asianmukainen arvo.

Seuraavassa kuvassa näkyy useista määritettyjä asiakasryhmiä.

![Asiakasryhmät.](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Luo uusi asiakkaan osoitekirja

Asiakas on yhdistettävä osoitekirjaan. Jos sellaista ei ole vielä luotu, sinun on luotava sellainen.

Luo osoitekirja noudattamalla seuraavia ohjeita.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Osoitekirja**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna nimi **Nimi**-ruutuun.
1. Syötä **Kuvaus**-ruutuun kuvaus.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkki osoitekirjasta.

![Osoitekirja.](media/address-book.png)

## <a name="create-a-default-customer"></a>Oletusasiakkaan luominen

Luo oletusasiakas noudattamalla seuraavia ohjeita.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse avattavasta **Tyyppi**-luettelosta "Henkilö".
1. Valitse tai syötä avattavassa **Asiakastili**-luettelossa tilinumero (esim. "100001").
1. Valitse tai syötä avattavassa **Etunimi**-valikossa nimi (esim. "Oletus").
1. Valitse tai syötä avattavassa **Toinen etunimi**-valikossa nimi (esim. "Vähittäiskauppa").
1. Valitse tai syötä avattavassa **Sukunimi**-valikossa nimi (esim. "Asiakas").
1. Valitse tai syötä avattavassa **Valuutta**-valikossa valuutta (esim. "USD").
1. Valitse avattavassa **Valuutta**-luettelossa aiemmin luotu asiakasryhmä.
1. Valitse avattavasta **Osoitekirja**-valikossa olemassa oleva osoitekirja.
1. Valitse **Tallenna**, jos haluat tallentaa ja palata uuden asiakkaan asiakastietonäyttöön.

> [!NOTE]
> Oletusasiakkaalle ei tarvitse lisätä osoitetta.

Seuraavassa kuvassa näkyy esimerkki asiakkaan luomisesta.

![Oletusasiakkaan luominen.](media/default-customer-creation.png)

Seuraavassa kuvassa näkyy oletusarvoinen asiakasmääritys.

![Esimerkkiasiakkaan määritys.](media/default-customer-configuration1.png)

Useimmat asiakastietonäytön oletusarvot voidaan säilyttää, mutta kaksi arvoa on muutettava.

1. Laajenna asiakastietonäytöllä **Myyntitilauksen oletusarvot**.
1. Valitse avattavassa **Sivusto**-luettelossa esimääritetty sivusto tai syötä sivusto.
1. Valitse avattavassa **Varasto**-luettelossa varasto tai syötä esimääritetty varasto.

Seuraavassa kuvassa näkyy esimerkki asiakasmäärityksestä.

![Esimerkkiasiakkaan määritys.](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Lisäresurssit

[Kanavien yleiskatsaus](channels-overview.md)

[Kanavan määrittämisen edellytykset](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
