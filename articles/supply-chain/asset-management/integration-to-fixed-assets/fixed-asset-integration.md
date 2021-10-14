---
title: Resurssien hallinnan integraatio käyttöomaisuuteen
description: Tässä ohjeaiheessa selitetään, miten käyttöomaisuus ja käyttöomaisuusmoduulit integroidaan toisiinsa, jotta käyttöomaisuus voidaan linkittää kunnossapitoon.
author: johanhoffmann
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 40e4fdce50b335668a53d2efe53b7cf6c66f364f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567580"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Resurssien hallinnan integraatio käyttöomaisuuteen

[!include [banner](../../includes/banner.md)]

Integroimalla **resurssinhallinta**- ja **käyttöomaisuus**-moduulit toisiinsa käyttöomaisuus voidaan linkittää kunnossapitoon. Käyttöomaisuuden käyttäjät voivat sitten luoda kunnossapitoresurssin uudesta tai aiemmin luodusta käyttöomaisuudesta, ja käyttöomaisuuden hallinnan käyttäjät voivat liittää ylläpito-omaisuuden olemassa olevaan käyttöomaisuuserään. Tämän toiminnon avulla käyttöomaisuuden käyttäjät voivat myös helposti tarkastella kustannuksia, jotka kirjattiin liittyvien kunnossapitoresurssien työtilauksista.

> [!NOTE]
> Tässä ohjeaiheessa *ylläpidettävät resurssit* viittaavat **resurssinhallinta**-moduulin ja *käyttöomaisuus* viittaa **käyttöomaisuus**-moduulin varoihin.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Käyttöomaisuuden luomien uusien kunnossapitoresurssien oletussijainnin määrittäminen (valinnainen)

Tämän valinnaisen kokoonpanon avulla voit asettaa oletustoiminnallisen sijainnin uusille ylläpidettäville resursseille, jotka luodaan käyttöomaisuudesta. Tämä konfiguraatio on tavallisesti suoritettava vain kerran, jos suoritat sen loppuun.

Voit tehdä määrityksen noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Resurssinhallinta \> Asetukset \> Resurssinhallinnan parametrit**.
1. Valitse **Käyttöomaisuus**-välilehden **Toiminnallinen sijainti** -kentässä valmiille tuotteille käytettävä oletussijainti.
1. Valitse toimintoruudussa **Tallenna**.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Integroitujen ylläpito- ja käyttöomaisuuden käsitteleminen

Tässä osassa on toimintosarja, jossa on erilaisia tapoja, joilla voit käsitellä integroituja resurssinhallinta- ja käyttöomaisuustoimintoja.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Aiemmin luodun ylläpidettävän resurssin yhdistäminen käyttöomaisuuserään

Seuraa näitä ohjeita yhdistääksesi aiemmin luodun ylläpidettävän resurssin käyttöomaisuuserään.

1. Mene kohtaan **Resurssien hallinta \> Resurssit \> Kaikki resurssit** (tai **Aktiiviset resurssit**).
1. Valitse resurssi.
1. Valitse **Käyttöomaisuus** -pikavälilehden **Käyttöomaisuuserän numero** -kentässä aiemmin luotu käyttöomaisuuserä.
1. Valitse toimintoruudussa **Tallenna**.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Näytä valittuun ylläpidettävä resurssiin liittyvä käyttöomaisuuserä

Seuraa näitä ohjeita näyttääksesi käyttöomaisuuserän, joka liittyy valittuun ylläpidettävään resurssiin.

1. Mene kohtaan **Resurssien hallinta \> Resurssit \> Kaikki resurssit** (tai **Aktiiviset resurssit**).
1. Valitse resurssi.
1. Valitse linkki **Käyttöomaisuus** -pikavälilehden **Käyttöomaisuuserän numero** -kentässä.

    Valitun resurssin **käyttöomaisuus**-sivu avataan. ( Tämä sivu löytyy yleensä kohdasta **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Näytä valittuun käyttöomaisuuserään liittyvä ylläpidettävä resurssi

Seuraa näitä ohjeita näyttääksesi ylläpidettävän resurssin, joka liittyy valittuun käyttöomaisuuserään.

1. Siirry kohtaan **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.
1. Valitse resurssi.
1. Valitse sitten toimintoruudussa **Resurssinhallinta**-välilehden **Näytä**-ryhmässä **Ylläpidettävä resurssi**.

    **Ylläpidettävä resurssi** -sivu, joka liittyy valittuun käyttöomaisuuserään, avataan. (Yleensä tämä sivu löytyy kohdasta **Resurssinhallinta \> Resurssit \> Kaikki resurssit**.)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Käyttöomaisuuteen liittyvien ylläpitokustannusten tarkasteleminen

Käyttöomaisuuden hallinnan työtilauksia voi kirjata ylläpidettävään resurssiin, ja kullakin näistä työtilauksista on yleensä kustannus. Kun käyttöomaisuuserä liitetään ylläpidettävään resurssiin, voit tarkastella siihen liittyviä kustannuksia suoraan käyttöomaisuudesta.

Seuraa näitä ohjeita näyttääksesi ylläpitokustannukset, jotka liittyvät käyttöomaisuuserään.

1. Siirry kohtaan **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.
1. Valitse resurssi.
1. Valitse sitten toimintoruudussa **Resurssinhallinta**-välilehden **Näytä**-ryhmässä **Ylläpitokustannukset**.

    **Ylläpitokustannukset**-sivu avautuu ja siihen liittyvät kustannukset näkyvät.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Luo uusi ylläpidettävä resurssi olemassa olevaan käyttöomaisuuserään

Seuraa näitä ohjeita yhdistääksesi uuden ylläpidettävän resurssin aiemmin luotuun käyttöomaisuuserään.

1. Siirry kohtaan **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.
1. Valitse resurssi.
1. Valitse sitten toimintoruudussa **Resurssinhallinta**-välilehden **Uusi**-ryhmässä **Luo ylläpidettävä resurssi**. (Jos tämä vaihtoehto ei ole käytettävissä, ylläpidettävä resurssi on ehkä jo liitetty valittuun käyttöomaisuuserään.)
1. Viimeistele resurssin luominen [Luo resurssi](../objects/create-an-object.md) -kohdassa kuvatulla tavalla.

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Luo uusi käyttöomaisuuserä ja lisää siihen olemassa oleva ylläpidettävä resurssi

Seuraa näitä ohjeita yhdistääksesi uuden käyttöomaisuuserän uuteen ylläpidettävään resurssiin.

1. Siirry kohtaan **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.
1. Valitse toimintoruudussa **Uusi**.
1. Viimeistele käyttöomaisuuden luominen [Luo käyttöomaisuus](../../../finance/fixed-assets/tasks/create-fixed-asset.md) -kohdassa kuvatulla tavalla.
1. Valitse sitten toimintoruudussa **Resurssinhallinta**-välilehden **Uusi**-ryhmässä **Luo ylläpidettävä resurssi**.
1. Viimeistele resurssin luominen [Luo resurssi](../objects/create-an-object.md) -kohdassa kuvatulla tavalla.

### <a name="remove-the-association-between-two-assets"></a>Kahden käyttöomaisuuserän liitoksen poistaminen

Joissakin tapauksissa ylläpidettävä resurssi on ehkä irrotettava käyttöomaisuudesta. Jos esimerkiksi haluat [luoda uuden ylläpidettävä resurssin](#new-maintenance-from-fixed) käyttöomaisuudesta, sinun on ensin poistettava kaikki olemassa olevat liitokset.

Seuraa näitä ohjeita poistaaksesi olemassa olevan liitoksen ylläpidettävän resurssin ja käyttöomaisuuserän väliltä.

1. Mene kohtaan **Resurssien hallinta \> Resurssit \> Kaikki resurssit** (tai **Aktiiviset resurssit**).
1. Etsi ja avaa käyttöomaisuus.
1. Poista **käyttöomaisuus**-pikavälilehden **toiminnallinen sijainti** -kentän arvo.
1. Valitse toimintoruudussa **Tallenna**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]